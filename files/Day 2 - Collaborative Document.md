![](https://i.imgur.com/iywjz8s.png)


# Day 2 - Collaborative Document
2023-10-04 Good Practices in Research Software (2023-10-02-ds-cr)

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: [link](https://codimd.carpentries.org/SIGfo1wqReec2P-zc_YPmQ?both)

Collaborative Document day 1: [link](https://codimd.carpentries.org/qctl8zmsSgKwpTzATXTp2Q?both)

Collaborative Document day 2: [link](https://codimd.carpentries.org/SIGfo1wqReec2P-zc_YPmQ?both)

## 👮Code of Conduct

Participants are expected to follow those guidelines:
* Use welcoming and inclusive language
* Be respectful of different viewpoints and experiences
* Gracefully accept constructive criticism
* Focus on what is best for the community
* Show courtesy and respect towards other community members

For more details, see [here](https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html).

Want to report a Code of Conduct incident and you prefer to do it anonymously? You can do it [here](https://goo.gl/forms/KoUfO53Za3apOuOK2).

## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, just raise your hand.

If you need help from a helper, place a pink post-it note on your laptop lid. A helper will come to assist you as soon as possible.

## 🖥 Workshop website
For information about this workshop, agenda and setup.
[https://esciencecenter-digital-skills.github.io/2023-10-03-ds-cr/](https://esciencecenter-digital-skills.github.io/2023-10-03-ds-cr/)

## 🛠 Setup
We will assume everyone can access the command line on their laptop and managed to follow these [**setup instructions**](https://esciencecenter-digital-skills.github.io/2023-10-03-ds-cr/#:~:text=the%20CET%20timezone.-,Setup,-To%20participate%20in).

Please put a pink post-it note on you laptop lid, if you need a bit more help with the setup. 


## 👩‍🏫👩‍💻🎓 Instructors

Jaro Camphuijsen, Giulia Crocioni, Olga Lyashevska

## 🧑‍🙋 Helpers

Carlos Murilo Romero Rocha

## 👩‍💻👩‍💼👨‍🔬🧑‍🔬🧑‍🚀🧙‍♂️🔧 Roll Call
Name/ pronouns (optional) / job, role / social media (twitter, github, ...) / background or interests (optional) / city


## 🗓️ Agenda

|  Time | Topic                                  |
| -----:|:-------------------------------------- |
| 09:30 | Welcome and icebreaker                 |
| 09:45 | Writing modular code                   |
| 10:30 | **Coffee break**                       |
| 10:45 | Writing modular code                   |
| 11:30 | **Coffee break**                       |
| 11:45 | Documentation                          |
| 12:30 | **Lunch Break**                        |
| 13:30 | Introduction to testing                |
| 14:15 | **Coffee break**                       |
| 14:30 | Introduction to Continuous Integration |
| 15:15 | **Coffee break**                       |
| 15:30 | More advanced testing                  | 
| 16:15 | Wrap-up                                |
| 16:30 | END                                    |

## 🏢 Location logistics
* Coffee and toilets are in the hallway, just outside of the classroom.
* If you leave the building, 
  be sure to be accompanied by someone from the escience center to let you back in through the groundfloor door
* For access to this floor you might need to ring the doorbell so someone can let you in
* In case of an emergency, you can exit our floor using the main staircase.
  Or follow green light signs at the ceiling to the emergency staircase.
* **Wifi**: Eduroam should work. Otherwise use the 'matrixbuilding' network, password should be printed out and available somewhere in the room.

## 🎓 Certificate of attendance
If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl .

## ❄️ Icebreaker
Lost on a deserted island...
![Deserted island image](https://codimd.carpentries.org/uploads/upload_2b49b30d1e66ebbec8aff7ec53ea677e.png)
Image by Robert Nickson at [Unsplash](https://unsplash.com/photos/ANP5Rz4Y6lc)


## 🔧 Exercises

If you are done with your exercise, or know the answer to a question, put the green post-it note on top of your laptop lid. 

#### 1. Modularity
Go to the [Modular code development](https://github.com/lyashevska/modular-code-dev) repo

##### Lessons learned from the exercise:
- Mohamed Benmahdjoub:
```
def fahrentheit_to_celcius(fahrentheit):
    celcius = (celcius * (9 / 5)) + 32
    return celcius

def celsius_to_fahrenheit(celcius):
    fahrenheit = (celcius * (9 / 5)) + 32
    return fahrenheit

def celsius_to_kelvin(celcius):
    kelvin = celcius + 273.15
    return kelvin

def kelvin_to_celcius(kelvin):
    celsius = kelvin - 273.15
    return celcius


def convert_fahrenheit(temperature):
    return fahrentheit_to_celcius(temperature), celsius_to_kelvin(celsius)

def convert_celcius(temperature):
    return celsius_to_fahrenheit(temperature), celsius_to_kelvin(temperature)

def convert_kelvin(temperature):
    return kelvin_to_celcius(temperature), celsius_to_fahrenheit(temperature)

def valid_temperature(temperature, unit):
    valid_dict = {"F": -459.67, "C": -273.15, "K": 0}
    return temperature >= valid_dict[unit] 


def conversion(temperature, unit):
    if(not valid_temperature(temperature, unit)):
        return "Invalid temperature"
    conv_dict = {"F":convert_fahrenheit, "C":convert_celcius, "K": convert_kelvin}
    return conv_dict[unit](temperature)

# to run
if __name__ == "__main__":
    print(conversion(0, "C"))
```

#### 2. Think of good and bad examples 
Write down your thoughts in the collaborative documents.
Respond with emojis :+1: :scream_cat: to your colleagues' answers.
- Think of projects of which you like the documentation. What do you like about them?
- Think of projects for which you don’t like the documentation. What don’t you like about them? Are you missing anything?

**NB: You can choose a mature library with lots of users for this exercise, but try to also think of less mature projects you had to collaborate on, or papers you had to reproduce.**

- Enya: SpecPy documentation is  [incomplete and outdated](https://imspectordocs.readthedocs.io/en/latest/tutorial.html)
- Lars Leijten: Modularized code that doesn't make it clear where it starts makes it quite difficult to understand.  
- Victoria: React documentation is great, it includes screenshots, diagrams, "pitfalls" and embedded codesandbox environment https://react.dev/learn
- Izzy: Good documentation has a list of functions and [examples](https://docs.wradlib.org/en/latest/notebooks/basics/wradlib_workflow.html). Bad documentation just says ["I'm not like the other guys!"](https://pysolar.readthedocs.io/en/latest/#)
- Miró: Good example ([xarray](https://docs.xarray.dev/en/stable/index.html)); lots of examples / a get-started documentation.
- Martijn: Many python libraries have good documentation (NumPy, seaborne, ...) where all function inputs are described clearly. Personally, I also like it if an example is included. Furthermore, a clear installing guide in necessary. Bad documentation is sometimes very outdated. I try their precise examples and it all malfunctions. 
- Marleen: Student projects are well documents (sometimes), reproducing somebody else's work can be very difficult if it isnt documented, even the contents of folder can help a lot.
- Giovanni: GOOD documentation is a code with each line commented about what it does. BAD terminolgy too specific and not beginner friendly.
- Ingeborg: good example: [jsoniq](https://www.jsoniq.org), bad: [signnet](https://cran.r-project.org/web/packages/signnet/index.html)
- Pascal: GOOD: function description inputs and output (alos types and sizes) are clearly documented at the start of a the function
- John Douros: Most well known python libraries appear to have documentation much better than my own code/projects. Good example: xESMF
- Sobhan: Structure- Short explanations- I/O- Demo- Propper referencing- requirements - versions- Personalisation explanation. [example](https://github.com/AntixK/PyTorch-VAE)
- Cecile: Good example: pycbc gravitational wave software (https://pycbc.org/pycbc), very structured lot of Classes and functions Bad example: My thesis
- Kaouther Mouheb: Good example: Numpy <3 I like that everything is well explained and also *examples*. Bad example: SimpleITK, I never find a straightforward answer to what I'm looking for and end up asking ChatGPT (who also struggles)
- Stefan Kirsch: Learning R, and coming mostly from Matlab, I realized how much worse the documentaiion of R is (at least for my taste). The R documentation is often very acedemic and uses a lot of 
- João Vargas: good documentation for a radiative spectrum calculation [Radis](https://radis.readthedocs.io/en/latest/)
- Renske: pandas has good documentation :)
- Deniz=  Good documentation: https://keras.io/guides/  Bad documentation: https://github.com/deniz-kilic/planets or https://github.com/lyashevska/modular-code-dev
- Gijs overview of program/software structure (high-level) in code comments (low level)
or

#### 3. Writing good comments

Let's take a look at two example comments (comments in python start with `#`):
#### Comment A
```python
# Now we check if temperature is larger than -50:
if temperature > -50:
    print('do something')
```

#### Comment B
```python
# We regard temperatures below -50 degrees as measurement errors
if temperature > -50:
    print('do something')
```
 Which of these comments is best? Can you explain why?
 Write your answer in the collaborative document (before looking at others' answers)

- Gijs: second, it explains why you want to do this check, the check is self-expanatory
 - Enya: B. The information in comment A is already clear from the code itself. B provides relevant additional information: why the function is executed.
 - Sobhan: B Since its related to ultimate goal of the function.
- Tugba: B, it explains why they wrote it.
- Izzy & Marcella: A says in words exactly what the next line does. B explains why. However, if the print statement were written such that we simplu raise a measurement error, the comment becomes unneccessary entirely!
- João Vargas: B is better since it provides more context and information than A. The comment in A just repeats the information that is already seen in the code.
- Deniz = Case 2 because it gives context of the decision for the if condition. Csase A is not clear why -50C is relevant
- Kaouther: A is just reading the next line so it's redundent, B provides more information and context.
- Pascal: The bottom coment is better, because the code itself is clear in what is does, so that does not need any comments, but we only want to know why it does so.
- Renske: comment B, because it adds information on top of what can be understood from the code (namely why this decision was made)
- Martijn: comment B, it also explains the reason why we do the temperature check.

#### 4. Test-driven development

The function `fizz_buzz()` takes an integer argument and returns it, BUT:

- It fails on zero or negative numbers
- It returns "Fizz" on multiples of 3
- It returns "Buzz" on multiples of 5
- It instead returns "FizzBuzz" on multiples of 3 and 5

You will use test-driven development to write this function.

1. Create an empty function `fizz_buzz()`
2. Go through the conditions listed above, one by one:
    1. Write a test for the condition
    2. Edit the `fizz_buzz()` function until the test passes
3. Share your tests in the collaborative document.

What did you think of this style of developing?

-  nice that the function can be spaghetti but as long as it passes the test, no worries, test legacy code and leave it be :) 


##### **notes, comments and doubts:**

- João Vargas
```python
def test_wrongvar():
  # I return -1 when the wrong type is used
  assert fizzbuzz("abc") == -1
  assert fizzbuzz(1.0)   == -1
  assert fizzbuzz(-2)    == -1
  
def test_evennumbers():
  for i in range(2,19,2):
    if( i % 5 == 0 or i % 3 == 0 ):
      continue
    assert fizzbuzz(i) == i
    
def test_multiples_of_three():
  for i in range(3,31,3):
    if( i % 5 == 0 ):
      continue
    assert fizzbuzz(i) == "fizz"
    
def test_multiples_of_five():
  for i in range(5,51,5):
    if( i % 3 == 0 ):
      continue
    assert fizzbuzz(i) == "buzz"
    
def test_multiples_of_three_and_five():
  for i in range(15,151,15):
    assert fizzbuzz(i) == "fizzbuzz"
```

- Izzy:

```python
import pytest
import random


def fizz_buzz(num: int) -> int | str:

    if type(num) != int:
        raise TypeError("Input not an integer.")

    if num == 0:
        raise ValueError("Input cannot be zero.")
    
    if num < 0:
        raise ValueError("Input cannot be negative.")
    
    if num % 3 == 0 and num % 5 == 0:
        return "fizzbuzz"
    
    if num % 3 == 0:
        return "fizz"
    
    if num % 5 == 0:
        return "buzz"

    return num


def test_multiples_3():
    assert fizz_buzz(3) == "fizz"
    assert fizz_buzz(9) == "fizz"
    

def test_multiples_5():
    assert fizz_buzz(5) == "buzz"
    assert fizz_buzz(10) == "buzz"

    
def test_multiples_3_and_5():
    assert fizz_buzz(15) == "fizzbuzz"
    r = random.randint(1, 100)
    assert fizz_buzz(3*5*r) == "fizzbuzz"


def test_integers():
    assert fizz_buzz(1) == 1
    assert fizz_buzz(7) == 7


def test_neg_numbers():
    with pytest.raises(ValueError):  
        fizz_buzz(-1)


def test_zero():
    with pytest.raises(ValueError):  
        fizz_buzz(0)


def test_string():
    with pytest.raises(TypeError):  
        fizz_buzz("hi")

        
def test_float():
    with pytest.raises(TypeError):  
        fizz_buzz(5.1)
```


- Kaouther

```python
from argparse import ArgumentTypeError
import contextlib


def fizz_buzz(number):
    if not isinstance(number, int):
        raise ArgumentTypeError('Number must be an integer')
    if number <= 0:
        raise Exception('Number should be strictly bigger than 0')
    if number % 15 == 0:
        return "FizzBuzz"
    elif number % 3 == 0:
        return "Fizz"
    elif number % 5 == 0:
        return "Buzz"
    else:
        return number

# Define a testing function
@contextlib.contextmanager
def assert_raises_exception(exception_type):
    try:
        yield
    except exception_type as e:
        pass
    else:
        raise AssertionError(f"Expected {exception_type} but no exception was raised")

def test_fizz_buzz_integer():
    with assert_raises_exception(ArgumentTypeError):
        fizz_buzz(25.33) 
        fizz_buzz("25.33") 

def test_fizz_buzz_failure():
    with assert_raises_exception(Exception):
        fizz_buzz(0)
    with assert_raises_exception(Exception):
        fizz_buzz(-2)

def test_fizz_buzz_fizz():
    assert fizz_buzz(3) == "Fizz"

def test_fizz_buzz_buzz():
    assert fizz_buzz(5) == "Buzz"

def test_fizz_buzz_fizzbuzz():
    assert fizz_buzz(15) == "FizzBuzz"

def test_fizz_buzz_other():
    assert fizz_buzz(2) == 2
```

### 5. Full-cycle collaborative workflow

The exercise takes 30-40 minutes.

In this exercise, everybody will:

A. Set up automated tests with GitHub Actions
B. Make test fail / find a bug in their repository
C. Open an issue in their repository
D. Then each one will clone the repo of one of their exercise partners, fix the bug, and open a pull request (GitHub)
E. Everybody then merges their co-worker’s change


#### Step 1: Create a new repository on GitHub

- Select a different repository name than your colleagues (otherwise forking the same name will be strange)
- Before you create the repository, select “Initialize this repository with a README” (otherwise you try to clone an empty repo).
- Share the repository URL with your exercise group via shared document or chat

- gijs https://github.com/Derks8834/derks-CI-template 
- Cecile https://github.com/Cecilevdstappen/Continues_integration.git
- John: https://github.com/itokaris/myfinalrepo2
- Renske: https://github.com/RenskeW/nlesc-ci-exercise
- Miró: https://github.com/MirovdWorp/cont_integration_test.git
- Pascal: https://github.com/PBJdeKoster/Exercise_eScienceCenter

- Enya: https://github.com/enyasb/ContInt_esb

- Giovanni: https://github.com/giolandrix/giovanni_collaborative_integration_exercise.git


- Deniz https://github.com/deniz-kilic/cintegrationtestrep.

- Dion https://github.com/dlinssen/testrepo/issues/1
- Victoria https://github.com/Victoria-Bruno/CI_exercise

#### Step 2: Clone your own repository, add code, commit, and push

Clone the repository.

Add a file `example.py` containing:

```python=
def add(a, b):
    return a + b

def subtract(a, b):
    return a + b  # do not change this line until prompted to do so.
```

Write a test function `def test_add()` for `add` to check that this function is working properly. Do NOT add a test function for `subtract` (yet).
Run pytest to ensure it works 

Then stage the file (`git add <filename>`), commit (`git commit -m "some commit message"`),
and push the changes (`git push`).


#### Step 3: Enable automated testing

In this step we will enable GitHub Actions.
- Select "Actions" from your GitHub repository page. You get to a page "Get started with GitHub Actions". 
- Select the button for "Set up this workflow" under Python Application. ("update is configure")

![](https://codimd.carpentries.org/uploads/upload_bddaa81119e9608e8027bd0be24f4589.png)

Search for and select “Python application” as the starter workflow.

GitHub creates the following file for you in the subfolder `.github/workflows`:


   ```yaml
# This workflow will install Python dependencies, run tests and lint with a single version of Python
# For more information see: https://help.github.com/actions/language-and-framework-guides/using-python-with-github-actions

name: Python application

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python 3.9
      uses: actions/setup-python@v2
      with:
        python-version: 3.9
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install flake8 pytest
        if [ -f requirements.txt ]; then pip install -r requirements.txt; fi
    - name: Lint with flake8
      run: |
        # stop the build if there are Python syntax errors or undefined names
        flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics
        # exit-zero treats all errors as warnings. The GitHub editor is 127 chars wide
        flake8 . --count --exit-zero --max-complexity=10 --max-line-length=127 --statistics
    - name: Test with pytest
      run: |
        pytest
   ```

Replace `pytest` by `pytest example.py`:
```yaml
   - name: Test with pytest
     run: |
       pytest example.py
```
![](https://i.imgur.com/1TFZPRe.png)


Commit the change by pressing the "Start Commit" button.

#### Step 4: Verify that tests have been automatically run

Observe in the repository how the test succeeds. While the test is executing, the repository has a yellow marker.
This is replaced with a green check mark, once the test succeeds.

![](https://i.imgur.com/b8dI8XH.png)

Green check means passed.

Also browse the "Actions" tab and look at the steps there and their output.

#### Step 5: Add a test which reveals a problem

After you committed the workflow file, your GitHub repository will be ahead of your local cloned repository. Update your local cloned repository:

```
$ git pull origin main
```

Next uncomment add a test function `test_subtract` for to check that the `subtract` function can subtract two numbers from each other, and push it to your remote repository.
Verify that the test suite now fails on the “Actions” tab (GitHub).


#### Step 6: Open an issue on GitHub
Open a new issue in your repository about the broken test (click the “Issues” button on GitHub and write a title for the issue). The plan is that your colleague will fix the issue through a pull request

#### Step 7: Fork and clone the repository of your colleague

Fork the repository using the GitHub web interface. 
Make sure you clone the fork after you have forked it. Do not clone your colleague’s repository directly.


#### Step 8: Fix the broken test

Fix the function now and run pytest to check that it works.
Then push to _your fork_. Check whether the action now also passes.

#### Step 9: Open a pull request (GitHub)

Then before accepting the pull request from your colleague, observe how GitHub Actions automatically tested the code.

If you forgot to reference the issue number in the commit message, you can still add it to the pull request: `my pull request title, closes #NUMBEROFTHEISSUE`

#### Step 10

Observe how accepting the pull request automatically closes the issue (provided the commit message or the pull request contained the correct issue number).

Discuss whether this is a useful feature. And if it is, why do you think is it useful?

## 🧠 Collaborative Notes
    
Welcome to the 2<sup>nd</sup> day of the workshop! Today will be a great day!

### 1. Developing modular code

#### What is modularity?
- Building software from smaller pieces. 
- We build individual parts of code that are self-contained and independent, deals with one specific task. From these components we can build complex behaviour. Small cohesive untis usually work better than one complex big thing!
- Modularity makes your code ease to understand, change, and maintain.

#### What are these elements ?
- functions
- classes
- modules
- packages
- libraries

#### Why writing modular code ?
This makes your code easier to:
- understand
- test
- maintain
- debugg
- reuse
- less complex (concept of`separation of concerns`)

**Remember**: in separting you project into self-contained and cohesive units you increase its capabilities and its power!

#### What is a good module?
- A good module performs a limited, clearly definied task. It has a proper name and is readable.
- Readability is not the same as being as short as possible! By just using a function with a clear name, you make things more readable.
- A good module is 'pure', it does not have a state. This means it does not interact with the outside world except input and output. It has no side-effects.
**example**: <u>a stateful function changes its environment and interacts with external resources. This is something we always want to avoid in our code.</u>

#### Indentifying opportunities for modularity?
- focus on readability: modular code is more readable. It is read more frequently than it is writen.
- "Code smell" is a polite way to say readability "stinks", but code will be read. If code is easily readable, it is understandable for you (later) and others and can be more easily extended in the future. 
- https://refactoring.guru/refactoring/smells 

#### Indentify future functions
- Don't Repeat Yourself (DRY): You should not be repeating code. Anything that is repeated should be in a function instead.
- Candidates for a function can be identified by their actions (`plot`, `read`, `get`, `put`...). The naming of functions often goes by their action. Functions should be named to make the action obvious. If you see nested code, e.g. loops within loops, that is often a hint the code can be rewritten in a better way.

We will cover tests later, but each module should have a test. Tests help you identify places code can be improved. 

**Remember:**
- <u>If the test is very complex and difficult to make, it may be an good indicator that code can be improved!</u>

- <u>If you cannot test something at all, this may be an indication that the function probably can be re-written in a better way!</u>

#### Lessons learned from the "Modularity" exercise:
After `refactoring` (i.e., the process of rewriting the same code), we noticed that the code is now:
- more robust, modular and readable.
- easier to be tested: each function/unit can be tested separatetly.
- can be reused: `conversion_mod.py` or `conversion_mod_class.py` can be used in another project in the future.
- maintained: each module and functions can be altered indepentently without having to change the whole code base.
- extended: further independent "pieces" or "blocks" (modules, functions) can be added in the future.

### 2. Documentation

Documentation is not only for others but also for yourself (for example in the future).

#### What kinds of documentation do we have?
- Web sites like in https://pages.github.com/
- Docstrings in functions (in-code documentations)
- README files
- Tutorials
- API documentation: autogenerated from your code, e.g., `doxygen`, `sphinx`

##### README files
this is the first thing a user or collaborator sees. What should be there? Something covering parts or files of the project. Author and contact info. Installation guide. The overall purpose of the project and context. Citation, lisence, usage. Some things can be in a readme or in additional files, but readme is a good entry point e.g. changelog, license.

##### In-code documentation

This refers to proper placement of `comments` and `docstrings`. This makes your code readable to your collaborators/co-developers.
- There can be many reasons to not write much in terms of comments. Comments should never be used to replace version control or improper variables/function naming.
- Docstrings are special kinds of comments. They can be used to describe the functionality of a module/function and also to generate documentation.

##### User/API documentation
To generate a `sphinx` documentation:

Activate your conda environment
```bash
conda activate coderefinery
```
Make a directory `doc-example`
```bash
mkdir doc-example/
```
Run `sphinx` and follow the instructions
```bash
sphinx-quickstart
```
Edit the `index.rst` file
```bash
nano index.rst
```
Add
```bash
nano some_feature.md
```
Edit the `conf.py` file
```bash
nano conf.py
```
Add
```bash
extensions = ["myst_parser"]
```
Generate the documentation
```bash
sphinx-build . _build
```

To open the documentation:
Linux users type:

`$ xdg-open _build/index.html`

macOS users type:

`$ open _build/index.html`

Windows users type:

`$ open _build/index.html`

Or find the file `~/Desktop/doc-example/_build/index.html` in your file explorer.

### 3. Testing

#### Why do we need test ?
- Prevent functionality by detecting error early in the project and facilitate reproducibility
- Help users. With this, they can easily verify correct installation
- Help developers to refactor your code in the future

#### Test types
- Unit test: test only small units of your software, e.g., a function
- Integration test: test unit interaction, e.g., check the proper interaction between two modules
- .... other types of testing aiming at checking the integration of the software as a whole or that eventual new changes made do not affect other existing parts of the software

#### How much test is enought?
test metrics:
- lines of code
- test coverage: checks to which extent your software is being coverted by your tests.

#### Pytest
The most recommended way to test your `python` code:
- collects and runs all test functions starting with `test_`

Example of pytest for unit tests
```bash
mkdir pytest-example
cd pytest-example
```
Make a file `example.py` and with `nano example.py` write the follow code:
```bash
def sum(a, b)
    return a + b

def test_sum()
    assert sum(2,3) == 5
```
Activate your conda environment
```bash
conda activate coderefinery
```
Check the version of `pytest`
```bash
pytest --version
```
Run the test
```bash
pytest example.py
```
Add an extra assert into `example.py` using `nano example.py`:
```bash
def sum(a, b)
    return a + b

def test_sum()
    assert sum(2,3) == 5
    assert sum('space', 'ship') == 'spaceship'
```

<u>Impure functions</u>: functions that contain one or more side effects. It mutates data outside of its lexical scope and does not predictably produce the same output for the same input; see also the definition of `stateful function` above

**Remember**
When testing:
- Use `pure` functions whenever possible.
- If testing is hard, this means that your code needs to be more modular.
- You do not have to strive for 100% test coverage.
- Testing removes the dread of refactoring.


### 4. Continuous Integration

#### What is continuous integration ?
automating the integration of code changes from multiple contributors 

#### What is it good for ?
- Linting (checks whether your code follows some code format convention)
- Automated testing (run tests automaticaly on your GitHub repo every time you make a commit)
- Security analyses
- Send messages
- Build and compiling
- Deploying

#### Advantages of CI
- This good practice is a time-investiment with returns
- CI saves time and keeps your project clean
- You are able to check errors/mistakes early on your project

## 📚 Resources
- [Workshop slides](https://nlesc-slides.github.io/2023-06-19-ds-cr)

- [Lesson github repository](https://github.com/esciencecenter-digital-skills/good-practices-in-research-software-development) This is where you can open an issue to give your feedback and improvements on the teaching materials.

- https://refactoring.guru/refactoring/smells

- [Numpy docstring conventions](https://numpydoc.readthedocs.io/en/latest/format.html)

- [Python exception/error types](https://docs.python.org/3/library/exceptions.html)

- [Pytest documentation](https://docs.pytest.org/en/7.1.x/contents.html)

- [Testing frameworks for Fortran](https://fortranwiki.org/fortran/show/Unit+testing+frameworks)

- [Documentation Teaching materials](https://coderefinery.github.io/documentation/)

- [Testing Teaching materials](https://coderefinery.github.io/testing/)

- [Five recommendations for FAIR software](https://fair-software.nl/)

- [Choose an open source license](https://choosealicense.com/)

- [Automated documentation deployment using github actions and github pages](https://coderefinery.github.io/documentation/gh_workflow/)