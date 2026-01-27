# Learning PDF using GAN

## Introduction
This project is done as a part of college assignment.
In this project, air quality data is used.
Only NO2 values are taken from the dataset.

---

## Data Used
The dataset contains air quality data of India.
From the dataset, NO2 column is selected.
Missing values are removed before using the data.

---

## Method Used
First, NO2 values (x) are converted into new values (z).
The formula used is:

z = x + a * sin(b * x)

The values of a and b are calculated using my roll number.

After this, a simple GAN is used.
The generator generates fake z values.
The discriminator checks whether the z values are real or fake.

---

## Output
After training the GAN, new z values are generated.
Using these values, the probability density function (PDF) is plotted.

---

## Graphs

### Histogram based PDF
<img width="452" height="342" alt="image" src="https://github.com/user-attachments/assets/6ea4e643-697b-457c-aae6-ed82d4bd6b5e" />


### KDE based PDF
<img width="453" height="342" alt="image" src="https://github.com/user-attachments/assets/36ce5473-96a0-4a05-ab62-2f70e91d4201" />


---


## Tools Used
Python  
Pandas  
PyTorch  
Matplotlib
