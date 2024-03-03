# Fully Homomorphic Encryption based on Learning with Error Scheme using Python

## Overview
Fully Homomorphic Encryption (FHE) is a cryptographic technique that allows computations to be performed on encrypted data without decrypting it first. This README provides an overview of implementing FHE based on the Learning with Error (LWE) scheme using Python. 

## Features
- **Encryption and Decryption**: Implementations for encrypting and decrypting data using the LWE scheme.
- **Homomorphic Operations**: Support for performing homomorphic addition and multiplication operations on encrypted data.
- **Key Generation**: Generation of public and private keys for encryption and decryption.
- **Integration with Python Applications**: Easily integrate FHE into your Python applications for secure computation on encrypted data.

## Installation
1. Clone or download this repository to your local machine.
   ```
   git clone https://github.com/your_username/fhe-learning-with-error-python.git
   ```
2. Navigate to the project directory.
   ```
   cd fhe-learning-with-error-python
   ```
3. Install required dependencies.
   ```
   pip install -r requirements.txt
   ```

## Usage
1. Import the FHE library into your Python project.
   ```python
   import fhe
   ```
2. Generate public and private keys.
   ```python
   public_key, private_key = fhe.generate_keys()
   ```
3. Encrypt your data.
   ```python
   encrypted_data = fhe.encrypt(public_key, plaintext_data)
   ```
4. Perform homomorphic operations on encrypted data.
   ```python
   result = fhe.homomorphic_operation(public_key, encrypted_data1, encrypted_data2)
   ```
5. Decrypt the result.
   ```python
   decrypted_result = fhe.decrypt(private_key, result)
   ```
6. Use the decrypted result in your application.

## Example
```python
import fhe

# Generate keys
public_key, private_key = fhe.generate_keys()

# Encrypt data
plaintext_data1 = 5
plaintext_data2 = 7
encrypted_data1 = fhe.encrypt(public_key, plaintext_data1)
encrypted_data2 = fhe.encrypt(public_key, plaintext_data2)

# Perform homomorphic addition
result_addition = fhe.homomorphic_addition(public_key, encrypted_data1, encrypted_data2)

# Perform homomorphic multiplication
result_multiplication = fhe.homomorphic_multiplication(public_key, encrypted_data1, encrypted_data2)

# Decrypt results
decrypted_result_addition = fhe.decrypt(private_key, result_addition)
decrypted_result_multiplication = fhe.decrypt(private_key, result_multiplication)

print("Homomorphic Addition Result:", decrypted_result_addition)
print("Homomorphic Multiplication Result:", decrypted_result_multiplication)
```

## Contributing
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Create a new Pull Request.


## Acknowledgments
- Thanks to all contributors who helped improve this implementation.
