# Pulse generator
A python package to generate pulse operating on Qubit 
The operation setting in script:

function/parameter1/parameter2...,duration,amplitude
## functions
f(x): x from 0 to T
duration: T - the duration of this function
amplitude: A - the prefactor used to scale function 
### Linear series
#### flat
<img src="https://render.githubusercontent.com/render/math?math=f(x)=A">

### gauss series
<img src="https://render.githubusercontent.com/render/math?math=f(x) = Ae^{-\frac{1}{2}(\frac{x-x_0}{\sigma})^2}">
p1: sfactor - the factor devide length will get the sigma of gaussian function

#### cmd: gauss

<img src="https://render.githubusercontent.com/render/math?math=\sigma = \frac{T}{sfactor}"><img src="https://render.githubusercontent.com/render/math?math=x_0 = \frac{T}{2}">

#### cmd: gaussup

<img src="https://render.githubusercontent.com/render/math?math=\sigma = \frac{2T}{sfactor}"><img src="https://render.githubusercontent.com/render/math?math=x_0 = T">

#### cmd: gaussdn

<img src="https://render.githubusercontent.com/render/math?math=\sigma = \frac{2T}{sfactor}"><img src="https://render.githubusercontent.com/render/math?math=x_0 = 0">


### derivative gauss series
<img src="https://render.githubusercontent.com/render/math?math=f(x) = A\frac{(x-x0)}{\sigma^2}e^{-\frac{1}{2}(\frac{x-x_0}{\sigma})^2 })">
p1: sfactor - the factor devide length will get the sigma of gaussian function

#### cmd: dgauss

<img src="https://render.githubusercontent.com/render/math?math=\sigma = \frac{T}{sfactor}">, <img src="https://render.githubusercontent.com/render/math?math=x_0 = \frac{T}{2}">

#### cmd: dgaussup

<img src="https://render.githubusercontent.com/render/math?math=\sigma = \frac{2T}{sfactor}">, <img src="https://render.githubusercontent.com/render/math?math=x_0 = T">

#### cmd: dgaussdn

<img src="https://render.githubusercontent.com/render/math?math=\sigma = \frac{2T}{sfactor}">, <img src="https://render.githubusercontent.com/render/math?math=x_0 = 0">


### cmd: DRAG

<img src="https://render.githubusercontent.com/render/math?math=f(x) = e^{i\theta }(Ae^{-\frac{1}{2}(\frac{x-x_0}{\sigma})^2} {+} i B\frac{(x-x0)}{\sigma^2}e^{-\frac{1}{2}(\frac{x-x_0}{\sigma})^2 })">

<img src="https://render.githubusercontent.com/render/math?math=\sigma = \frac{T}{sfactor}">, <img src="https://render.githubusercontent.com/render/math?math=x_0 = \frac{T}{2}">, <img src="https://render.githubusercontent.com/render/math?math=B = A\times dratio">

p1: sfactor - the factor devide length will get the sigma of gaussian function<br />
p2: dratio  <br />
p3: angle of rotation axis - in angle unit<br />

### cmd: gestep
Gaussian step edge function