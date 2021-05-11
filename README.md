fips-pystring
=========

fipsified pystring (https://github.com/imageworks/pystring)

fips build system: https://github.com/floooh/fips

## How to integrate:

Add the dependency to your fips.yml file:

```yaml
imports:
    fips-pystring:
        git: https://github.com/deadwanderer/fips-pystring
```

Use pystring as dependency in your targets:

```cmake
fips_begin_*(...)
    ...
    fips_deps(pystring)
fips_end_*(...)
```
