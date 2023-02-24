
### Memory unit format
- example: if a memory unit is adressing by bit, then  adress( 0000A000H ~ 0000BFFFH) has: 1FFFH(BFFFH - A000H + 1 = 2000H), which is 8k(8*1024) store unit

## CRC (Cyclic Redundancy Check)
- coding by creating polynomial
- length: if a data has k bit (10000000's digits is 8,so k=8), and has r bit checking bit, total length will be k+r
### How to create a CRC code
1.if the original data is 101011, and the arranged polynomial(P= x^4 + x + 1) 
2.unfold all the x's power in the polynomial ( P= 1*x^4 + 0*x^3 + 0*x^2 + 1*x^1 + 1*x^0), which is 10011 (P has 5 bit, P- 1  =highest power of the polnomial)
3.add (P-1)*0 after the original data(101011)-(M: 1010100000)
4.use M divide P(P is the divisor), get a remainder R(R has n bits)
5.add R at the end of the original data
- example:  101011(origin), P=10011  
- origin turns into 1010110000
- 1010110000/10011=101100, remainder = 0100
---------------too difficult, solved later-------------------

# Words
- if a machine's word length is n, and the first bit is the sign bit(0 for positive and 1 for negative)
- then the highest number it represents would be: 
- for example n=8, 1111 1111 ,first bit is the sign bit, then highest value= 111 1111= 1000 0000-1 = 2^(n-1)-1
- ok

## IEEE754 standard
- a technical standard for floating-point computation 
## floating-point number
- usually in this form: N = (2^E)*F, E= Exponent ,F=Mantissa
- Exponent in 'offset binary'
- Mantissa in 'true form'
- length of Exponent decides the range
- length of Mantissa decides the precision
## floating-point range(floating point<1)
- if a code got 6 exponent, a plus/minus sign, 8 mantissa
- exponent in AUTH form, mantissa in complement form
- then its range sould be:  minimum: -2^(63),  maximum: (1-2^(-8))*2^63


## Overflow
- digits calculation usually uses twos complemt formats
- for example: binary in 8 number= 0~255(1111 1111)
- 0~127 represents 0 and positive number(0~127)
- 128~255 represents negative number(-128~-1)
- in this way, if (positive number)+ (positive number)>127  {99+99=198, 198>127}, 198 is negative, this is called"overflow"
### How to find overflow
1. reselts:  p+p=n, n+n=p, p-n=n, n-p=p
2. decimal
3. OV = 1

## Hamming code
- add k checking number in data
- if data has 48 numbers, k should be (2^k -1 >=k+ n)
### Hamming code Verification
- if a data got 10 bits 1111111111. each bit got a number, we called it 9876543210
- then its hamming code should be: 9 8 7 6 5 4 (H4) 3 2 1 (H3) 0 (H2) (H1)
- 9 was checked by H4、H3、H2(9 was at 14th of the code, 14=8+4+2）
- 5 was checked by H4、H2( 5 was at 10th, 10= 8+2)
- 4 was checked by H4、H1(4 at 9th, 9=8+1)
- 
------------ forming process too complex, won't decribe here  -------

# Code
## reverse form
- expect the first bit, all reverse(true:1000 0000---1111 1111)
## complement form
- if x's complement code is 90H, then:
- 90H's binary= 1001 0000
- a code's complement's complement = true form
- 1001 0000's complement= reverse form + 1= 1111 0000(first number represents negative or negative)
- so its true form is 1111 0000, x should be decimal so x= -112 (first number =1 means negative)
### complement form range
- minimum:-1
- maximum: 63(2^6-1)
### Why use complement Form
- when showing data in complement form, positive/negative and other bits can be handled together(minus can be handled as plus), in order to simplify the structure design


# Spatial locality
- Definition: All those instruction which are stored nearby to the recently executed instruction have high chances of execution.
# Temporal Locality
- Definition: A instruction which is recently executed have high chances of execution again.


# Addressing
## Immediate addressing
- NOT addressing mode:Instruction format that directly includes the data to be acted on( as part of the instruction)
## Direct addressing
- Instruction that conatins the actual address of the data. Operand field directly specifies the memory location where the data
is residing.(operand in Memory unit)
## Register Addressing
- register contains the operand(Instruction will give the register's name)
## Indirect addressing
- contents of the address are spectified in the instruction, address are used to provide the desired memory reference
## Relative addressing
- designating locations in relation to the location counter or to some symbolic location.(Operand address+a value, so that the programm can float)
## Indexed addressing
- Method that generates address, which modifies the specific address(specific address was given by the contents of a specified index register)


# BW (Bandwidth)
- data transportation ability
- for example is a Bus got a 32bit width, 200Mhz clock rate,  every 5 cycles can transport 32bit
- then this BUs got a (200Mhz/5) * (32bit/8=4byte)= 160Mbps

# Streamline
- already know, pass
- using asynchronous control system WON'T enhance its efficiency
- TO reach the highest efficiency, all part of streamline should take the same time to operate

# Certificate Authority
- character: CA, A, B
- If B has applied a credential from CA, and A wants to verify it
- then A needs the 'Public key' of CA to verify
## example
- IF A and B wants to communicate, A's letter has digital signature
- When B receive the letter, B need to use A's public key to verify it
## algorithm could be used on Certificate Authority
- RSA are usually for signing abstracts.
- IDEA and RC4 suitable for data transportation encrypting
- MD5 for Abstract
# Keys encryption
- DES( data encryptiong standard) encryption algorithm that converts plain text into blocks then uses a key to convert it to ciphertext.
# PKI(Public Key Infrastructure)
- To secure the CA not to be modified and sent to the owner, need to use  **CA's private key** for signature.

# Encryption
## RC5
### RC5 definition
- a fast block cipher developed based on symmetric key encryption.
- **Feature: quite fast**  (it uses only primitive computer operations)
- <font color=red>which means it's suitable for numerous text encryption</font>
- allows a variable number of rounds and variable bit size key to add flexibility
- _**requires less memory for execution**_, (which enables RC5 to be used for various purposes like desktop operation, smark cards.etc）
### How does RC5 works?
- in RC5 algorithm, the input key can be of variable length
- Once the values are decided, the values will remain the same for a particular execution of the Cryptographic algorithm
- In RC5, the plain text message is divided into two blocks A and B each of 32 bits. Then two subkeys are generated 0 and 1. 
- These subkeys are added into A and B respectively. This process produces C and D respectively and marks the end of the One-Time Operation.
- Then the process of the round begins. In each round, the following operation is performed:
- Bitwise XOR
- Left circular shift
- addition to the next subkey, for both C and D. This, is the addition operation, and then the result of the addition mod is 2^w is performed
- -------very complex, only need to know definition-------------------


## IDEA
- AES
