# File format

## Introduction

Praesidium uses a custom vault file format, this format is __guaranteed__ to be stable across major versions

## Terminology
* A Praesidium vault is called an __Arca__
* A secret stored inside an Arca is called an __Arcanum__

## Specification

### Overview

| Section                         | Description                                                        |
|---------------------------------|--------------------------------------------------------------------|
| [Magic bytes](#magic-bytes)     | Identifies the file as a Praesidium vault                          |
| [Salt](#salt)                   | Random number used for key derivation                              |
| [Nonce](#nonce)                 | Random number used for vault encryption                            |
| [Vault header](#vault-header)   | Vault metadata                                                     |
| [Vault objects](#vault-objects) | Vault secrets                                                      |
| [Auth tag](#auth-tag)           | Cryptographic value to ensure integrity of the first four sections |

### Magic bytes

These are the string "PRAESIDIUM" encoded in ASCII -> (in hex) `50 52 41 45 53 49 44 49 55 4D`

### Salt



### Nonce

### Vault header

| Field name        | Data type | Offset |
|-------------------|-----------|--------|
| Version           | `u64`     | 0      |
| Object count      | `u64`     | 8      |
| Creation date     | `u64`     | 16     |
| Access date       | `u64`     | 24     |
| Modification date | `u64`     | 32     |

### Vault objects



### Auth tag


