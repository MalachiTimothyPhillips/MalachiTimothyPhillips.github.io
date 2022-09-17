---
title: 'C++17 Features: `std::apply` and fold expressions'
date: 2022-09-17
permalink: /posts/2022/09/cpp-17-std-apply-and-fold-expressions/
tags:
  - C++
---

`std::apply` and fold expressions in C++17: simplifying parameter packs
======

Often, I find myself in a scenario where I need to "iterate" over the elements inside a tuple.
Prior to C++17, the basic idea behind accomplishing this was through the use of parameter packs and `std::index_sequence`.
However, with the introduction of `std::apply` and fold expressions, this task is much simpler.

```cpp
#include <functional>
#include <iostream>
#include <typeinfo>
#include <initializer_list>
#include <tuple>
#include <vector>
#include <set>
#include <unordered_set>
#include <string_view>

// stolen from https://stackoverflow.com/questions/81870/is-it-possible-to-print-a-variables-type-in-standard-c/56766138#56766138
// get useful type information without needing to use c++filt
// does the unmangling for you!
template <typename T>
constexpr auto type_name() {
  std::string_view name, prefix, suffix;
#ifdef __clang__
  name = __PRETTY_FUNCTION__;
  prefix = "auto type_name() [T = ";
  suffix = "]";
#elif defined(__GNUC__)
  name = __PRETTY_FUNCTION__;
  prefix = "constexpr auto type_name() [with T = ";
  suffix = "]";
#elif defined(_MSC_VER)
  name = __FUNCSIG__;
  prefix = "auto __cdecl type_name<";
  suffix = ">(void)";
#endif
  name.remove_prefix(prefix.size());
  name.remove_suffix(suffix.size());
  return name;
};

int main(){

  std::initializer_list initializer = {1, 2, 3, 4, 3, 2, 1};
  auto createSet = [=](){
      return std::set<int>(initializer);
  };

  auto createUnorderedSet = [=](){
      return std::unordered_set<int>(initializer);
  };

  auto createVector = [=](){
      return std::vector<int>(initializer);
  };

  auto createMultiSet = [=](){
      return std::multiset<int>(initializer);
  };

  auto printContainer = [](auto& containerCreator){
      auto container = containerCreator();
      std::cout << "Iterating over container of type : " << type_name<decltype(container)>() << "\n";
      for(auto&& entry : container){
          std::cout << "\t" << entry << "\n";
      }
  };

  std::apply([=](auto&&... containerCreator){
      (printContainer(containerCreator),...);
  }, std::tuple{createSet, createUnorderedSet, createVector, createMultiSet});

}
```

That's it -- just:

```cpp
std::apply([=](auto&&... containerCreator){
  (printContainer(containerCreator),...);
}, std::tuple{createSet, createUnorderedSet, createVector, createMultiSet});
```