# ToDo:

# stuff to add

1. General definition of a QEC code
    + encoding and recovery
        + and describe all the parts in detail

2. example and discussion of discretization of errors (not yet done)
    + should i discuss this?

3. include example of noise and describe it as stochastic! (show channel!!)

4. discuss connection, maybe include this somewhere
    + logical error rate <- how does each of the following influences this?!
    + correctable errors 
    + and distance
    + threshold 

6. noise model
    + equations and exmaple circuits?
    + go into more detail behind the assumption of $t$ weight errors -> and why we can call them t weight errros

7. code capcatiy model, as a quantum state transportation case and only noise while transporting

8. computation relation between different error syndromes if both errors are applied consecutive

9. fssa include images as examples
9.1 redo all calculations and half the error -> bootstrap interval of 95% is two times the standard deviation!

10. find paper about bootstrapping
10.1 include image and extend calculations explaining this process

# feedback not implemented yet

0. rework the chapter titles 
1. QEC cycle as numbered enviorment 
2. cosets of centralizer image, do it with the structure before ? at least discuss
3. What to say about nkd codes?
4. cosets of stabilizer group and logical cosets -> make those point clearer earlier -> discuss at some point with maarten
5. states and quotient elements is the similiar as the logical operations and implementation of such operators  (not 1-to-1) 
6. computation relation between different error syndromes, two errors happening in the same detection circuit
7. add results to the abstract
8. use \emph{}

# new stuff

4. Syndrome extraction 
    + add circuit for steane type error correection

0. add principle of fault tolerant check and independency of qec cycles



