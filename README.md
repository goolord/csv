# csv

Simple comparative benchmarks for CSV parsing libraries.

The "file" benchmarks are IO-based: reading from a file into a list or
vector of rows which is then forced with a deepseq. Conveniently, the
differences between each library are reproducibly distinct.

<!-- RESULTS -->

## file

|Name||
|---|---|
|String/cassava/decode/Vector ByteString|0.270 ms|
|String/cassava/decode/[ByteString]|0.408 ms|
|String/csv-conduit/readCSVFile/[ByteString]|1.232 ms|
|String/csv-conduit/readCSVFile/Vector ByteString|1.397 ms|
|String/csv-conduit/readCSVFile/[String]|1.762 ms|
|String/csv|3.780 ms|
|String/sv/Data.Sv.Parse/attoparsecText|8.873 ms|
|String/sv/Data.Sv.Parse/attoparsecByteString|9.413 ms|
|String/sv/Data.Sv.Parse/trifecta|14.76 ms|
