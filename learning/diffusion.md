Feb 21 2025

i implemented heat diffusion like this 
def heatDiffusionBetweenLatitudes(temperatures, diffusionConstant, timestep):
    return diffusionConstant * (np.roll(temperatures, -1) - 2 * temperatures + np.roll(temperatures, 1)) * timestep

with diffusion constant of 0.1 and 60s timestep

this is what the max temperatures in my lat,lon grid were for each timestep
250.00112769617297
250.00233089529152
250.0045306209875
250.01476772534932
250.06621872212767
250.30691895316698
251.4317238454694
256.7300714097802
281.8417455859569
401.47144439542586
973.7878203580125
3721.441574195733
16938.83949118047
77633.79541104453
321137.35459848074
5960354869381.694
3.2514037469461993e+38
1.2592936530244058e+141
overflow

when i turned diffusion to 0, the max temps were
250.00111744140625
250.00223487785135
250.00335230772887
250.00446972943243
250.00558714135562
250.00670454189205
250.00782192943535
250.0089393023792
250.0100566591172
250.0111739980431
250.01229131755056
250.01340861603333
250.01452589188517
250.01564314349986
250.01676036927122
250.0178775675931
250.01899473685936

im having a little bit of a hard time grasping what's happening because i do have outgoing radiation 
def outgoingRadiation(greenhouseCoefficient, temperature):
    stefanBoltzmannConstant = 5.67e-8
    return (1 - greenhouseCoefficient) * stefanBoltzmannConstant * (temperature ** 4)

and i dont understand why this didnt explode with temperature. although now that i write it i mean if you have 10^100 even 50% of that is still a massive number so the outgoing radiation likely did explode but the exploding factor was so big that it overflowed inspite of this

what really seems to be happening is that with a high diffusion constant, the temperature at the equators quickly diffused away to the poles over and over. and the outgoing radiation did try to keep up but so much heat was being stored by the poles that it exploded. but this doesn't really make sense to me either. if diffusion is 0 that means no energy is being pushed away from the latitude it lands in. i didnt make any change to the total amount of heat energy coming in to the system or how much was removed, how did temperature possibly explode like this?