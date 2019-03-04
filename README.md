# 22-Febrero

function [ dtdy ] = Ejercicio1( t,y )
dtdy = t/y;
end
function [ t,y ] = CallEjercicio1( )
tspan = [0 10];
y0 = 1;
[t, y ]= ode45(@Ejercicio1,tspan,y0);
plot(t,y)
end
%---------------------------------------------------------------------------
function [ dtdy ] = Ejercicio2( t,y )
a = 20;
b = 1;
dtdy = a*y - b*y.^2;
end
function [ t,y ] = CallEjercicio2( )
tspan = [0 1];
y0 = 10;
[t, y ]= ode45(@Ejercicio2,tspan,y0);
plot(t,y)
end
%---------------------------------------------------------------------------
function [ dtdy ] = Ejercicio3( t,y )
dtdy = exp(2*y)*sin(t);
end
function [ t,y ] = CallEjercicio3( )
tspan = [0 1.5];
y0 = 0;
[t, y ]= ode45(@Ejercicio3,tspan,y0);
plot(t,y)
end
%---------------------------------------------------------------------------
function [ dxdy ] = Ejercicio4( x,y )
dxdy = exp(x)/(2*y);
end
function [ x,y ] = CallEjercicio4( )
tspan = [0 10];
y0 = 1;
[x, y ]= ode45(@Ejercicio4,tspan,y0);
plot(x,y)
end
