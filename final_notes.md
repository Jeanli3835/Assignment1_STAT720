I don't understand "Increase the variety of area influence factors and predictors" -- what does this mean??

It would probably make sense to log-transform the life expectancy (since it's positive), although it's possible that the coefficient of variation of the conditional distribution is small enough (i.e., the values are bounded away from zero, equivalently there won't be too much skew in the conditional distribution) that you can get away with an untransformed Gaussian response ...

dplyr has a `relocate` function that will do what you want to move life expectancy to the last column ...

Mean imputation is slightly dangerous (arguably not *more* dangerous than removing incomplete cases, but for different reasons).


You should **not** do best subset feature selection before modeling! This will definitely mess up your inference. This was a large subject of discussion during the first few weeks of the course ... In general it's a bad idea even in a predictive context -- it's best to make feature selection and/or shrinkage part of your modeling procedure rather than a pre-modeling filter, unless you have so much data that you need to trim it for computational reasons ... (similar comments apply to checking multicollinearity)

I think you can do the standardization more easily with `datawizard::standardize` by using the `select=` argument (e.g. `select=is.numeric` which will standardize both integer and floating-point values)

Did you not center variables?

I'd like to see data points (not just `geom_encircle`) on exploratory plots ...

Why colour outliers red? (They're less important than you think they are ...)

The life expectancy -by-year plot is weird. Did you mean to group by country?

When your model stops by hitting the maximum number of evaluations you always have to let it run longer before you can make any conclusions ... (it is *extremely* ambitious to fit an 8x8 covariance matrix ...) 

What does "transforming the response variable using the log of the Gamma distribution" mean?


I don't think these are actually fixed effect coefficient plots? There should be only 9 fixed-effect coefficients (see the lme4 summary output)

A good deal of your output doesn't really make sense ...

mark: 15/20

