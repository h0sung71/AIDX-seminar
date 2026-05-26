### Brayton cycle
Compressor: input air low T low P -> low T(theoretically) high P
Combustor : chemical energy -> thermal energy
Turbine :
- for propulsion, the turbine brings the energy to the compressor. In this stage, the pressure does not go down to ambient, to leave the energy for propulsion.
- for stationary, the addtional turbine connected to the generator uses the leftover energy after the first turbine to generate the electricity. 
- Cycle output -> cycle input : heat exchange with atmosphere

### Combustor
primary zone
- separated by primary jets, recirculating some of hot product gas toward injector
- phi ~ 1.4

secondary zone
- dilution jets cooling down the product gas
- phi ~ 0.7

diffusion zone
- phi ~ 0.3

casing
- containing the high pressure gases, sustaining the pressure difference

liner
- containing the high temperature gases injecting primary/dilution jet into the combustor through multiple holes
- the pressure difference is negligible

### Fundamental on Flame
**premixed flame vs non-premixed flame**
 swirl flow generate negative pressure in the core which brings the surrounding air into the center, called recirculation.
- elliptic flow : upstream is influenced by downstream by recirculation

NEXT GENERATION
1) for propulsion rapid non-premixed is selected for stability
2) for stationary fully premixed is selected for emission
3) liner geometry is changed from cylindrical to conical shape.

### Combustion analysis
Mass balance ("stoichiometry ratio")
- defined with complete combustion (no inefficiency and pollutant)
- FAR fuel air ratio <1
- AFR air fuel ratio >1

lean burn
- excess oxygen (**"15%"** oxygen in standard) : this concentration has to be measured in "dry" condition (no H2O)
- CO2 3%
- H2O 4 %
- N2 78%

NOx emission
- 95% NO(major pollutant)
- 5% NO2(yellow color, it is visible!)
- N2O (notrious oxide, major concern for NH3 fuel)
- NOx emission is non-negligible when T>1900 K


Energy balance ("adiabatic flame temperature")
 - enthalpy is conserved
 - adiabatic temperature changes with inlet temperature and vitiation  ratio

**Equilibrium**
 elementary kinetic reaction set
 CH4 heat release chemistry
- fast equilibrium: CH4 -> CH3 -> CH2O -> CHO -> CO
- slow kinetics : CO -> CO2
  expression : CO + 1/2 O2 = CO2
  equation : Kp(T) = b/(fe^(1/2)) (P/n_T)^(-1/2)   
  Arrhenius Equation : d(CO)/dt = -A(CO)(OH)exp(-E/RT)
  control : increased time, increased oxygen, mixing
- fuel pyrolysis : HC, SOOT
  same as CO; fast formation & slow oxygen
  same control strategy
- Thermal NO pollutant
  "slow" formation : N2+O -> NO + N
   Then, fast formation follows : N + O2 -> NO +O
   So, d(NO)/dt = 2 A(N2)(O)exp(-E/RT)
  "Frozen" reduction : no reduction process
  control : reduced temperature (RQL, lean)
- Prompt NO
  CxHy + N2 -> **HCN** + **NHz**
  Control strategy : Rich primary, delay addition of oxygen (for secondary reactions of HCN and NHz)
- Fuel NO
  Quiet much with NH3 fuel
  N + O2 -> NO + O
  N + OH -> NO + H

### Fuels
**Hydrocarbon**
 Aliphatic (straight chains or single-bond rings)
 - Paraffinic hydrocarbons (Alkanes)
   CnH2n+2
   C1 to C4 : gases
   C5 to C19 : liquids
   C20 + : Solids (waxes)
 - Naphthenic hydrocarbons (Cycloalkanes)
   CnH2n
   C-cycle
   similar to paraffins
 - Olefinic (Alkenes)
   one double-bond (unsaturated hydrocarbons)
   chemical active with compounds
   undesirable
 
 Aromatic (alternating single and double-bond rings)
 ex) Benzene, Naphthalene
- Unsaturated hydrocarbons
- lower energy content
- Soot Forming
- Strong Solvents
- Hygroscopicity

**Fuel requirement**
- Pumpability
- High thermal stability
- No filter clogging
- No vapor locking
- High heat content

**Sustainable Aviation Fuels (SAFs)**
- Jet Petroleum-8 (JP-8)
- JET A
- JET B
- Hydrotreated Renewable Jet (HRJ)
- Fischer-Tropsch Derived Fuels

