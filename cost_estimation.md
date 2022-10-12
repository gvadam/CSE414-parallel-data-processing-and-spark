Selection: R.a > 200
    X = (max(a,R)-v)/(max(a,R)-min(a,R)) = (250-200)/(250-150)= 0.5
    X * B(R) = 0.5 * 1000 = 500
Block-at-a-time nested loop join: R.a = S.a
    B(R) + B(R) * B(S) = 500 + 500 * 2000 = 1,000,500
Unclustered nested loop join: S.b = U.b
    B(RS) + T(RS)*(T(U)/V(b,U)) = 1,000,500 + (4*10^8)*(10^4/250) = 1.6 * 10^10
Projection: R.a, S.c
    1.6 * 10^10