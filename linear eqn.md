 # System of homogeneous equation 

from numpy import matrix, linalg
import numpy as np

#matrix A elements
NR = int(input("Enter the no of rows:"))
NC = int(input("Enter the no of coloums:"))

print("Enter the elements of cofficienr matrix(A) in a single (line seperated by space):")
Coefficients_Entries = list(map(float,input().split()))
Coefficients_Matrix = np.array(Coefficients_Entries).reshape(NR,NC)

print("Cofficients matrix (A) is as follows:",'\n',Coefficients_Matrix,'/n')

#matrix B elements
print("Enter the elements of coloumns matrix (B) in a single line (seperated by space):")
Coloumn_Entries = list(map(float,input().split()))
Coloumn_Matrix = np.array(Coloumn_Entries).reshape(NR,1)

print("Coloumns matrix (B) is as follows:",'/n',Coloumn_Matrix,"/n")

#soloution of homogenous system of equation using gauss eliminstion method

Solution_of_the_system_of_Equations = np.linalg.solve(Coefficients_Matrix, Coloumn_Matrix)

print("Solution of the system of equations using Gauss elimination method")

print(Solution_of_the_system_of_Equations)