# Glucometer Project Home
# ![Profile Image](images/image.jpg)


[Home](#home) | [Background/Proposal](#background) | [Current Work](#current-work) | [Code](#code) | [Team Photos](#team)

This GitHub page will be used to store my work for a group <a href="https://bpaulina25.github.io/CBE3300B/">  glucometer project </a>.

# Glucometer Images will go here
# ![Glucometer Image 1](image/sample.jpg)

# Project Overview

# Review of glucometer electrochemical reactions
Glucose monitoring devices are currently dominated by electrochemically mediated analytical techniques. The main governing reaction in glucose concentration determination is the aerobic oxidation of glucose, shown below. The chemistry involved is the oxidation of glucose via the enzyme glucose oxidase (GOx) to produce glucono-d-lactone (GNL). The dissolved oxygen re-oxidizes the enzyme, producing hydrogen peroxide (H2O2)

$\alpha \text{-D-glucose} \rightleftharpoons \beta \text{-D-glucose}$                            (1)

$\beta \text{-D-glucose} + \text{O}_{2} \overset{\text{GO}_{x}}{\rightarrow}$

\text{H}_{2}\text{O}_{2} + \text{GNL}                  (2)

H2O2 --> 2H+ + O2 + 2e-                               (3)

O2 + 4e- --> 2O2-                                    (4)

A relatively high stock concentration (250 g/L) of b-D-glucose in PBS will be used for preparing dilutions of experimental blood serum simulant. If preparation of fresh glucose is needed, time for anomeric equilibrium be taken into account (1), as glucose oxidase (GOx) is only active on the b-D glucose conformation (2). Otherwise measurements will not be reliable due to fluctuating b-D-glucose concentration.  

As shown in (2), the amount of dissolved molecular oxygen present and H2O2 produced is in molar equivalence with the glucose, and electroanalytical methods can be employed to measure the current generated at the electrode and determine glucose concentration in whole blood/blood serum. 

H2O2 is an electrochemically active species, and is oxidized on the test strip (usually a Pt anode) in the form of (3). Monitoring the amount of oxygen consumed via Clark electrodes (4) can also allow for glucose concentration determination using selective oxygen reduction. 

These preceding reactions represent the enzyme interactions of first-generation blood sugar test strips. However, the limitations of this approach are mainly due to oxygen’s poor performance as an electron acceptor due to its reduced solubility of oxygen in blood and susceptibility to oxygen deficit [add link]. Additionally, measurement of H2O2 concentration via amperometric methods tended to require high operating potentials for sufficient selectivity [add link]. Thus, mediator ions were integrated into second-generation glucose biosensors to more accurately measure glucose concentration-dependent current generation. A proposed mechanism is seen below [add link]:

Fe(III)cat-GOxRED + (5)

In these test strips, the enzyme is re-oxidized by the mediator. Then, the mediator reagent is re-oxidized at the anode surface, generating an electrical current proportional to the concentration of glucose. Ferrous compounds like ferrocenes and ferricyanide are a common selection due to high stability in both oxidized and reduced states. 

The test strips (AimStrip Plus Mini) used in our system are second-generation glucose biosensors that use potassium ferricyanide as the mediator, according to the SDS [add link]. Therefore, determination of electrode-type is not needed and amperometric analysis for the ferri/ferrocyanide couple can be implemented in our glucometer.

# Chronoamperometry:

In chronoamperometry, a step potential is applied to induce the Faradaic electron transfer that can be characterized by existing equations for diffusion controlled current generation. Prior to step potential, the potential of WE is held as a value that produces no faradaic electron transfers. Then a sufficiently lower/higher potential is applied to produce the desired reduction/oxidation of the target species. 

The Cottrell equation, below, will be used to construct the glucometer calibration curve between current and glucose concentration. 

i = (6)

In the case of ferri/ferrocyanide (assuming sat'd Ag/AgCl RE), the minimum step potential can be estimated from available data. The equilibrium potential for the RE vs. SHE is +0.197 V [link] and for ferri/ferrocyanide it is +0.356 V [link]. It follows that E = + 0.356 V - 0.197 V to give an estimated 160 mV as the expected step potential minimum. This will need to be experimentally confirmed.  

Trials will be conducted over a range of step potential values to assess a suitable positive applied potential to generate a diffusion controlled current (on an i vs t1/2 plot, according to (6)). Calculations can be done to determine an upper limit to the step potential to avoid interference from other oxidizable species in the analyte. Lag time will also need to be experimentally determined to avoid initial double layer charging not modeled in (6).

The glucometer will apply the step potential and record the relevant current value,
apply the calibration equation, and output the generated glucose concentration calculation.




# Current market glucometer product design features:

Typical features of glucometers currently available include, but are not limited to, the following:

Copy over



# Preliminary firmware development:

Soft power circuit 
Memory – Date/Time
Multiple users(?)
Display configuration
Battery life monitoring
