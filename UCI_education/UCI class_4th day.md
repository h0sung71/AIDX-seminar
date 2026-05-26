### CFD Modeling
Anchor CFD with real and Iterate
Results need to be considered on a comparative basis

Process
 - Discretize the domain to form the computational mesh
 - Define Boundary Conditions
 - Mass flow rates, pressures, etc at inlets and oulets
 - Solve iteratively
 - Visualize / Post-process
 - Highly computationally demanding

Mesh Topologies
 - Hexahedral : High quality solution for conditions where the flow is aligned to the mesh (6 faces)
 - Tetrahedral : smear gradients, require more cells than Hex mesh (4 faces)
 - Polyhedreal : Good for cases where the flow is not aligned to any single direction (12 faces), store more information in each cell

Wall Modeling
 - Wall function: log-law boundary layer profile, only applicable when the boundary layer is smoothly attached to the wall, applications: airfoils, cars (rule of thumb 30< y+ <200)
 - Resolve Boundary layer: No assumed boundary layer profile, minimum 5 layers, applications: mixer, injector, swirler (rule of thumb y+ ~1)
 - y+ : normalization of physical boundary layer thickness

#### Turbulence
RANS: solves time-averaged partial differential equations
 - Model all scales
 - turbulent kinetic energy & dissipation rate
 - steady OR unsteady
 - coarse mesh OK
 - Good tool for trial & error 

LES: solves filtered partial differential equations
 - resolve **large** scale only whereas modeling small scales
 - Higher fidelity, more accurate, more computationally expensive
 - Need to resolve 80 % of the kinetic energy - **Fine mesh required**
 - Sub-grid scale turbulence modeled
 - Unsteady only
 - Good tool for final examination

#### With chemical reaction
*Chemical time scales are much smaller than fluid time scales*
Simplify chemistry to a few reactions
 - Fast, but limited accuarcy
 - Mixing time scale can be calculated from turbulent time scale
 - No emission information

Solve the detailed reaction set with acceleration techniques
- Incorporates detailed chemistry
- Computationally expensive and slow

Flamelet based approach
 - Most widely approach for gas turbine combustor CFD
 - Describe the flame within each cell as a flamelet
 - Solve additional transport equations for each of these terms
 - Pre-compute the chemistry, (may with reduced reaction mechanism)
 - Assume the same **diffusivity** regardless of species: H2 is not applicable

#### Sprays
Impractical to track every Droplet
Parcels: Track groups of particles
 - The properties of every particle within each parcel are identical
 - Convergence challenging for regions where the spray is very dense (flow should drive droplets, not vice versa)
 - In the region where the fuel droplet is dominant, the parcels approach slows down the evaporation rate too much 
 - Collision modelling is limited accuarcy

### Combustion instabilities
Low frequency : Rumble, Helmholtz Mode, Cold Tone
Mid frequency : Longitudinal Mode, Circumferential Mode, Azimuthal Mode, Hot Tone
High frequency : Screech, Transverse Mode

**Feedback loop**
Mass flow rate perturbation might occurs in different frequency from imposed.
Flow of fuel and air through injector: m ~ sqrt(delta P)
Flow through combustor exit: m ~ P_chamber/sqrt(T)

t_convection : u' -> q' :  time for reactants to arrive at flame
t_combustion: q' -> p' = t_mixing + t_evaporation + t_reaction
t_acoustic: p' -> u' : time for noise to travel from flame to source of reactants

**Feedback Loop**
Limit cycle amplitude
 - Pressure amplitude at Driving (gamma) = Damping (beta)
 - p' losses equal gains
Mitigation strategies
 - Disrupt likely mode shapes
 - Misalign phases p' and q'
 - Damp p'
 - Baffles
 - Trip Rings
 - Reactive Filters: low pass, high pass, band stop filter
 - Resonator at pressure anti-node
 - Adjusting residence time
 - Increasing pilot

