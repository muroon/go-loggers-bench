# test result

```
$ make
go get -u github.com/sirupsen/logrus
go get -u gopkg.in/inconshreveable/log15.v2
go get -u github.com/op/go-logging
go get -u github.com/cihub/seelog
go get -u github.com/go-kit/kit/log
go get -u github.com/rs/zerolog
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Gokit.*Text"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkGokitTextPositive     	 6294870	       981.4 ns/op	     256 B/op	       4 allocs/op
BenchmarkGokitTextPositive-2   	11309568	       540.2 ns/op	     256 B/op	       4 allocs/op
BenchmarkGokitTextPositive-4   	19437433	       308.4 ns/op	     256 B/op	       4 allocs/op
BenchmarkGokitTextNegative     	193044313	        31.03 ns/op	      32 B/op	       1 allocs/op
BenchmarkGokitTextNegative-2   	339195705	        20.71 ns/op	      32 B/op	       1 allocs/op
BenchmarkGokitTextNegative-4   	439369250	        14.41 ns/op	      32 B/op	       1 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	51.560s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Logrus.*Text"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkLogrusTextPositive     	 2795073	      2038 ns/op	     520 B/op	      15 allocs/op
BenchmarkLogrusTextPositive-2   	 5552964	      1096 ns/op	     520 B/op	      15 allocs/op
BenchmarkLogrusTextPositive-4   	 8990570	       792.0 ns/op	     520 B/op	      15 allocs/op
BenchmarkLogrusTextNegative     	1000000000	         2.501 ns/op	       0 B/op	       0 allocs/op
BenchmarkLogrusTextNegative-2   	1000000000	         1.197 ns/op	       0 B/op	       0 allocs/op
BenchmarkLogrusTextNegative-4   	1000000000	         0.6162 ns/op	       0 B/op	       0 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	28.193s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Log15.*Text"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkLog15TextNegative     	 6672973	       980.7 ns/op	     440 B/op	       3 allocs/op
BenchmarkLog15TextNegative-2   	11096697	       546.3 ns/op	     440 B/op	       3 allocs/op
BenchmarkLog15TextNegative-4   	20557663	       350.3 ns/op	     440 B/op	       3 allocs/op
BenchmarkLog15TextPositive     	 2454541	      2360 ns/op	     904 B/op	      14 allocs/op
BenchmarkLog15TextPositive-2   	 3016521	      1973 ns/op	     904 B/op	      14 allocs/op
BenchmarkLog15TextPositive-4   	 2725156	      2146 ns/op	     904 B/op	      14 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	46.391s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Gologging.*Text"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkGologgingTextNegative     	32017290	       178.0 ns/op	     144 B/op	       2 allocs/op
BenchmarkGologgingTextNegative-2   	51252198	       116.5 ns/op	     144 B/op	       2 allocs/op
BenchmarkGologgingTextNegative-4   	82014998	        78.31 ns/op	     144 B/op	       2 allocs/op
BenchmarkGologgingTextPositive     	 3388404	      1675 ns/op	     912 B/op	      16 allocs/op
BenchmarkGologgingTextPositive-2   	 6313071	      1073 ns/op	     912 B/op	      16 allocs/op
BenchmarkGologgingTextPositive-4   	 9484798	       683.8 ns/op	     912 B/op	      16 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	41.348s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Seelog.*Text"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkSeelogTextNegative     	93949437	        63.40 ns/op	      40 B/op	       2 allocs/op
BenchmarkSeelogTextNegative-2   	175952673	        34.02 ns/op	      40 B/op	       2 allocs/op
BenchmarkSeelogTextNegative-4   	293679906	        20.94 ns/op	      40 B/op	       2 allocs/op
BenchmarkSeelogTextPositive     	 2875939	      1804 ns/op	     432 B/op	      11 allocs/op
BenchmarkSeelogTextPositive-2   	 2905508	      2159 ns/op	     432 B/op	      11 allocs/op
BenchmarkSeelogTextPositive-4   	 2898346	      2109 ns/op	     432 B/op	      11 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	48.138s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Zerolog.*Text"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkZerologTextPositive     	11473489	       475.6 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologTextPositive-2   	23450034	       262.4 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologTextPositive-4   	43410866	       152.9 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologTextNegative     	1000000000	         4.025 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologTextNegative-2   	1000000000	         1.958 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologTextNegative-4   	1000000000	         1.103 ns/op	       0 B/op	       0 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	27.551s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Fortiolog.*Text"
PASS
ok  	github.com/imkira/go-loggers-bench	0.481s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Gokit.*JSON"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkGokitJSONPositive     	 1467907	      3802 ns/op	    1592 B/op	      24 allocs/op
BenchmarkGokitJSONPositive-2   	 3104496	      1934 ns/op	    1592 B/op	      24 allocs/op
BenchmarkGokitJSONPositive-4   	 5536983	      1276 ns/op	    1592 B/op	      24 allocs/op
BenchmarkGokitJSONNegative     	92853193	        56.51 ns/op	     128 B/op	       1 allocs/op
BenchmarkGokitJSONNegative-2   	145019312	        41.54 ns/op	     128 B/op	       1 allocs/op
BenchmarkGokitJSONNegative-4   	210371913	        30.99 ns/op	     128 B/op	       1 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	51.291s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Logrus.*JSON"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkLogrusJSONNegative     	12144952	       535.3 ns/op	     496 B/op	       4 allocs/op
BenchmarkLogrusJSONNegative-2   	18498244	       289.2 ns/op	     496 B/op	       4 allocs/op
BenchmarkLogrusJSONNegative-4   	35571994	       221.1 ns/op	     496 B/op	       4 allocs/op
BenchmarkLogrusJSONPositive     	  941757	      5704 ns/op	    2256 B/op	      34 allocs/op
BenchmarkLogrusJSONPositive-2   	 2052878	      3129 ns/op	    2256 B/op	      34 allocs/op
BenchmarkLogrusJSONPositive-4   	 3775473	      1633 ns/op	    2258 B/op	      34 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	48.043s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Log15.*JSON"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkLog15JSONNegative     	 4632020	      1210 ns/op	     632 B/op	       5 allocs/op
BenchmarkLog15JSONNegative-2   	 9865024	       588.8 ns/op	     632 B/op	       5 allocs/op
BenchmarkLog15JSONNegative-4   	18723184	       328.2 ns/op	     632 B/op	       5 allocs/op
BenchmarkLog15JSONPositive     	 1000000	      5226 ns/op	    2056 B/op	      30 allocs/op
BenchmarkLog15JSONPositive-2   	 1260622	      4683 ns/op	    2056 B/op	      30 allocs/op
BenchmarkLog15JSONPositive-4   	 1325517	      4500 ns/op	    2056 B/op	      30 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	46.937s
go test -cpu=1,2,4 -benchmem -benchtime=5s -bench "Zerolog.*JSON"
goos: darwin
goarch: amd64
pkg: github.com/imkira/go-loggers-bench
cpu: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz
BenchmarkZerologJSONNegative     	737410134	         8.315 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologJSONNegative-2   	1000000000	         4.146 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologJSONNegative-4   	1000000000	         2.196 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologJSONPositive     	 8967524	       669.4 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologJSONPositive-2   	17348766	       343.2 ns/op	       0 B/op	       0 allocs/op
BenchmarkZerologJSONPositive-4   	34598036	       183.0 ns/op	       0 B/op	       0 allocs/op
PASS
ok  	github.com/imkira/go-loggers-bench	34.063s
```
