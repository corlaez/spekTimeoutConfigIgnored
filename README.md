## Spek's configurations ignored in multiplatform project

gradle.properties are ignored:

* `spek2.discovery.parallel.enabled=true`
* `spek2.execution.parallel.enabled=true`
* `spek2.execution.test.timeout=1`

The vmOption: `-DSPEK_TIMEOUT=1` is also ignored.

## Run tests

Maven > fullstack > Tasks > verification > jvmTest

## Reference 

https://github.com/spekframework/spek/issues/952

# Update 1

I need to propagate the properties manually as in
https://github.com/spekframework/spek/blob/2.x/integration-test/build.gradle.kts#L105

This allows `spek2.execution.test.timeout=1` to work. However, tests are still sequential