Gaseous Fuel Requirements
- "Superheat" to avoid hydrocarbon condensation
- "Superheat" to avoid Moisture Condensation
- Unwanted components must be removed
- Heavier hydrocarbons separated prior to transporting

### Emission Regulations
- Vented Fuel: At alititude
- Smoke : Takeoff and Climb
- HC & CO : Low IDLE, Ground Idle
- NOx : All high power, cruise

Standard are defined only for landing-takeoff operations (LTO)
Regulatory parameter is mass of emission produced during a prescribed LTO cycle per unit of rated takeoff thrust

Aero engine Emission Standards 
- CAEP/11 (2019): NOx -54% of CAEP/8 by 2027 (~2.5 ppm)
- CAEP/10 (2017): Adopts CO2 emission standard for aircraft
  /> 5,700 kg take off mass or higher
- CAEP/11 (2019): nvPM mass
- No Federal EPA standard for smoke, HC/CO, particulate
- SOx emission <150 ppm

NOx "Entitlement"
- certain curve range vs adiabatic flame temperature
- hydrogen has disadvantage on NOx regulation, since it is regulated based on "mass"; ppmvd@15% O2 for H2 is 37 % higher for CH4
- N2O : important for high pressure lean strategies
  N2 + O -> N2O + O -> 2NO
- Prompt : N2 + CH -> HCN + N (short residence times)
- NNH : important for lean H2
- NOx has dependencies of pressure/residence time in higher equivalence ratio

Smoke
- Aromatics > Alkenes > Alkanes, also correlation with # C-C bonds
### Aerodesign
- The air split ratio is roughly estimated based on effective area ratio
- Air 30 % injector / 22 % primary air / 19 % dilution air / 20% liner cooling / 8 % leakage on interface b/w combustor and turbine
- Air 52 % injector / 0 % primary air for Dry low-emission combustor

- Design Temperature profile
  Tmax = Maximum Recorded Temperature
  T3 = Inlet Temperature
  T4 = Mean Exit Temperature
- Pattern Factor = (Tmax-T4)/(T4-T3) = f(L/D x P/q)
  L = liner length
  D = liner diameter
  p = Liner pressure-loss factor
  q = reference dynamic head
  dynamic velocity = mass/density/area
- Profile factor = (Tmr-T4)/(T4-T3)
  Tmr = maximum circumferential mean temperature
- Turbine profile factor = (T4r-T4des)max/(T4-T3)
  maximum temperature difference between the averaged radius temperature and design temperature at the radius

- Pressure drop
  3 to 6 %
- pressure-loss factor

- Radial Swirler is compacter than axial swirler
- Swirl number = Axial flux of angular momentum / axial flux of axial momentum
- Recirculation is aerodynamic **Spark Plug** : key to stability

- Single jet penetration
  Y/dj = 0.82 J^0.5 (X/dj)^0.33
  J = momentum flux ratio
  only valid for 90 % penetration, initial trajectory
  if the penetration is at angle of theta, Y/dj = Y/dj_90% sin(theta)
  Ymax/dj = 1.4 Y/dj = 1.25 J^0.5 (X/dj)^0.33

- mutliple jet penetration
  Ymax.dj = 1.25 J^0.5 (mg/mg+mj)
  mg : approach gas mass flow rate
  mj : mass flow rate through holes

- Golden rule
  cylindrical liner Ymax = 0.333 D
  annular liner Ymax = 0.4 h

### Diffuser
Transition from **compressor** to **combustion casing**
Converts kinetic energy in the airflow to static pressure
Distributes air to different areas of the combustor
Reduce pressure drop by decreasing flow speed

Condition
- Inlet Mach number ~ 0.3 - 0.5
- Outlet Mach number ~ 0.2 - 0.3
- Does NOT reduce swirl <- should be done by compressor stators
- Maximum expansion angle < 9 degree to avoid separation

Axial Diffuser -> Radial diffuser : used for compact engines, associated with radial compressor, have to be carful with turning flows

Flared diffuser : common design in early gas turbine
Reverse diffuser
Dump diffuser
Split diffuser
Hybrid axial/radial
**Advanced designs**: Boundary layer bleed, Vortex control at the corner

Recovery Factor
Flat wall prediffuser design
Corrections for inlet boundary layer thickness
Flow separation region in curved wall diffuser
