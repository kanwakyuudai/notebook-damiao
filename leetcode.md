## 204. Count Primes
> My solution, time limit exceed
```JS
// see if is a prime number
function isPrime(n) {
  if (n < 2) {return false;}
  for (let i = 2; i <= Math.sqrt(n); i++) {
    if (n % i === 0) {return false;}
  }
  return true;
}

// count primes using loop
var countPrimes = function(n) {
  if (n < 2) {return 0;}
  let count = 0;
  for (let i = 2; i < n; i++) {
    if (isPrime(i)) {count++;}
  }
  return count;
};
```

> A good solution using Sieve of Eratosthenes
```JS
var countPrimes = function (n) {
	// create an array for all the numbers from 0 to n and marked them as true
    let isPrime = new Array(n).fill(true);
	// mark 1 as false as it is not prime for sure
    isPrime[1] = false;
	// start looping from 2 as we already mark 1 as Not Prime before
	// if you do not understand why the condition is i*i < n, it's ok, keep looking
    for (let i = 2; i * i < n; i++) {
		// i.e. n = 100, i = 2, j = 4, 6, 8, ...
		// 4, 6, 8, ... will be marked as false and can be skipped
        if (!isPrime[i]) continue;
		// for any number n, its power n^2 is not prime
		// also for n^2 + n, n^2 + 2n, n^2 + 3n... are not primes as well
        for (let j = i * i; j < n; j += i) isPrime[j] = false;
    }
	// to better understand the loop, here is an example:
	// n = 10, i starting from i = 2, i * i = 4 < 10, execute the loop
	// isPrime[2] = true, go to the second loop
	// j = i * i = 4, 4 < 10, execute the loop
	// isPrime[4] = false, j = j + i = 6, 6 < 10, isPrime[6] = false, so as isPrime[8] = false
	// now i = 3, i * i = 9 < 10, keep going
	// isPrime[3] = true, gogogo
	// j = i * i = 9 < 10, isPrime[9] = false, j = j + i = 12 > 10, stop the second for loop
	// then increment i to i = 4, i * i = 16 > 10, for loop ends
	// notice that we did not touch isPrime[5] and isPrime[7] so that both of them remain true
	// after the loops, isPrime = [true, false, true, true, false, true, false, true, false, false]
	// the first one, which is isPrime[0] = true, it doesn't matter because in the later time
	// we start counting from the number 1
    let count = 0;
	// simply counting the number of true in the array
    for (let i = 1; i < n; i++) {
        if (isPrime[i]) count++;
    }
    return count;
};
```

## 69. Sqrt(x)
> newton method
```JS
var mySqrt = function(n) {
  var x = n
  if (n === 0) {return 0}
  for (var i = 0; i < 10000; i++) {
    x = (x + n / x) / 2
  }
  return Math.floor(x)
};
```

> xieran's bisection method
```JS
var mySqrt = function(n) {
  let low = 0
  let high = n
  // search range

  while (high - low > 1) {
    let mid = Math.floor((low + high) / 2)
    if (mid * mid > n) {
      high = mid - 1
      // avoid mid
    } else if (mid * mid < n) {
      low = mid
    } else {
      // in case of mid * mid === n
      return mid
    }
  }

  if (high * high <= n) {return high}
  // handle 4, 9, 16, 25,... cases
  else {return low}
};
```

## 50. Pow(x, n)
> My solution using loop, time limit exceed at `myPow(2.00000, -2147483648)` case
```JS
var myPow = function(x, n) {
  if (n === 0) {return 1}
  else if (n > 0) {
    let res = 1
    for (let i = 0; i < n; i++) {
      res *= x
    }
    return res
  } else {
    let res = 1
    for (let i = 0; i < -n; i++) {
      res *= x
    }
    return 1 / res
  }
};
```

