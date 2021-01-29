# MyNote
Kullback-Leibler Divergence has its origins in information theory. The primary goal of information theory is to quantify how much information is in data. The most important metric in information theory is called Entropy, typically denoted as $H$. The definition of Entropy for a probability distribution is: $$H=-\sum_{i=1}^Np(x_i)\cdot \log p(x_i)$$
If we use $\log_2$ for our calculation we can interpret entropy as "the minimum number of bits it would take us to encode our information". The number of bits tells us the lower bound for how many bits we would need, on average, to encode the number of teeth we would observe in a single case.

What entropy doesn't tell us is the optimal encoding scheme to help us achieve this compression. Optimal encoding of information is a very interesting topic, but not necessary for understanding KL divergence. The key thing with Entropy is that, simply knowing the theoretical lower bound on the number of bits we need, we have a way to quantify exactly how much information is in our data. Now that we can quantify this, we want to quantify how much information is lost when we substitute our observed distribution for a parameterized approximation.

# Measuring information lost using Kullback-Leibler Divergence
Kullback-Leibler Divergence is just a slight modification of our formula for entropy. Rather than just having our probability distribution pp we add in our approximating distribution qq. Then we look at the difference of the log values for each: $$D_{KL}(p||q)=\sum_{i=1}^N p(x_i) \cdot (\log p(x_i)-\log q(x_i))=E[\log p(x)-\log q(x)]=\sum_{i=1}^N p(x_i) \cdot \log \frac{p(x_i)}{q(x_i)}$$

# Divergence not distance

It may be tempting to think of KL Divergence as a distance metric, however we cannot use KL Divergence to measure the distance between two distributions. The reason for this is that KL Divergence is not symmetric. That is, $$D_{KL}(p||q)\neq D_{KL}(q||p)$$

来源： https://www.countbayesie.com/blog/2017/5/9/kullback-leibler-divergence-explained
