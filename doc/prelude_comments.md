## blocky
Blocky is the compression algorithm developed for the diploma thesis of FemtoLAS.

It groups numbers with similarities and then uses the LZMA compression (a 7zip compression algorithm) which greatly improves the results.


# istream
istream is used to convert the compressed data back into a format which is usable by OpenFOAM.


# ostream
ostream is used to output the data as the compressed file format.


# streambuf
streambuf is in charge of the reading and writing operations.
It includes the methods sync, underflow and overflow.
  
### sync
If data is entered but neither underflow nor overflow is called, sync writes that data into the stream-buffer in randomly chosen intervals.
### underflow
If the stream-buffer is empty and there is an attempt to remove values from it this method is called.
### overflow
If the stream-buffer is full and there is an attempt to put more data into it this method is called.
