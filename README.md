![image](https://user-images.githubusercontent.com/90667844/155042734-9878e6ef-b07c-45b4-9847-7916f5a72f9e.png)

# fintech_finder
### A web application that customers can use to find fintech professionals from a list of candidates, hire them, and pay them.

## Technologies
This analysis leverages python 3.7 with the following packages and libraries:
* [web3](https://web3py.readthedocs.io/en/stable/)
* [bip44](https://pypi.org/project/bip44/)
* [dotenv](https://pypi.org/project/python-dotenv/)
* [streamlit](https://streamlit.io/)
* [ganache](https://trufflesuite.com/ganache/?utm_source=devportal)
---

## Installations
```python
pip install streamlit
pip install web3
pip install python-dotenv
pip install bip44
```
---

## Imports

### fintech_finder.py
```python
import streamlit as st
from dataclasses import dataclass
from typing import Any, List
from web3 import Web3
w3 = Web3(Web3.HTTPProvider('HTTP://127.0.0.1:7545'))
```
### crypto_wallet.py
```python
import os
import requests
from dotenv import load_dotenv
load_dotenv()
from bip44 import Wallet
from web3 import Account
from web3 import middleware
from web3.gas_strategies.time_based import medium_gas_price_strategy
```
---

## Usage
1.a. In the terminal, navigate to the folder where you've cloned the repository.

1.b. Create a Ganache account. Use the "Quickstart" option to generate a mnemonic seed phrase. Create a .env file in the repository and add the seed phrase.

2. In the terminal, run the Streamlit application by using `streamlit run fintech_finder.py`.

3. In the Sidebar of the web application, select the person you would like to hire and for how many hours. Then click the "Send Transaction" button to send the payment. A successfull payment will show a "Validated Transaction Hash." 

4. Inspect the successfull transactions in Ganache: 

  a. Address, balance, and transaction (TX) count:
![image](https://user-images.githubusercontent.com/90667844/155033128-241622a7-93ab-4262-988c-c05a872ff49f.png)

  b. Transaction details:
![image](https://user-images.githubusercontent.com/90667844/155039954-6337e0a4-923e-4969-9218-e4a9f08ed412.png)
---

## Contributors
[Noah Beito](https://www.linkedin.com/in/noah-beito/)
---
## License
[MIT](https://github.com/git/git-scm.com/blob/main/MIT-LICENSE.txt)
