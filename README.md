# 3D-Model-Steganography
Hybrid model for Cryptography and Steganography
It defines a class called SecureFaceSteganography which is designed to hide secret messages within a 3D face model (.obj file). This technique is called steganography.
!pip install pycryptodome and !pip install trimesh: These lines install the necessary libraries. pycryptodome is used for encryption, and trimesh is for working with 3D models.
import ...: This section imports the required Python modules, including libraries for numerical calculations (numpy), encryption (Crypto), hashing (hashlib), random number generation (secrets), data structures (struct), 3D model handling (trimesh), and spatial data structures (scipy.spatial).
This code implements a sophisticated 3D Face Steganography system that allows secure embedding and extraction of encrypted messages within 3D face models. Here's a breakdown of its key features:

1. Encryption Mechanism
- Uses AES-128-CBC encryption
- Generates cryptographically secure random passphrase
- Applies key derivation with salt using SHA-256
- Pads messages to ensure secure encryption

2. Data Embedding Process
- Identifies landmark regions on the face (forehead, cheeks, jaw, nose, chin)
- Uses a KD-tree to find vertices near landmark points
- Computes vertex importance based on geometric features
- Embeds encrypted message bits by slightly displacing vertices along their normal vectors

3. Key Methods
- `encrypt_message()`: Encrypts input message
- `decrypt_message()`: Decrypts encrypted data
- `embed_in_face_model()`: Hides encrypted data in 3D face model
- `extract_from_face_model()`: Retrieves hidden message from modified model

4. Security Features
- Uses cryptographically secure random number generation
- Implements salting and key derivation
- Minimizes potential facial model corruption by using small displacement scales

The system allows hiding messages in 3D face models with minimal detectable changes, providing a unique steganographic approach.
