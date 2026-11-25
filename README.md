# ESP32 WebAssembly Network Latency

An ESP32 project exploring network latency with WebAssembly. The Python exporter starts a benchmark through the board’s serial menu and saves the emitted measurements as a CSV file.

## Export benchmark results

With the benchmark firmware running and the serial monitor closed, install PySerial and run the exporter. Set `--port` to the serial port assigned to your board.

```sh
python -m pip install pyserial
python export_csv.py --port COM10 --count 1000 --out bench_results.csv
```

The exporter waits for the firmware menu and captures the output over serial at 115200 baud by default.
