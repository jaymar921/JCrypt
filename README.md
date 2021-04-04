# JCrypt
Encryption/Decryption (University Project)

This repository is made for educational purpose only
I programmed this using Java since it's the only programming language that I have knowledge.

I have provided 2 classes which is the Signature class and the JCrypt class

(Signature class)
  This class is capable of generating a random key that will be used for 
  the JCrypt class
  
  Declaration
	
  Signature sign = new Signature();
  
	Constructor Parameters
		Signature(String signatureName, int signatureValue);  <- generated key will be manual/fixed
		Signature(String signatureName);                      <- generated key will be random
		Signature();                                          <- generated key will be random
	
  Generating a key
  sign.generateKey();
	
      returns a String of this pattern (00000XXX000XXX000XZ)
	    where:
            -0 is a random digit
            -x is a random capital letters
            -z is a random capital letters but is used to determine if the generated key is (R)random or (M)manual/fixed
						
(JCrypt class)
	This class will will use the key that is provided by the
	signature class to encrypt/decrypt the data in string
	
  Declaration
		JCrypt crypt = new JCrypt(String signature);
		
	Constructor Parameters
		JCrypt(String data, String signature, String path, String filename) 
		JCrypt(String data, String signature, String path) 
		JCrypt(String data, String signature) 
		JCrypt(String signature)                        <- this will be the best option when declaring the JCrypt class
		
	Methods
		Setting the class::
		passObject(String data)          <- gets the string data that will be used for encryption/decryption'
		setSignature(String signature)   <- change the signature
		
		Operations::
		getEncrypted()                   <- returns a string of encrypted data
		getDecrypted()                   <- returns a string of decrypted data
		
		Save/Load a file::
		//if the filename or path is not provided during the declaration, it will
		//save the file as "data.jcrypt" as default
		save()                           <- save the encrypted/decrypted string to a file
		load()                           <- loads a file that contains a string
		
This project just for educational purpose only, I just wanted to share my creativity to everyone
		
	
