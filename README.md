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

## Phase Shift Keying
In general it's the idea of sending different symbols in same amplitude and frequency, carrier frequency, but with different phases.

### BPSK Binary Phase Shift Keying
The simplest one this family is BPSK where 'binary' refers to the use of 2 phase offsets -one for the logic high and the other for logic low, that's why we just need 1 bit per symbol-and the best case is to have the maximum difference between these offset which is 180 degree.
#### Tuning Paramters
* M-ary = 2
* Number of bits per symbol: 1

### QPSK Quadrature Phase Shift Keying
What if we want the symbol to be represented by more than just one bit -or in case the symbols set includes more than two symbols-, then we use QPSK that allows to transfer two bits of data per symbol. and clearly, the advantage is higher data rate.
For maximum seperation beetween offsets here, it will be 90 degree.
#### Tuning Paramters
* M-ary = 4
* Number of bits per symbol: 2

### QAM16
Following the same idea we know can transfer more bits per symbol.
#### Tuning Paramters
* M-ary = 16
* Number of bits per symbol: 4

### QAM64
#### Tuning Paramters
* M-ary = 64
* Number of bits per symbol: 8

### FSK Frequency Shift Keying
Here instead of changing the phase we change the frequency.
#### Tuning Paramters
* M-ary = 8
Number of bits per symbol: 3

* Note: in QAM, BER curve sometomes goes down than the theoretical one, which is not ture, but i can't fixed it till know.