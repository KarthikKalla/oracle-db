# Change Log

## v2.7.0 - 2023-11-01

- ⚙️ **Chore**: Update backend and frontend dependencies
- ⚙️ **Chore**: Minimum required Grafana runtime version is now 9.5.13

## v2.6.4 - 2023-09-07

- 🐛 **Fix**: Fix bug causing configuration page not working in some cases

## v2.6.3 - 2023-08-25

- ⚙️ **Chore**: Remove "Generated SQL" button from the query editor as it duplicates the functionality of the query inspector

## v2.6.2 - 2023-08-24

- ⚙️ **Chore**: add debug container

## v2.6.1 - 2023-08-23

- ⚙️ **Chore**: e2e test support

## v2.6.0 - 2023-06-09

- ⚙️ **Chore**: Configuration page UI and UX overhaul

## v2.5.1 - 2023-06-08

- ⚙️ **Chore**: backend libs updated with golang:1.20.5

## v2.5.0 - 2023-05-31

- 🚀 **Feature**: [Secure socks proxy](https://grafana.com/docs/grafana/next/setup-grafana/configure-grafana/proxy/) support added

## v2.4.6 - 2023-05-23

- ⚙️ **Chore**: Fixes a bug with the QueryEditor onBlur event so it fires the correct onChange prop

## v2.4.5 - 2023-05-05

- ⚙️ **Chore**: Updating Dockerfiles to use Go version `1.20.4` which contains security fixes

## v2.4.4 - 2023-05-03

- ⚙️ **Chore**: Backend binaries are now compiled with Go version `1.20.4` which contains security fixes

## v2.4.3 - 2023-04-19

- ⚙️ **Chore**: Backend binaries are now compiled with Go version `1.20.3` which contains security fixes
- ⚙️ **Chore**: Minimum required Grafana runtime version is now 8.4.7

## v2.4.2 - 2023-04-19

- ⚙️ **Chore**: Backend dependencies updated

## v2.4.1 - 2023-03-30

- ⚙️ **Chore**: Remove unused images in screenshots folder

## v2.4.0 - 2023-03-28

- 🚀 **Feature**: Prevent from using kerberos when TNSNames option is disabled
- 🚀 **Feature**: Prevent from running query on editor blur
- 🐛 **Fix**: Fix Generated SQL in code Editor
- 📝 **Documentation**: Fix formatting and cleanup in docs

## v2.3.0 - 2023-02-10

- 🚀 **Feature**: Data source config page improvements

## v2.2.8 - 2022-12-15

- ⚙️ **Chore**: Backend dependencies updated
- ⚙️ **Chore**: Backend binaries are now compiled with Go 1.19.4

## v2.2.7 - 2022-11-01

- backend binaries are compiled with go 1.19.3

## v2.2.6 - 2022-10-14

- follow-up on obfuscate password input: replace input field with SecretInput from @grafana/ui
- update dependencies to v8.4.7
- update docs

## v2.2.5 - 2022-10-14

- obfuscate password input in datasource setting
- update docs

## v2.2.4 - 2022-10-05

- Update the feature for response data size

## v2.2.3 - 2022-09-28

- Update docs

## v2.2.2 - 2022-09-28

- User can define query response data size with environment variable `GF_PLUGINS_ORACLE_DATASOURCE_MAX_RESPONSE_SIZE`
- Update `DEV_GUIDE.md` for ARM64 developers

## v2.2.1 - 2022-09-06

- ⚙️ **Chore**: Add back the format selector in the query editor

## v2.2.0 - 2022-07-22

- ⚙️ **Chore**: update linux amd64 oracle client to 21.6

## v2.1.3 - 2022-06-09

- 🐛 **Fix**: set exec permissions

## v2.1.2 - 2022-05-17

- Fix libs for rhel/centos 7.x

## v2.1.1 - 2022-05-17

- Add libs for rhel/centos 7.x

## v2.1.0 - 2022-05-05

- Reduce size of Linux zip

## v2.0.9 - 2022-03-03

- Re-implement timezone translation

## v2.0.8 - 2022-01-13

- Adds error message that warns user when response message size is larger than 16Mb
- Adds the option to compile back-end for ARM64 processors

## v2.0.7 - 2022-01-10

- ⚙️ **Chore**: Update Licensing

## v2.0.6 - 2021-08-10

- Adds documentation for RHEL 8 libnsl dependency
- Fixes an issue where hidden queries were still being executed
- Fixes an issue where queries with just whitespace (empty) were being executed.

## v2.0.4 - 2021-04-12

- ⚙️ **Chore**: Update SDK

## v2.0.2 - 2020-10-09

- Fixed signed plugin issue

## v2.0.1 - 2020-10-06

- Fixed configuration editor to allow tnsname and kerberos options to be selected during manual setup
- Adjusted configuration editor entry field sizes

## v2.0.2 - 2020-10-09

- Fixed signed plugin issue

## v2.0.1 - 2020-10-06

- Fixed configuration editor to allow tnsname and kerberos options to be selected during manual setup
- Adjusted configuration editor entry field sizes

## v2.0.0 - 2020-10-01

- Compatible with Grafana v7.1+

Key Features:

- Conversion to dataframes for easier use with different visualizations and data transformations
- Updated to use InstantClient v19, supporting stcp connections
- Query editor now uses monaco for syntax

Bugfixes:

- Connection cache will expire idle connections to prevent slow responses

Note: Time Zone support not included in v2.0.0, to be added in next minor release.
All connections and results are processed as UTC.

## v1.2.2 - 2020-08-28

- Fix for kerberos authentication error output

## v1.2.1 - 2020-08-19

- NEW: Support for TNSNAMES and Kerberos Authentication
- Fix for issue #133 (redact message on connection error)
- Fix field comparisons for Annotation Queries
- Increase max message size to 16MB

## v1.2.0 - 2020-05-15

- Now compatible with Grafana v7.0.0
- Now grafana-cli installable

## v1.1.7 - 2020-03-27

- Fix for Edge Browser

## v1.1.6 - 2020-03-25

- New fill options for macros (intervals now the same as other sql datasources)
- New timezone configuration setting for datasource (default is UTC)
- 🐛 **Fix**: removed auto-quoting of time columns in macros

## v1.1.5 - 2020-02-13

- Better handling of macro `$__timeGroup`
- Implements fill options for `$__timeGroup` similar to other sql datasources
- Upgrade build to go-1.13.7
- Converted to go mod
- Additional test coverage

## v1.1.4 - 2020-02-05

- Connection pool size is now working
- Profiling setting now working
- Fix for backend crash when nil values are return
- Fix for locking issue causing backend to hang
- Fix quoting issues
- Implement braces for macros
- Now allows sql statements inside macros

## v1.1.3 - 2019-12-18

- GF_PLUGIN_ORACLE_DATASOURCE_POOLSIZE can be used to increase/decrease the size of the connection pool with Oracle. The new default is `50`

## v1.1.2 - 2019-11-04

- GF_PLUGIN_PROFILER must be set to "oracle-datasource" to enable profiling. default is false.

## v1.1.1 - 2019-09-20

- Remove connection string output from debug mode
- Refactor to clean up go lint warnings

## v1.1.0 - 2019-07-20

- Fixes panic of backend plugin on windows
- Update to all package dependencies

## v1.0.9 - 2019-06-10

- Return message when query results are too large
- Prevent crash due to attempting too large response
- Additional handling of nullable columns
- Updated packages

## v1.0.8 - 2019-05-15

- Now handles nullable column for value field when transforming to timeseries

## v1.0.7 - 2019-05-09

- lower query cache TTL to 60 seconds
- fix leak due to deferred close inside loop
- reuse fingerprint vs recalculating (small performance gain)
- detect errors iterating rows
- add more debug output
- updated vendored packages

## v1.0.6 - 2019-04-25

- Now provides info level log line when type is not matched
- Added additional data types
  - converts to type FLOAT: SQLT_INT, SQLT_UIN, SQLT_FLT, SQLT_VNU, SQLT_LNG, SQLT_BFLOAT, SQLT_BDOUBLE
  - converts to type STRING: SQLT_STR, SQLT_LVC, SQLT_VST, SQLT_VBI, SQLT_LBI, SQLT_LVB
  - converts to type DATE: SQLT_DATE
  - converts to type BYTES: SQLT_FILE
- 🐛 **Fix**: when a query returns no results (and data types as a part of the results), the types are not cached to allow future queries with results update the cache

## v1.0.5 - 2019-04-08

- gRPC: hardcode message size to 16MB vs 4MB
- enable alerting

## v1.0.4 - 2019-03-29

- Plugin now links oracle libraries from plugin directory, no need for installation externally on system (linux only, windows requires install)

## v1.0.3 - 2019-03-18

- Support additional field type SQLT_NUME
- Better type conversions
- Add quoted time field to variable interpolation

## v1.0.2 - 2019-03-04

- Update golang dependencies

## v1.0.1 - 2019-02-05

### Fixed

[#13](https://github.com/grafana/oracle-datasource/issues/13)

- High CPU utilization issue fix via short-term cache of column types
- Connection errors fixed by testing cached connections before returning to caller

## v0.0.1 - 2018-05-09

Initial Release
