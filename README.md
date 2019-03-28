# Digital-Communications-Matlab-Simulink-Project
A Simulation for the performance of different modulation schemes, BPSK, QPSK, FSK, QAM(16-64) in an AWGN environment.

## Some General Paramter Tuning
1. In Random Integer Generator:
    * Sample Time = 1
    * Samples per frame = 1000

2. In case of using the Raised Cosin Filter, I choose the following values:
    1. In AWGN Channel:
    * Filter span in symbols: 16
    * Input samples per symbol & Output samples per symbol: 2
    2. In Error Rate Calculation block:
    * Recieve Delay = 16
    
3. To generate BER gragh:
    * add a sink block paramter
    * make Eb/No = EbNo, in AWGN channel
    * IN Error Rate Calculation block:
        * checkbox stop simulation
        * Target number of errors: maxNumErrs
        * Maximum number of symbols: maxNumBits
    where EbNo, maxNumErrs and maxNumBits are variables in the base workspace

### BPSK Binary Phase Shift Key
* M-ary = 2
* Number of bits per symbol: 1
### QPSK Quadrature Phase Shift Key
* M-ary = 4
* Number of bits per symbol: 2
### QAM16
* M-ary = 16
* Number of bits per symbol: 4
### QAM64
* M-ary = 64
* Number of bits per symbol: 8
### FSK Frequency Shift Key
* M-ary = 8
Number of bits per symbol: 3

* Note: in QAM, BER curve sometomes goes down than the theoretical one, which is not ture, but i can't fixed it till know.