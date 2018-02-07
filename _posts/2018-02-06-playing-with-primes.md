---
layout: post
title:  "Playing with primes"
date:   2018-02-06
---

<p class="intro"><span class="dropcap">P</span>rime numbers are an important portion of mathematics. Their concept is simple and were discovered a long time ago, but still there is a lot of research going on them. Their applications are in many fields and one popular example is in field of cryptography(used in RSA encryption).</p>

<p class="intro">A prime number is a positive integer greater than 1 which is only divisible by itself and 1. Other way to say this is that a prime number is a positive integer greater than 1 which cannot be evenly divided by any integer greater than 1 and smaller than it.</p>

# Checking for Prime

To check if a given number is prime or not, there are multiple ways.

The most basic one is to just check for all numbers between $$[2, N - 1]$$ that if any of those divides $$N$$ evenly or not. If any of those divides $$N$$, then $$N$$ is not prime, else $$N$$ is prime. Complexity of this approach is $$O(N)$$. 

In the above approach, we are dividing $$N$$ by nearly all positive integers below it. Let's optimise it. Let's say that a number $$X$$ is a divisor of $$N$$, then there must be another number $$Y = N / X$$ which is also a divisor of $$N$$. Also, their product is equal to $$N$$. So, if $$X \leq \sqrt{N}$$, then $$Y$$ must be greater than or equal to $$\sqrt{N}$$. So, for every divisor of $$N$$ greater than $$\sqrt{N}$$, there exist a corresponding divisor of $$N$$ which is lesser than or equal of $$\sqrt{N}$$. So, there is no need to go beyond $$\sqrt{N}$$. Just check if a number upto $$\sqrt{N}$$ divides $$N$$ or not. If so, then $$N$$ is not prime, else it is a prime number.

# Sieve of Eratosthenes

Sieve of Eratosthenes makes use of the concept that only multiples of some prime number are composite. In other words, instead of checking divisibility for every number, we just mark the multiples of prime numbers as only those are divisible by that prime number. This helps in fast calculations of primes in some given range.

```

for(int i = 2; i < siz; i++)
		if(primes[i] == 0)				//If i is prime, mark all it's multiple as composite.
			for(int j = 2 * i; j < siz; j += i)
				primes[j] = 1;

```

In above code, if i is prime, then primes[i] will be 0, else 1, after the completion of algorithm. ``siz`` is limit upto which we run the sieve. This can only be upto the order of $$10^7$$ as we can't declare an array of order larger than that.

Now, one can easily check for any number below ``siz`` that it is prime or not in constant time after applying the sieve. Hence, it is usually used where prime check is to be applied for multiple numbers or in some questions requiring prime factorisation.

Complexity of prime sieve is $$O(N * log(N) * log(log(N)))$$, where $$N$$ is the integer upto which seive is run.

# Derivatives of Sieve of Eratosthenes

The above implementation was just to check if a number is prime or not, but Sieve of Eratosthenes can be used in some other ways too by just tweaking it a bit.

We can easily find the number of distinct prime factors for each number in a range.

```

for(int i = 2; i < siz; i++)
		if(factors[i] == 0)					//If i is prime,
			for(int j = i; j < siz; j += i)	//increment no. of factors of it's multiples and
				factors[j]++; 				//itself by 1.

```

In above code, we increment the count of factors for each multiple of current prime number.

The best application of Sieve of Eratosthenes is factorisation in $$log(N)$$ time.

```

for(int i = 2; i < siz; i++)
		if(!min_factor[i]) {				//If i is prime, 
			for(int j = i; j < siz; j += i)	//and for each of it's multiple,
				if(!min_factor[j])			//If multiple doesn't yet have any
					min_factor[j] = i;		//smallest factor, make i as one.
		}

while(n != 1) {
		int r = min_factor[n];			//Take the smallest multiple
		printf("%d ", r);				//of val and divide val by it
		val /= r;						//until it becomes 1.
}

```

Above code just finds the minimum prime factor of each number in range $$[2, siz)$$. Using minimum prime factor, we can factorise any number upto ``siz`` in $$log(N)$$ time.

To factorise the number, we'll divide it by it's least prime factor. After that, a new smaller number will be produced which will also have a least prime factor. We'll keep on dividing until we are left with 1. We'll then have all the prime factors. One can see that a number can't have more than $$log(N)$$ factors.(Note that in whole post $$log(N)$$ is of base 2).

To prove that a number can't have more than $$log(N)$$ factors, let's assume that $$N$$ has all factors smallest as possible, which is 2. So, $$N = 2^x$$ and $$x$$ is the number of factors of this number. Taking $$log$$ both sides, we get $$x = log(N)$$. Also, a prime factor is gonna be greater than or equal to 2. So, number of factors is always lesser than or equal to $$log(N)$$.

There's also one more important derivative of Sieve of Eratosthenes, which is segmented sieve. Segmented sieve is used when you don't require calculating primes in range $$[2, siz)$$, but in a range in which numbers can go upto $$siz^2$$ and length of range is upto ``siz``.

In segmented sieve, we first compute all primes in range $$[2, siz)$$. Then, we smartly mark all multiples of these primes in the required range. We only require primes upto ``siz`` because if there is no prime divisor of a number upto it's square root, then it has no prime divisor and is itself prime.

One can easily find good implementations of Segmented sieve over the internet.

# Large primes and factorisation of large primes

By large numbers, I mean numbers of order from $$10^8$$ and upto $$10^{18}$$. There are few algorithms which can help solving problems involving large primes.

The most basic prime check for large numbers is to just check divisibility upto it's square root. For a number upto $$10^{12}$$, number of divisibility checks will be upto $$10^6$$.

There are algorithms which can check for prime very fast for large numbers such as **Fermet primality testing** and **Miller-Rabin primality testing**. But, these can only tell that a number is probable prime, which means that result isn't always correct but probability of correctness in very high.

This post was just to get you acquainted with prime numbers and some of the popular number theory algorithms related to them. To learn about primes in deep, one can just search over the net as there are plenty of good resources available.

Thanks for reading. Happy coding!!