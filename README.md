# 7-segment-display-using-iverilog
A 7-segment display is an electronic device showcasing numeric digits and some characters by illuminating seven segments. It's widely used in digital clocks, calculators, and meters for its simplicity and readability.



This repository contains Verilog code for simulating a simple seven-segment display, along with a testbench to verify its functionality.

## Description

The Verilog modules in this repository simulate a seven-segment display, which is commonly used in digital displays to represent decimal digits. The display consists of seven LEDs arranged in a specific pattern to display numbers from 0 to 9. Each LED segment is controlled independently to display the desired digit.

The following Verilog modules are included:
- `and2`: Implements a two-input AND gate.
- `or2`: Implements a two-input OR gate.
- `and3`: Implements a three-input AND gate using two `and2` gates.
- `or3`: Implements a three-input OR gate using two `or2` gates.
- `a_segment`, `b_segment`, `c_segment`, `d_segment`, `e_segment`, `f_segment`, `g_segment`: Implement segments of the seven-segment display, corresponding to the segments labeled A, B, C, D, E, F, and G respectively.
- `seven_segment`: Integrates the segment modules to simulate the entire seven-segment display.

## Usage

To simulate the seven-segment display, follow these steps:

1. Compile the Verilog source files using the Icarus Verilog compiler:
    ```bash
    iverilog -o test sevensegment.v seven_segment_tb.v
    ```

2. Run the compiled executable to execute the simulation:
    ```bash
    vvp test
    ```

3. View the simulation results using GTKWave:
    ```bash
    gtkwave seven_segment_test.vcd
    ```

## Files Included

- `sevensegment.v`: Verilog module defining the components of the seven-segment display.
- `seven_segment_tb.v`: Verilog testbench for simulating the seven-segment display.
- `lib.v`: Verilog module defining basic logic gates used in the simulation.
- `seven_segment_test.vcd`: Value Change Dump (VCD) file containing simulation results.

## Contributing

Contributions to improve the functionality or documentation of this project are welcome! If you'd like to contribute, please follow these steps:
1. Fork this repository.
2. Create your feature branch (`git checkout -b feature/my-feature`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature/my-feature`).
5. Open a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
