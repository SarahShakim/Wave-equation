# Wave-equation

## The wave equation describes the propagation of waves under ideal circumstances using the partial differential equation.

![image](https://user-images.githubusercontent.com/58648072/130010554-c7bdb4f1-5a46-4da5-9445-31cb17858a09.png)

## There are two second partial derivatives. One that describes time and one that describes space.

The solution is computed using 4 steps:

1. Error checking is done to ensure that  ![image](https://user-images.githubusercontent.com/58648072/130010734-62eaed7f-f41e-426a-87eb-a2581cfd1974.png). If that condition is not met, the calulated ratio as well as the acceptable nt value should be provided. 
2. Initilize the matrix as well as the boundary values
3. Solving for the next column using Euler's method
4. If there are insulated boundary conditions, after the interior points of the column has been evaluated, it has to be readjusted to account for the insulated boundary conditions. 

**Example: Solving the wave equation using the command [x4a, t4a, U4a] = wave1d( 1, [0, pi],  10, [0, 10], 42, @u4a_init, @du4a_init, @u4a_bndry ) and displaying the solution using mesh( t4a, x4a, U4a )**

![image](https://user-images.githubusercontent.com/58648072/130011069-31fd3024-d443-4059-a4f2-e63e20ac57d8.png)

![image](https://user-images.githubusercontent.com/58648072/130011088-1d7eab24-6587-4806-9dee-39e762b46cdb.png)

**Example: Solving the wave equation using the command [x4a, t4a, U4a] = wave1d( 1, [0,pi],  10, [0, 3\*T], n_t, @u4a_init, @du4a_init, @u4a_bndry ) where one of the boundary conditions is insulated.**

![image](https://user-images.githubusercontent.com/58648072/130011359-6b2d2aa5-46d5-48d1-a4e1-7eac268384a6.png)

_Because there is an insulated boundary at one end, when it gets to that end, the wave will travel in a reflected direction rather than going back in the same direction. The period in both direction is the same however they are shifted due to the insulated boundary._

![image](https://user-images.githubusercontent.com/58648072/130011493-3e0d650a-33ea-4d64-9ac9-8c9f74cafee7.png)
