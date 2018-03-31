# bank-tech-test

A practice tech test from Makers Academy. I've chosen to do it with Python as
it fits in with my blog which can be found at:

## Getting Started

* Open

```
git clone https://github.com/noel1uk/bank-tech-test.git
```

## Running the tests
To run tests you need to install Pytest in the root of the project. You need pip to install Pytest, to install pip:

```
sudo easy_install pip
```

```
pip install -U pytest
```

To install FreezeGun, simply:
```
pip install freezegun
```

To install Mock

```
pip install mock
```

Then type pytest in terminal


## Checking the coverage


To check for coverage you need to have pytest-cov. Install it with:

```
pip install pytest-cov

```
Then type:

```
py.test --cov ./
```

## How to use

Got into the directory and open irb or another REPL such as ipython.

It's made up of three classes:

__Account__
Which has has balance and history attributes.
It has deposit, withdraw and save_transaction methods.

It can be used like this:

![Alt text](https://raw.githubusercontent.com/noel1uk/bank-tech-test/757dbd830d8e7938f010d3b900fcba799d0f668c/images/account.png?raw=true "Optional Title")

The deposit and withdraw methods use the save_transaction method to save transaction details to the history attribute.

__Formatter__

The Formatter class takes the account history as a parameter. It has reverse method reverses the order of the lists, the format_integer method which gives the integers two decimal places and converts them into strings. The to_string method  changes the lists into strings and transforms them into strings to complete in the form requested by the project requirements.

![Alt text](https://github.com/noel1uk/bank-tech-test/blob/images/images/formatter.png?raw=true "Optional Title")

__View__

The View class takes the processed_history attribute from the Formatter class object and prints it to screen.

![Alt text](https://github.com/noel1uk/bank-tech-test/blob/images/images/view.png?raw=true "Optional Title")


## User stories

```
As an account holder,
I want to be able to deposit money into my account,
so that I can have somewhere to keep money.
```

```
As an account holder,
I want to be able to withdraw money from my account,
so that I can get my money back
```

```
As an account holder,
I want to be able to see any transactions I have made,
so that I can see how much money I have put in and withdrawn
```

```
As an account holder,
I want to be able to see when I have made transactions,
so that I can remind myself when I have made withdrawals and deposits
```

### Acceptance criteria

**Given** a client makes a deposit of 1000 on 10-01-2012  
**And** a deposit of 2000 on 13-01-2012  
**And** a withdrawal of 500 on 14-01-2012  
**When** she prints her bank statement  
**Then** she would see

```
date || credit || debit || balance
14/01/2012 || || 500.00 || 2500.00
13/01/2012 || 2000.00 || || 3000.00
10/01/2012 || 1000.00 || || 1000.00
```
