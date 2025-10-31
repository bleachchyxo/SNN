Run your circuit using;

    ngspice -b circuit.cir

And the output must be like the following;

 
    Note: No compatibility mode selected!


    Circuit: * simple led circuit simulation with dc source

    Doing analysis at TEMP = 27.000000 and TNOM = 27.000000

    Using SPARSE 1.3 as Direct Linear Solver

    Initial Transient Solution
    --------------------------

    Node                                   Voltage
    ----                                   -------
    1                                            5
    2                                     0.731816
    v1#branch                           -0.0194008


    No. of Data Rows : 508
    Note: Simulation executed from .control section

It should create a `voltage_output.txt` file. Now run;

    gnuplot -e "set xlabel 'Time (seconds)'; set ylabel 'Voltage (V)'; set yrange [0.72:0.74]; plot 'voltage_output.txt' using 1:3 with lines title 'LED Voltage'; pause -1 'Press Enter to continue'"

