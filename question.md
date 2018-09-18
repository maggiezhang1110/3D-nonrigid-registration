# Q&A
## unsolved problems
##### 1. After image interpolation, Gaussian blur is necessary or not?
should not (however, may exist zero)
##### 2. Get to know the original T and compare it
找ground truth, translation and rotation
##### 2. C T 2nd step 卷积
A：取消卷积，直接乘(with jaco)
<br>
Result: no identical difference
<br>
A:try without jacobian now
<br>
Result:
<br>
A: try 5*5 Gaussian kernel 
<br>
Result:
<br>
A: try .. indentical kernel 
<br>
Result:
##### 3. Check Jacobian again   own task
从头到尾 pay attention to nan 
## finished
##### 4. Read more paper        own task
为什么不用geo方法  
##### 4.1.1intensity-based 
z.B:PASHA
<br>
Initial affect results a lot. It is very easy to be stuck in local optimum. 
##### 4.1.2.geo-based(feature-based) 需要extract points 坐标的距离 (surface, feature) 
landmark based; ICP 
<br>
need initialization: prior knowledge, marker, mannual initialization(GUI)
<br>
after registration, validation is necessary.
##### 4.1.3.gradient-based 
powell or best neighbour....phase correlation method
estimated the probability density function of the gradient directions by applying a Gaussian kernel
##### 4.1.4. hybrid algorithm
for instance, geo+intensity (how to extract feature points)
##### 4.2. some conclusion extracted from papers
(projection, back-projection, reconstruction......) <br>
For difficult, majority of published registration methods employed a rigid transformation(3 rotations, 3 translatio<br>
(ii) the shift from surface-based registration to intensity- based (“voxel-property-based”) registration, which has certainly increased, with intensity-based techniques now forming the basis of the vast majority of registration approaches;<br>
The four most striking ones are the dominance of intensity-based approaches –taking into account the full contents of the images to be registered –over segmentation-based and landmark-based approaches, the upswing of nonlinear (‘curved’ ) transformations especially in registration research, the expansion of inter-subject registration e.g. to enable atlas-based segmentation, and the emer- gence of publicly available, generic and easy-to-use software pack- ages for medical image registration<br>
down sampling or blur may suppress some image features, increasing the risk of trapping in local minimum

##### 5.  是否是算法的原因 还是 图像的形状 对比ssd 参数原因还是算法原因
uniform registration
from results, we can see the uniform deformation is caused by algorithm. 
## solved
##### 2.How to assess the outcome of 3d registration 
对比2维切片，求均值， 综合比较
