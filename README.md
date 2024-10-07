java c
Foundations of Applied Mathematics
MATH 4700 – Fall 2024
Homework 2
Due Thursday, October 3 at 12:00 PM
This homework has 100 points plus 65 bonus points. Full credit will generally be awarded for a solution only if it is presented both correctly and efficiently using the techniques covered in the class and readings, and if the reasoning is properly explained. You will not generally receive full credit, even for a correct answer, if your method of calculation is substantially less efficient than what you should be able to do based on the class. Substantial points on each problem will be associated with explicit statements concerning each concept you are using, and explanations for any numbers introduced in your calculations. You should simplify your expressions and answers as much as possible (either as a decimal or fraction), unless otherwise specified. If you score more than 100 points, the extra points do count toward your homework total.
1. (20 points) Use perturbation theory to obtain an approximation for all small real-valued roots of the equation
sin x − ϵ cos x = x
where 0 < ϵ ≪ 1. Your approximation for each root should consists of a nonzero main term plus one nonzero correction term. As always, you should also include a formal term describing the order of magnitude of the error in the approximation.
2. (20 points plus 35 bonus points)
(a) (20 points) If ϵ is a small positive number (0 < ϵ ≪ 1), construct a good approximation for the largest real-valued root x∗ (in the sense that x∗ ≥ x′∗for any other real-valued root x′∗) of the equation
ϵ(x2 + x−1) = 3 (1)
Your answer should consist of a nonzero main term, the most important nonzero correction term, and an estimate of the error of your approximation. Be sure to fully justify your reasoning. You won’t be penalized if you want to calculate all the roots, so long as you find them correctly, but you won’t get any bonus points either.
(b) (10 bonus points) If ϵ is a small number (|ϵ| ≪ 1), construct a good approxi-mation for the largest real-valued root x∗ (in the sense that x∗ ≥ x′∗for any other real-valued root x′∗) of the equation
ϵ(e2x + e−x) = 3
Your answer should consist of a nonzero main term, the most important nonzero correction term, and an estimate of the error of your approximation. Be sure to fully justify your reasoning.
(c) (10 bonus points) Use the method of successive approximations, with two iter-ations from a starting value, to obtain an alternative analytical approximation to the largest real-valued root of Eq. (1). Note that if the root x∗. you are trying to approximate is going toward infinity, then 1/x∗ will approach 0, and you might try setting up successive approximations on 1/x∗ and then invert the results to get approximations for x∗.
(d) (5 bonus points) Set up a numerical algorithm for your method of successive approximations to evaluate higher order numerical (not cumbersome analytical) approximations to the solution of the largest real-valued root of the equation for various small values of ϵ.
(e) (10 bonus points) Quantitatively compare the results from the method of suc-cessive approximations using N = 2, 3, 4 iterations with both your perturbation theory result from 2a and an accurate root-finding algorithm (probably using an existing algorithm in your favorite numerical software distribution). Document your computational work.
3. (35 points plus 25 bonus points) Consider a spacecraft which is in orbit about a planet. The equations describing its motion are Newton’s laws, which in radial coordinates read:

