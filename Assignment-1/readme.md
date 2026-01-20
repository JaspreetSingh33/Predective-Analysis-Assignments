# Assignment-1: Probability Density Function using Transformed NO2 Data

## 1. Objective
The goal of this assignment is to:

1.Transform the NO2 feature using a roll-number–based non-linear function.

2.Learn the parameters of a probability density function (PDF) on the transformed data.

## 2. Dataset
- Dataset name:India-Air-Quality-Data
- Source:Kaggle
- Feature used:NO₂ (Nitrogen Dioxide concentration)

## 3. Step-1: Data Transformation
- Let NO2 be the feature x.
- roll number r:102303163
- Value of ar:0.05×(r mod7)
- Value of br:0.3×(r mod5+1)
- Transformation formula(z):Tr(x)=x+(ar*​sin(br​x))

## 4. Step-2: Probability Density Function
- Given PDF formula : p^​(z)=c⋅e−λ(z−μ)2
- Meaning of μ : Mean of data
- Meaning of λ : Lambda (λ) is the parameter that controls the spread (width) of your probability curve.
- Meaning of c : normalization constant
-  μ       : mean(z)
- variance : var(z)
- λ        : 1/(2*σ^2)​
- c        : c=sqrt(π/λ)

## 5. Results
-  μ=25.805243726878015
-  λ=0.0014598199664884292
-  c=0.021556324533225906


