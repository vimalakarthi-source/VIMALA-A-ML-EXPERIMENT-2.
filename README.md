## DATE: 28/08/2026








## AIM:






Compute descriptive statistics and empirical probabilities; generate samples from distributions.







## THEORY:









Descriptive statistics and sampling basics used throughout ML.








## ALGORITHM:







Use pandas.Series for statistics; numpy.random for sampling.









## PROGRAM:








```

import numpy as np
import pandas as pd
heights = np.array ([160,165,170,175,180,185,190,195,200,155])
s= pd.Series(heights)
print("Mean:",s.mean())
print("Median:",s.median())
print("Std dev:", round(s.std(),3))
print("variance:", round(s.var(),3))
print("p(height>170):", (s>170).mean())
sample = np.random.normal(loc=s.mean(), scale=s.std(),size=10)
print("Random sample (10) from normal around mean:",
      np.round(sample,2))


```












## OUTPUT:

















```

Mean: 177.5
Median: 177.5
Std dev: 15.138
variance: 229.167
p(height>170): 0.6
Random sample (10) from normal around mean: [193.45 166.75 184.87 157.63 196.97 180.07 210.   159.12 201.73 196.3 ]

```







## RESULT:

















Students learn central tendency, spread, and simple empirical probability estimation.
