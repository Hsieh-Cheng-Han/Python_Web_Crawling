# Manual for Android App, Assignment4

## 1. User Interface

Here is the user interface of the App **SDPEncrypter** :

<img src="https://i.ibb.co/44jL7NP/normal.png" alt="normal" border="0" width="230" height="400">

 As you can see, there are three fields which you can key value into. 
 
The first field is **Message**, where you can key in the message string which you would like to encrypt.

The second field is **Alpha Value**, where you can specify an integer used in [Affine Cipher](https://en.wikipedia.org/wiki/Affine_cipher) encryption as **a**.

The third field is **Beta Value**, where you can specify an integer used in Affine Cipher encryption as **b**.
  
Below are speficied input types for all three fields :


| Field | Input Type |
| ----- | ----------- |
| Message | A **non-empty string** containing at least one alphabet |
| Alpha Value | A **positive integer** smaller and coprime to 26 |
| Beta Value | An **integer** falling in the range [0,1,2...25] |

## 2. Encryption Algorithm

Below illustrates how the encryption algorithm does :

### 1. Within the input message, each letter in the alphabet is assigned a numeric value between 0 and 25 based on its position in the alphabet (i.e., a=0, b=1, c=2, …).

### 2. For each letter in the alphabet, where the numeric value is x, the encrypted value of the letter is defined as E(x) = (αx + β) % 26, as in an Affine Cipher.

### 3. The encrypted character for the input letter is calculated by taking the encrypted number, which is a value between 0 and 25, and translating it back into a letter (again, where a=0, b=1, c=2, …). In addition, all non-alphabetic characters must remain unchanged.

### 4. Capitalization of alphabetic characters will be inverted (i.e., all lowercase characters are transformed into upper case characters and vice versa).
