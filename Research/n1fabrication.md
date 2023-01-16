# Design and fabrication of model rocket airframe using 3D printing

## Abstract

In this paper, we describe the method to design and fabricate the airframe of the model rocket. Considering the lack of commercially available model rockets in Kenya, we designed and fabricated a low-cost model rocket using 3D printing. The airframe subsystem comprises a nose cone, body tube, fins, and parachute. For the material of the parachute, we chose nylon considering the lightweight and strength. The aerodynamic stability was confirmed by calculating the static margin using Openrocket software. 
We launched the developed model rocket and confirmed each subsystem worked properly. We believe this model rocket will be used for further development of the flight control system. 3D printing allowed us to iterate over the designs and to make changes effectively. 

## Introduction

### Background information

Nakuja is a team of students from Jomo Kenyatta University of Agriculture and Technology (JKUAT) and Pan African University Institute for Basic Sciences Technology and Innovation (PAUSTI). We are focused on learning as we design, build and launch a rocket into the earth's orbit. The project began in June 2019 with the initial goal to design a rocket using a liquid propellant, which remains our primary goal[1]. The culture at JKUAT emphasizes building tangible engineering solutions to solve the needs of humans. This may sound controversial but JKUAT is leading its way in the best engineering universities in the East Africa Region. With this culture deeply engraved in every human that passes through JKUAT, Dr Aoki decide to make space exploration a reality in Kenya. Model rocketry has been a dream for most engineering students and some end up pursuing aerospace and aeronautical engineering. High powered rocketry began in the mid-1980 with the availability of large motors that were safe. Model rocketry was accepted wholeheartedly when the Nakuja project was launch. For a start, we planned to go up to 50m to test the skills we had acquired while reading. This imposed some constraints on the airframe of the model rocket. We decide to go with a 50mm wide body and a 1-metre long rocket. Since we needed to build and test the rockets almost weekly there was no cheaper way of producing model rockets than 3D printing. Additive manufacturing also referred to as 3D printing is a rapidly growing field that is to radically change the manufacturing landscape. With the advent of even chocolate 3D printers, it is safe to assume a lot of research is going on to help achieve that. As the cost of entry for 3d printing continues to fall, material wastage and energy being minimal, smaller production runs which are often faster and less expensive and easy to recreate and optimize parts we saw it as a suitable candidate for manufacturing. We also had in mind PVC which offered some disadvantages at that moment. Additive manufacturing allows the fabrication of digital design parts using a layer by layer additive process, continually adding material to the base layer as you progress up.

### Introduction 2

This study develops and tests a small solid-propellant rocket utilizing additive manufacturing during design and fabrication. For this, we will be using an F class motor, with passive control to be able to fly up to 50m. We carried a small payload inside. Examples of such rockets are model rockets for education and research [2, 3] and rockets for scientific instruments[4]. We subdivided our rocket into modules that were designed and fabricated independently. This design technique is used in smartphones and also cars, where you can control the product more effectively as modules e.g the apple A-series chip. 

## Method

Product modularization is the process of decomposing a complex system into standardized and more easily manageable subsystems with major characteristics:

1. The subsystems are composed of a high percentage of standard off-the-shelf components
2. The subsystems are easily serviceable and recyclable
3. The subsystem itself or any of its components can be replaced or upgraded by the user at will
4. The modular system offers time or cost savings or another significant benefit to the user, compared with a non-modular system for the same task.

All AM parts are, by definition, one-off parts; complex and straightforward , standardized parts are equally difficult to supply . From this data , it's clear that a modularity-based design process for additively manufactured products requires a wedding of both modularity principles and traditional non-modular design principles.

### Rocket design

