## Introduction 
#### M/M/c queue is one of the specific type of continuous time Markov chain. It consists of a set of states {0, 1, 2,... \} denoting the 'population' of a system. Let $n$ denotes the number of customers in the system. State transitions occur as soon as a customer arrives or departs from the system. Arrivals are Poisson with rate $\lambda$, there are $c$ servers, and each server has an independently and identically distributed exponential service-time distribution with mean $\frac{1}{\mu}$. The rate of service completions (or "deaths ") depends on the number of customers in the system. If there are $c$ or more customers in the system, then all $c$ servers must be busy. Since each server processes customers with rate $\mu$, the combined service-completion rate for the system is $c\mu$. When there are fewer than $c$ customers in the system, $n < c$, only $n$ of the $c$ servers are busy and the combined service-completion rate for the system is $n\mu$. Thus
#### $$\mu_n= n\mu, \quad 1\leq n < c,$$
#### $$\mu_n= c\mu, \quad n\geq c.$$
#### <!-- $$\begin{aligned} &\mu_n \coloneqq \begin{cases}\begin{array}{ll} n\mu,&1\leq n < c,\\ c\mu, & n\geq c\\ \end{array}\end{cases} ,\\\end{aligned}$$\\Remove all lines above this line before making changes to the file --> <!-- Remove all lines above this line before making changes to the file -->
####  Thus the steady-state probabilities $p_n$ of the system are
#### $$p_n=p_0\left(\frac{\lambda^n}{n!\mu^n}\right), \quad \text{for}~ 0\geq n < c. $$  $$p_n=p_0\left(\frac{\lambda^n}{c^{n-c}\mu^n}\right), \quad \text{for}~ n\geq c. $$
#### Additionally, $$\sum_{n=0}^{\infty}{p_n}= 1, $$
#### yields $$p_0=\left(\sum_{n=0}^{c-1}\frac{r^n}{n!}+\sum_{n=c}^{\infty}\frac{r^n}{c^{n-c}c!}\right)^{-1},$$ where $r=\frac{\lambda}{\mu} ~\text{and} ~ \rho= \frac{r}{c}= \frac{\lambda}{c\mu}$ is the traffic intensity for a multi server queue. 
#### This gives $$p_0=\left(\sum_{n=0}^{c-1}\frac{r^n}{n!}+\frac{r^c}{c!(1-\rho)}\right)^{-1}, \quad \text{for}~ \frac{r}{c}=\rho<1.$$

#### The existence of a steady-state solution depends on the condition that $\rho < 1$ or $\lambda < c\mu$. This is intuitive, for if $\lambda > c\mu$, the mean arrival rate is greater than the mean maximum potential service rate, so the system size increases without bound over time.
### Performance Measures:
* #### Average number of customers in the system $(L)$ is given by $$L= \sum_{j=0}^{\infty}{jp_j}=r+\left(\frac{r^c\rho}{c!(1-\rho)^2}\right)p_0.$$
* #### Average number of customers waiting in the queue for service $(L_q)$ can be obtained as $$L_q=\left(\frac{r^c\rho}{c!(1-\rho)^2}\right)p_0.$$
* #### Average time a customer spends in the system $(W)$ is obtained using Little's law, $L=\lambda W$, and is given as $$W=\frac{1}{\mu}+\left(\frac{r^c}{c!(c\mu)(1-\rho)^2}\right)p_0.$$
* #### Average time a customer spends in the queue $(W_q)$ is obtained using Little's law, $L_q=\lambda W_q$, and is given as $$W_q=\left(\frac{r^c}{c!(c\mu)(1-\rho)^2}\right)p_0.$$

