# Plots
![Pattern](https://zhaoxin-hu.github.io/ECE222A/HW3/P3.jpg)<br/>

# Lines
```matlab
clc
clf
close all


deltatheta = 1;
deltaphi = 1;
M = 16;
N = 16;
kdx = pi;
kdy = 1.2*pi;
ax = 0;
ay = 0;

phi_deg = (0:deltaphi:359);
% phi_deg = phi_deg([2:178,182:358]);
phi = phi_deg*pi/180;
theta_deg= (0:deltatheta:179);
% theta_deg = theta_deg([2:178]);
theta= theta_deg*pi/180;
[PHI,THETA] = meshgrid(phi,theta);

R = UnnormPattern(THETA,PHI);
for i = 1:180
    nan_ind = isnan(R(i,:));
    inf_ind = isinf(R(i,:));
    a = R(i,:);
    a(nan_ind) = 0;
    a(inf_ind) = 0;
    R(i,:) = a;
end
% R2(isnan(R1))=0;
% R(~isfinite(R2))=0;
clip = 1e2;
R(R>clip) = 0;
R_max = max(max(R))
[x,y]=find(R==R_max)

X=R.*sin(THETA).*cos(PHI);    
Y=R.*sin(THETA).*sin(PHI); 
Z=R.*cos(THETA);

mesh(X,Y,Z)

xlabel ('X')
ylabel('Y')
zlabel ('Z')

function Pun = UnnormPattern(theta,phi)
M = 16;
N = 16;
kdx = pi;
kdy = 1.2*pi;
ax = 0;
ay = 0;
psix = kdx*sin(theta).*cos(phi)+ax;
psiy = kdy*sin(theta).*sin(phi)+ay;
Pun = abs(sin(M*psix/2).*sin(psix/2)./(sin(N*psiy/2).*sin(psiy/2)));
end

function Pn = NormPattern(theta,phi)
Pun = UnnormPattern(theta,phi);
Pun_max = 1;
Pn = Pun/Pun_max;
end
```