In order to demonstrate the additive manufacturing-based approach, we designed a simple small solid-propellant rocket. We were using an F65 motor. The diameter was 40mm and length of 200mm. This motor was designed by the propulsion team at Nakuja. This forms our basis of design. We decided to make a 50mm internal diameter and the motor will be mounted using a motor mount and an engine block. We designed 4 parts namely the nose cone, payload chamber, body tube and tail section. Our initial designs were done in openrocket. Head over to Edit then Preference menu. Configure the atmospheric condition. {Insert image of preferences tab}. Since we will be using additive manufacturing we selected black tough PLA since it was readily available. Move over to the materials tab and add the material you are intending to use if it is not included. {Insert the material image}. The next step is to get the thrust curves from the propulsion team. Get the motor thrust curves from Nakuja Propulsion Team for the N1 motor. Found [here](https://github.com/nakujaproject/N1-motor.git). If you want to use the N1 motors created by the Nakuja Propulsion team, go to general settings then under the user-defined curves add N1-motor\ directory, which we have just cloned, inside there. {Insert motor config image}.
Nose cone configs:

* Parabolic series
* Length 250mm

Parachute

* 1000mm Diameter
* 120 mm length of strings

Shroud lines:

* 6mm 0.25 inch
* 8 lines
* 100mm lenth

Shock cord

* 12mm 0.5 inch
* 100mm length

Body tube:

* Inside diameter 50mm
* Outside diameter 53.6mm
* Length 100mm

Altimeter

* Diamater 50mm
* Length 100mm

Electronics bay

* Inside diameter 48mm
* Outside diameter 50mm
* Length 120mm
* Altimeter block at 5mm from the nose cone

2 Extra tube

* Inside diamter 50mm
* Outside diameter 53.6mm
* Length 150mm
  
2 Launch lugs

* Inside diameter 10mm
* Outside diameter 13.6mm
* Length 30mm

Tail

* Inside diamter 50mm
* Outside diameter 53.6mm
* Length 250mm

Trapezoidal fins

* Thickness 3.6mm

Engine block

* Diamter 50mm
* length 10mm
  

### Parachute Ejection

This is how we will eject our parachute so that we can be able to recover our rocket after launch. There are many ways to recover the rocket mainly subdivided into pyrotechnics and non-pyrotechnics. I decided to use non-pyrotechnics as it mainly faults tolerant and easier to make.

One mechanism in DetMech was developed to automatically detach a rocket from its parachute line based on the apogee of the rocket. It is designed to assist in recovering rockets stagged by their parachutes. This method utilizes the use of a servo motor to open and close the hatch in order to eject the parachute.

How it works
The mechanism is based on a simple clamp that holds the latch onto the nose cone. At the appropriate time, after maximum height has been reached with a specified delay, the clamp is moved which releases the parachute. By attaching the latch, nose cone and payload chamber to the parachute you will have a better chance of recovering the whole rocket.

The clamp is made up of a micro servo arm which is made of plastics. The latch on the other hand is made up of tough PLA material used in 3D printing the whole rocket. There can be a large lateral force on the clamp during parachute opening. Aerodynamically, it has a low profile.

The bottom plate, payload chamber, which houses the electronics, is attached to the nose cone with screws rather than being glued due to large forces involved. The main parachute line should be fitted with a shock cord to reduce the stress on the clamp.

There is a little groove is to prevent the latch from moving side to side. This mechanism is controlled by the flight computer. This gives the rocket crew a chance t retrieve the rocket easily.

### Recovery mechanism

This is the actual deployment of the recovery mechanism in slowing down the rocket. This also includes opening latches to push out parachutes.

Some examples of the recovery mechanisms are:

1. Parachutes. This is the most effective method of the recovery system.
2. Side deployment. The parachute is ejected on the outside of the rocket using some kind of spring mechanism
3. Inline deployment. The parachute is ejected along the axis of the rocket.
4. Streamer. It is deployed the same as the parachute.
5. Wings, glider. This is commonly used as a passive control.
6. Changing CG, This involves changing the weight of the rocket in order to shift stability.
7. Changing CP, centre of pressure in order to move air surfaces to change the flight's stability.
8. Balloon. A balloon can be inflated from an internally stored pressure chamber in order to increase the rocket's drag.

For the N1 rocket, we choose the parachute system. This is to slow the rocket to an acceptable descent rate to ensure the survival of the avionics. There is usually a backup system e.g deploying to parachutes or using two different methods.

A parachute is basically a flexible device whose function is to produce drag. It slows down the rocket to a decent speed.

Dual deployment means there is a primary and secondary parachute to reduce the impact. The first is generally stronger to overcome large velocities and stabilize the rocket. The second one is attached to the first one via a tow-line and is used to reduce drift away from the launch site.

A shock cord, rubber band, is used as a gravity coupler. This is to store kinetic energy before opening up the parachute.

The main canopy is attached to the towline to provide a soft landing

{Insert images}

![Parachute Forces](img/parachuteForces.png)

From the diagram above we can clearly see, according to Newton, the addition of more drag (an adverse force) results in a lower acceleration.

{Insert images}

![Newton Second Law](img/Newton2ndLaw.png)

Whether the body decelerates (negative acceleration) or not depends on the velocity and altitude of the parachute deployed.

If the body has a high velocity at parachute ejection, the drag may be greater than the weight.  In this case, the body will decelerate. If the body has a low velocity at parachute ejection, the drag may be lower than the weight.  In this case, the body will accelerate.

Velocity changes so as the drag. At the equilibrium point, the drag is equal to the weight.

If drag starts off lower than weight, acceleration will be positive. This increases velocity and drag. Drag will eventually equal weight and acceleration become zero.

When velocity isn't changing it has reached terminal velocity and it will descend at a constant velocity.

For terminal velocity drag = weight.

The parachute design process needs:

* desired shape
* weight
* drag coefficient
* determine impact velocity
* canopy area

At terminal velocity, the drag should be equal to the weight, 9.8067 N

The drag coefficient itself depends on the Reynolds number Re. For a small enough Reynolds number (of the order of a few thousands or smaller) the dependence is mild and the drag coefficient is approximately constant.

{Insert images}

![Area calculation](img/areaCalc.png)

Hints:

1. Get the atmospheric temperature of where I am testing, [Juja](https://www.accuweather.com/en/ke/juja/828638/hourly-weather-forecast/828638)
2. Calculate the air density of where you are testing, [Juja](https://www.omnicalculator.com/physics/air-density?c=KES&v=P:1013!hPa,Temp:28!C,aaa:1.000000000000000,T:11!C)
3. Check if our area provides the drag equal to the weight, [here](https://www.omnicalculator.com/physics?c=USD&v=Cd:0.7,u:2!ms,rho:1.1661!kgm3,A:6.00702!m2)

### CFD

Now that the designs are established, performance analysis on the rocket designs can begin. In order to guide expectations from the launch experiments and aid in interpreting the results, some preliminary performance knowledge is significant . To estimate these performance characteristics, a digital wind tunnel model was constructed using the Autodesk computational fluid dynamics (CFD). First, the drag coefficients for every of the designs were calculated so as to supply input for preliminary analytical performance analysis. For each of the designs, the coefficient of drag was found at various speeds, from 10 to 100 m/s, and plotted. The fluid tested was air at one atmosphere of pressure, 28 degrees Celsius, and with a medium turbulence factor of 0.05. The cross-sectional areas for every rocket design were identical; the differences in drag were thanks to the varied geometry combinations of fins.
The geometry of each rocket was created using commercial 3-D modelling software and imported into the Autodesk Fusion geometry environment. Within this environment, a fluid domain was modelled around the rocket; the domain was square in cross-section and provided approximately 0.5 m of fluid distance from each surface of the rocket.
Upon geometry and fluid domain definition, the model was meshed using the Autodesk CFD mesh environment. The mesh was set to fine for the entire domain, generating around 1.8 million elements per rocket, 380, 000 of which were in the domain very near the interface between the rocket and fluid.
The centre of mass and centre of pressure for the rocket was found automatically by the software. The airspeed was set within this domain. Convergence tolerance was specified to be 1 × 10−5 with no limit on the allowed number of model iterations.
The model was then analyzed in Autodesk CFD to find the drag coefficients on the rocket bodies. The drag was measured by tracking the force on the rocket body, in the direction of fluid flow, until a steady-state was reached. The average number of iterations to a convergence of 1 × 10−5 was about 650, requiring around 25 min to run for each case.

### FEA

As the drag coefficients were calculated in the previous section, an analytical dynamic analysis can be performed on the rockets in order to predict the flight altitude (apogee). The flight analysis is subjected to the following assumptions:
The air is static (no significant wind); 
The properties of the air remain constant throughout the flight; 
At the top of a time delay following burnout, the rocket motor will stop free-flight motion by ejecting the payload, during this case, an instrument package and recovery system.

## Results

The main purpose of this study was to develop, design, and test an airframe design supported feature modularization into complex parts, rather than part modularization into subassemblies. The rocket airframes utilized in this study were inbuilt three parts; the booster, the payload, and therefore the ogive . In a real aircraft, like a test rocket or missile, the booster section would contain all the propulsion components, the payload section would contain the warhead or instruments, and the nose cone would carry the guidance system and computer. Based on the necessity of the mission and therefore the sizes of the AM equipment available, the amount and scope of the complex parts are often adjusted.
The rockets used in this study were deliberately manufactured out of polylactic acid (PLA) because it is biodegradable and fully recyclable; if any rockets were lost, the pollution to the environment would be minimal. Rockets made up of the quality ABS would be significantly lighter but aren't in the least environmentally friendly or as easily recyclable.

## References

[1]. https://nakujaproject.com/about.html
[2]. Sneider, C.; Kurlich, K.; Pulos, S.; Friedman, A. Learning to control variables with model rockets: A neo-piagetian study of learning in field settings. Sci. Educ. 1984, 68, 465–486. [Google Scholar](https://scholar.google.com/scholar_lookup?title=Learning+to+control+variables+with+model+rockets:+A+neo-piagetian+study+of+learning+in+field+settings&author=Sneider,+C.&author=Kurlich,+K.&author=Pulos,+S.&author=Friedman,+A.&publication_year=1984&journal=Sci.+Educ.&volume=68&pages=465%E2%80%93486&doi=10.1002/sce.3730680410) [CrossRef](https://dx.doi.org/10.1002/sce.3730680410)
[3]. Stein, G. H. Forty Years of Model Rocketry: A Safety Report; Publication of the National Association of Rocketry: Marion, IA, USA, 1997; Available online: [http://www.nar.org/pdf/40years.pdf](http://www.nar.org/pdf/40years.pdf) (accessed on 18 January 2017)
[4]. Wilkening, D. Airborne Boost-Phase Ballistic Missile Defense. Sci. Glob. Secur. 2004, 12, 1–67. [Google Scholar](https://scholar.google.com/scholar_lookup?title=Airborne+Boost-Phase+Ballistic+Missile+Defense&author=Wilkening,+D.&publication_year=2004&journal=Sci.+Glob.+Secur.&volume=12&pages=1%E2%80%9367&doi=10.1080/08929880490464649) [CrossRef](https://dx.doi.org/10.1080/08929880490464649)
[5]. https://www.mdpi.com/2226-4310/4/2/17/htm
[6]. http://vestnikmai.ru/eng/publications.php?ID=116216&mobile=Y
