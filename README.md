# Assignment-7

# Calculating the stress by Boussineq's Theory
Q= int(input("Enter the value of given load : "))
z= int(input("Enter the distance of vertical stress : "))
r= int(input("Enter the distance of horizntal stress: "))
stress = (3*Q*(1/(1+(r/z)**2)) ** 2.5)/(2*3.14*(z**2))
print("The value of stress is", stress)

# Stress when Radius is Constant
Q = float (input("Enter the value of Load in kN: "))
M= int (input ("Number of data values of depth: "))
pi = 3.14159265359
r = float (input("Radial Distance: "))
Z = []
for j in range (1, M+1):
  print ("Enter depth in z".format (j))
  Value_Z = float (input ()) #this line was not indented correctly, causing the error
  Z.append (Value_Z) #this line was not indented correctly, causing the error
  Stress = ((3*Q)/(2*pi*Value_Z* Value_Z)) * ((1/ (1+ ( (r/Value_Z) **2))) )**2.5 # Q was missing
  print ("Stress: ", Stress, " kN/m^2")

  # To Determine the bearing capacity of soil with water table
BulkDensity =float(input("Enter the value of Bulk Density of soil:"))
SatDensity = float(input("Enter the value of Saturated Density of soil:"))
WaterDensity = float(input("Enter the unit Weight of Water:"))
Df= float(input("Enter the value of depth of footing:"))
Dw = float(input("Enter the value of water table above footing level:"))
Dw1= float(input("Enter the value of Water table below the level of footing:"))
B = float(input("Enter the value of width of footing:"))
Nq= float(input("Enter the value of Nq:"))
N = float(input("Enter the value of N gamma (N):"))
SubDensity = 0  # You need to assign a value to SubDensity
SatDensity = 0   # You need to assign a value to SatDensity
WaterDensity = 0 # You need to assign a value to WaterDensity
print ("Submerged Weight of soil is:", SubDensity)
# The bearing capacity of soil when water table is at ground
print ("CASE A")
qu= (SubDensity* Df*Nq) + (0.5*0.8*B*SubDensity*N) # Changed Ng to Nq
print ("The value of ultimate bearing capacity of soil is:", qu)
# Approximate calculation of Bearing capacity of soil is.
Rw= 0.5 + 0.5*(Dw/B)
print ("The value of Rw is:", Rw)
Rw1 = 0.5 + 0.5*(Dw1/8)
print ("The value of Rw1 is:", Rw1)
qu= (BulkDensity*Df*Nq*Rw) + (0.5*0.8*3*BulkDensity *N*Rw1) # Changed Ng to Nq
print ("The value ultimate bearing capacity of soil is:", qu)
# Case B
print ("CASE B")
qu= (BulkDensity * Df*Nq) + (0.5*0.8*8*SubDensity) # This line has a syntax error, it's unclear what the intended calculation is.
print ("The value of ultimate bearing capacity is:", qu)
Dw = float(input("Enter the value of water table above footing level:"))
Dwl = float(input("Enter the value of Water table below the level of footing: "))
print ("The approximate value of ultimate bearing capacity is: ")
Rw = 0.5 + 0.5*(Dw/B)
print ("The value of Rw is:", Rw)
Rw1= 0.5 + 0.5* (Dw1/8)
print ("The value of Rw1 is:", Rw1)
qu= (BulkDensity * Df * Nq * Rw) / (0.5 + 0.8*8*BulkDensity * Rw1) # Changed Ng to Nq and corrected NR1 to Rw1
print ("The approximate value of ultimate hearing capacity is: ", qu)
# Case C
print ("CASE C")
x = float(input("Enter the value of depth of water below footing:"))
# Assuming you have defined BulkDensity, SubDensity, B, and N elsewhere
qu = (BulkDensity * Nq) + (0.5 * 0.8 * ((BulkDensity * x) + (SubDensity * (B - x)) * N)) # Changed Ng to Nq
print ("The value of ultimate bearing capacity is:", qu)
Dw = float(input("Enter the value of water table above footing level:"))
Dw1= float(input("Enter the value of Water table below the level of footing:"))
print ("The approximate value of ultimate bearing capacity is:")
Rw= 8.5+ 8.5*(Dw/B)
print ("The value of Rw is:", Rw)
Rw1 = 0.5 + 0.5*(Dw1/8)
print ("The value of Rwl is: ", Rw1)
qu= (BulkDensity * Df * Nq * Rw) + (0.5*0.8*8*BulkDensity*N*Rw1) # Changed Ng to Nq and corrected the typo Bulk_Density to BulkDensity
print ("the value of ultimate bearing capaciy is:", qu)
