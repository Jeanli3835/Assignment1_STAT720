It's best practice to name your chunks, and in general to make self-contained HTML (see edits to QMD file) if you're going to share the document

I think there are missing values? but your complete_cases statement got rid of them ...

Use `message=FALSE` to suppress all the package startup messages

Q 1b: 1 observation per RE group (`country:year`) is *not* too sparse for a Poisson model (it's a way to incorporate overdispersion)

The way to handle "failure to converge in xxx evaluations" is to *increase the max number*

It would be good to plot models on a log(1+x) scale

Whenever possible plot data points, not just encircling shapes ...

"random effect of the intercept grouped by year is zero" ? no ... (but yes, it is 4 orders of magnitude smaller than the other variances ...

how did you decide the variance was "a little bit small" ????

Why bother to show the diagnostic plot for the GLM (no REs)?

*Never* plot coefficient plots without scaling! This is misleading you into thinking the effects are small ...

Q2

treatment is unidentifiable as random effect across patients -- each patient gets only one treatment!

picking treatment as a grouping variable doesn't make sense -- only two levels, and not exchangeable.

The standard deviations of patientID are alarmingly large for effects on the logit scale.

I would have dropped the slope rather than the intercept from the RE (e.g. (1|treatment) )

Where are the confidence intervals on the estimates?  Again, don't plot unscaled coeffs on the same plot ...

Q4: thank you for trying.

mark: 7.5/10

