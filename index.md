<link rel="stylesheet" href="style.css">

# Glucometer Project Home
 
[Home](#home) | [Proposal](#proposal) | [Current Work](#work) | [Code](#code) | [Team Photos](#team)

<div id="home"></div>
<div id="proposal"></div>
<div id="work"></div>
<div id="code"></div>
<div id="team"></div>


<div class="tab-content" id="content-home">
  <h2>Home</h2>
  <p>Welcome! Overview of project will go here...</p>
  <p>This GitHub page will be used to store my work for a group <a href="https://bpaulina25.github.io/CBE3300B/">  glucometer project </a>.</p>
  <p>Until then, click around to learn more about what I'm working on!</p>
</div>

<div class="tab-content" id="content-proposal">
  <h2>Proposal</h2>
  <p><b>Review of glucometer electrochemical reactions</b></p>
  <p>Glucose monitoring devices are currently dominated by electrochemically mediated analytical techniques. The main governing reaction in glucose concentration determination is the aerobic oxidation of glucose, shown below. The chemistry involved is the oxidation of glucose via the enzyme glucose oxidase (GOx) to produce glucono-d-lactone (GNL). The dissolved oxygen re-oxidizes the enzyme, producing hydrogen peroxide in molar equivalence.
  <ul>
  <li>a-D-glucose <--> b-D-glucose        (1)</li>
  <li>b-D-glucose + O2 -GOx-> H2O2 + GNL  (2)</li>
  <li>H2O2 --> 2H+ + O2 + 2e-             (3)</li>
  <li>O2 + 4e- --> 2O2-                   (4)</li>
  </ul>
  <p>A relatively high stock concentration (250 g/L) of b-D-glucose in PBS will be used for preparing dilutions of experimental blood serum simulant. If preparation of fresh glucose is needed, time for anomeric equilibrium be taken into account (1), as glucose oxidase (GOx) is only active on the b-D glucose conformation (2). Otherwise measurements will not be reliable due to fluctuating b-D-glucose concentration. As shown in (2), the amount of dissolved molecular oxygen present and H2O2 produced is in molar equivalence with the glucose, and electroanalytical methods can be employed to measure the current generated at the electrode and determine glucose concentration in whole blood/blood serum. H2O2 is an electrochemically active species, and is oxidized on the test strip (usually a Pt anode) in the form of (3). Monitoring the amount of oxygen consumed via Clark electrodes (4) can also allow for glucose concentration determination using selective oxygen reduction. </p>

  <p>These preceding reactions represent the enzyme interactions of first-generation blood sugar test strips. However, the limitations of this approach are mainly due to oxygen’s poor performance as an electron acceptor due to its reduced solubility of oxygen in blood and susceptibility to oxygen deficit [add link]. Additionally, measurement of H2O2 concentration via amperometric methods tended to require high operating potentials for sufficient selectivity [add link]. Thus, mediator ions were integrated into second-generation glucose biosensors to more accurately measure glucose concentration-dependent current generation. In these test strips, the enzyme is re-oxidized by the mediator. Then, the mediator reagent is re-oxidized at the anode surface, generating an electrical current proportional to the concentration of glucose. Ferrous compounds like ferrocenes and ferricyanide are a common selection due to high stability in both  oxidized and reduced states. 
   
  <p>The test strips (AimStrip Plus Mini) used in our system are second-generation glucose biosensors that use potassium ferricyanide as the mediator, according to the SDS [add link]. Therefore, determination of electrode-type is not needed and amperometric analysis for the ferri/ferrocyanide couple can be implemented in our glucometer.</p>
  
  <p><b>Analytical methods: Chronoamperometry</b></p>

  <p>In chronoamperometry, a step potential is applied to induce the Faradaic electron transfer that can be characterized by existing equations for diffusion controlled current generation. Prior to step potential, the potential of WE is held as a value that produces no faradaic electron transfers. Then a sufficiently lower/higher potential is applied to produce the desired reduction/oxidation of the target species. The Cottrell equation, below, will be used to construct the glucometer calibration curve between current and glucose concentration. (add) </p>
  
  <p>In the case of ferri/ferrocyanide (assuming sat'd Ag/AgCl RE), the minimum step potential can be estimated from available data. The equilibrium potential for the RE vs. SHE is +0.197 V [link] and for ferri/ferrocyanide it is +0.356 V [link]. It follows that E = + 0.356 V - 0.197 V to give an estimated 160 mV as the expected step potential minimum. This will need to be experimentally confirmed. Trials will be conducted over a range of step potential values to assess a suitable positive applied potential to generate a diffusion controlled current (on an i vs t1/2 plot, according to (6)). Calculations can be done to determine an upper limit to the step potential to avoid interference from other oxidizable species in the analyte. Lag time will also need to be experimentally determined to avoid initial double layer charging not modeled in (6).</p>

  <p>The glucometer will function as an amperometric biosensor that will apply the step potential and record the relevant current value, apply the calibration equation, and output the generated glucose concentration calculation. </p>


  <p><b>Preliminary firm-/software development</b></p>
    <ul>
    <li>1. Power on/off buttons and time-out response </li>
    <li>2. CA analyte detection/initiation </li>
    <li>3. Memory - Date/Time syncing and daily averaging or ~100 past readings storage </li>
    <li>     a. <a href="https://www.adafruit.com/product/3800">Itsy Bitsy M4</a> MCU; will look into memory and RAM capabilities</li>
    <li>4. Display configuration </li>
    </ul>

  <p><b>Comparison glucometer device: The <a href="https://www.germainelabs.com/wp-content/uploads/2020/08/AimStrip-Plus-BG-Flyer-02-19.pdf"> AimStrip Plus Meter</a></b></p>
    <ul>
    <li>1. 20-600 mg/dL range </li>
    <li>2. 10 second response time </li>
    <li>3. 300 reading date/timestamped memory </li>
    <li>4. GOx and K3[Fe(CN)6] enables electrode </li>
    <li>5. English & Spanish instructions </li>
    <li>6. Available error grid data </li>
    <li>7. ISO 15197 accuracy requirements </li>
    <li>     a. Above 100 mg/dL: 土 15 mg/dL </li>
    <li>     b. Below 100 mg/dL: 15% margin of error </li>
    <li>     c. Consensus error grid </li>
    <li>     d. Specificity to hypoglycemia is more important </li>
    </ul>  
</div>

<div class="tab-content" id="content-work">
  <h2>Current Work</h2>
  <p>Proposed calibration methodology </p>
  <p> Using a known concentration of a glucose in PBS (40-200 mg/dl?) sample, a range of potentials steps (0-400 mV?) will be applied to determine the minimum potential for a diffusion-controlled current characterized by the Cottrell equation. The minimum potential will be utilized to avoid other oxidizable species from reacting at the higher potentials.</p>
  <p> Lag time before data collection will also be experimentally determined to allow time for the reacion to occur and the exclusion of capacitive current data. </p>
  <p> Once these parameters are determined, a calibration curve can be constructed over the specified glucose concentration range. </p>
</div>

<div class="tab-content" id="content-code">
  <h2>Code & Development</h2>
  <p>Add code.</p>
</div>

<div class="tab-content" id="content-team">
  <h2>Team Photos</h2>
  <p>Meet the  team working on this project!</p>
</div>

