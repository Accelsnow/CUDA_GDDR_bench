```
cmake -B . build
cmake --build build
```

The above commands create an executable gddr in build folder.
Execute ./gddr produces a list of strides to latencies.
Project configured for RTX 4090, which can only be compile on devices with CC89. To run on devices with CC other than 89, change CMakeLists.txt.

Two python scripts are used to generate a line chart and a histogram. They parse the output file of ./gddr 'stride_latencies.txt' and open a GUI that displays the matplot graph.
