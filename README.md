# Digital-Communications-Matlab-Simulink-Project
A Simulation for the performance of different modulation schemes, BPSK, QPSK, FSK, QAM(16-64) in an AWGN environment.

## Some General Paramters Tuning
1. In Random Integer Generator:
* Sample Time = 1
* Samples per frame = 1000

2. In case of using the Raised Cosin Filter, I choose the following values:
    1. In AWGN Channel:
    * Filter span in symbols: 16
    * Receive delay: 16
    * Input samples per symbol & Output samples per symbol: 2
    * Eb/No : EbNo, a variable in base workspace