# PYcrypt

- PYcrypt is a polymorphic 'python backdoors' crypter written in python .
The output  is fully undetectable .

- PYcrypt can inject malicious python file into  a normal file with multi-threading system .

- Run it with superuser's permissions .
- PYcrypt output is Fully undetectable  .

Encryption Module

![Alt text](https://image.ibb.co/jO9mdd/Encryption_Module.png "Encryption Module ")


# Usage :

 - sudo  ./PYcrypt.py --file=backdoor.py --output=output_backdoor.py # encrypt backdoor.py and output file is output_backdoor.py
 - sudo ./PYcrypt.py --file=shell.py # encrypt shell.py and default output file  is backdoor.py but you can edit it in source code
 - sudo ./PYcrypt.py --help # PYcrypt help
 - sudo ./PYcrypt.py --backdoor-file=payload.py --file=test.py --output=hacked.py # inject payload.py with  test.py into hacked.py with multi-threading system
 
 # How it work ? 
 
 * Encryption module :
 
 - PYcrypt add some junkcode .
 - PYcrypt use a python internal module 'py_compile' who compile the code into bytecode to a .pyc file .
 - PYcrypt convert .pyc file into normal .py file .
 - And in this way we can obfuscate the code
 - The md5sum will change too
 
* Injection  module :

- it inject a malicious python file  into a normal file with multi-threading system .

 # Test with SpyralScanner
 
Before :
 
SHA256:	fe6a1a9aef68a8ce22d9db6e5e0ab9d17551e23fa2a3d45f5a9faf1577fc8d5a
File name:	netsecnow.py
Detection ratio:	2 / 32

After  :

SHA256:	c7aa4c8d8f77b898a8e23bd7ca0b52c8d1a353a69b94f4872e39697c9ee2b0df
File name:	netsecnow_crypt.py
Detection ratio:	0 / 32


 
