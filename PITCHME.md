---
## Write your own Bitcoin clone in Python
### But first, make your self at home...

 - Python 3 installed:
   - Windows: use the installer
   - Mac: `brew install python3`
 - The `python3` executable available in the terminal:
   - Windows users:
     * add it to your user's %PATH%
   - Try running `python3 -m "this"`
 - Use an editor you're comfortable with (e.g. PyCharm)

<style> .slides:first-child { font-size: 90% !important; } </style>


---
## Your host

 - My name is __*Rigel*__
   * I work as an Architect for Wipro Digital
   * Co-founder of the Dublin Linux User Group
   * Member of the Blockchain Association of Ireland
 - My Github URL is https://github.com/zedr
 - Feel free to connect on Linkedin: https://linkedin.com/in/rigeldiscala

---
# Welcome!

 > "I had to write all the code before I could convince myself that I could
 > solve every problem"

__*The author of Bitcoin.*__

---
## Goals

 1. Have fun
 2. Build our own cryptocurrency
 3. Be amazed

---
## How it will work

 - Divided in __*4 Acts*__
 - We'll start from zero, __nada__, nothing
 - 10 minute break between each Act

---
## If you get stuck

Visit the URL in the footnote:

https://tinyurl.com/pycoin-latest

Download the file and craic on.

---
# Caveats

 0. First time I run this workshop! (__*yikes*__!)
 1. __*Not*__ an expert in any of these fields:
   - ICOs
   - Crypto
   - Finance
 2. We will take unsafe shortcuts
 3. A subset of Bitcoin, not all of it (e.g. no wallets)
 4. "Type along" style; diverge at your own risk!

---
# Quick Quiz
## Win __*monetary*__ prizes!

---
## Who invented Bitcoin?

 1. Al Gore
 2. Satoshi Nakamoto
 3. Ryuichi Sakamoto

---
## What is __*fiat*__ currency?

 1. Money you pay to "fix it again"
 2. Money based on the Gold Standard
 3. Money for nothing

---
## What Python keyword is used to create generators?

 - `gen`
 - `yield`
 - `weep`

---

![](assets/winner.jpg)

---
## What is money?

 - A store of value
   - Can be reliably stored and retrieved
 - A medium of exchange
   - Intermediation, avoid bartering
 - A unit of account
   - Used to measure the value of things
 - A standard of deferred payment
   - Debt is key to our financial system

---
### No, really, what is money?

 - And where does its value come from?
   - Scarcity? (e.g. gold)
   - Labor? What is gained exactly?
   - Debt?

 - What stops up from creating our own money?

---
# Act 1: the peer-to-peer network

---
## Radios

 - Information transmitted and received through space using eletromagnetic energy
 - Anybody with a full-duplex radio system and an antenna can join the conversation
 - A radio tuner is necessary to tune into a specific frequency (3kHz - 300GHz)


![](assets/radiolondra.jpg)

---
## CB - Citizens band radio

In Ireland: Band D (~27MHz)

![](assets/cb2.jpg)


---
## Let's start coding: main.py

---
## A simple repl

 - Read -> Eval -> Print -> Loop

![](assets/repl.png)

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
# Symmetric encryption

---
# One-time pads

---
# Number stations

![](https://www.youtube.com/embed/ryKvsB0uzvo)

---

 - Sharing a secret
    - with padlocks
    - or with one padlock

---
# Symmetric encryption

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
# Encryption and decryption

---
# Signatures

---
# Signing network messages

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

 - We won't cover:
    - multiple inputs
    - transaction fees
    - wallets

 - We will have Coinbase (mining rewards)
 - We need multiple outputs (for Coinbase)

---
# Act 4: The Blockchain

---
# Blocks

    - Link to an ancestor block
        - Except for the Genesis block
    - one or more transactions

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
