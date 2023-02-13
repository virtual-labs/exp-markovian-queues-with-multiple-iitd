## Introduction 
#### M/M/c queue is one of the specific type of continuous time Markov chain. It consists of a set of states {0, 1, 2,... \} denoting the 'population' of a system. Let $n$ denotes the number of customers in the system. State transitions occur as soon as a customer arrives or departs from the system. Arrivals are Poisson with rate $\lambda$, there are $c$ servers, and each server has an independently and identically distributed exponential service-time distribution with mean $\frac{1}{\mu}$. The rate of service completions (or "deaths ") depends on the number of customers in the system. If there are $c$ or more customers in the system, then all $c$ servers must be busy. Since each server processes customers with rate $\mu$, the combined service-completion rate for the system is $c\mu$. When there are fewer than $c$ customers in the system, $n < c$, only $n$ of the $c$ servers are busy and the combined service-completion rate for the system is $n\mu$. Thus
#### $$\mu_n= n\mu, \quad 1\leq n < c,$$
#### $$\mu_n= c\mu, \quad n\geq c.$$
#### $$\begin$$
####  Thus the steady-state probabilities $p_n$ of the system are
#### $$(\lambda+\mu)p_n=\mu p_{n+1}+\lambda p_{n-1}, \quad \text{for}~ n\geq 1,$$
#### $$\lambda p_0= \mu p_1. $$
#### Thus we can write $p_n$ as
#### $$p_n=p_0\left(\frac{\lambda}{\mu}\right)^n, \quad for~ n\geq 1. $$
#### Additionally, $$\sum_{n=0}^{\infty}{p_n}= 1, $$
#### yields $$p_0=\frac{1}{\sum_{n=0}^{\infty}{\rho^n}},$$ where $\rho= \frac{\lambda}{\mu}$ is the traffic intensity for a single server. 
#### This gives $$p_0=1-\rho, \quad for~ \rho<1,$$
#### and $$p_n=(1-\rho)\rho^n, \quad for~ \rho<1.$$
#### which is the full steady-state solution for the M/M/1 system. The existence of a steady-state solution depends on the condition that $\rho<1$ or $\lambda<\mu$. This is intuitive, for if $\lambda>\mu$, the mean arrival rate is greater than the mean service rate, so the system size increases without bound over time. Note that the system is perfectly balanced when $\lambda=\mu$, but is unsatble, since it has no spare service capacity to handle random variation in arrivals and services.
### Performance Measures:
* #### Average number of customers in the system $(L)$ is given by $$L= \sum_{j=0}^{\infty}{jp_j}=\frac{\rho}{1-\rho}.$$
* #### Average number of customers waiting in the queue for service $(L_q)$ can be obtained as $$L_q=L-\frac{\lambda}{\mu}.$$
* #### Average time a customer spends in the system $(W)$ is obtained using Little's law, $L=\lambda W$, and is given as $$W=\frac{1}{\mu-\lambda}.$$
* #### Average time a customer spends in the queue $(W_q)$ is obtained using Little's law, $L_q=\lambda W_q$, and is given as $$W_q=\frac{\rho}{\mu-\lambda}.$$
* #### For the service time random variable $X$, average service time of a customer $(E[X])$ can be evaluated as $$E[X]=\frac{1}{\mu}.$$
