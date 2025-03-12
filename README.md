Code Signing Implementation Using ECDSA
This project implements a code signing system using the Elliptic Curve Digital Signature Algorithm (ECDSA). The implementation includes a validator component that verifies the authenticity of a product using digital signatures.
Project Overview
Code signing is a security practice that uses digital signatures to verify the authenticity and integrity of software. This project demonstrates the key components of a code signing system:

Key generation (public/private key pair)
Product creation
Digital signature generation
Certificate validation

Prerequisites

Google Colab or Python 3.6+
Required Python libraries:

cryptography



Implementation Details
Key Components

Key Generator: Creates ECDSA public and private keys
Product: A simple Python program that prints a message with a student ID
Signer: Signs the product using the private key
Validator: Verifies the signature using the public key

Workflow

Generate a public/private key pair using ECDSA
Create a simple product (Python script)
Sign the product using the private key
Validate the product's signature using the public key
Execute the product only if the signature is valid

Security Features

Uses ECDSA with the SECP256R1 curve (NIST P-256)
SHA-256 hash function for creating message digests
Base64 encoding for signature storage
Validation before execution to prevent unauthorized code from running

Usage
Installation
!pip install cryptography
Running the Project

Generate keys:

pythonCopyprivate_key, public_key = generate_keys()

Create the product:

pythonCopyproduct_code = create_product("YOUR_STUDENT_ID")

Sign the product:

pythonCopysignature = sign_product(product_code)

Validate and execute:

pythonCopyvalidate_product(product_code)
Testing
The project includes tests for both valid and invalid scenarios:

Valid scenario: The original product passes validation and executes
Invalid scenario: A tampered product fails validation and is blocked from execution

Theoretical Background
This implementation is based on the principles of digital signatures described in:

Boneh and Shoup, Chapter 13
Rosulek, Chapter 13
Code Signing Whitepaper, CA Security Council
D. Cooper et al., Security considerations for code signing

Author: ANU 
student ID: 11696378
