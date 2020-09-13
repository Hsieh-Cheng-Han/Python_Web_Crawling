# Manual for Android App, Assignment4

## 1. User Interface

Here is the user interface of the App **SDPEncrypter** :

<img src="https://i.ibb.co/44jL7NP/normal.png" alt="normal" border="0" width="230" height="400">

 As you can see, there are three fields which you can key-in value. 
 
The first field is **Message**, where you can key-in the message string which you would like to encrypt.

The second field is **Alpha Value**, where you can specify an integer used in [Affine Cipher](https://en.wikipedia.org/wiki/Affine_cipher) encryption as **a**.

The third field is **Beta Value**, where you can specify an integer used in Affine Cipher encryption as **b**.

Press the `ENCRYPT` button and the encrypted message will show up on the screen.
  
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

## 3. Example 

When Input Message = "Cat & Dog" ans set α = 3,  β = 8

The encrypted Message will be "oIN & rYA"

<img src="https://i.ibb.co/1KQHQY2/2020-09-13-11-55-01.png" alt="2020-09-13-11-55-01" border="0" width="230" height="400">

Here is the explanation:
"C" has value 2, 2*3+8=14, which corresponds to "o" (lowercase since "C" is capitalized).

"a" has value 0, 0*3+8=8, which corresponds to "I" (capitalized because "a" is lowercase).

## 4. Error Warning

If you key-in invalid values, the system will pop out an error warning.

Here are three error examples:

### 1. There is no any alphabetic character in the input message.

<img src="https://i.ibb.co/MGgm6zn/2020-09-13-11-56-29.png" alt="2020-09-13-11-56-29" border="0" width="230" height="400">

### 2. Alpha value is not coprime to 26.

<img src="https://i.ibb.co/njghCnH/2020-09-13-11-57-11.png" alt="2020-09-13-11-57-11" border="0" width="230" height="400">

### 3. Beta value is not in the range [0,1,2,...25].

<img src="https://i.ibb.co/PFJrzgg/2020-09-13-11-57-27.png" alt="2020-09-13-11-57-27" border="0" width="230" height="400">

Notice that each error message is independent so it is possible to pop up multiple error warnings.

If the error warning occurs, the encrypted message will be set to an empty string(so no result will show up in the screen).


