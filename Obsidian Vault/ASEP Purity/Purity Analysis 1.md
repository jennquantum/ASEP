### $2 \times 2$ ASEP 


In the $2 \times 2$ case, we consider the parametrization 

$$ \begin{align} \lambda_1&=\frac{1}{2}\left(1-\left(\sqrt{\lambda_{2}}-\sqrt{\lambda_4}\right)\right)²\\
\lambda_3&= \frac{1}{2}\left(1-\left(\sqrt{\lambda_{2}}+\sqrt{\lambda_4}\right)\right)²\end{align}$$


and that the purity equates to ff:

$$
\begin{align}\sum_i \lambda_i² &= \frac{3}{2}\lambda_{2}^2+3 \lambda_{2}\lambda_{4}-\lambda_{2}+\frac{3 }{2}\lambda_{4}^2-\lambda_{4}+\frac{1}{2} \\
&= \frac{3}{2} \left(\lambda_2+\lambda_4-\frac{1}{3}\right)^2+\frac{1}{3}\end{align} 
$$


### $2 \times n$ ASEP


In general, we find a similar parametrization

$$ \begin{align} \lambda_{1}&= \frac{1}{2}\left(1-\left(\sqrt{\lambda_{2n-2}}-\sqrt{\lambda_{2n}}\right)- s\right)²\\
\lambda_{2n-1}&= \frac{1}{2}\left(1-\left(\sqrt{\lambda_{2n-2}}+\sqrt{\lambda_{2n}}\right)-s\right)²\end{align}  $$


where $s = \sum_{i=2}^{2n-3} \lambda_i$ and the purity is computed as:



$$
\begin{align}
\sum_i \lambda_i² &= \left(\frac{3 }{2}\lambda_{2n-2}^2+\frac{3 }{2}\lambda_{2n}^2+3 \lambda_{2n-2}\lambda_{2n}-\lambda_{2n-2}-\lambda_{2n}+\frac{1}{2} \right)+ \left(\frac{s^2}{2}+s( \lambda_{2n-2}+\lambda_{2n})-s\right)\\ &+\sum_{i=2}^{2n-3} \lambda_i² \end{align} 
$$


Looking closely, it seems very similar to the 2x2 case with extra terms comprising of the middle eigenvalues...


By observing the construction in smaller dimensional cases, I conclude the ff: 


==*For any $2 \times n$ ASEP state, the purity is given as*== 


$$
\begin{align} Tr(\rho²) &= \left(\frac{1}{2n-1}\right) +\frac{3}{2} \left(\lambda_{2n-2}+\lambda_{2n}-\frac{1}{2n-1}\right)^2+ \frac{1}{2}\left(\sum_{i=2}^{2n-3} \lambda_i-\frac{\sum_{i=2}^{2n-3} i}{2n-1}\right)^2\\
&+ \sum_{i=2}^{2n-3} \left( \lambda_i -\frac{1}{2n-1}\right)^2 +....\end{align} 
$$

#### Examples: 


1. In the ==***$2\times 3$** case*==, we have the following: 

 $$ \begin{align} \sum_i \lambda_i² &= \left(\frac{3 }{2}\lambda_{4}^2+ \frac{3 }{2}\lambda_{6}^2+ 3 \lambda_{4}\lambda_{6}-\lambda_{4}-\lambda_{6}+\frac{1}{2} \right)\\
 &+
 \left(\frac{(\lambda_{2}+\lambda_{3})^2}{2}+(\lambda_{2}+\lambda_{3})\lambda_{4}+(\lambda_{2}+\lambda_{3}) \lambda_{6}-(\lambda_{2}+\lambda_{3})\right)+(\lambda_{2}²+\lambda_{3}²)\\
\end{align} 
$$


This factorizes as follows; 


