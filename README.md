# record-tuple-size-test

The [Haskell record variant comparison spreadsheet][1] claimed that records and
tuples have at most 63 fields.  The aim of this was to verify or refute that
assertion.

The results so far have been that tuples have a maximum of 62 fields, not 63, but
no upper limit on the number of fields on a record has yet been found in either GHC
8.2.2 or GHC 7.8.4.

To use this as a test, run:

```
stack clean
stack build --resolver=X
```

where X represents a resolver for the compiler version you want to use.  My tests were with `lts-11.7` and `lts-2.22`.

[1]: https://docs.google.com/spreadsheets/d/14MJEjiMVulTVzSU4Bg4cCYZVfkbgANCRlrOiRneNRv8/edit#gid=0 
