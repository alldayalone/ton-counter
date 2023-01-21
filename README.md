# Learning how to write smart contracts on FunC and Tact languages and deploy on TON blockchain

## Prerequisites:
1. Install func and fift. Follow https://blog.ton.org/step-by-step-guide-for-writing-your-first-smart-contract-in-func guide
2. Install node, yarn
3. Created TON wallet in testnet
4. Get API key in https://toncenter.com/
5. Create .env and set variables

## Install
```
yarn install
```

## What's in the repository?

src/env.ts - env variables
src/sendMoney.ts - Send transfers in TON (mnemonic in env used as sender)

src/contracts/* - Smart contract "Counter" in FunC lang
src/build/* - Build output for it
src/deploy.ts - Script to deploy it
src/counterTest.ts - Script to test it (get value, add number to counter). Everything works in testnet blockchain

src/tact/contracts/* - Smart contract Counter in Tact language
src/tact/build/* - Build output for it
src/tact/build/counter_Counter.code.dc - FunC
src/tact/build/counter_Counter.code.ts - Typescript class for deployment, getters and sending messages
src/tact/build/counter_Counter.code.md - Documentation
src/tact/build/counter_Counter.code.boc - BOC
src/tact/deploy.ts - Script to get a ton:// link for deployment (open with testnet tonkeeper) and qrcode (didn't work)
src/tact/counterTest.ts - Script to test. Uses TS class generated by tact
