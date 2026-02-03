#  TOPSIS Implementation, Python Package, and Web Application

**Name:** Jaspreet Singh  
**Roll Number:** 102303163  

This assignment consists of three parts:

1. Command Line TOPSIS implementation  
2. Python Package creation and upload to PyPI  
3. Web Application for TOPSIS with email result and live hosting  

---

##  Part I — Command Line TOPSIS Program

A Python program `topsis.py` was created that implements the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method.

### Features

- Accepts CSV file as input
- Accepts weights and impacts from command line
- Validates inputs and handles errors
- Computes TOPSIS Score and Rank
- Generates output CSV file

### Run Command

```bash
python topsis.py data.csv "1,1,1,2" "+,+,-,+" result.csv
```

---

##  Part II — Python Package Creation and Upload to PyPI

In this part, the TOPSIS command line program was converted into a proper Python package and uploaded to **PyPI**.

###  Package Name

`Topsis-JaspreetSingh-102303163`

###  Package Structure

```
Topsis-JaspreetSingh-102303163
│
├── topsis_jaspreet_102303163
│   ├── __init__.py
│   └── topsis.py
│
├── setup.py
├── README.md
└── requirements.txt
```

###  setup.py Configuration

```python
from setuptools import setup, find_packages

with open("README.md", "r", encoding="utf-8") as fh:
    long_description = fh.read()

setup(
    name='Topsis-JaspreetSingh-102303163',
    version='0.3',
    author='Jaspreet Singh',
    author_email='jaspreetsinghupkar@gmail.com',
    description='TOPSIS implementation using command line',
    long_description=long_description,
    long_description_content_type="text/markdown",
    packages=find_packages(),
    install_requires=['pandas', 'numpy'],
    entry_points={
        'console_scripts': [
            'topsis=topsis_jaspreet_102303163.topsis:main',
        ],
    },
)


```

###  Building the Package

```bash
python setup.py sdist bdist_wheel
```

###  Uploading to PyPI

```bash
twine upload dist/*
```

###  Installing the Package

```bash
pip install Topsis-JaspreetSingh-102303163
```

###  Running the Package

```bash
topsis data.csv "1,1,1,2" "+,+,-,+" result.csv
```

###  PyPI Link

https://pypi.org/project/Topsis-JaspreetSingh-102303163/

---

##  Part III — Web Application for TOPSIS

A Flask-based web application was developed where users can:

- Upload CSV file
- Enter weights and impacts
- Provide email address
- Receive result CSV via email

### Technologies Used

- Flask
- Pandas, NumPy
- Gmail SMTP (App Password)
- HTML/CSS Dark UI
- Hosted on Render

### How it Works

1. User uploads CSV
2. Server runs TOPSIS algorithm
3. Result CSV is generated
4. Result is sent to user's email

###  Live Web App

https://topsis-web-42ui.onrender.com

###  GitHub Repository

https://github.com/JaspreetSingh33/topsis-web

---

##  Learnings from Assignment

- Implementation of TOPSIS algorithm
- Error handling in command line programs
- Creating Python packages with `setup.py`
- Uploading packages to PyPI using `twine`
- Creating Flask web applications
- Sending emails using Gmail SMTP and App Passwords
- Deploying web apps using Render
- Using Git and GitHub for version control

---

##  Conclusion

This assignment demonstrates the complete pipeline from:

**Algorithm → Command Line Tool → Python Package → Web Application**

All three parts were successfully implemented and tested.