$$
\begin{align} \sum_i \lambda_i² &= \left[\frac{1}{5} \right]+\left[\frac{3}{2} \left(\lambda_4+\lambda_6-\frac{1}{5}\right)^2 \right]+ \left[\frac{1}{2} \left(\lambda_2+\lambda_3-\frac{2}{5}\right)^2 \right]\\ &+\left[\left(\lambda_2-\frac{1}{5}\right)^2+\left(\lambda_3-\frac{1}{5}\right)^2\right]+\left[(\lambda_2+\lambda_3) \left(\frac{\lambda_4+\lambda_6}{2}-\frac{1}{5}\right)+\left(\frac{\lambda_2+\lambda_3}{2}-\frac{2}{5}\right) (\lambda_4+\lambda_6)\right]\\
&+\left[\frac{1}{25} +\frac{1}{25} \right]\\ 
 \end{align} 
$$



2. In the ==$2\times 4$ case==, we have the following: 

$$ \begin{align} \sum_i \lambda_i² &= \left(\frac{3 }{2}\lambda_{8}^2+ \frac{3 }{2}\lambda_{6}^2+ 3 \lambda_{8}\lambda_{6}-\lambda_{8}-\lambda_{6}+\frac{1}{2} \right)\\
 &+
 \left(\frac{(\lambda_{2}+\lambda_{3}+\lambda_{4}+\lambda_{5})^2}{2}+(\lambda_{2}+\lambda_{3}+\lambda_{4}+\lambda_{5})(\lambda_{8}+ \lambda_{6})-(\lambda_{2}+\lambda_{3}+\lambda_{4}+\lambda_{5})\right)\\ 
 &+(\lambda_{2}²+\lambda_{3}²+\lambda_{4}²+\lambda_{5}²)\\
\end{align} 
$$


This factorizes as follows; 


$$
\begin{align} \sum_i \lambda_i² &= \left[\frac{1}{7} \right]+\left[\frac{3}{2} \left(\lambda_8+\lambda_6-\frac{1}{7}\right)^2 \right]+ \left[\frac{1}{2} \left(\lambda_{2}+\lambda_{3}+\lambda_{4}+\lambda_{5}-\frac{4}{7}\right)^2 \right]\\ &+\left[\left(\lambda_2-\frac{1}{7}\right)^2+\left(\lambda_3-\frac{1}{7}\right)^2+\left(\lambda_4-\frac{1}{7}\right)^2+\left(\lambda_5-\frac{1}{7}\right)^2\right]\\ 
&+ \left[\frac{1}{2} \left(\lambda_{2}+\lambda_{3}-\frac{2}{7}\right)^2+\frac{1}{2} \left(\lambda_{4}+\lambda_{5}-\frac{2}{7}\right)^2 \right]\\
&+\left[(\lambda_{2}+\lambda_{3}+\lambda_{4}+\lambda_{5}) \left(\lambda_8+\lambda_6-\frac{6}{7}\right)+\left(\lambda_{2}+\lambda_{3}+\lambda_{4}+\lambda_{5}-\frac{4}{7}\right) (\lambda_4+\lambda_6)\right]\\
&+ \left[\left(\lambda_{2}+\lambda_{3}\right)\left(\lambda_{4}+\lambda_{5}\right)+ 2\lambda_{2}\left(\lambda_{3}+\lambda_{4}+\lambda_{5}\right)+ 2\lambda_{3}\left(\lambda_{2}+\lambda_{5}\right)+ 2\lambda_{3}\lambda_{5}\right]
 \end{align} 
$$




......................................


# Therefore, in conclusion (for now): 



*Every $2 \times n$ ASEP state has purity* 

$$
\begin{align} Tr(\rho²) &= \left(\frac{1}{2n-1}\right) +\frac{3}{2} \left(\lambda_{2n-2}+\lambda_{2n}-\frac{1}{2n-1}\right)^2+ \frac{1}{2}\left(\sum_{i=2}^{2n-3} \lambda_i-\frac{\sum_{i=2}^{2n-3} i}{2n-1}\right)^2\\
&+ \sum_{i=2}^{2n-3} \left( \lambda_i -\frac{1}{2n-1}\right)^2 +....\end{align} 
$$