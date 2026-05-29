# Feature-Encoding-Scaling

1. Difference between Label Encoding and One-Hot Encoding?
Label Encoding
Converts categorical values into numerical values.
Example:
Male = 1
Female = 0
Used for ordinal or binary data.
One-Hot Encoding
Creates separate columns for each category.
Example:
City_Hyderabad
City_Chennai
Used for nominal data where no ranking exists.
2. When should you use Standardization vs Normalization?
Standardization
z=
σ
x−μ
	​

x
μ
σ
z=
σ
x−μ
	​

≈1.2
Φ(z)≈88.5%
Mean becomes 0
Standard deviation becomes 1
Suitable for:
KNN
Logistic Regression
SVM
Normalization

x
′
=
x
max
	​

−x
min
	​

x−x
min
	​

	​


Scales values between 0 and 1
Suitable for:
Neural Networks
Deep Learning
3. What is the Dummy Variable Trap?
Occurs when one encoded variable can be predicted from another variable.
Causes multicollinearity issues in machine learning models.
Solution

Use:

pd.get_dummies(drop_first=True)
4. Why do distance-based algorithms like KNN require scaling?

Algorithms such as:

KNN
K-Means
SVM

calculate distances between data points.

If one feature has larger values than others, it dominates the distance calculation.

Scaling ensures equal contribution from all features.

5. Can we apply One-Hot Encoding to high-cardinality features?

Yes, but it creates many columns.

Problems
High memory usage
Increased computation time
Curse of dimensionality
Alternatives
Target Encoding
Frequency Encoding
Embedding techniques
