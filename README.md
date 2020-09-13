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
| Message | A **string** containing at least one alphabet |
| Alpha Value | A **positive integer** smaller and coprime to 26 |
| Beta Value | An **integer** falling in the range [0,1,2...25] |
