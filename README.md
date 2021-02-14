## Spek Timeout configuration ignored

Using The new or old timeout configurations don't seem to have any effect on a kotlin multiplatform project.

For the new config, add to gradle.properties:
`spek2.execution.test.timeout=1`

For the old config edit the configuration of the maven taks and add vmOptions:
`-DSPEK_TIMEOUT=1`

## Run tests

Maven > fullstack > Tasks > verification > jvmTest

## Reference 

https://github.com/spekframework/spek/issues/952
