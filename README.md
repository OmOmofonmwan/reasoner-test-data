# Reasoner Test Data

Builds maven test data artifacts for SNOMED and other data sources that are not open source licensed.

Building test data artifacts is skipped by default.

To build test data artifacts:
* mvn clean install -DskipTestDataBuild=false

### SNOMED Test Data

The snomed-test-data module packages data in the SNOMED release format with the following conventions:
* The base directory is `${user.home}/data/snomed`
* The release directory is the release archive filename e.g. `SnomedCT_InternationalRF2_PRODUCTION_20190731T120000Z`
* The included files are those in `Snapshot/Terminology`

To package a different SNOMED release, create a new sub-module similar to an existing one and change the edition property:
* `<snomed.edition>SnomedCT_InternationalRF2_PRODUCTION_20190731T120000Z</snomed.edition>`

These artifacts are used for integration testing in the [IKM Elk Reasoner project](https://github.com/ikmdev/ikm-reasoner)

### Tinkar Test Data

The tinkar-reasoner-test-data module packages test dbs for testing tinkar reasoner service implementations.

### Team Ownership - Product Owner

Data Team - Eric Mays (External) <emays@mays-systems.com>