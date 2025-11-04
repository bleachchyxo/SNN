code

    just look at this code, dont answer until future intructions; cat circuit.cir
    * Simple LED circuit simulation with DC source
    V1 1 0 DC 5
    R1 1 2 220
    D1 2 0 LED

    .model LED d(IS=1e-14)

    .control
    tran 0.1ms 50ms
    print V(2) > voltage_output.txt
    .endc
    .end

    
output

    ngspice -b circuit.cir

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

voltage_output.txt

    head voltage_output.txt
                     * simple led circuit simulation with dc source
                     Transient Analysis  Tue Nov  4 20:24:05  2025
    --------------------------------------------------------------------------------
    Index   time            v(2)
    --------------------------------------------------------------------------------
    0       0.000000e+00    7.318156e-01
    1       1.000000e-06    7.318156e-01
    2       2.000000e-06    7.318156e-01
    3       4.000000e-06    7.318156e-01
    4       8.000000e-06    7.318156e-01
