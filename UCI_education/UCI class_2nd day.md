### Combuston system cooling
'Cool' fuel
'Hot' air
'Great' heat load

Acceptable durability - Industrial
 15,000 hrs between repairs
 30,000 hrs life
Acceptable durabilty - Aero
 1,000 hrs between repairs
 5,000 hrs life

Failure modes & causes
 - Meltdown
 - Distortion/Creep
 - Oxidation, especially for ceramic materials
 - Coking
 - Cracking
 - Corrosion

Radiation
 - Nonluminous gas radiation from CO2, H2O in certain wavelength range
   when the wavelength overlaps each other, the particle absorbs the radiation one another and the radiation on the wall decreases.
 - Luminous Radiation from micro-particle (carbon)
 - Luminosity factor ~ C/H ratio in fuel; more C comes to more radiation (carbon)
 - Beam length : double the size, double beam length, increase radiation on the wall
 - liner wall material : different reflection

**Modern cooling Techologies**
Film cooling
 - louvre series
 - Design point (the distance between louvres)
 - **causes CO** to remain in product gas
Effusion cooling
 - efficient ~ 20% reduction in needed cooling air
 - located after a starting louvre
 - Expensive process (many holes N >10,000)
 - Usually laser drilled
Augmented backside cooling (ABC)
 - Turbulence Enhancement outside of the liner
 - Impingment Jets toward the other side of the liner
Thermal barrier coating (TBC)
Dome cooling
 - Splashplate : deflects high-velocity hot gases, promotes cooling air film, reduces hot spot formation, flow optimization
 - Double Dome : dump plate is cooled down
 - There are solid -> not efficient to attenuate acoustic, and generate CO
Extended surface enhancement
 - Pins or Fins
 - cooling tiles
 - insulating tiles
 - dimple cooling : curved surface should be carefully controlled, otherwise thermal growing happens
 - **Thermal barrier coatings** (TBC):
  > effective with backside cooling
  > Bondcoat layer for differential expansion
  > Thermally grown oxide (TGO) may develop and cracks as it gets thicker (problem)
  > TBC sintering, phase changes (problem)

Ceramic combustor liner
 - lower strength
 - brittle
 - costly
 - attchment problems
 - SiC subject to H2O vapor attack
Injector cooling
 - minor compared to the liner cooling
 - heat loading is considered as much as the liner's
 - Effusion "swirl" cooling
 - impinging tip cooling : large surface tip
 - ceramic injector tip
 - Fuel tube insulation for liquid fuel to prevent choking
Fuel cooling
 - hydrogen is the best gas for cooling
 - Using liquid fuel should be aware of overheated (choking), otherwise it blocks the passages.
Cooling step
1. Parallel cooling : 70 % to injector, 30 % to outside liner
2. Serial cooling : 10 % to hit the liner, 90% to liner->injector

**Modeling**
Liner heat balance
 - can be done with Excel for simple geometry
 - coupling with fluid and solid domains
 - typically not necessary if only interested in combustor exit profile
Validation
 - Embedded thermocouples
 - Irradiated SiC Crystals
 - Temperature sensitive paint on surface (Thermal paint)

### Fuel injector design
**Requirement**
 Stable combustion
 Consistent light off & relight
 Wide operating range
 Acceptable pressure drop
 Low emission
 Dual fuel capability
 Good durability
 Acceptable cost
 Field replacable
 Repairable
 Resistant to fouling and plugging
 Manufacturable

**Challenges**
 burnout
 oxidation/corrion
 fouling/plugging
 fretting : virbrating component damanges the adjoint surface
 cracking/joint failure
 Flashback/Autoignition

Lean-premixed injector
 recirculation by primary air swirler
 Pilot fuel injector
Dual fuel injector
 Gas fuel upstream of liquid fuel circuits
 require purge system to prevent gas fuel from entering dormant liquid fuel circuits