not used anymore:
% @inproceedings{grover_search_algo,
%     author = {Grover, Lov K.},
%     title = {A fast quantum mechanical algorithm for database search},
%     year = {1996},
%     isbn = {0897917855},
%     publisher = {Association for Computing Machinery},
%     address = {New York, NY, USA},
%     url = {https://doi.org/10.1145/237814.237866},
%     doi = {10.1145/237814.237866},
%     booktitle = {Proceedings of the Twenty-Eighth Annual ACM Symposium on Theory of Computing},
%     pages = {212–219},
%     numpages = {8},
%     location = {Philadelphia, Pennsylvania, USA},
%     series = {STOC '96}
%     }

% % Chemistry molecule algo      
% @article{chemistry_example_algo,
% author = {Alán Aspuru-Guzik  and Anthony D. Dutoi  and Peter J. Love  and Martin Head-Gordon },
% title = {Simulated Quantum Computation of Molecular Energies},
% journal = {Science},
% volume = {309},
% number = {5741},
% pages = {1704-1707},
% year = {2005},
% doi = {10.1126/science.1113479},
% URL = {https://www.science.org/doi/abs/10.1126/science.1113479},
% eprint = {https://www.science.org/doi/pdf/10.1126/science.1113479},
% abstract = {The calculation time for the energy of atoms and molecules scales exponentially with system size on a classical computer but polynomially using quantum algorithms. We demonstrate that such algorithms can be applied to problems of chemical interest using modest numbers of quantum bits. Calculations of the water and lithium hydride molecular ground-state energies have been carried out on a quantum computer simulator using a recursive phase-estimation algorithm. The recursive algorithm reduces the number of quantum bits required for the readout register from about 20 to 4. Mappings of the molecular wave function to the quantum bits are described. An adiabatic method for the preparation of a good approximate ground-state wave function is described and demonstrated for a stretched hydrogen molecule. The number of quantum bits required scales linearly with the number of basis functions, and the number of gates required grows polynomially with the number of quantum bits.}}


# Master Thesis Structure

# Title: Circuit Level Characterization of Steane Type Error Correction

# Abstract

Fault-tolerant quantum computing relies on quantum error correction (QEC) schemes whose performance can be characterized by a threshold: a critical physical error rate below which logical errors can be suppressed by increasing the code distance. In this thesis, we investigate the threshold for Steane type error correction circuits which perform syndrome extraction by logical encoded ancillas in a fault-tolerant and single-shot setting.
We determine the logical error rate under circuit-level noise model with faults in both gate operations and measurements, assuming access to fault tolerant logical ancilla preparations. Decoding is performed using an efficient maximum likelihood decoder designed for the surface code and compared to minimum weight perfect matching. 
We find that the threshold are beautiful and amazing ... as compared to ...
We investigate single shot properties of steane type syndrome extraction by computing the threshold as function of the number of rounds and compare with standard repeated surface code syndrome extraction under circuit level noise, using the same decoders (ML, MWPM).
We find ....

Topic XY require further investgation

# Overview (Write first)

Rough intro to Quantum Computing 
    +  

Rough intro error correction

With rapidly increasing number of qubit in QC platform ...
We can pay the tradeoff of more physical qubit for a faster operation.
Constant (in time) overhead ft qec (Gottesmann paper)
luis likes historic overviews: development of fitting plattforms

The performs of a code is charactized by the threshold, ...,
and to calculate this under realistic conditions we have to take into account that errors occur in every part in the circuit even in the QEC, so called circuit level noise.

Overview of requirements for the platform


## Overview of the thesis

The thesis is organized as follows:

1. describe each chapter and what can be found there, what is interesting for the reader 


# Quantum Computing (How do I do nothing)


## ideal Quantum Circuits and Quantum Memories

0. Why should we do quantum experiment, name some interesting advantages/algos

0. concept of quantum memory experiments
    + show a circuit with the basic principle





# Quantum Error Correction (QEC)

Motivation: Why is it needed, and what are the basic prinicples
    + Example

0. What is the basic theoretical idea behind Quantum error correction 
    + Encode log data in higher dimensional hilbertspaces 
    + Use redundancy for error correction
1. what are the main problems/Why doe we need Quantum error correction?
    + (no clone theorem) find better arguments xD
        + this is not really the problem <- does exist in classical computing as well
    + measurements collapse quantum states 
    + find some good papers to cite
2. What is the definition of a successful recovery
    + -> concept of FT recovery/residual error


### Threshold Theorem

0. why is the concept of threshold relevant
1. explain how to determine threshold (may be later?)

Meaning of threshold vs distance for the capacity of a code (maybe a bit to early)

## Stabilizer Codes and their Structure

0. What is a stabilizer code
    + Concept of code stabilizers 
    + Resulting Group structure:
        + Stabilizer Group
        + Centralizer and Cosets
        + Pauli Group and how it is detectable
    + Principle of Syndrome and why it is not enough -> leads to Decoding Problem
1. Code distance and correctable errors
    + uncorrectable vs undetectable
    + here talk about the difference between threshold and distance?
2. General Properties of stabilizer codes
    + Are all stabilizer codes CSS codes? No!
    + Setup introduction to Surface/Toric codes

### Unrotated Surface Code

0. Defintion & Structure
    + logical and stabilizers
    + Scaling with distance 
    + Properties (Transversal CNOTs)
1. Benefits  
    + in comparison to toric code/planar
    + and some scientific consensus
2. Existence of Rotated Surface code and reasons why we did not choose this one
3. Footnote/comment on the existence of a phase transition and the existence to the RBIM mapping 

#### Logical State prepartion/Preparation of Logical States (ToDo)

0. Important for steane type error correction
0. How are we preparing a logical |0> / |+> state,
    + show that they are logical 0 or +
    + talk about pauli frame tracking -> random coset of centralizer 
    + still observable fixed to be correct 
        + tricial but not that trivial
1. FT preparation for arbitrary distances is an open problem? correct?!
        

## Pauli Error 

0. What are real world physical noise process (some examples)
1. How to find a good theoretical approach to model those
    + assumption model them as pauli errors
1. introduce 
    + bit-/phase- flip noise
    + introduce depolirizing noise

### Code Capacity Model

0. Just errors on data qubits
1. Simplest model
    + Surface code is designed for this model 
2. describe the resulting error model

### Circuit Level Noise

0. Ancilla qubits and gates are faulty 
    + more realworld like
    + motivate the need to think about syndrome extraction
0. concept of fault tolerance and residual error
    + error on qubits only with prob p
1. Principal of fault tolerance check
2. Add two qubit depolirizing noise 
3. describe the resulting full error model

#### Phenomological Noise Model

0. Defintion
1. Why useful?


# Syndrome Extraction

0. talk about influence of circuit level noise 
    + -> need to think about a smart way of syndrome extraction
1. ToDo: How does the group picture change?
    + can we find a nice way to express this?

## 'Basic'/repeated Surface code ancilla syndrome extraction ciruit

0. Talk about basic layout
    + for code capcity case
    + explain concept of hook error 
2. error on ancilla qubit and how they propagate through correction
    + -> not fault tolerant
    + -> d repeated measurements needed (ToDo find good paper)

## Steane Type Syndrome Extraction = Steane Type Error Correction

0. Log trival operations
1. Error Propagations through CNOTs
Resulting Conditions:
0. Works for all codes with transversal CNOTs (-> CSS Codes)(understsand <- direction )

Properties:

0. Discuss Ordering 
    + X/Z vs. Order symmetry
1. Discuss how to treat residual error and why it is still correctable
2. Discuss trade offs 
    + change more space requirement for less time requirement
    + Footnote: Discuss One Shot
3. Discuss State Preparation problem?
    + TODO!
    + Aware that is a weak point


# Decoding 

0. From Syndrome to Correction
    + Explain in Group picture image
1. How to find the correct Recovery
    + different approaches 
2. definiton of logical error rate 
    + how to count logical errors

## ML Decoding

+ Use algorithm blocks to use the preexisting structure to make a clear structured argument how ML works

+ First for code capacity noise

0. Definiton using group structure
    + show to be optimal decoding strategy
1. Why is it hard?
    + scaling
2. Note the 1-px pz, mistake 

## MWPM Decoding

+ Use algorithm block!

+ keep short/appendix

0. Definiton: Perfect Matching on the Matching graphs 
    + uniform p -> shortest error chain -> cyclic in p
1. Shortly Describe the Method, Principal of matching Graphs (how much detail?)
2. Describe benefits and disadvantages in relation to ML 
3. Talk about time correlated MWPM?
    + this is needed for Multi Round experiments 

### Different level of information 

...


## Pauli Frame Tracking

0. Motivate uses case 
    + Express as virutal correction (by change of next input, in case of clifford)
1. Introduce basic concept 
    + track pauli (all clifford)
    + save on needed physical gates
2. Relevance in this work 
    + given that all operations are non clifford

# Propagated/Effective Error Model  

+ Put details here

# Implementing Steane Type Syndrome Extraction (Appendix)

+ generate Syndrome and Observable

0. Stim
Describe Circuit:
1. State prepartion circuit:
    + State prepartion Circuits and their variants
    1. starts in arbitrary Coset -> Pauli Frame Tracking
    2. ToDo: different ways of simulating FT log prepared states

2. Steane Type Error Correction:
    1. Order vs X-/Z-Symmetry
    2. Detectors need to be deterministic 
        + not truly pauli frame tracking but similar (tracking base syndrome)
        + only trigger on change
    3. Repeat for Multi Rounds

4. FT-Check
    1. Final Error Free Syndrome Extraction -> Check if observable is recoverable up to corretable error
    2. Motivate why we can use MWPM regardeless of other Decoding choice
        + fall back to p beeing cyclical in MWPM

5. Observable
    1. Shortly discuss the influence of different choices of logical observables

Stim generates Syndrome and observable result. 

Modifiable parameters of Circuit

0. Distance
1. Rounds
2. Observable
    + X
    + Z
    + ToDo: X & Z
3. Noise Model
    + Code capcity
    + Circuit Level Noise
4. State Preparation (ToDo)
5. Order 
    + not implemented for reasons -> symmtry (ToDo, just to show)

## Implementation of Decodings

0. given Syndrome -> determines correct Prediction
1. all assume independet X and Z noise (could implement for correlated noise (TODO?))

### ML* Implementaion:

0. Propagate Error Model -> split up 
    + discuss if we find anything interesting in this new model
1. use newly calculated phenomological noise model for ML Decoding
2. Discuss if this is truly ML implementation
3. Discuss numerical imprecission Problems
    + quantify those (TODO)


### MWPM Implementation:

1. All knowing:
    + just pymatching over the full circuit, more info
2. comparable amount of information     
    + assuming perfect syndrome extraction (compare ML to MWPM)
    + DEM from basic surface code (noise rate not relevant, short discussion)
3. Mutliple rounds correlated MWPM, but with perfect syndrome extraction
    + Shortly discuss problem in using pymatching
    + TODO acutally implement this


## Comparison: Surface Code repated measurements (standard way)

0. shortly describe the difference
1. find good argumenation why we need d rounds of measurement readout for ft


((einordnen in das übrige))
## Different Runs

### Single Round

1. MWPM: all info
2. MWPM: assume perfect syndrome extraction for surface code 
3. ML: assume perfect syndrome extraction for surface code 

### Multi Round

1. MWPM: all info
2. MWPM: repeated single round decoding (TODO)
    + point out difference: aka change of incomming state
3. ML: repated single round decoding

### How to determine Threshold aka. FSSA/Data collapse

0. describe implementation
1. argue why per round is not needed 

((end))

## Finit Size Scaling analysis aka. how to determine threshold (Move to a different point in the thesis)

0. Motivate on why we need this:
    + determine thershold
    + threshold beeing a oder/unorder transition as described in ML chapter
0. explain how this methods works 
0. show assumptions 


# Results

Short note on implementation

## Code capacity Setting  (may move to implementation)

+ benchmarking
0. show basic curves, show threshold and determined threshold and fssa results
1. compare to literatur values to determined threshold
2. discuss difference to literatur (small scale effects)

## Single Round Steane Type Error Correction

1. Compare different decoding strategies 
2. compare different observables -> show difference in order

## Mutli Round Steane Type Error Correction

1. Show threshold develops over multiple rounds
    + compare decoder
    + compare observable
2. compare to repeated

## Different State Preparations 

Show obvious approaches would not work



## Discussion

More details, comparison between the methods

# Conclusion

Hightlight the interesting parts 

If we can afford more qubits, we can get a higher threshold.

Look for qubits error rates of platforms:
    + atomic qubits -> trapped ions, neutral atoms 


## Outlook
Replacing Surface code with other codes is not interesting in the context of steane type error correction.

FT State preparation investigation arbitrary distances and so


# Appendix

Implementation Details
