# nmpstat
## Add numa information to mpstat data. 
### We parse mpstat data and append the Numa data however this requires lscpu to be installed

To run default will print all nodes as per notmal mpstat output 

``` nmpstat 1 100 0```
```
21:12:33     NODE   SOCK   CORE   CPU    %usr     %nice    %sys     %iowait  %irq     %soft    %steal   %guest   %gnice   %idle
21:12:34                          all    1.41     0.00     0.12     0.08     0.00     0.04     0.00     0.00     0.00     98.34
21:12:34     0      0      0      0      25.49    0.00     0.98     0.00     0.00     0.98     0.00     0.00     0.00     72.55
21:12:34     0      0      1      1      4.04     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     95.96
21:12:34     0      0      2      2      0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:34     0      0      3      3      0.99     0.00     1.98     0.00     0.00     0.00     0.00     0.00     0.00     97.03
21:12:34     0      0      4      4      0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:34     0      0      5      5      0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:34     0      0      0      12     1.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     99.00
21:12:34     0      0      1      13     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:34     0      0      2      14     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:34     0      0      3      15     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:34     0      0      4      16     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:34     0      0      5      17     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
```

This would run for 100 1 second samples on node 0

``` nmpstat 1 100 1```
```
21:12:29     NODE   SOCK   CORE   CPU    %usr     %nice    %sys     %iowait  %irq     %soft    %steal   %guest   %gnice   %idle
21:12:30                          all    0.08     0.00     0.08     0.00     0.00     0.00     0.00     0.00     0.00     99.83
21:12:30     1      1      6      6      0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      7      7      0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      8      8      0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      9      9      0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      10     10     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      11     11     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      6      18     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      7      19     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      8      20     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      9      21     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      10     22     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
21:12:30     1      1      11     23     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     0.00     100.00
```