> xieran's recursion method, using formula:
> $$
x^n\left\{
\begin{aligned}
& 1 & n &= 0 \\
& x & n &= 1 \\
& x^\frac{n}{2} \times x^\frac{n}{2} & n &= even\\
& x^\frac{n-1}{2} \times x^\frac{n-1}{2} \times x & n &= odd\\
\end{aligned}
\right.
> $$

```JS
var myPow = function(x, n) {
  if (n < 0) {return 1 / myPow(x, -n)}
  if (n === 0) {return 1}
  if (n === 1) {return x}
  if (n % 2 === 0) {
    let recursion = myPow(x, n / 2)
    return recursion * recursion
  } else {
    let recursion = myPow(x, (n - 1) / 2)
    return recursion * recursion * x
  }
};
```
> xieran's 2nd solution, split exponent
```JS
var myPow = function(x, n) {
  if (n < 0) {return 1 / myPow(x, -n)}
  if (n === 0) {return 1}
  // handle special value cases
  let result = 1
  let base = x
  // copy x as base
  let exponent = 1
  // exponent from 1
  let remainRaisePow = n
  // count remain how many times raised to power n

  while (true) {
    if (exponent * 2 > remainRaisePow) {
      // if is about to beyond target exponent
      result *= base
      remainRaisePow -= exponent
      // reduce remain times
      base = x
      exponent = 1
      // reset base and exponent

      if (remainRaisePow === 0) {break}
      else {continue}
    }
    base *= base
    // base raised to 2 power
    exponent *= 2
    // record now is 2^1, 2^2, 2^4, 2^8,...
  }
  return result
};
```
> xieran's final solution, binary traversal
```JS
var myPow = function(x, n) {
  if (n < 0) {return 1 / myPow(x, -n)}
  let result = 1
  let base = x

  while (n > 0) {
    let eachDigit = n % 2
    n = (n - eachDigit) / 2
    if (eachDigit) {
      result *= base
    }
    base *= base
  }
  return result
};
```

## 258. Add Digits
> My solution, using `.charAt`
```JS
var addDigits = function(num) {
    let sum = 0;
    let numStr = num.toString();

    for (let i = 0; i <= numStr.length; i++) {
        sum += Number(numStr.charAt(i));
    }
    if (sum < 10) {
       return sum;
    }
    else {
       return addDigits(sum);
    }
}
```

> Same way, but not using String
```JS
var addDigits = function(num) {
  let sum = 0
  while (num > 0) {
    let eachDigit = num % 10
    num = (num - eachDigit) / 10
    sum += eachDigit
  }

  if (sum < 10) {
    return sum
  } else {
    return addDigits(sum)
  }
};
```

> Math method
```JS
var addDigits = function(num) {
  let mod = num % 9
  if (num === 0) {return 0}
  if (mod === 0) {return 9}
  else {return mod}
};
```

## 326. Power of Three
> My solution, using recursion
```JS
var isPowerOfThree = function(n) {
  if (n <= 0) {
    return false;
  } else if (n === 1){
    return true;
  } else {
    return isPowerOfThree(n / 3);
  }
};
```

> Using loop
```JS
var isPowerOfThree = function(n) {
  if (n < 1) {return false}
  while (n % 3 === 0) {n = n / 3}
  return n === 1
};
```

> No loop or recursion
```JS
var isPowerOfThree = function(n) {
  if (n < 1) {return false}
  if (Math.pow(3, 19) % n === 0) {return true}
  return false
};
```

## 202. Happy Number
> My solution, using `String.charAt()` method
```JS
var isHappy = function(n, count = 0) {
  count++;
  if (count > 6) {return false}
  let str = n.toString();
  let sum = 0;

  for (let i = 0; i < str.length; i++) {
    sum += Number(str.charAt(i)) ** 2;
  }

  if (sum === 1) {return true}
  else if (sum > 1 && sum < 4) {return false}
  else {return isHappy(Number(sum), count)}
};
```

> xieran's solution
```JS
var isHappy = function(n) {
  let sum = 0
  while (n > 0) {
    let eachDigit = n % 10
    n = (n - eachDigit) / 10
    sum += eachDigit ** 2
  }
  if (sum === 1) {return true}
  else if (sum === 4) {return false}
  // infinite loop
  else {return isHappy(sum)}
};
```

## 504. Base 7
> Using built-in funtion `.toString(7)` or
```JS
var convertToBase7 = function(num) {
  let sign = 1
  if (num < 0) {
    num = -num
    sign = -1
  }
    // kept sign of num, for later use
  let base7 = ''

  do {
    let eachDigit = num % 7
    num = (num - eachDigit) / 7
    base7 = eachDigit + base7
  } while (num > 0)

  if (sign === -1) {return '-' + base7}
  return base7
};
```

## 507. Perfect Number
> My solution, using formula $2^{n-1} \times(2^n-1)$ and $2^n-1$ must be prime number
```JS
function isPrime(n) {
  if (n < 2) {return false;}
  for (let i = 2; i <= Math.sqrt(n); i++) {
    if (n % i === 0) {return false;}
  }
  return true;
}

 var checkPerfectNumber = function(num) {
  for (var i = 2; i <= 100; i++) {
    var prime = true;
    for (var j = 2; j < i; j++) {
      if (i % j === 0) {
        prime = false;
      }
    }
    if (prime) {
      var perfect = 2 ** (i - 1) * (2 ** i - 1);
      if (num === perfect && isPrime(2 ** i - 1)) {
        return true;
      } else if (perfect < num) continue;
      else return false;
    }
  }
};
```

> xieran's solution, traversal every factor of given number
```JS
 var checkPerfectNumber = function(num) {
  let loopRange = Math.sqrt(num)
  // in order to reduce loop times
  let sum = 1
  // let sum = 1, since 1 must be a factor

  for (let i = 2; i < loopRange; i++) {
    // due to sum start from 1, therefore loop start from 2
    // here cannot be i <= loopRange, will handle it later
    if (num % i === 0) {
      let pairFactor = num / i
      // once num can be divisible by i, we also find its pair factor
      sum += i + pairFactor
    }
  }

  if (Number.isInteger(loopRange)) {sum += loopRange}
  // plus given number's squre root, if it's an integer
  if (sum === num) {return true}
  else {return false}
};
```

## 461. Hamming Distance
> My solution, fill `'0'` to shorter binary string before compaire, which is actually no need
```JS
var hammingDistance = function(x, y) {
  let xBase2 = x.toString(2)
  let yBase2 = y.toString(2)

  if (xBase2.length > yBase2.length) {
    let bitDiff = xBase2.length - yBase2.length
    for (let i = 0; i < bitDiff; i++) {
      yBase2 = '0' + yBase2
    }
  } else if (yBase2.length > xBase2.length) {
    let bitDiff = yBase2.length - xBase2.length
    for (let i = 0; i < bitDiff; i++) {
      xBase2 = '0' + xBase2
    }
  }
  // compaire length of 2 string, fill '0' to make them equally length


  let count = 0

  for (let i = 0; i < xBase2.length; i++) {
    if (xBase2.charAt(i) !== yBase2.charAt(i)) {
      count++
    }
  }
  return count
};
```

> xieran's solution
```JS
var hammingDistance = function(x, y) {
  let distance = 0

  while (x > 0 || y > 0) {
    let xDigit = x % 2
    x = (x - xDigit) / 2
    let yDigit = y % 2
    y = (y - yDigit) / 2

    if (xDigit !== yDigit) {distance++}
  }
  return distance
};
```

## 509. Fibonacci Number
> Recursion solution, very simple, but high O(n)
```JS
var fib = function(n) {
  if (n === 0) {return 0}
  if (n === 1) {return 1}
  return fib(n - 1) + fib(n - 2)
};
```

> Loop solution, right move 2 variables n times
```JS
var fib = function(n) {
  // Fibonacci Number: 0, 1, 1, 2, 3, 5, 8, 13,...
  let a = 0
  // 0 of Fibonacci Number
  let b = 1
  // First of Fibonacci Number

  while (n-- > 0) {
    b = b + a
    a = b - a
  }

  return a
};
```
