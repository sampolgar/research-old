F41 = GF(41) # Define the Galois Field with 41 elements
R41.<x> = PolynomialRing(F41) # Define the polynomial ring in variable x over F41
A = Matrix(F41, [
[36, 16, 36, 35],
[8, 16, 5, 13],
[0, 0, 0, 0],
[35, 30, 37, 21],
[4, 34, 24, 20],
[40, 36, 40, 7]
])

B = Matrix(F41, [
[3, 29, 23, 27],
[39, 12, 18, 14],
[0, 0, 0, 0],
[0, 0, 0, 0],
[0, 0, 0, 0],
[0, 0, 0, 0]
])

C = Matrix(F41, [
[0, 0, 0, 0],
[0, 0, 0, 0],
[40, 36, 40, 7],
[4, 23, 22, 34],
[35, 30, 37, 21],
[4, 34, 24, 20]
])

S = vector(F41, [1, 3, 35, 9, 27, 30])

Lx = R41(list(S _ A))
Rx = R41(list(S _ B))
Ox = R41(list(S \* C))

print("Lx = " + str(Lx))
print("Rx = " + str(Rx))
print("Ox = " + str(Ox))
