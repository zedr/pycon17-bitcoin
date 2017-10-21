---
# Setup

 - Python 3 installed:
   - Windows: use the installer
   - Mac: `brew install python3`
 - The python3 executable available in the terminal:
   - Windows: add it to your user's %PATH%
 - Use an editor you're comfortable with

---
# Quick Quiz
## Monetary prizes!

---
# Who invented Bitcoin?

 - Al Gore
 - Satoshi Nakamoto
 - Ryuichi Sakamoto

---
# What is fiat currency?

 - Money you pay Tony to fix it again
 - Money based on the Gold Standard
 - Money created by banks

---
# What Python keyword is used to create generators?

 - gen
 - yield
 - weep

---
# Brief intro

 - Myself

---
# Goals

 1. Have fun
 2. Build our own cryptocurrency
 3. Be amazed

---
# How it will work

 - Divided in Acts
 - Start from scratch
 - In each Act we will build a component
 - 10 minute break between each Act

---
# Caveats

 1. Not an expert in any of these fields:
   - ICOs
   - Crypto
   - Finance
 2. We will take unsafe shortcuts
 3. A subset of Bitcoin, not all of it (e.g. no wallets)
 4. First time I run this workshop! (be kind, be patient)
 5. "Type along" style; diverge at your own risk!

---
# Please

 - Ask questions at any time
 - Use the cheat mode to catch up

---
# Act 1: the peer-to-peer network

---
# Radios

---
# Start coding: main.py

---
# A simple repl

---
# Networking

 - Broadcast addresses

---
# asyncio

 - Protocols
 - The event loop

---
# event loops

---
# Act 2: asymmetric encryption

---
# Number stations

![](https:///www.youtube.com/embed/QnXPqUU6fI0?t=53)

---

 - Sharing a secret
    - with padlocks
    - or with one padlock

---
# Public key cryptography

 - what it is
 - RSA

---
# Implementing a RSA-like cypher

 - start with a prime number
 - generate prime numbers
 - implement extended euclidean algorithm
 - implement multiplicative inverse
 - define P, Q, CONSTANT, MODULUS, PRIVATE_KEY, PUBLIC_KEY
 - implement enc single char
 - implement enc string
 - prime factorisation
    - factoring very large numbers is very hard
    - there is only *one* set of prime factors for any number

---
# Layered view (Satoshi client)

 Validating transactions; Managing blockchain, mempool, peers  (Consensus and Policy code)
                   | 
      Scripting engine / Signatures (Consensus code)
                   | 
             Network layer  (P2P code) 
                   | 
             P2P Messages

https://en.bitcoin.it/wiki/Bitcoin_Core_0.11_(ch_1):_Overview

---
# Layered view (simple)

 - Protocol
 - Network
 - Carrier

---
# Act 3: Transactions

---
# Transaction fees
 - A tx fee paid is the difference between the inputs and the outputs

---
# Wallets

 - We're not using them.

---
# Act 4: The Blockchain

---
# anatomy of a block

 - First transaction must be coinbase (i.e. only 1 input), the rest must not be.

---
# Initial Block Download

Once a new node joins the network, its first order of business is to **download**
and **validate** the entire blockchain.

---
# Act ?: proof of work

 - Why?
 - HashCash

---
# Proof of work

 - Hard to produce
 - Selectable amount of work
 - Easily verifiable

---
# Consensus

The longest valid chain is the canonical one.