Golden rules
 for swirling airflow
 - SN ~ 0.6 - 1.2
 - angle ~ 40 - 60 degree
 - Larger SN leads to unstable recirculation zones
 - axial swirler produces swirl close to forced vortex
 - radial swirler produces swirl close to free vortex
 for air side dP
 - typlically 3 - 6 %
 - Too low -> flashback propensity
 - Too high -> detrimental engine cycle
 for expansion ratio
 - liner size : x2 - x4 of injector diameter
 - liner length : x1 - x1.5 of liner size
 - 
Can combustors
 generally one injector per can in small engines
 large engines might have as many as 7 injectors
Annular systems
 primary zone defined by H/W ~ 1.2 - 1.7
 number of injectors ~ pi(Ro^2-Ri^2)/(H/W (Ro-Ri)^2)

Effective area
 Ae = Cd Ageom
 Large holes Cd ~ 0.6 - 0.8
 Small holes Cd ~ 0.8 - 0.95
 Swirlers ~ 0.3 - 0.6 (radial) or 0.6 - 0.8 (Axial)

Pressure drop of 1D flow in injector
 DP = 1/(2 rho) (mass_flow_rate / Ae)^2
 DP = 0.5 rho Ve^2 for orifices

Fuel injection through 'spokes'
 Area weighted hole spacing
 Swirl and tube wakes aid mixing
 Entry area should be **larger** than total hole area

Velocity and fuel-air profiles
 Axial velocity is at root to calculating oscillations
 With "flat" profile, easiest to calculate these term

Flashback
 Flame transition -> Flame propagation -> Flame holding
 Flame speed at quenching distance in boundary layer
 Autoignition

Pilot Flames
 partial premixing
 lower swirl
 To stabilize main flame requires 2 - 5 % of fuel flow
 To damp oscillation requires 10 - 15 % of fuel flow

Helmholtz resonators
 Liner features Helmholtz resonators around its periphery
 Resonators can be applied to liner, injector, fuel system

### Liquid Fuel
atomizer, injector, nozzle ... all of these things have been designed to optimates following steps:
- breakup
- heatup
- vaporization

**BREAKUP**
 Reyleigh number : high -> strong inertia -> easy to breakup
 Weber number : high -> easy to breakup, atomization
 Oh = sqrt(We)/Re
 Increasing U,d,rho & decreasing surface tension leads to easy breakup
 Controlling viscosity is not effective to shift the regime
 Secondary breakup : single bubble into various size of mini bubble
 - We_crit = 8/Cd (critical weber number)
 - D_max = 12 X surface_tension_fuel / (density_air X relative_velocity^2)
 - Increasing pressure decreaes the maximum size of atomized fuel

 Mean diameters
  - Sauter mean diameter (SMD)
  - Rosin-rammler distribution function
 Types of injectors
  - singuler : no pumping is required
  - plain jet orifice
  - simplex atomizer
  - plain jet air-blast
 drop size
  - SMD/dt = 4.53 (t/do)+0.0091 for singular
  - SMD ~ sqrt(time)/(relative_velocity sqrt(density_air)) for air-blast
  - SMD ~ surface_tension / relative velocity for promp plain jet
  - there are many empirical equations for injector types in the reference
  - no golden rule for drop size
 Spray pattern
  - linear patternator
  - optical methods
 Superheated fuel injection
  - Flash atomization
  - Very turbulent

**Evaporation**
 The diameter constantly decreases after heatup in steady state
 drop lifetime : D-squared la
  - D0^2-D^2 = lambda X time
  - time_evaporation = D0^2/lambda
 effective evaporation constant
  - accounts for droplet heatup & convective effect
  - drop_mass/drop_life = m/t =(rho pi/6 D^3)/(D^2/lambda)
 Spray
  - average rate of fuel vaporization : n(density_fuel pi/6 D0 lambda)
  - n drops of initial diameter D0
  - FAR = n(density_fuel pi/6 D0^3)/(Volume density_air)
  - mf = (density_air lambda Volume FAR)/D0^2 