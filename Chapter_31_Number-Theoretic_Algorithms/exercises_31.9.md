## 31.9 Integer factorization

### 31.9-1

> Referring to the execution history shown in Figure 31.7(a), when does POLLARDRHO print the factor 73 of 1387?

$$x = 84, y = 814$$.

### 31.9-2

> Suppose that we are given a function $$f : \mathbb{Z}_n \rightarrow \mathbb{Z}_n$$ and an initial value $$x_0 \in \mathbb{Z}_n$$. Define $$x_i = f(x_{i - 1})$$ for $$i = 1,2,\dots$$. Let $$t$$ and $$u > 0$$ be the smallest values such that $$x_{t+i} = x_{t+u+i}$$ for $$i = 0, 1, \dots$$. In the terminology of Pollard's rho algorithm, $$t$$ is the length of the tail and $$u$$ is the length of the cycle of the rho. Give an efficient algorithm to determine $$t$$ and $$u$$ exactly, and analyze its running time.

### 31.9-3

> How many steps would you expect POLLARD-RHO to require to discover a factor of the form $$p^e$$, where $$p$$ is prime and $$e > 1$$?

$$\Theta(\sqrt{p})$$.

### 31.9-4 $$\star$$

> One disadvantage of POLLARD-RHO as written is that it requires one gcd computation for each step of the recurrence. Instead, we could batch the gcd computations by accumulating the product of several $$x_i$$ values in a row and then using this product instead of $$x_i$$ in the gcd computation. Describe carefully how you would implement this idea, why it works, and what batch size you would pick as the most effective when working on a $$\beta$$-bit number $$n$$.