Figure 1: Schematic of spacecraft in orbit about a planet, viewed from above the north pole of the planet.
The variables and parameters appearing here have the following meaning:
• t is time
• r = r(t) denotes the distance of the spacecraft from the center of the planet.
• θ = θ(t) denotes the angular position of the spacecraft; it ranges from 0 to 2π radians as the spacecraft traces a complete orbit. It suffices for simplicity to consider the spacecraft as always flying above the equator of the planet; the angle θ then just denotes its angular position from the point of view of an observer looking down from the North Pole.
• M is the mass of the planet
• G is the universal gravitational constant (not the same as the gravitational constant g used for gravitational effects near the surface of the earth)
I’ve extended you the courtesy of canceling out the factors of the mass of the spaceship from the problem so you don’t have to fuss with this irrelevant parameter.
Now suppose that a spacecraft has been flying for a while in this exact circular orbit and at time t1 the spacecraft fires its rockets for a short time in the forward direction. This has the effect of slowing down its rotational velocity r代 写MATH 4700 – Fall 2024 Foundations of Applied Mathematics Homework 2
代做程序编程语言 dt/dθ (suddenly) by an amount u but not changing its radial velocity dt/dr. Moreover, assume the rockets are on for such a short time that the position of the rocket moves only a negligible amount during the rocket firing, and the angular velocity of the rocket is only slightly changed from what it was before the rockets started firing. (For those who understand the terminology, this means the same thing as treating the effect of the rockets as an instantaneous small impulse). After the rockets finish firing, the spacecraft’s trajectory will be somewhat different than its original orbit; in fact it may not be circular anymore. In any case, the equations (2) describe the motion of the spacecraft after the rockets finish firing. We want to use these equations to predict how the spacecraft will behave over a few orbits after the rocket firing. Nondimensionalize the equations of motion (2) in an intelligent way to set up for a perturbation theory calculation of the spacecraft’s motion after the rockets have finished firing. You should supply an appropriate and complete set of initial conditions to be applied at the time tf at which the rockets have finished firing, and nondimensionalize these intelligently as well.
Note that for full credit, you should express the equations of motion and initial condi-tions in completely nondimensional terms, with no dimensional quantities remaining. The variables should be properly normalized to prepare for a successful perturbation theory. All new variables and parameters you introduce should be clearly defined in terms of the original variables and parameters.
(a) (25 points) Perform. a perturbation theory to compute the motion of the space-craft after the firing of the rockets, including a main term, one nonzero correction term arising from the rocket impulse, and an estimate of the error of your approx-imation.
You might find it useful to observe the second equation in Eq. (2) can be equiva-lently written as the conservation of orbital angular momentum:

But the calculation can also be done without using this information.
(b) (5 points) Over what time scale would you say your approximation from part 3a remains valid? Provide a clear explanation for your answer.
(c) (5 points) Over what range of distances from the center of the planet can the spacecraft be found after the rocket finishes firing?
(d) (25 bonus points) Solve the equations for the spacecraft’s motion exactly, and show that the results from your perturbation theory are in agreement with the exact solution.
4. (25 points plus 5 bonus points) A microorganism is swimming on a two-dimensional thin film, and feels a slight disturbance from the fluid flow generated by a distant second swimming microorganism moving along the x axis, starting at the origin (0, 0). The equation of motion of the first swimming microorganism under consideration can be written:

with initial conditions
x(t = 0) = 0,
y(t = 0) = d,
θ(t = 0) = π/3
where t is time, (x(t), y(t)) denotes the position of the first swimming microorgan-ism, and θ(t) denotes the orientation (angular direction its head is facing) of the first swimming microorganism. The parameters appearing in this model are:
• v1 is the natural swimming speed of the first swimming microorganism, absent flow disturbances,
• v2 is the swimming speed of the second swimming microorganism,
• d is the initial distance between the two microorganisms (since the first one starts at (0, d) and the second one starts at (0, 0)).
• α and γ are some physical constants representing (in different ways) the strength of hydrodynamic disturbance of the second microorganism on the first
• δ is a regularization parameter proportional to the diameter of the first swimming microorganism
(a) (15 points) Obtain an expression for the trajectory of the first microorganism that indicates a leading order correction to its straight line trajectory caused by the hydrodynamic disturbance from the second microorganism, plus an estimate for the error of your approximation. You may assume δ = 0 for this part, which should greatly simplify the calculations.
(b) (5 points) Over what time scale would you say your approximation from part 4a remains valid? Provide a clear explanation for your answer.
(c) (5 points) Over large times (within the time frame. stated in part 4b), characterize quantitatively how the speed and orientation of the first swimming organism is changed by the disturbance from the second swimming organism. Your answers here should include the simplification from consideration of long times.
(d) (5 bonus points) Provide a precise characterization for when the simplification of setting δ = 0 in the calculation of part 4a could be justified.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
