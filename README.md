# NNP_Chem Encrypted Distribution

This repository intentionally contains only encrypted release archives for `NNP_Chem`.

## What is published here

- `NNP_Chem-YYYYMMDD.tar.gz.age`
- `NNP_Chem-YYYYMMDD.tar.gz.age.sha256`

The plaintext source code is not published in this repository.

## Verify and decrypt

Install `age`, then decrypt with the passphrase shared out of band:

```bash
age -d -o NNP_Chem-YYYYMMDD.tar.gz NNP_Chem-YYYYMMDD.tar.gz.age
tar xzf NNP_Chem-YYYYMMDD.tar.gz
```

You can verify the checksum before decrypting:

```bash
shasum -a 256 -c NNP_Chem-YYYYMMDD.tar.gz.age.sha256
```

## Notes

- Treat the passphrase as a secret, not a short keyword.
- The passphrase should be shared over a separate channel.
