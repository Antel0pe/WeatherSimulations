∂t/∂v​+(v⋅∇)v=−1/p * ​∇P+ν∇2v+g

the left side tells us how acceleration of air changes and the right side is the forces that cause air to ac/decelerate

**The Pressure Gradient Force Term**
−1/p * ​∇P

p = density
∇P = pressure gradient

the pressure gradient compares our point's pressure to surrounding point's pressure. we can think about it like spatially where air was moving from and to. if the air moves from low to high pressure, the pressure gradient is positive. if pressure gradient is negative it moved from high to low. you can think of if it as current pressure - previous pressure. if current pressure is lower then gradient is negative meaning we moved from high to low. but to be clear it's not doing current - previous but rather looking at current location to surrounding and if current is lower then high then move from current to high. 

if we ignore density for a moment, air moves from high pressure areas to low pressure areas. so if we have a positive pressure gradient meaning from low to high, the negative sign at the start will tell us to move backwards. so if you went from low to high, the air particle should move backwards from high to low. however if we moved from high to low which means pressure gradient is negative, the negative sign will make it positive and tell us to keep moving forward to high to low. the bigger the pressure gradient the higher the force. 

the density of 1/p is a scaling factor. whatever direction the pressure gradient force is telling us to go in, make it bigger or smaller depending on the density. if density is small, then 1/p will be a bigger number than if density was big. so if density is small theres less particles in the way to prevent us from going in a certain direction. if density is very high there are lots of particles preventing us from going a certain way so even if the pressure gradient is big, the actual movement will be smaller. 

so in general how much pressure there is on our point to move from it's current location to previous or rather nearby locations which is where it would have come from.  

**Viscosity**
ν∇^2 v

this term tells us about the force of viscosity on our point of air. ν is the viscosity and ∇^2 v compares our air parcel's velocity compared to the average of it's neighbors. 

if our air is moving much faster than surrounding air, this number is big. if our air is moving much slower than everyone else, this term is very negative. you can think of this term as how much force is acting on our point of air to make it fit in with the rest of the velocity. so if this term is big meaning our air is moving much faster you can imagine this as a force pushing our air back to slow down to everyone else's velocity. if this number is negative meaning we're much slower than everyone else, this force pulls us forward to speed up. the first v is a scaling factor calling the viscosity coefficient. 

honey is a high viscous liquid, water is low viscous. 

if there's a lot of viscosity in our fluid like honey then we resist movement but if we are then we move forward for a long time like honey. so it basically just says whatever force is acting on our point, strengthen it in whatever direction it was already moving. so if there was a lot of force pushing us back, if we're in honey make it even stronger, resist movement even more. if we're in a low viscous liquid, eh whatever keep moving, slow down eventually. if we were being pulled forward then with high viscous liquid we'd be pulled even more and with low viscous we'd be pulled a little bit. 

so in total how much force is acting for/against us in terms of viscosity of our fluid. 

**Gravity**
just adds gravity downwards force to every point. in general gravity is not exactly the same at every point on earth but the effect is small enough that all but the most advanced models use it as a constant. 

**Local Acceleration**
∂v​/∂t

how fast the wind speed is changing at a single point in time like at a weather station. if wind is getting faster, positive, if wind slowing down, negative

**Advection**
(v⋅∇)v

this term is about how wind speed changes as an air particle moves in a certain direction. so if we're focusing on one wind particle and it's moving at 10km/h north. as it moves into the north cell, there might be wind blowing west and this air particle will be affected by that motion since the conditions that made the wind blow west will start acting on our particle whether that be pressure or whatever. 

this term tracks how our air particle's velocity change in the x, y, z components. how does the x velocity change as we move further x-wards, how does it change as we move further y-wards, how does it change as we move z-wards, and for each of y velocity and z velocity. 

this term isn't about tracking how external forces like pressure cause our air particle to move in a certain direction but how our air particle responds to those forces. the air particle is influenced by external forces but advection doesnt apply them it just tracks the effect of their force on our particle. 

advection captures how our air particle's momentum gradually changes over time as different forces act on it. 