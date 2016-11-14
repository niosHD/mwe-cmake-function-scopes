CMake and Scopes for Function Definitions
=========================================

Minimal working example which shows how CMake resolves function definitions across different scopes.

The CMake Documentation on [function](https://cmake.org/cmake/help/v3.7/command/function.html) only defines that a function opens a new scope but does not clarify how functions interact with scopes themselves.

On CMake 3.5.1, the following output is generated:

```
-- Maindir Func
-- VAR = MAINDIR
-- Subdir Func
-- VAR = SUBDIR
-- Subdir Func
-- VAR = MAINDIR
```

CMake seems to use the last definition of a function it encounters, independent of current scope. Otherwise, the following output would have been generated:

```
-- Maindir Func
-- VAR = MAINDIR
-- Subdir Func
-- VAR = SUBDIR
-- Maindir Func
-- VAR = MAINDIR
```
