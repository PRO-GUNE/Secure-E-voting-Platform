# Secure-E-voting-Platform
A secure e-voting platform implemented based on security principles of blind signatures ensuring confidentiality, integrity, authenticity, untraceability requirements

## About
- A streamlit based implementation for a secure e-voting platform. Concept of blind signatures is used to ensure the confidentiality and validity of votes.

- Different key-pairs based on RSA Encryption scheme are used for encrypting/decrypting and blind signatures. The scheme is implemented from scratch using helper functions given in `src\utils`.

- Database models are used to provide abstraction for database calls. Transactions are used when adding votes to votepool to ensure correctness of the system. A Remote SQL database is used for hosting the database.

- A psuedo-blockchain approach is used when adding votes to the votepool to ensure integrity and authenticity of the votes. This is done by involving the key of the previous vote when calculating the key of the next vote.

## Usage
- Clone the repository
- Install streamlit using the following command
```bash
pip install streamlit
```

- Run the Trusted Authority server using the following command from the src directory
```bash
export FLASK_APP=trustedAuthority/app.py
python -m flask run
```

- To run the streamlit app, run the following command from the src directory
```bash
python -m streamlit run client/app.py
```

