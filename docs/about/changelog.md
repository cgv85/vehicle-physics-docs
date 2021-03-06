# Changelog

This list is a brief summary of the most significant additions to Vehicle Physics Pro along time.
It doesn't include minor changes nor fixes.

Licensees may access the full development details via GIT revision logs:

- [Vehicle Physics Core (Source Code version)](http://projects.edy.es/trac/edy_vehicle-physics-core/log/)
- [Vehicle Physics Core (SDK version)](http://projects.edy.es/trac/edy_vehicle-physics-pro-sdk/log/)
- [Specialized Assets](http://projects.edy.es/trac/edy_vehicle-physics-specialized-assets/log/)
- [Sample Assets](http://projects.edy.es/trac/edy_vehicle-physics-sample-assets/log/)

<hr>

#### June 2018

- New **VPChassisInertia** component that configures a specific set of colliders to represent the inertia of the vehicle chassis. The inertia defines the understeer / oversteer behaviour.
- Support for the **Logitech G29** steering wheel.

#### May 2018

- New individual **Clutch block** that may be inserted in any point of the driveline (note that this block is not a replacement for the standard clutch, which is part of the Engine block).
- New **advanced debugger** component that shows the state values of each block in the driveline.

#### April 2018

- New **snapshot save / restore** feature. Allows to save the full state of the vehicle and completely restore it later. Very useful on automated tests.
- New engine type: **Synchronous Drive**. Simulates a synchronous electric motor that enforces a specific RPMs in the output applying up to a given amount of torque.
- Support for **D-BOX motion platforms** [[D-BOX site]](http://tech.d-box.com/training-and-simulation/automotive/). The new add-on component VPDboxOutput sends all the vehicle telemetry and state to the D-BOX API.
- New **dual-drive steering** vehicle setup for caterpillars (TrackVehicleController). Supports smooth speed transitions and neutral rotation.
- New **Bulldozer controller** (VPBulldozerController) for simulating this very special type of vehicle: engine, torque converter, locked differential, two clutches and two caterpillars.


#### March 2018

- New components for designing and implementing **automated vehicle tests**.
- New automated tests: acceleration times, braking time and distance.
- New feature to **export telemetry data to CSV** for further analysis. This is especially useful in automated tests.

#### December 2017

- New **minimal build mode** keeping the essential vehicle features only.
- Unity menu integration (Component > Vehicle Physics).

#### November 2017

- Major reorganization of files and folders
- New **driveline helper** script for easily building common drivelines.

#### June 2017

- Support for **Multi-body vehicles**. Wheels may now belong to different rigidbodies in the same vehicle.

#### April 2017

- New component **VPTireFrictionModifier** for configuring tire friction for specific wheels.
- New **damper calculation** replacing PhysX's (faulty by design)
- New high-level component for managing the vehicle settings in a comprehensive way (i.e. safe, sport, race...)
- New experimental **bike controller** (two-wheeled vehicle)

#### March 2017

- Suspension may now be modified via vehicle add-ons (VehicleBehaviour).
- Major suspension improvements.

#### February 2017

- New **VPXboxInput** component for simulating gamepads and other devices via XInput.
- Support for **Thrustmaster T500RS** steering wheel.

#### January 2017

- New component for **non-linear speed gauges** (i.e. Volkswagen Scirocco).
- New **VPLiquidCargo** component for simulating sloshing liquids in confined tanks (liquid cargo, fuel tank...)

#### December 2016

- **Custom camera modes**: different camera configurations may now be specified per vehicle.
- Significant performance optimizations based on the profiler data.
- New **VPSelfDrive** component designed to be the building brick for AI and autonomous vehicles.

#### November 2016

- **Electronic Stability Control (ESC)**. Applies the brakes to individual wheels asymmetrically in order to counteract oversteer / understeer.
- **Anti-Spin Regulation (ASR)**. Allows the vehicle to move when one of the traction wheels loses grip. In such case, brakes are applied to the wheel with less traction.

#### September 2016

- New **Steering Aids**: limit the steering angle with speed, automatic counter-steering.
- Added order of execution for the VehicleBehaviour Update and FixedUpdate methods.
- New camera **auto-FoV** feature in the LookAt mode.
- New **Speed Control Aids**: cruise speed, speed limiter.

#### August 2016

- New **Replay system** with rewind & continue, playback forwards / reverse, jump, fast forward / reverse, save and load.
- New VPHeadMotion component for easily setup the driver's view with inertial movements.

#### July 2016

- **Traction Control System (TCS)**. Limits the tire slip by reducing or suppressing engine torque.

#### May 2016

- New **vehicle component protocol**. Vehicle add-on components now inherit from VehicleBehaviour for keeping in sync with their host vehicle.

#### April 2016

- New **fuel consumption model** for combustion engine
- New **VPVehicleJoint** component for easily rigging articulated vehicles
- New **VPDeviceInput** component [[documentation]](https://veh	iclephysics.com/components/vehicle-input/#vpdeviceinput) for using any DirectInput device including force feedback
- New **anti-roll bar** component providing suspension linkage between two wheels
- New **dynamic suspension** component for adjusting suspension with load dynamically

#### March 2016

- New **VPPerformanceDisplay** component [[documentation]](https://vehiclephysics.com/components/vehicle-telemetry/#vpperformancedisplay) providing live performance charts for a variety of data from the vehicle.

#### February 2016

- **Anti-lock braking system (ABS)** [[video]](https://www.youtube.com/watch?v=t0NFt3d-jbg). Releases the brake pressure in each wheel to prevent wheel slip.
- New **vPDamage** component for modifying meshes and wheels with impacts.

#### January 2016

- Major code refactoring.

#### November 2015

- New **retarder brake** feature. Mostly used on transport
- New inspector drawers for blocks and components

#### October 2015

- New **drag factor** for the ground materials.
- New experimental mass scale factor.

#### September 2015

- New ground materials feature: grip, visual effects, audio effects.
- Support for the **Logitech G27** steering wheel.
- New **visual effects** component: dashboard lights and gauges, steering wheel, brake lights, reverse lights.

#### August 2015

- New wheel sleep feature. Keeps the vehicle perfectly steady on slopes.
- New custom gravity feature.

#### From 2010 to 2015

_Code name: NinjaVehicle_

- Engine (incl. torque curves, inertia, idle control, stall)
- Clutch (incl. torque converter)
- Gearbox (incl. manual, automatic, auto-shift, parking mode)
- Steering (incl. ackerman, toe, multi-axle steering)
- Transmission (incl. differential and transfer case settings)
- Axles (incl. brake circuits and steering modes)
- Differential (incl. open, locked, viscous, LSD, torsen)
- Wheels (incl. tire friction, suspension)
- Direct drive motor
- Telemetry
- Brakes
- Aerodynamics
- Dynamics solver
- Vehicle Controller inspector
