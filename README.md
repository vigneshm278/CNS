## EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## Name: VIGNESH M
## Reg: 212223240176 

## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


## PROGRAM :-
~~~
def caesar_cipher(text, shift, encrypt=True):
    def shift_char(char, shift):
        shift_base = ord('A') if char.isupper() else ord('a')
        return chr((ord(char) - shift_base + shift) % 26 + shift_base)
    
    if not encrypt:
        shift = -shift  # Reverse the shift for decryption
    
    result = "".join(shift_char(char, shift) if char.isalpha() else char for char in text)
    
    return result

# Get input from user
message = input("Enter the message: ")
shift = int(input("Enter the shift value: "))

encrypted = caesar_cipher(message, shift, encrypt=True)
decrypted = caesar_cipher(encrypted, shift, encrypt=False)

print(f"Original: {message}")
print(f"Encrypted: {encrypted}")
print(f"Decrypted: {decrypted}")
~~~



## OUTPUT :-
![image](https://github.com/user-attachments/assets/c6ffad41-729f-42bf-a09c-00608a4cd30c)


## Result :
Thus, encryption and decryption of the given message by using Ceaser Cipher encryption algorithm is implemented successfully.

