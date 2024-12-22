

## README.md (https://github.com/tact-lang/tact/blob/main/tact-docs-main/README.md)
# ARCHIVED! The actual docs are moved to the compiler repo, see: https://github.com/tact-lang/tact/tree/main/docs

<img src="public/banner.jpeg">


## Welcome to Tact Documentation 🌈

Hello there! This is the community-driven repository for Tact Language Documentation.

Latest documentation is always available at: [docs.tact-lang.org](https://docs.tact-lang.org)

Our goal here is to create a welcoming and rich resource that benefits all Tact developers, from beginners to experts.

## Join the Tact Community 🌟

Tact is not just a technology; it's a growing community of developers like you! Whether you are just starting out or have tons of experience, your contributions are valuable.

Here's how you can contribute:

- Organize or clarify information 📝
- Make Pull Requests to improve the code or docs 🚀
- Share tutorials, guides, and articles 📚

Join our community chats to stay updated and collaborate:
* [Tact Telegram Community](https://t.me/tactlang)

## How Can You Contribute?

Contributing is not just encouraged; it's easy!

If you've solved a challenging problem or found a better way to explain a complex topic, share it:

— Got an idea? [Open an Issue](https://github.com/tact-lang/tact-docs/issues/new/choose).  
— Ready to contribute? [Set up your Development Environment](#set-up-your-development-environment).

## Set Up Your Development Environment

Before you submit your amazing contributions, ensure they work seamlessly.

### Quick Cloud Setup 🌩️

Use Gitpod for a hassle-free cloud-based IDE experience:

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/tact-lang/tact-docs)

### Local Setup 🏠

1. Clone this GitHub repository.
2. Make sure to have the latest version of [NodeJS LTS](https://nodejs.org/en/download/) installed.
3. Open your terminal in the project directory.
4. Install dependencies without modifying the `yarn.lock`:

    ```
    yarn deps
    ```

5. Start your local development server:

    ```
    yarn dev
    ```

This will open a new browser window displaying your local version of the documentation. Most updates are automatically reflected.

## License 📄

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)


## cspell.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/cspell.json)
{
  "$schema": "https://raw.githubusercontent.com/streetsidesoftware/cspell/main/cspell.schema.json",
  "version": "0.2",
  "language": "en",
  "words": [
    "basechain",
    "bounceable",
    "cheatsheet",
    "Cheatsheet",
    "cheatsheets",
    "Cheatsheets",
    "comptime",
    "Comptime",
    "Decompilation",
    "decompilation",
    "decompiles",
    "decompiling",
    "dnsresolve",
    "Epva",        // part of a base64 string
    "Fift",
    "ipfs",
    "IPFS",
    "jetton",
    "Jetton",
    "Jettons",
    "jettons",
    "jojo",
    "masterchain",
    "Masterchain",
    "mathrm",
    "nanotons",
    "nextra",
    "omelander",  // some superhero
    "Offchain",
    "quadtree",
    "quadtrees",
    "RAWRESERVE",
    "respecifying",
    "Satoshi",
    "seamus",
    "Seamus",
    "seqno",
    "shardchains",
    "stdlibs",
    "STON.fi",
    "TIMELOCK",
    "timeouted",
    "Timeouted",
    "Toncoin",
    "Toncoins",
    "Uninit",
    "vogons",     // 42 vogons
    "workchain",
    "workchains",
    "xtwitter"
  ],
  "ignoreRegExpList": [
    "\\(#.*\\)",
    "^\\[.+\\]: .+",       // link declarations like [foo]: /ref/stdlib-ownable#bar
    "\\[.+\\]\\[.+\\]",    // links like [`Resumable{:tact}`][res]
    "\\[.+\\]\\(.+\\)",    // links like [`self.toCell().asSlice(){:tact}`](/ref/core-cells#cellasslice)
    "address\\(\".+\"\\)", // Ton addresses
    "mathrm\\{.+\\}",      // LaTeX subset
    "\\[#.+\\]",           // [#nativereserve-combining-modes-with-flags]
    "href=\".+\"",         // href="/cookbook/dexes/stonfi"
    "\".+\": \".+\"",      // "from": "kQBrSAP2y7QIUw4_1q0qciHfqdFmOYR9CC1oinn7kyWWRuoV",
    "Urls"
  ],
  "flagWords": [],
  "ignorePaths": [
    ".github/temp-archive",
    "components/icons",
    "dist",
    "grammars/grammar-ohm.json",
    "grammars/grammar-tact.json",
    "next.config.js",
    "node_modules",
    "out",
    "package.json",
    "pages/cookbook/dexes/_meta.js",
    "pages/ref/spec.mdx"
  ]
}


## package.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/package.json)
{
  "type": "module",
  "dependencies": {
    "@vercel/analytics": "^0.1.8",
    "next": "^13.1.2",
    "nextra": "^2.13.4",
    "nextra-theme-docs": "^2.13.4",
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "scripts": {
    "clean": "rm -fr .next out",
    "deps": "yarn install --frozen-lockfile",
    "dev": "yarn deps && yarn clean && next",
    "build": "yarn deps && yarn clean && next build",
    "post-build": "echo 'spell checking, link checking, formatting'",
    "build-pages": "yarn build && node ./scripts/redirects-generate.js",
    "next": "next",
    "spell": "cspell \"**\""
  },
  "devDependencies": {
    "@svgr/webpack": "^8.1.0",
    "@types/node": "^18.11.19",
    "@types/react": "18.2.61",
    "cspell": "^8.8.4",
    "typescript": "^4.9.5"
  },
  "license": "CC-BY-4.0",
  "packageManager": "yarn@1.22.22"
}


## tsconfig.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/tsconfig.json)
{
  "compilerOptions": {
    "baseUrl": ".",
    "lib": [
      "dom",
      "dom.iterable",
      "esnext"
    ],
    "allowJs": true,
    "skipLibCheck": true,
    "strict": false,
    "forceConsistentCasingInFileNames": true,
    "noEmit": true,
    "incremental": true,
    "esModuleInterop": true,
    "module": "esnext",
    "moduleResolution": "node",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "jsx": "preserve",
    "paths": {
      "@components/*": ["components/*"]
    }
  },
  "include": [
    "next-env.d.ts",
    "**/*.ts",
    "**/*.tsx"
  ],
  "exclude": [
    "node_modules"
  ]
}


## description-of-guides.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/description-of-guides.mdx)
import { Steps } from 'nextra/components'

[Guides](/book/guides/getting-started) are in-depth articles describing how to make a specific project or explore certain ideas of Tact and TON with respect to their implications and applications in real-life contracts.

<Cards>
  <Cards.Card
    arrow
    title="Go to the first guide"
    href="/book/guides/getting-started"
  />
</Cards>


## getting-started.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/guides/getting-started.mdx)
# Welcome to Tact

There are two ways to start with Tact: using a template or starting from scratch.

We recommend using a template, as it contains a **simple contract** that can be deployed to the TON blockchain, along with examples of implementing unit tests and helper functions for contract deployment.

## Getting started from template

To get started, you can use the template project. It contains a simple contract that can be deployed to the TON blockchain, as well as examples of implementing unit tests and helper functions for contract deployment.

> To create a project from the template, simply create a new repository from the template project: https://github.com/tact-lang/tact-template.

## Getting started from scratch

Tact is distributed via `npm` package manager and is meant to be installed to TypeScript/JavaScript projects:

```bash
yarn add @tact-lang/compiler
```

Then you need to create a `tact.config.json` file in the root of your project. It should contain the following:

```json
{
  "projects": [
    {
      "name": "sample",
      "path": "./sources/contract.tact",
      "output": "./sources/output"
    }
  ]
}
```

Add an example contract to `./sources/contract.tact`:

```tact
import "@stdlib/deploy";

message Add {
    amount: Int as uint32;
}

contract SampleTactContract with Deployable {

    owner: Address;
    counter: Int as uint32;

    init(owner: Address) {
        self.owner = owner;
        self.counter = 0;
    }

    fun add(v: Int) {

        // Check sender
        let ctx: Context = context();
        require(ctx.sender == self.owner, "Invalid sender");

        // Update counter
        self.counter = (self.counter + v);
    }

    receive(msg: Add) {
        self.add(msg.amount);
    }

    receive("increment") {
        self.add(1);
    }

    get fun counter(): Int {
        return self.counter;
    }
}
```

Add a build script to `package.json`:

```json
{
  "scripts": {
    "build": "tact --config ./tact.config.json"
  }
}
```

Now you can run `yarn build` and get the compiled contract in `./sources/output` folder.


## deploy.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/guides/getting-started/deploy.mdx)
# Deploy your contract

Template project provides a handy way to deploy contracts, but you can do it yourself as well.

## Deploying with typescript and deploy link

To deploy a smart contract in TON you need to send a message with `init` data attached to it. The easiest way to get an `init` for your contract is using a generated typescript bindings that would help to call an init function.

```typescript
import base64url from 'base64url';
import qs from 'qs';
import { Address, beginCell, storeStateInit, contractAddress, toNano } from '@ton/core';
import { Counter } from './output/sample_Counter';

// Forming an init package
let owner = Address.parse("some-address");
let init = await Counter.init(owner);
let testnet = true;

// Contract address
let address = contractAddress(0, init);

// Amount of TONs to attach to a deploy message
let deployAmount = toNano("0.5");

// Create string representation of an init package
let initStr = base64url(
  beginCell().store(storeStateInit(init)).endCell().toBoc({ idx: false })
);

// Create a deploy link
console.log(
  `ton://transfer/` +
    address.toString({ testOnly: testnet }) +
    "?" +
    qs.stringify({
      text: "Deploy",
      amount: deployAmount.toString(10),
      init: initStr,
    })
);
```

After running this code you will get a link that you can open in your favorite TON wallet. It will open a transfer page with a deploy message already filled in. You can change the amount of TONs to attach to a deploy message and click on the `Send` button. After a few seconds your contract will be deployed and you will see a transaction in your wallet.


## first.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/guides/getting-started/first.mdx)
# Writing your first contract

TON contract is an isolated object that have state and code, can send and receive messages and export get-methods for off-chain reading of a contract state.

The code of the contract dictates how:

- it manipulates it's own state
- it reacts to incoming messages
- exposes it's state to off-chain world

## Contract example

This contract allows to increment counter by anyone in the network, stores the owner of the contract and exposes counter value and owner address to off-chain world.

```tact
contract Counter {

    owner: Address;
    counter: Int as uint32;

    init(owner: Address) {
        self.owner = owner;
        self.counter = 0;
    }

    receive("increment") {
        self.counter = (self.counter + 1);
    }

    get fun counter(): Int {
        return self.counter;
    }

    get fun owner(): Address {
        return self.owner;
    }
}
```

## Contract state and init

This contract has two state variables that persisted between contract calls: `owner` and `counter`. The state variables are declared in the contract header and initialized in the `init` function. The `init` function is called **before** contract is deployed.

`counter` variable is declared as `Int as uint32` which means that it will be stored as `uint32` in the contract state. The `Int` type is used to represent integer numbers in the contract code. `Int` is 257-bit signed integer. Size checks are performed only when storing. Overflowing `Int` causes an exception and aborting the transaction.

## Receiver

Notation `receive("increment")` means declaration of a `receiver` function that will be called when a text with value `"increment"` is sent to the contract. The function body can modify the state of the contract and send messages to other contracts. It is impossible to call `receiver` directly. If you need to reuse some logic you can declare a function and call it from `receiver`.

There are several receiver functions. All receiver functions are processed in the order they are listed below:

- `receive()` - called when an empty message is sent to the contract
- `receive("message")` - called when a text message with a specific comment is sent to the contract
- `receive(str: String)` - called when an arbitrary text message is sent to the contract
- `receive(msg: MyMessage)` - called when binary message of type `MyMessage` is sent to the contract
- `receive(msg: Slice)` - called when binary message of unknown type is sent to the contract
- `bounced(msg: Slice)` - called when outgoing message bounced

## Getters

There are two getters in this contract `counter` and `owner` that returns current counter value and `owner` of a contract. Getters are **not accessible from other contracts** and exported only to off-chain world.


## test.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/guides/getting-started/test.mdx)
import { Callout } from 'nextra-theme-docs'

# Writing Tests with Blueprint

## Overview

Test toolkit (usually, sandbox) already included to the TypeScript SDK named [Blueprint](https://github.com/ton-org/blueprint). You can create demo project and launch default test with two steps:

1. Create a new Blueprint project:
```bash
npm create ton@latest MyProject
```

2. Run a test:
```bash
cd MyProject
npx blueprint test
```

As a result you'll see corresponding output in the terminal window:

```bash
% npx blueprint test

> MyProject@0.0.1 test
> jest

 PASS  tests/Main.spec.ts
  Main
    ✓ should deploy (127 ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        1.224 s, estimated 2 s
Ran all test suites.
```

## Basic Usage
Testing of smart contracts allows for the coverage of security, optimization of gas spending, and examination of edge cases.
Writing tests in Blueprint (that based on [Sandbox](https://github.com/ton-org/sandbox)) works through defining arbitrary actions with the contract and comparing their results with the expected result, for example:

```typescript
it('should execute with success', async () => {                              // description of the test case
    const res = await main.sendMessage(sender.getSender(), toNano('0.05'));  // performing an action with contract main and saving result in res

    expect(res.transactions).toHaveTransaction({                             // configure the expected result with expect() function
        from: main.address,                                                  // set expected sender for transaction we want to test matcher properties from
        success: true                                                        // set the desirable result using matcher property success
    });

    printTransactionFees(res.transactions);                                  // print table with details on spent fees
});
```


### Writing Tests for Complex Assertion

The basic workflow of creating a test is:
1. Create a specific wrapped `Contract` entity using `blockchain.openContract()`.
2. Describe the actions your `Contract` should perform and save the execution result in `res` variable.
3. Verify the properties using the `expect()` function and the matcher `toHaveTransaction()`.

The `toHaveTransaction` matcher expects an object with any combination of fields from the `FlatTransaction` type defined with the following properties

| Name                 | Type          | Description                                                                                                                                                         |
|----------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| from                 | Address?      | Contract address of the message sender                                                                                                                              |
| on                   | Address       | Contract address of the message destination  (Alternative name of the property `to`).                                                                               |
| value                | bigint?       | Amount of Toncoins in the message in nanotons                                                                                                                       |
| body                 | Cell          | Message body defined as a Cell                                                                                                                                              |
| op                   | number?       | Op code is the operation identifier number (crc32 from TL-B usually). Expected in the first 32 bits of a message body.                                              |
|success| boolean?       | Custom Sandbox flag that defines the resulting status of a certain transaction. True - if both the compute and the action phase succeeded. Otherwise - False.       |

You can omit those that you're not interested in, and you can also pass in functions accepting those types returning booleans (`true` meaning good) to check for example number ranges, message opcodes, etc. Note however that if a field is optional (like `from?: Address`), then the function needs to accept the optional type, too.


<Callout type="warning" emoji="⚠️">
Learn the whole list of matcher fields from the [Sandbox documentation](https://github.com/ton-org/sandbox#test-a-transaction-with-matcher).
</Callout>

## _meta.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/_meta.json)
{
  "hello": "Hello World",
  "wallet": "Wallet contract",
  "jetton": "Jetton contract",
  "design": "Contract's designing",
  "cookbook": "Cookbook"
}


## cookbook.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/cookbook.mdx)
import { Callout } from 'nextra-theme-docs'

# Tact Cookbook

Tact Cookbook is to provide a centralized repository of valuable information and experience from experienced Tact developers for future developers.

This article is more focused on every day tasks Tact developer resolve during the development of smart contracts.

<Callout type="warning" emoji="⚠️">
This is a concept article. We're still looking for someone experienced to write it. Read more about contributing on [Tact Cookbook ton-footstep](https://github.com/ton-society/ton-footsteps/issues/143).
</Callout>


## Basics
### How to write exception statements

To declare exceptions in Tact suggested to use special function `require(condition, error message)`

```tact
//  throw "Empty counter" message when condition is equal True

require(ok1 && ok2 && ok3, "Invalid signature");

require(ctx.value >= ton("1"), "Invalid value");
```
<Callout type="warning" emoji="⚠️">
Highly recommended to avoid native Func functions like `nativeThrow()`.
</Callout>


## Receivers
### How to declare a unified Tact receiver for comments
```tact
TODO
//  throw "Empty counter" message when condition is equal True
receive()
```
<Callout type="warning" emoji="⚠️">
**Warning template**
</Callout>

<Callout type="info" emoji="📚️">
**Info template**
</Callout>

## design.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/design.mdx)
# Contract's design

### General approach for designing

#### What is main stages in contract developing?
The developer of a smart contract has a lot of responsibility.  Any vulnerability in the logic could attract a malicious attacker or leak its funds because of bad gas management.

At the beginning of the journey, the developer needs to take care that it is well thought out:
- coins management
- safety of your contract
- gas usage
- storage architecture

In terms of storage it’s good practice to have it fixed size and not to use growing (specially by users) dict’s, since const of operations with dict’s depend’s on the dict size you can easily got out of gas if your dict is too big.

[source](https://t.me/hackatonx/3078/3699)

#### We have an event in Ethereum, do we have such a tool in TON?



## _meta.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/hello/_meta.json)
{
  "hello-1": "Tact and TON terms",
  "hello-2": "Tact project structure",
  "hello-3": "Tact contract structure",
  "hello-4": "Receivers and Getters",
  "hello-5": "Contract deployment",
  "hello-6": "Get data from contract"
}


## hello-1.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/hello/hello-1.mdx)
import { Callout } from 'nextra-theme-docs'

# Tact Hello World

## Tact and TON terms

In this guide, we will walk through the process of creating and deploying a simple smart contract using the Tact program language.
The main goal is trying and touch the smart contract developing process and find out what you should learn next.
You need to spend about one-two hours, depending on your background knowledge.

<Callout>
Did you notice something unclear, incorrect or get stuck with some issue in this guide? Please ask a question in the Telegram [chat](https://t.me/tactlang) or text me directly [@iftryalexg](https://t.me/iftryalexg).
Guide will be updated ASAP and all unclear points will be clarified 🚒💦🔥.
</Callout>

### Tact's facts #1

Five things you need to know in the beginning:

* Smart contract is a computer program that stores and executes in blockchain.
* Blockchain is a shared and structured way to keep data. Data stored in blockchain is impossible to edit and be replaced with fake.
* TON Blockchain works on its own special program software, called the Ton Virtual Machine (TVM). 
* Tact is a computer language for developing smart contracts on the TON blockchain.
* Tact uses JavaScript frameworks, so basic knowledge of them helps you learn it faster. However, if you are just a newcomer it is possible to learn from the scratch.


<Callout type="info" emoji="📚️">
 **Blockchain** is like a digital notebook where important information is written down and shared with many people. Once something is written in the notebook, it can't be changed or erased. It's like a permanent record that everyone can trust. But instead of a notebook, it is stored on multiple servers. And instead of just one person writing in it, many people can write in it at the same time. This way, everyone can see and agree on the information that is written in the blockchain. And because it's placed on a multiple servers, it's safe and can't be lost or changed by accident.
</Callout>


### Tactical practice #1
#### Set up your environment

Get ready to build your own blockchain creation! First, you'll need to gather a few tools to help you along the way.

- **Git** is like a magic toolbox for developers. It helps you keep track of all the different parts of your project, so you can work on them together with your team. You can download it [here](https://git-scm.com/downloads).
- **NodeJS** is a central tool in JavaScript world. We'll be using JavaScript and its special version called TypeScript to create our smart contract. You can download it  [here](https://nodejs.org/en/download/).
- **JavaScript IDE** is like your own personal workshop. It's where you'll be building and designing your code, a text editor for code with highlighting. A popular choice is [VS Code](https://code.visualstudio.com/download), for example. Get it now and let's get building!
- **Tact language** extension for IDE makes it more comfortable to work. For example, in VS Code you can install an [extension](https://marketplace.visualstudio.com/items?itemName=ton-community.tact-vscode).

After the preparation of developer tools is done, download *tact-guide-template* project and open it in your IDE.

```bash
git clone https://github.com/ton-community/tact-guide-template
cd tact-guide-template
```


## hello-2.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/hello/hello-2.mdx)
import { Callout } from 'nextra-theme-docs'

# Tact Hello World

## Tact contract structure

### Tact's facts #2

**tact-guide-template** is basic demo project for developing smart contract on Tact language. Let's learn general things about this:

* By default, this project has a number of additional frameworks used in it, that specified in `yarn`.
* Most important directory for us placed in `tact-guide-template/sources/` directory and contents following:
```
+--tact-guide-template
|   +--sources
|   |  +-- contract.deploy.ts
|   |  +-- contract.spec.ts
|   |  +-- contract.tact

```
*  `contract.tact` - Tact language smart contract will be written here. 
*  `contract.spec.ts` - contents tests for using `yarn tests` for launching local tests. Not necessary part for deployment.
*  `contract.deploy.ts` - contents instructions to generate a deployment link. This link includes all necessary information to deploy our smart contract in blockchain.
<Callout type="info" emoji="📚️">
When a smart contract is delivered in TON Blockchain as bytecode he becomes **deployed**.
</Callout>

As a result we will use three yarn commands to work with Tact project:
```bash
yarn build # To build contract
yarn test # To test contract
yarn deploy # To deploy contract
```

### Tactical practice #2
#### Get template from GitHub

Update dependencies in project via yarn:
```bash
yarn install
```

Now check, that everything is ok, input command:

```bash
yarn build
```
This command will initiate the Tact compiler to build the current `tact.contract`.
Currently, the contract has no content, but the compiler should work.
The result of success executing this should be seen in your terminal window like the following:

![1](public/tact-hello-world/tact-hello-world-1.png)


## hello-3.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/hello/hello-3.mdx)
# Tact Hello World

## Tact contract structure

### Tact's facts #3

#### Contracts and Messages
A lot of important details you should learn to understand how TON works, but here, we simplify our field of knowledge and goals.
So, let's say, **contracts** and **messages** are our main characters in blockchain.

1. **Contract** - is a computer program that lives on the blockchain. It can store information and carry out certain actions based on the instructions that are written inside it.

2. **Message** - is a command that we send to the contract. It tells the contract what to do and can include information like how much funds to transfer or what information to deliver.

On the scheme, you can see a representation of how blockchain works, where different **contracts** communicate with each other by **messages**.

![Tact deploy](public/tact-hello-world/tact-hello-world-5.png)

#### Get functions
Additional general tool, that extends functions of the contract - is **getter** or **get function**. This feature allows to get read-only information from contract's data. Usually, get-function is using to deliver information(for example, smart-contract current balance) to the application, but it is impossible to call it from another contract.
![Tact deploy](public/tact-hello-world/tact-hello-world-7.png)

Read more about contract structure [here](../../first).

#### Smart contract development
In summary, the main goal of smart contract developers is to declare and write the logic of actions in a smart contract correspondingly to messages it gets from other smart contracts. If it is necessary to get information and deliver it off-chain(common web app), there are get functions that should be declared.

Let's talk about the design of our contract.
Our smart contract is like a piggy bank with several common features:
1. _Keep Total value_. We will keep `Total` integer value in blockchain.
2. _Get Total value_. Special tool for reading current `Total` value from blockchain. We can read this directly from blockchain via special `get` method.
3. _Processing "Increment" text comment command_. When contract gets a message, it checks what the message says. If the message says "Increment," it will add `1` to the `Total` inside the piggy bank and update it.
4. _Processing `Add` message command_. If the message says "Add," it will add a specific number to the Total inside the piggy bank and update it.

Additional restriction for our smart contract - It will check if the person sending the message is the owner of the piggy bank or not. This way, only the owner can add or increment the `Total` inside the piggy bank.

### Tactical practice #3
#### Import modules

Come back to `tact-guide-template` project via IDE(VS Code) and begin to write the contract file `contract.tact`. That, our first Tact string is declaring an additional library, where some useful Tact functions are defined.

```tact
import "@stdlib/deploy";
```

`@stdlib/deploy` module extends our tools with `Trait` Deployable, so we can use it Trait later for implementing contract's deployment feature easier.
Note, that Tact language consists of some unusual for classic program language entities, here is what we face in this guide:

| Type     | Description                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Contract | Tact type that declares `contract` entity in it's `{}` block.                                                                                          |
| Message  | Tact type for convenient `message`'s declaration.                                                                                                      |
| Trait    | Struct similar to Contract, but serves as extension for Contract(it's similar to interfaces or inheritance for Classes in classic Object‑oriented PL). |
| Address  | Smart contract address in according TON standards. You'll see this parameter as sender or destination of messages.                                     |

Read more on the [Tact type system](../../guides/types) page.

#### Define Structure
Next step, we need to specify our message `Add`, that will force contract do actions according to 4th feature.
Here we specified, that our message should content Integer number of 32-bit length.

```tact
//previous code
message Add{
  amount: Int as uint32;
}
```

#### Contract body and fields
Now we begin declare our contract, we will call it SampleTactContract. Also, we need specify our contract's own properties, that will be stored in its storage: `owner` and `counter`.

```tact
//previous code

contract SampleTactContract with Deployable {

  owner: Address;
  counter: Int as uint32;

```

As said before `Address` defined in the Tact [Type system](../../../ton-docs/ton-docs/docs/develop/tact/docs/tact-types.md) that describes smart-contract's language. General information about Address in TON placed [here](../../../ton-docs/ton-docs/docs/learn/overviews/addresses.md).
* `owner` - is Address of owner set in for `SampleTactContract`, and we will use it for double check if message sent by owner or not.
* `counter` - integer number stored in contract that keep current value of iteration results.

#### Writing Init function

Before we can use contract in Blockchain we should define its initial process. In our case, it means, that we should declare contract's function, that will define our `owner` and `counter` in particular.
This tool in smart contracts called `init()` function, and we need describe its behaviour next:

```tact
//previous code

init(owner: Address) {
  self.owner = owner;
  self.counter = 0;
}
```

Where `self` - special Tact keyword of current level struct, here we using it for contract's fields we declared. Function `init()` will:
* Accept one argument of type `Address`, set this in contract's field `owner`.
* Initialize `counter` value equal to 0.

```tact
//previous code

contract SampleTactContract with Deployable {

  owner: Address;
  counter: Int as uint32;

  init(owner: Address) {
    self.owner = owner;
    self.counter = 0;
  }

// receivers definition here

// get functions definition here
```


We defined basic structure of our contract. Next step is adding receivers and get functions.



## hello-4.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/hello/hello-4.mdx)
import { Callout } from 'nextra-theme-docs'

# Tact Hello World

## Receivers and Getters

### Tact's facts #4
Here we will learn more about existing tools in Tact for defining contract's behavior in general.
 `init()` - is one of them, and below listed all of them:


| Entity      | Description                                                                                                                                                                                                |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fun`       | Special Tact keyword for declaring function. Functions serve for the convenient abstraction of logic and optimization that helps code be more readable. |
| `init()`    | Function that declares initial values will be stored in contract's data. It will be use in Deployment process, when contract creates in Blockchain. It is mandatory to be defined for the contract.                                                        |
| `context()` | Tact stdlib helper that gets common properties about current incoming messages such as sender's Address, message's body and message value.                                                                           |
| `receive()` | Special function of contract serves to declare behavior of contract with messages.                                                                                                                       |
| `get fun`   | Special keywords of contract serves to declare get functions. According to name, this uses to get information from its data.                                                                               |



### Tactical Practice #4
#### Declare fun

Ok, one more time, we need extend our contract's behaviour

```tact
//previous code

fun add(v: Int) {

    let ctx: Context = context();
    require(ctx.sender == self.owner, "Invalid sender");

    self.counter = (self.counter + v);
}
```

Declare function `add` that will do following things:
1. Get incoming integer argument `v`.
2. Check current incoming message `sender` is equal to `owner` we set for contract in deployment process.
3. If this check passed add to current `counter` value `v` and update `counter` value in contract. If required is not pass, throw exception message "Invalid sender".

#### Declare receivers
```tact
//previous code

receive(msg: Add) {
    self.add(msg.amount);
  }
}

receive("increment") {
    self.add(1);
  }
}
```
Here we are specified two receive functions. This means, that if we get message in contract that correspond of one the receiver contract execute one of them. In other case, contract will do nothing.
`receive()` function expects an incoming argument of String type, Message struct or custom Tact Struct.
Take a look our receivers:
* `receive(msg: Add)` - specifies actions with messages defined in the beginning by Message add. It will content only one integer number of 32-bits length, that we called amount and nothing else. This receiver invokes function `add(amount)`.
* `receive("increment")` - specifies actions with messages, that contents comment string "increment" in its body. Here we invoke function `add(v)` with `v = 1`, so we increment contract's counter by one.


#### Declare getter

Last function we need to specifier is get function counter, that will return value of current counter value from contract.
Now our contract is ready, we need compile this, so run:

```tact

contract SampleTactContract with Deployable {
    //previous code

    get fun counter(): Int {
      return self.counter;
    }

```

<Callout type="info" emoji="📚️">
**Getters** are not accessible from other contracts and exported only to off-chain world.
</Callout>


#### Build contract

Command `yarn build` will compile `contract.tact` and place result in `tact-template/src/output`.

![Tact compile scheme](public/tact-hello-world/tact-compiler-scheme.png)

Run yarn command from terminal:

```bash
yarn build
```

<Callout type="info" emoji="💡">
If you faced some compile issue and can't figure out what is wrong, just compare with target contract placed in `sources/example/increment.tact` or [here](https://github.com/ton-community/tact-guide-template/blob/main/sources/example/increment.tact).
</Callout>

## hello-5.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/hello/hello-5.mdx)
import { Callout } from 'nextra-theme-docs'

# Tact Hello World

## Contract deployment

### Tact's facts #5

Now we on finale stage. We need to deploy our contract to Blockchain. To do this, we will use Ton wallet application.
<Callout type="info" emoji="📚️">
In this way, we avoid a lot of details about the deployment process, but you can find more details about this in followed low-level guides.
</Callout>

* To deploy our new contract we need send message with init information in its to address of our contract. 
* We can know destination address of contract because of definition of Address depends on only from contract's data and code. We know both. 
* To send message in blockchain it is necessary to communicate with TON blockchain nodes. Wallet application will do this with own API, so we will avoid this details in current lesson.
* To send outgoing message in TON, sender should pay fees. In our case, we need some funds on Ton wallet to pay this action.


![Tact deploy](public/tact-hello-world/tact-hello-world-6.png)

<Callout type="warning" emoji="⚠️">
Note, this design of deployment is used just for clarity. Deploying via Wallet App, Working with public API is convenient for learning purposes and does not best practice for projects in the production environment.
</Callout>


### Tactical Practice #5
#### Deploy the contract

Before deployment, according to said before we need to prepare Ton wallet contract with funds. We will use test environment, that maintained with test nodes and called testnet(production calls mainnet).

1. To do this we need install one of ton wallet for testnet:

* Sandbox - separate application for testnet - [Android](https://play.google.com/store/apps/details?id=com.tonhub.wallet.testnet)/[iOS](https://apps.apple.com/app/ton-development-wallet/id1607857373)/[MacOS](https://apps.apple.com/app/ton-development-wallet/id1607857373)
* Tonkeeper(to switch on testnet, open dev menu tap several times in settings on diamond icon) - [Android](https://play.google.com/store/apps/details?id=com.ton_keeper)/[iOS](https://apps.apple.com/us/app/tonkeeper/id1587742107)/[MacOS](https://apps.apple.com/us/app/tonkeeper/id1587742107)

2. Create wallet in application according native wallet apps instructions.

3. Get test Toncoins for your wallet from Telegram [testgiver bot](https://t.me/testgiver_ton_bot).

4. Get address from your wallet and input it in deployment script - `contract.deploy.ts`. 
For me, it was `kQDND6yHEzKB82ZGRn58aY9Tt_69Ie_uz73e2VuuJ3fVVcxf`:

```tact"
//previous code
// Parameters
let owner = Address.parse('kQDND6yHEzKB82ZGRn58aY9Tt_69Ie_uz73e2VuuJ3fVVcxf'); // Replace owner with your address
```

5. Run `contract.deploy.ts` script to get deployment link in terminal with following command in terminal:

```bash
yarn deploy
```
It will ask from you wallet you want use, choose what you used before(Tonkeeper/Sandbox).

6. Read deployment link through reading QR or open URL link via your testnet TON wallet, confirm outgoing message in wallet application.

![deployment-1](public/tact-hello-world/tact-deployment-process-2.png)

<Callout type="info" emoji="💡️">
If you faced some compile issue and can't figure out what is wrong, just compare it with the target contract placed in `sources/example/increment.tact` or [here](https://github.com/ton-community/tact-guide-template/blob/main/sources/example/increment.tact).
</Callout>


## hello-6.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/hello/hello-6.mdx)
# Tact Hello World

## Get data from contract

### Last Tact and next steps

We sent deployment message and deploy our Contract. We can check result with blockchain [testnet explorer](https://testnet.tonapi.io/). 
Take your deployed contract address from terminal window or follow ready-made link and check result of sent message in explorer.
In the case of tutorial, deployed contract address was `kQAd00TX4YPxBfyWjArkionTZJVMoRzFQUM2ntQBcFycWYr4`.
If you saw in blockchain explorer same for your contract...

![deployment-2](public/tact-hello-world/tact-deployment-process-3.png)

Yes! You successfully created and deployed your own smart contract, congrats!

Let's try to find out how it works now?
Another blockchain explorer allows to use get function. Let's check current Total value in our contract:
1. Find your deployed contract again in another blockchain explorer testnet - [ton.cx](https://testnet.ton.cx/). In the tutorial it is: `kQAd00TX4YPxBfyWjArkionTZJVMoRzFQUM2ntQBcFycWYr4`. 
2. Open Get methods tab.
3. Input get method name - `counter` in _Arbitrary method_ field. Run this and check result (it shows in hexadecimal format). 

![deployment-4](public/tact-hello-world/tact-deployment-process-4-b.png)

Now, lets try to send `Add(1)` message, according to our plan we should send common message with "increment" comment to our contract.

All you need open Wallet app(Sandbox/Tonkeeper) you used before, input your deployed contract address in destination address and type "increment" text in comment(message) field and send it. 
Check your `counter` value after this, make sure that counter value changed.

#### What to read next?

* [Wallet.tact contract deployment through public API](../wallet)
* [Jetton.tact contract overview and deployment](../jetton)

#### Useful social
* [Tact Telegram chat](https://t.me/tactlang)
* [Ton Dev News](https://t.me/tondevnews)
* [Ton Dev chat](https://t.me/tondev_eng)


#### Useful TON links
* [Tact main repository](https://github.com/ton-core/tact)
* [Ton official documentation](https://ton.org/docs/)
* [FunC journey](https://blog.ton.org/func-journey)
* [Ton Tutorials](https://ton-community.github.io/tutorials/01-wallet/)

## _meta.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/jetton/_meta.json)
{
  "jetton-1": "Digital token issue",
  "jetton-2": "Jetton standard explanation",
  "jetton-3": "Jetton deployment"
}


## jetton-1.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/jetton/jetton-1.mdx)
import { Callout } from 'nextra-theme-docs'

#  Jetton contract

## Digital token issue

<Callout>
Did you notice something unclear, incorrect or get stuck with some issue in this guide? Please ask a question in the Telegram [chat](https://t.me/tactlang) or text me directly [@iftryalexg](https://t.me/iftryalexg).
Guide will be updated ASAP and all unclear points will be clarified 🚒💦🔥.
</Callout>

### Jetton is a part of TON

Jettons is implementation fungible tokens on the TON Blockchain. Fungible Tokens means that they have a property that makes each Token be exactly the same (in type and value) as another Token. From the side of users - it's digital tool in blockchain, that allow to organize business process of distribution and keeping funds with zero trust functions in transaction.
In TON Blockchain Jettons declared according to [Jetton standard](https://github.com/ton-blockchain/TEPs/blob/master/text/0074-jettons-standard.md). This standard already fully successfully
implemented with FunC language and support in libraries in various languages. Some of them, you can find and research [here](docs/develop/dapps/defi/tokens).

The scope of this article are:
* Remind how Fungible Tokens works in TON blockchain.
* Research how jetton standard could be implemented in the Tact language.

<Callout type="warning" emoji="⚠️">
Note, that jetton.tact is used for learning goals and was not thoroughly tested. It should test necessary before use in production.
</Callout>

### Jetton as example of designing architecture

Implementation of jetton demonstrate how relationships between contracts could be implemented. Idea of scaling in TON allows to think about Jetton standard as a workable process even if userbase will grow in digits.
It becomes possible, because in Jetton standard we have no any parts, that could slow down. But why does this possible and what the price?
- This is possible, because every part of jetton processing become independent element(smart contract) of the whole jetton wallets. No matter how many users will come, it's just increase quantity of smart contracts, shards and will not slow down blockchain.
- Price we have to pay is increasing of complexity of development. Asynchronous messages increase number of cases, we have to handle in smart contracts. Developers of smart contract have to solve this during at very first steps of designing smart-contract.

### Classic issue of fungible token

Suppose we have amount of users with wallets(wallet smart contract) with funds on them in native Blockchain currency. Now, we want somehow to add tokens to user's wallet.

In the [ERC20](https://ethereum.org/ru/developers/docs/standards/tokens/erc-20/) standard we keep balance and processing transaction in special token contract. This contract stores a map of wallet addresses and their token balances.
If we want to deliver to user information about his token balance, we read data from his wallet and token contract.
![jetton-1](public/tact-jetton/tact-jetton-1.png)
Both actions will be delivered to off-chain space, where we will display and use it in our application.
Here, Wallet A, Wallet B - regular wallet contracts.


Then, how to implement token transfer? We can use special transfers between wallet contracts, that will update their balance in Token Master.

![jetton-2](public/tact-jetton/tact-jetton-2.png)

With sharding paradigms in TON blockchain we can without problem support a million of users and millions of transactions. But for Token Master will always live in one shard, and become unscalable now.

![jetton-5](public/tact-jetton/tact-jetton-5.png)

And what we can do, to solve this issue? Redesign our solution to case, where every atomic part(smart contract) of our process is a small blockchain, that will never grow to infinity.

## jetton-2.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/jetton/jetton-2.mdx)
import { Callout } from 'nextra-theme-docs'

# Jetton contract

## Jetton standard explanation

### Reveal the Jetton
In TON digital tokens was named Jettons. Now, we will walk through the Jetton standard and see how problems we met previously were solved.

Because of sharding, where payload on Blockchain will split to different nodes, we need keep our contracts as small blockchains.

<Callout type="info" emoji="📚 ">
Every time you noticed, that your contract keep growing to infinity map in your contract-like-big-monolith - something in designing of service went wrong.
</Callout>

To keep possibility make our smart contracts split shards we want keep all smart contracts as small blockchain.

Let's take a look how regular transfer Jetton works according to standard.
![jetton-6](public/tact-jetton/tact-jetton-6-b.png)

Here scheme of transfer tokens from user of _Wallet App A_ to user _Wallet App B_:
1. _Wallet App A_ requests _Wallet A_ to send Jetton transfer request message.
2. _Wallet A_ sends to _Jetton_A_ wallet message with request of sending jettons.
3. _Jetton A_ sends to _Jetton B_ value of jetton we want to transfer. Decrease his own balance of jettons.
4. _Jetton B_ get incoming message, increase its jetton balance, send notification to wallet contract _Wallet B_.

<Callout type="info" emoji="📚 ">
**Notification** necessary to find out what is balance of Jetton contract, because you have no option to get(use get method) information from contract.
</Callout>

If we will scale our user base, we just get growing of little blockchains. THere will not appear big monolith entity now.
![jetton-7](public/tact-jetton/tact-jetton-7.png)

When quantity of actual contracts become to large, they will split to different shardchains.
Each of these contracts has fixed size state and each contract may live in own shardchain. In this way contracts can live in one shardchain(i.e. Shard 1) and never touch other smart contracts.

![jetton-8](public/tact-jetton/tact-jetton-8.png)



## jetton-3.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/jetton/jetton-3.mdx)
# Jetton contract
## Jetton deployment

### Jetton tact demo project

Take example of project from GitHub:

```bash
git clone https://github.com/ton-community/tact-jetton
cd tact-jetton
```

### Minter
In `jetton.tact` defines minter contract, that will deploy initial contracts of jetton wallets with special "Mint" message.
Minter, usually used before Token become using by users, to distribute to all owners. In current case, we will deliver all Tokens to one owner and instantly deactivate option of mint again.
Look briefly to our contract:


```tact
import "@stdlib/jetton";

message Mint {
    amount: Int;
}

contract SampleJetton with Jetton {

    totalSupply: Int as coins;
    owner: Address;
    content: Cell?;
    mintable: Bool;

    init(owner: Address, content: Cell?) {
        self.totalSupply = 0;
        self.owner = owner;
        self.mintable = true;
        self.content = content;
    }

    receive(msg: Mint) {
        let ctx: Context = context();
        self.mint(ctx.sender, msg.amount, ctx.sender);
    }

    receive("Mint!") {
        let ctx: Context = context();
        self.mint(ctx.sender, 1000000000, ctx.sender);
    }
}
```
This contract receive "Mint" message, and if it happens he invokes `mint()` function,
that declared in `@stdlib/jetton`. Function `mint()` creates a message and sends it to the new jetton-wallet contract address.

![jetton-8](public/tact-jetton/tact-jetton-9.png)
1. _Wallet App A_ send request to _Wallet A_ send mint message to minter. Currently Minter does not exist in blockchain.
2. _Wallet A_ send "Mint" message to Minter's contract address. When it delivered, Minter become deployed and invoke in its mint() function.
3. _Minter_ send to _Jetton A_ address Transfer message with token's supply value. When it delivered, Jetton A contract become deployed.

### Deployment of jetton wallets for new users
Similar process happens when user of _Wallet App A_, want to send tokens to user of _Wallet App B_.
The trick is, our contract Jetton always send information and the whole code to another address. When it comes to destination, code executes and from case was it deployed before or already deployed.
In this case - the [transfer jetton message](https://github.com/ton-core/tact/blob/main/stdlib/libs/jetton/messages.tact#L1) invokes `init()` function and transfers tokens, as a result, deploys the _Jetton B_ smart contract with token balance sent from _Jetton A_.
![jetton-8](public/tact-jetton/tact-jetton-10.png)

From [jetton/wallet.tact](https://github.com/ton-core/tact/blob/main/stdlib/libs/jetton/wallet.tact#L38), we can see, that it will create initial data for new jetton wallet contract:

```tact
//previous code

       let init: StateInit = initOf JettonDefaultWallet(self.master, msg.destination);
        let walletAddress: Address = contractAddress(init);
        send(SendParameters{
            to: walletAddress, 
            value: 0,
            mode: SendRemainingValue, 
            bounce: true,
            body: TokenTransferInternal{
                amount: msg.amount,
                queryId: msg.queryId,
                from: self.owner,
                responseAddress: self.owner,
                forwardTonAmount: msg.forwardTonAmount,
                forwardPayload: msg.forwardPayload
            }.toCell(),
            code: init.code,
            data: init.data
        });
        
```

Here, `initOf` allows to calculate new contract's init data.
It calculates from address of regular `Wallet B`, here `msg.destination` and address of _Minter_ contract `self.master`. Because we always know both, we can be sure which address we will use as our destination.

To display all data clear, application should read each element of process with get methods. It is job, that, for example, have to do blockchain explorers.
![jetton-8](public/tact-jetton/tact-jetton-11.png)

### Deployment of tact.jetton

This project has ready-made example of script for deploying jetton in testnet. Specify following things: 

* Input your deployment Testnet wallet seed in `tact-wallet/sources/jetton.deploy.ts`:
```ts
  // Insert your test wallet's 24 words, make sure you have some test Toncoins on its balance. Every deployment spent 0.5 test toncoin.
  let mnemonics = "multiply voice predict admit hockey fringe flat bike napkin child quote piano";
```

* Input owner address at same `jetton.deploy.ts`:
```ts
  // Owner should usually be the deploying wallet's address.
  let owner = Address.parse('kQDND6yHEzKB82ZGRn58aY9Tt_69Ie_uz73e2V...');
```
* Note, that in deployment script using walletV4. If you want use your V3R2, you need change wallet contract here.

* Run deployment script
```bash
  yarn deploy
```

As a result of successfully deployment, you should deploy two contracts:
* Minter, Token Master - [example](https://testnet.ton.cx/address/EQDupHQXvagCZ3RpkeMZ0dQMI2ACY-jowmCZQ_Y84aSqKw-Z).
* Jetton Wallet of first owner, Wallet A - [example](https://testnet.ton.cx/address/EQA7EdSn6hMMwC7g01w2FwtiZuJE7GZCxss7n3MD26nD6S65).


## What to read next?

This article was inspired by the following materials about jetton standards:
* [how-to-shard-your-ton-smart-contract-and-why-studying-the-anatomy-of-tons-jettons](https://blog.ton.org/how-to-shard-your-ton-smart-contract-and-why-studying-the-anatomy-of-tons-jettons)
* [TON Keeper founders Oleg Andreev and Oleg Illarionov on TON jettons](https://www.youtube.com/watch?v=oEO29KmOpv4)
* [Fungible tokens (Jettons) standard](https://github.com/ton-blockchain/TEPs/blob/master/text/0074-jettons-standard.md)

### Useful social
* [Tact Telegram chat](https://t.me/tactlang)
* [Ton Dev News](https://t.me/tondevnews)
* [Ton Dev chat](https://t.me/tondev_eng)

### Useful TON links
* [Tact main repository](https://github.com/ton-core/tact)
* [Ton official documentation](https://ton.org/docs/)
* [FunC journey](https://blog.ton.org/func-journey)
* [Ton Tutorials](https://ton-community.github.io/tutorials/01-wallet/)

## _meta.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/wallet/_meta.json)
{
  "wallet-1": "What is wallet",
  "wallet-2": "Wallet structure",
  "wallet-3": "Deployment with API"
}


## wallet-1.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/wallet/wallet-1.mdx)
import { Callout } from 'nextra-theme-docs'

# Tact wallet contract
## What is wallet

This article explains how wallet contract works in Tact, how to deploy and test this.

<Callout>
Did you notice something unclear, incorrect or get stuck with some issue in this guide? Please ask a question in the Telegram [chat](https://t.me/tactlang) or text me directly [@iftryalexg](https://t.me/iftryalexg).
Guide will be updated ASAP and all unclear points will be clarified 🚒💦🔥.
</Callout>

### Set up your environment

For this project you should install 


* **Git**. Essential tool for every developer to work with repositories. Download it [here](https://git-scm.com/downloads).
* **NodeJS**. We will use JavaScript with TypeScript mode as the most popular choice for dApp development on TON. Download it [here](https://nodejs.org/en/download/).
* **JavaScript IDE**. Your normal choice for development. [VSCode](https://code.visualstudio.com/download), for example.
* **Wallet app**. You need one of TON noncustodial testnet [wallet app](docs/participate/wallets/apps) (better with support Walletv4), for example [Sandbox](https://apps.apple.com/app/ton-development-wallet/id1607857373)/[Tonkeeper](https://tonkeeper.com/). This is as part of simplify demonstration, you also can get access to your wallet from code, example added in demo. 

- [Tact SDK and libraries full list](docs/develop/tact/introduce/tact-sdk)


### Tact wallet demo project
Get tact-wallet project from git:

```bash
git clone https://github.com/ton-community/tact-wallet
cd tact-wallet
```

This project has ready to use TACT compiler, typescript + jest with [@tact-lang/emulator](https://github.com/tact-lang/tact-emulator), example how to test and deploy.
You have ready-to-use commands configured for contract. Try to input them in terminal and look how it works:

```bash
yarn test # To test contract
yarn build # To build contract
yarn deploy # To deploy contract via deployment link
yarn deploy-api # To deploy through API(need to input deployment wallet in wallet.deploy-api.ts before using)
```

### Briefing for Tact project structure

In the `tact-wallet/sources/` directory placed core project files, that defines what `yarn` commands will do:

1. File `wallet.tact` contract on Tact language, that will be compiled with Tact compiler in `yarn build`
2. File `wallet.spec.ts` contents unit tests for `yarn tests` command. This command allow to launch local tests on your local IDE. Not necessary for deployment.
3. File `wallet.deploy.ts` is a helper, that allow to deploy your `wallet.tact` compiled file(src/output) with deployment link. From the beginning you can deploy your smart contract via [Sandbox](https://apps.apple.com/app/ton-development-wallet/id1607857373)/[Tonkeeper](https://tonkeeper.com/) application.
4. Describes alternative deployment script `wallet.deploy-api.ts` for `yarn deploy-api` according to your `contract.tact` to send deployment message from deployment wallet. You need to input your deployment wallet 24 words [here](sources/wallet.deploy-api.ts#L19).


### What is wallet contract general idea?

Wallet similar to usual smart contract serve as a platform for managing and transferring funds in a decentralized and secure manner. However, it is important to note that while a smart contract may have built-in features for handling funds, additional steps may be necessary to make the user experience more convenient and secure. This may involve handling additional user stories and implementing additional features to meet real-life requirements.

Let's describe small list of feature for wallet contract:
* Deployment of smart contract where placed information of its owner with public key.
* Requests for action with funds by owner.
* Get and handle messages from other smart-contracts, including incoming transfer of funds.


<Callout type="info" emoji="📚️">
Explorers recognize contract's type by hash of the smart contract's code or/and by interfaces founded in smart contract. If you check your common wallet contract with [explorer](https://tonscan.org/)([testnet explorer](https://testnet.tonscan.org/)), you will see that it recognized with type "wallet". From this side, tact-wallet contract is a new version, and it will have different hash(because of original FunC contract and FunC compiled from Tact will be absolutely different). On the same reason current wallet application will not support Tact contract until they add its tact version to their applications.
</Callout>



## wallet-2.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/wallet/wallet-2.mdx)
import { Callout } from 'nextra-theme-docs'

# Tact wallet contract
## Wallet structure

### Contract structure

Tact language allows to define behaviour of contracts with convenient tools as Contract, Trait, Receiver, Message. The usual Tact smart contract has such a structure:

* Includes
* Custom Messages and Structs declaration
* Contract's body
  * Fields
  * Init function
  * Functions
  * Receivers
  * Getters

  
### Wallet contract structure

As we mentioned earlier, contract consists of
1. Includes and struct definition
2. Contract's body

For contract wallet we will define struct Transfer as base struct for messages:

```tact

struct Transfer {
seqno: Int as uint32;
mode: Int as uint8;
to: Address;
amount: Int as coins;
body: Cell?;
}
```

Next will be wallet contract body with all included sections:

```tact

contract Wallet {

    // contract fields
    
    // init function
    
    // receivers functions
    
    // get functions

}

```
#### Wallet fields
Now, let's take a look one by one these section and find out their functions.
First - contract fields. In these section we describe data, that will be store in Blockchain inside contract's storage. Shortly, it calls on-chain.
For features of wallet contract we declare following:

* `seqno` - is field that store last executed transaction id. Used for deduplication of transactions.
* `key` - key of owner. Used for checks if transaction asked from wallet owner.
* `walletId` - wallet id, serves for supporting different(up to uint64) instance of wallets based on one key. For each `walledId` we deploy unique smart contract with access by same `key`.

```tact

contract Wallet {

    seqno: Int as uint32 = 0;
    key: Int as uint256;
    walletId: Int as uint64;

    // init function
    
    // receivers functions
    
    // get functions
}

```

#### Wallet init

The `init()` function define first state of our smart contract for deploying process. To deploy our wallet contract we will keep public key and id in its store. Usually, public keypair - public and secret keys computes locally on device which initiate deployment. Secret key stores locally for future signing transaction of owner, and public key sent as argument in `init()` function.
Wallet ID, according to definition of field allows to create several(up to uin64) wallets based on same keypair.

```tact
contract Wallet {

    // contract fields
    
    init(key: Int, walletId: Int) {
        self.key = key;
        self.walletId = walletId;
    }
    
    // receivers functions

    // get functions
    
}
```

#### Wallet receivers 

Contract receivers define how contract acts depending on what it was received in incoming message. Notice, that when contract sends outgoing message or do computation it pays network fees from its contract balance. Read more about fees in TON here. For wallet contract we describe the following:

* msg: TransferMessage - receiver that handles incoming message and performs outcoming message from our wallet. It will check op_code and seqno to be sure, that transaction valid. If requires successes, we will increment seqno counter and send outgoing message.
* msg: Slice - if msg_body is Slice we check that incoming message was not bounced before, and if this requirements successes increment our seqno counter.
* "notify" - receiver declares actions when incoming message contents string comment "notify". Here it will increment seqno field.
* "duplicate" - receiver declares actions when incoming message contents string comment "duplicate". Here it will increment seqno field.
* bounced() - special receiver for handling bounced messages.

```tact
contract Wallet {

    // contract fields
    
    // init function
    
    receive(msg: TransferMessage) {

        // Check Signature
        let op_hash: Int = msg.transfer.toCell().hash();
        require(checkSignature(op_hash, msg.signature, self.key), "Invalid signature");
        require(msg.transfer.seqno == self.seqno, "Invalid seqno");

        // Increment seqno
        self.seqno += 1;

        // Send message
        send(SendParameters{value: msg.transfer.amount, to: msg.transfer.to, mode: msg.transfer.mode, body: msg.transfer.body});
    }

    receive(msg: Slice) {
            self.seqno += 1;
    }

    receive("notify") {
            self.seqno += 1;
    }

    receive("duplicate") {
        // Create new wallet
        let walletInit: StateInit = initOf Wallet(self.key, self.walletId + 1);
    }
    
    bounced(msg: Slice) {
        // TODO: Handle
    }
    
    // get functions
    
}
    
```

<Callout type="info" emoji="📚️">
Incoming messages, that are not expected in the contract code with a corresponding `receiver()` will be bounced back to the sender.
</Callout>

#### Wallet getters

Get functions allows to get information about contract's data for free. It's helpfully for us, as we want get seqno before every transaction we want made.

* get publicKey() - returns Integer number of public key for smart contract;
* get walletId() - returns walletId that was used to initiate this wallet;
* get seqno() - returns current seqno of wallet

```tact

    // contract fields
    
    // init function
    
    // receivers functions

    get fun publicKey(): Int {
        return self.key;
    }

    get fun walletId(): Int {
        return self.walletId;
    }

    get fun seqno(): Int {
        return self.seqno;
    }
}

```

<Callout type="info" emoji="📚️">
**Getters** are not accessible from other contracts and exported only to off-chain world.
</Callout>

## wallet-3.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/.github/temp-archive/learn/wallet/wallet-3.mdx)
# Tact wallet contract
## Deployment with API


### Wallet deployment

For deployment wallet we have two demo options to run:

```bash
yarn deploy
yarn deploy-api
```

#### Deployment with user wallet application

As simple way offered to deploy smart contract with usual wallet application. The trick is that we just need specify our outgoing message with data we need(we've already done this) and input this data in message.
Wallet applications supports transfer links and QR, so we can use it for our deployment message.
The following scheme shows how deployment process via wallet applications works.

![Tact wallet deploy](public/tact-wallet/tact-deployment-1.png)

Step list here:
1. Install wallet application on device from which we will do deployment.
2. Get test Toncoins on our wallet application with bot.
3. Run deployment script for deployment:
```bash
yarn deploy
```
4. Use deployment link or QR with wallet application and confirm the sending of outgoing message.
5. Notice our new smart contract deployed on the address we sent the message.

#### Deployment with TON public API

The way, some applications in production uses is public API. It is acceptable solution for services that not requires operative updating data and just need sometimes send messages.
Demo script for this process needs to fill with your wallet 24 words of wallet in testnet, you also can use your wallet from previous step.
So, this wallet will call _deployment wallet_ and will be use in similar to wallet application way.

![Tact API deploy](public/tact-wallet/tact-deployment-2.png)

Step list here:
1. Install wallet application on device from which we will do deployment and get toncoins.(Using same wallet from previous step)
2. Input your test wallet 24 words in deployment script `source/wallet.deploy-api.ts`.
3. Run deployment with script:
```bash
yarn deploy-api
```
4. Notice in blockchain explorer our new smart contract deployed according address in console log where we sent the deployment message.

### Wallet tests overview

From the beginning example of unit tests distributed with contract in wallet.spec.contract.
You can launch test via `yarn test` or specify your own with help of jest and `@tact-lang/emulator` library.


### Summary about Tact wallet

Currently TON explorers uses interfaces(getters) and(sometimes) code hash as identifier of contract type, and wallet contract will absolutely different hash for its, so it will not work from the box.
This contract is generic FunC contract, so in production all application already set up for using original FunC contract, but still it is most used contract so it was used for learning and explanation purposes of how it works.
You can learn more about launching and testing your own tact contract from Jetton Tact article.

## What to read next?

### Useful materials
* [Jetton.tact contract overview and deployment](../jetton)
* [TON Hello World part 1: Step by step guide for working with your first TON wallet](https://ton-community.github.io/tutorials/01-wallet/)

### Useful social
* [Tact Telegram chat](https://t.me/tactlang)
* [Ton Dev News](https://t.me/tondevnews)
* [Ton Dev chat](https://t.me/tondev_eng)

### Useful TON links
* [Tact main repository](https://github.com/ton-core/tact)
* [Ton official documentation](https://ton.org/docs/)
* [FunC journey](https://blog.ton.org/func-journey)
* [Ton Tutorials](https://ton-community.github.io/tutorials/01-wallet/)

## grammar-func.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/grammars/grammar-func.json)
{
	"$schema": "https://raw.githubusercontent.com/martinring/tmlanguage/master/tmlanguage.json",
	"name": "FunC",
	"foldingStartMarker": "\\{\\s*$",
	"foldingStopMarker": "^\\s*\\}",
	"patterns": [
		{
			"include": "#keywords"
		},
		{
			"include": "#strings"
		},
		{
			"include": "#directives"
		},
		{
			"include": "#numeric"
		},
		{
			"include": "#comments"
		},
		{
			"include": "#storage"
		},
		{
			"include": "#functions"
		},
		{
			"include": "#variables"
		}
	],
	"repository": {
		"keywords": {
			"patterns": [
				{
					"name": "keyword.control.",
					"match": "\\b(if|ifnot|else|elseif|elseifnot|while|do|until|repeat|return|impure|method_id|forall|asm|inline|inline_ref)\\b"
				},
				{
					"name": "keyword.operator",
					"match": "(?<=\\s)(<=>|>=|<=|!=|==|\\^>>|\\~>>|>>|<<|\\/%|\\^%|\\~%|\\^\\/|\\~\\/|\\+=|-=|\\*=|\\/=|~\\/=|\\^\\/=|%=|\\^%=|<<=|>>=|~>>=|\\^>>=|&=|\\|=|\\^=|\\^|=|~|\\/|%|-|\\*|\\+|>|<|&|\\||:|\\?)(?=\\s)"
				},
				{
					"name": "keyword.other",
					"match": "\\b(false|true)\\b"
				}
			]
		},
		"directives": {
			"name": "storage.modifier.import",
			"begin": "#include|#pragma",
			"end": ";",
			"patterns": [
				{
					"begin": "\"",
					"end": "\"",
					"name": "string.quoted.double"
				},
				{
					"match": "(>=|<=|=|>|<|\\^)?([0-9]+)(.[0-9]+)?(.[0-9]+)?",
					"name": "constant.numeric"
				}
			]
		},
		"strings": {
			"name": "string.quoted.double.",
			"begin": "\"",
			"end": "\"(H|h|c|u|s|a)?"
		},
		"numeric": {
			"name": "constant.numeric",
			"match": "(-?([\\d]+|0x[\\da-fA-F]+))\\b"
		},
		"comments": {
			"patterns": [
				{
					"name": "comment.line",
					"match": ";;(.*)"
				},
				{
					"name": "comment.block",
					"begin": "{-",
					"end": "-}"
				}
			]
		},
		"storage": {
			"patterns": [
				{
					"name": "storage.type",
					"match": "\\b(var|int|slice|tuple|cell|builder|cont|_)(?=[\\s\\),\\[\\]])"
				},
				{
					"name": "storage.modifier",
					"match": "\\b(global|const)\\s"
				}
			]
		},
		"variables": {
			"patterns": [
				{
					"match": "(?!\")(`([^`]+)`|((?=_)_|(?={){|(?=})}|(?![_`{}]))([^;,\\[\\]\\(\\)\\s~.]+))",
					"name": "variable.name"
				}
			]
		},
		"functions": {
			"patterns": [
				{
					"match": "(?!\")(`([^`]+)`|(\\.|~)?((?=_)_|(?={){|(?=})}|(?![_`{}]))([^;,\\[\\]\\(\\)\\s~.]+))(?=[\\(])",
					"name": "entity.name.function"
				}
			]
		}
	},
	"scopeName": "source.func"
}


## grammar-ohm.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/grammars/grammar-ohm.json)
{
  "$schema": "https://raw.githubusercontent.com/martinring/tmlanguage/master/tmlanguage.json",
  "name": "Ohm",
  "scopeName": "source.ohm",
  "fileTypes": [
    "ohm"
  ],
  "patterns": [
    {
      "include": "#comment"
    },
    {
      "include": "#grammar"
    }
  ],
  "repository": {
    "grammar": {
      "patterns": [
        {
          "include": "#baseGrammar"
        },
        {
          "include": "#derivedGrammar"
        }
      ]
    },
    "baseGrammar": {
      "begin": "^\\s*([a-zA-Z_]\\w*)\\s*({)",
      "beginCaptures": {
        "1": {
          "name": "entity.name.class"
        },
        "2": {
          "name": "punctuation.bracket"
        }
      },
      "patterns": [
        {
          "include": "#comment"
        },
        {
          "include": "#ruleName"
        },
        {
          "include": "#ruleBody"
        }
      ],
      "end": "}",
      "endCaptures": {
        "0": {
          "name": "punctuation.bracket"
        }
      }
    },
    "derivedGrammar": {
      "begin": "^\\s*([a-zA-Z_]\\w*)\\s+(<:)\\s+([a-zA-Z_]\\w*)\\s*({)",
      "beginCaptures": {
        "1": {
          "name": "entity.name.class"
        },
        "2": {
          "name": "keyword.operator"
        },
        "3": {
          "name": "entity.other.inherited-class"
        },
        "4": {
          "name": "punctuation.bracket"
        }
      },
      "patterns": [
        {
          "include": "#comment"
        },
        {
          "include": "#ruleName"
        },
        {
          "include": "#ruleBody"
        }
      ],
      "end": "}",
      "endCaptures": {
        "0": {
          "name": "punctuation.bracket"
        }
      }
    },
    "ruleName": {
      "begin": "^\\s*([a-zA-Z_]\\w*)",
      "beginCaptures": {
        "1": {
          "name": "entity.name.function"
        }
      },
      "patterns": [
        {
          "include": "#comment"
        },
        {
          "include": "#formals"
        },
        {
          "include": "#ruleDescr"
        }
      ],
      "end": "([:+]?=)",
      "endCaptures": {
        "1": {
          "name": "keyword.operator"
        }
      }
    },
    "formals": {
      "begin": "(<)",
      "beginCaptures": {
        "1": {
          "name": "punctuation.bracket"
        }
      },
      "patterns": [
        {
          "name": "variable.parameter",
          "match": "[a-zA-Z_]\\w*"
        },
        {
          "name": "punctuation.delimiter",
          "match": ","
        }
      ],
      "end": "(>)",
      "endCaptures": {
        "1": {
          "name": "punctuation.bracket"
        }
      }
    },
    "ruleDescr": {
      "name": "comment.block.documentation",
      "begin": "(\\()",
      "beginCaptures": {
        "1": {
          "name": "punctuation.bracket"
        }
      },
      "end": "(\\))",
      "endCaptures": {
        "1": {
          "name": "punctuation.bracket"
        }
      }
    },
    "ruleBody": {
      "patterns": [
        {
          "include": "#comment"
        },
        {
          "include": "#builtInRulesLexical"
        },
        {
          "include": "#builtInRulesSyntactic"
        },
        {
          "include": "#terminal"
        },
        {
          "include": "#operator"
        },
        {
          "include": "#punctuation"
        },
        {
          "include": "#caseName"
        }
      ]
    },
    "builtInRulesLexical": {
      "name": "support.function",
      "match": "\\b(?:any|alnum|end|digit|hexDigit|letter|space|lower|upper|caseInsensitive|listOf|nonemptyListOf|emptyListOf|applySyntactic)\\b"
    },
    "builtInRulesSyntactic": {
      "name": "support.function",
      "match": "\\b(?:ListOf|NonemptyListOf|EmptyListOf)\\b"
    },
    "terminal": {
      "name": "string.quoted.double",
      "begin": "\"",
      "beginCaptures": {
        "0": {
          "name": "punctuation.definition.string.begin"
        }
      },
      "patterns": [
        {
          "name": "constant.character.escape",
          "match": "\\\\(?:x\\h{2}|u\\h{4}|u\\{\\h{1,6}\\}|t|r|n|b|'|\"|\\\\)"
        }
      ],
      "end": "(?:(?<!\\\\)|(?<=\\\\\\\\))\"",
      "endCaptures": {
        "0": {
          "name": "punctuation.definition.string.end"
        }
      }
    },
    "operator": {
      "name": "keyword.operator",
      "match": "<:|=|:=|\\+=|\\*|\\+|\\?|~|&|#|\\.\\.|\\.\\.\\.|\\|"
    },
    "punctuation": {
      "patterns": [
        {
          "name": "punctuation.delimiter",
          "match": "<|>|,"
        },
        {
          "name": "punctuation.bracket",
          "match": "(|)"
        }
      ]
    },
    "caseName": {
      "match": "(--)\\s*([a-zA-Z_]\\w*)",
      "captures": {
        "1": {
          "name": "punctuation.delimiter"
        },
        "2": {
          "name": "entity.name.tag"
        }
      }
    },
    "comment": {
      "patterns": [
        {
          "include": "#lineComment"
        },
        {
          "include": "#blockComment"
        }
      ]
    },
    "lineComment": {
      "name": "comment.line",
      "begin": "//",
      "beginCaptures": {
        "0": {
          "name": "comment.line.double-slash"
        }
      },
      "patterns": [
        {
          "include": "#todoComment"
        }
      ],
      "end": "$"
    },
    "blockComment": {
      "name": "comment.block",
      "begin": "\\s*/\\*",
      "beginCaptures": {
        "0": {
          "name": "comment.block.begin"
        }
      },
      "patterns": [
        {
          "include": "#todoComment"
        }
      ],
      "end": "\\*/",
      "endCaptures": {
        "0": {
          "name": "comment.block.end"
        }
      }
    },
    "todoComment": {
      "name": "keyword.comment.todo",
      "match": "(?i)\\b(FIXME|TODO|CHANGED|XXX|IDEA|HACK|NOTE|REVIEW|NB|BUG)\\b"
    }
  }
}


## grammar-tact.json (https://github.com/tact-lang/tact/blob/main/tact-docs-main/grammars/grammar-tact.json)
{
  "name": "Tact",
  "displayName": "Tact",
  "scopeName": "source.tact",
  "fileTypes": [
    "tact"
  ],
  "foldingStartMarker": "\\{\\s*$",
  "foldingStopMarker": "^\\s*\\}",
  "patterns": [
    {
      "include": "#comment"
    },
    {
      "include": "#annotation"
    },
    {
      "include": "#literal"
    },
    {
      "include": "#invalid"
    },
    {
      "include": "#constant"
    },
    {
      "include": "#type"
    },
    {
      "include": "#expression"
    },
    {
      "include": "#punctuation"
    },
    {
      "include": "#keyword"
    },
    {
      "include": "#function"
    },
    {
      "include": "#variable"
    }
  ],
  "repository": {
    "comment": {
      "patterns": [
        {
          "name": "comment.line.double-slash.tact",
          "begin": "//",
          "beginCaptures": {
            "0": {
              "name": "punctuation.definition.comment.line.double-slash.tact"
            }
          },
          "patterns": [
            {
              "include": "#todo"
            }
          ],
          "end": "$"
        },
        {
          "name": "comment.block.tact",
          "begin": "\\s*/\\*",
          "beginCaptures": {
            "0": {
              "name": "comment.block.begin.tact punctuation.definition.comment.begin.tact"
            }
          },
          "patterns": [
            {
              "include": "#todo"
            }
          ],
          "end": "\\*/",
          "endCaptures": {
            "0": {
              "name": "comment.block.end.tact punctuation.definition.comment.end.tact"
            }
          }
        }
      ]
    },

    "todo": {
      "match": "(?i)\\b(FIXME|TODO|CHANGED|XXX|IDEA|HACK|NOTE|REVIEW|NB|BUG)\\b(?-i)",
      "name": "keyword.comment.todo.tact"
    },

    "annotation": {
      "patterns": [
        {
          "comment": "@name() in native functions",
          "begin": "^\\s*(@name)\\s*(\\()",
          "beginCaptures": {
            "1": {
              "name": "entity.other.attribute-name.tact"
            },
            "2": {
              "name": "punctuation.brackets.round.tact"
            }
          },
          "patterns": [
            {
              "comment": "FunC identifier",
              "match": "(.*?)",
              "name": "entity.name.function.func.tact"
            }
          ],
          "end": "\\)",
          "endCaptures": {
            "0": {
              "name": "punctuation.brackets.round.tact"
            }
          }
        },
        {
          "comment": "One or more @inteface() before traits and contracts",
          "begin": "(?<!\\.)(@interface)\\s*(\\()",
          "beginCaptures": {
            "1": {
              "name": "entity.other.attribute-name.tact"
            },
            "2": {
              "name": "punctuation.brackets.round.tact"
            }
          },
          "patterns": [
            {
              "include": "#string"
            }
          ],
          "end": "\\)",
          "endCaptures": {
            "0": {
              "name": "punctuation.brackets.round.tact"
            }
          }
        },
        {
          "comment": "Asm arrangements",
          "begin": "(?<!\\.)(asm)\\s*(\\()",
          "beginCaptures": {
            "1": {
              "name": "entity.other.attribute-name.tact"
            },
            "2": {
              "name": "punctuation.brackets.round.tact"
            }
          },
          "patterns": [
            {
              "include": "#variable"
            },
            {
              "match": "->",
              "name": "keyword.operator.mapsto.tact"
            },
            {
              "match": "\\b([0-9]*)\\b",
              "name": "constant.numeric.decimal.tact"
            }
          ],
          "end": "\\)",
          "endCaptures": {
            "0": {
              "name": "punctuation.brackets.round.tact"
            }
          }
        },
        {
          "comment": "Fallback match",
          "match": "(?<!\\.)\\b(@name|@interface|asm)\\b",
          "name": "entity.other.attribute-name.tact"
        }
      ]
    },

    "literal": {
      "patterns": [
        {
          "comment": "Hexadecimal integer",
          "match": "\\b(0[xX][a-fA-F0-9](?:_?[a-fA-F0-9])*)\\b",
          "name": "constant.numeric.hex.tact"
        },
        {
          "comment": "Octal integer",
          "match": "\\b(0[oO][0-7](?:_?[0-7])*)\\b",
          "name": "constant.numeric.oct.tact"
        },
        {
          "comment": "Binary integer",
          "match": "\\b(0[bB][01](?:_?[01])*)\\b",
          "name": "constant.numeric.bin.tact"
        },
        {
          "comment": "Decimal integer WITH leading zero",
          "match": "\\b(0[0-9]*)\\b",
          "name": "constant.numeric.decimal.tact"
        },
        {
          "comment": "Decimal integer WITHOUT leading zero",
          "match": "\\b([1-9](?:_?[0-9])*)\\b",
          "name": "constant.numeric.decimal.tact"
        },
        {
          "comment": "Boolean literal",
          "match": "(?<!\\.)\\b(true|false)\\b",
          "name": "constant.language.bool.tact"
        },
        {
          "include": "#string"
        },
        {
          "comment": "self",
          "match": "(?<!\\.)\\b(self)\\b",
          "name": "variable.language.this.tact"
        }
      ]
    },

    "string": {
      "comment": "String literal",
      "begin": "\"",
      "beginCaptures": {
        "0": {
          "name": "punctuation.definition.string.begin.tact"
        }
      },
      "name": "string.quoted.double.tact",
      "patterns": [
        {
          "include": "#escape-sequence"
        }
      ],
      "end": "\"",
      "endCaptures": {
        "0": {
          "name": "punctuation.definition.string.end.tact"
        }
      }
    },

    "escape-sequence": {
      "comment": "Allowed escape sequences in strings",
      "match": "(?:\\\\)(?:(\\\\)|(\")|([nrtvbf])|(x[a-fA-F0-9]{2})|(u[a-fA-F0-9]{4})|(u\\{[a-fA-F0-9]{1,6}\\}))",
        "name": "constant.character.escape.tact",
        "captures": {
          "1": {
            "name": "constant.character.escape.backslash.tact"
          },
          "2": {
            "name": "constant.character.escape.double-quote.tact"
          },
          "3": {
            "name": "constant.character.escape.special.tact"
          },
          "4": {
            "name": "constant.character.escape.hex.tact"
          },
          "5": {
            "name": "constant.character.escape.unicode.tact"
          },
          "6": {
            "name": "constant.character.escape.unicodepoint.tact"
          }
        }
      },

      "invalid": {
        "patterns": [
          {
            "comment": "Anything starting with __gen or __tact",
            "match": "\\b__(?:gen|tact)[a-zA-Z0-9_]*\\b",
            "name": "invalid.illegal.identifier.tact"
          }
        ]
      },

      "constant": {
        "patterns": [
          {
            "comment": "self.storageReserve",
            "match": "(?<=self\\.)(storageReserve)\\b",
            "name": "constant.other.builtin.tact"
          },
          {
            "comment": "Other constants from the core library",
            "match": "(?<!\\.)\\b(SendRemainingValue|SendRemainingBalance|SendPayGasSeparately|SendIgnoreErrors|SendBounceIfActionFail|SendDestroyIfZero|SendOnlyEstimateFee|ReserveExact|ReserveAllExcept|ReserveAtMost|ReserveAddOriginalBalance|ReserveInvertSign|ReserveBounceIfActionFail)\\b",
            "name": "constant.other.builtin.tact"
          },
          {
            "comment": "ALL CAPS constants",
            "match": "\\b([A-Z]{2}[A-Z0-9_]*)\\b",
            "name": "constant.other.caps.tact"
          },
          {
            "comment": "Constant declaration or definition",
            "match": "(?<!\\.)\\b(const)\\s+([a-zA-Z_][A-Za-z0-9_]*)\\b",
            "captures": {
              "1": {
                "name": "keyword.other.tact"
              },
              "2": {
                "name": "constant.other.declaration.tact"
              }
            }
          },
          {
            "comment": "null",
            "match": "(?<!\\.)\\b(null)\\b",
            "name": "constant.language.null.tact"
          }
        ]
      },

      "type": {
        "patterns": [
          {
            "include": "#simple-type"
          },
          {
            "comment": "bounced<T>",
            "begin": "(?<!\\.)\\b(bounced)\\s*(<)",
            "beginCaptures": {
              "1": {
                "name": "entity.name.type.tact"
              },
              "2": {
                "name": "punctuation.brackets.angle.tact"
              }
            },
            "patterns": [
              {
                "include": "#simple-type"
              }
            ],
            "end": ">",
            "endCaptures": {
              "0": {
                "name": "punctuation.brackets.angle.tact"
              }
            }
          },
          {
            "comment": "map<K, V>",
            "begin": "(?<!\\.)\\b(map)\\s*(<)",
            "beginCaptures": {
              "1": {
                "name": "entity.name.type.tact"
              },
              "2": {
                "name": "punctuation.brackets.angle.tact"
              }
            },
            "patterns": [
              {
                "include": "#simple-type"
              },
              {
                "match": ",",
                "name": "punctuation.comma.tact"
              },
              {
                "include": "#as-tlb"
              }
            ],
            "end": ">",
            "endCaptures": {
              "0": {
                "name": "punctuation.brackets.angle.tact"
              }
            }
          },
          {
            "include": "#as-tlb"
          }
        ]
      },

      "simple-type": {
        "comment": "Simple types",
        "match": "(?<!\\.)\\b([A-Z][a-zA-Z0-9_]*)(\\??)",
        "captures": {
          "1": {
            "name": "entity.name.type.tact"
          },
          "2": {
            "name": "keyword.operator.optional.tact"
          }
        }
      },

      "as-tlb": {
        "comment": "Serialization",
        "patterns": [
          {
            "match": "(?<!\\.)\\b(as)\\s+(coins|remaining|bytes32|bytes64|int257|u?int(?:2[0-5][0-6]|1[0-9][0-9]|[1-9][0-9]?))\\b",
            "captures": {
              "1": {
                "name": "keyword.other.as.tact storage.modifier.tact"
              },
              "2": {
                "name": "entity.name.type.tact"
              }
            }
          }
        ]
      },

      "expression": {
        "patterns": [
          {
            "comment": "Logical operators",
            "match": "(\\|\\||&&|!!?)(?!=)",
            "name": "keyword.operator.logical.tact"
          },
          {
            "comment": "Bitwise operators",
            "match": "(\\^|&|\\||~|<<|>>)(?!=)",
            "name": "keyword.operator.bitwise.tact"
          },
          {
            "comment": "Augmented assignment operators",
            "match": "(\\+=|-=|\\*=|/=|%=|\\^=|&=|\\|=|<<=|>>=)",
            "name": "keyword.operator.assignment.tact"
          },
          {
            "comment": "Assignment operator",
            "match": "(?<![<>])=(?!=)",
            "name": "keyword.operator.assignment.equal.tact"
          },
          {
            "comment": "Comparison operators",
            "match": "([!=]=|<=?|>=?)",
            "name": "keyword.operator.comparison.tact"
          },
          {
            "comment": "Arithmetic operators",
            "match": "([+%*\\-])|(/(?!/))",
            "name": "keyword.operator.arithmetic.tact"
          },
          {
            "comment": "initOf expression",
            "match": "\\b(initOf)\\b",
            "name": "keyword.operator.new.tact"
          },
          {
            "comment": "Ternary expression",
            "begin": "(?!\\?\\.\\s*[^[:digit:]])(\\?)(?!\\?)",
            "beginCaptures": {
              "1": {
                "name": "keyword.operator.ternary.tact"
              }
            },
            "patterns": [
              {
                "include": "$self"
              }
            ],
            "end": "\\s*(:)",
            "endCaptures": {
              "1": {
                "name": "keyword.operator.ternary.tact"
              }
            }
          }
        ]
      },

      "punctuation": {
        "patterns": [
          {
            "match": ",",
            "name": "punctuation.comma.tact"
          },
          {
            "match": "[{}]",
            "name": "punctuation.brackets.curly.tact"
          },
          {
            "match": "[()]",
            "name": "punctuation.brackets.round.tact"
          },
          {
            "match": ";",
            "name": "punctuation.semi.tact"
          },
          {
            "match": ":",
            "name": "punctuation.colon.tact"
          },
          {
            "match": "\\.",
            "name": "punctuation.dot.tact"
          }
        ]
      },

      "keyword": {
        "patterns": [
          {
            "match": "(?<!\\.)\\b(import)\\b",
            "name": "keyword.control.import.tact"
          },
          {
            "comment": "Control flow keywords, prefixed by more than one dot",
            "match": "(?<=\\.\\.)\\b(else|catch|until|in(?!\\s*\\())\\b",
            "name": "keyword.control.tact"
          },
          {
            "comment": "Control flow keywords",
            "match": "(?<!\\.)\\b(if|else|try|catch|repeat|do|until|while|foreach|in(?!\\s*\\()|return)\\b",
            "name": "keyword.control.tact"
          },
          {
            "comment": "let and const",
            "match": "(?<!\\.)\\b(let|const)\\b",
            "name": "keyword.other.tact"
          },
          {
            "comment": "Serialization",
            "match": "(?<!\\.)\\b(as)\\b",
            "name": "keyword.other.as.tact storage.modifier.tact"
          },
          {
            "match": "(?<!\\.)\\b(struct)\\b",
            "name": "keyword.other.struct.tact"
          },
          {
            "match": "(?<!\\.)\\b(message)\\b",
            "name": "keyword.other.message.tact"
          },
          {
            "match": "(?<!\\.)\\b(trait)\\b",
            "name": "keyword.other.trait.tact"
          },
          {
            "match": "(?<!\\.)\\b(contract)\\b",
            "name": "keyword.other.contract.tact"
          },
          {
            "comment": "Constant and function attributes",
            "match": "(?<!\\.)\\b(abstract|virtual|override)\\b",
            "name": "keyword.other.attribute.tact storage.modifier.tact"
          },
          {
            "comment": "Function attributes",
            "match": "(?<!\\.)\\b(extends|get|inline|mutates)\\b",
            "name": "keyword.other.attribute.tact"
          },
          {
            "comment": "Function declaration/definition keywords",
            "match": "(?<!\\.)\\b(fun|native)\\b",
            "name": "keyword.other.function.tact"
          },
          {
            "comment": "Special functions",
            "match": "(?<!\\.)\\b(init|receive|bounced|external)(?=\\s*\\()",
            "name": "keyword.other.function.tact"
          },
          {
            "comment": "Reserved keywords",
            "match": "(?<!\\.)\\b(extend|public)\\b",
            "name": "keyword.other.reserved.tact"
          },
          {
            "comment": "Other keywords",
            "match": "(?<!\\.)\\b(primitive|with)\\b",
            "name": "keyword.other.tact"
          }
        ]
      },

      "function": {
        "comment": "Function declaration, definition or call",
        "match": "\\b((?:[a-zA-Z_][a-zA-Z0-9_]*))\\s*(\\()",
        "captures": {
          "1": {
            "name": "entity.name.function.tact"
          },
          "2": {
            "name": "punctuation.brackets.round.tact"
          }
        }
      },

      "variable": {
        "patterns": [
          {
            "comment": "Any valid Tact identifier",
            "match": "(?<!\\.)\\b(_)\\b",
            "name": "comment.unused-identifier.tact"
          },
          {
            "comment": "Any valid Tact identifier",
            "match": "\\b([a-zA-Z_][a-zA-Z0-9_]*)\\b",
            "name": "variable.other.tact"
          }
        ]
      }
    }
  }


## _app.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/_app.mdx)
{/*  import '../styles.css' */}

import React from "react"

export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />
}


## index.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/index.mdx)
# Learn all about programming in ⚡ Tact

import { Cards, Steps, Tabs } from 'nextra/components'

![Tact banner](public/banner.jpeg)

Tact is a new programming language for TON Blockchain that is focused on efficiency and simplicity. It is designed to be easy to learn and use, and to be a good fit for smart contracts. Tact is a statically typed language with a simple syntax and a powerful type system.

## Let's start! [#start]

<Steps>

### Ensure that the supported version of Node.js is installed and available [#start-1]

To check it, run `node --version{:shell}` — it should show you the version 22.0.0 or later.

### Run the following command [#start-2]

It will create a new project with the simple counter contract:

<Tabs items={['npm', 'yarn', 'pnpm', 'bun']} defaultIndex="1">
  <Tabs.Tab>
    ```shell
    npm create ton@latest -- simple-counter --type tact-counter --contractName SimpleCounter
    ```
  </Tabs.Tab>
  <Tabs.Tab>
    ```shell
    # recommended
    yarn create ton simple-counter --type tact-counter --contractName SimpleCounter
    ```
  </Tabs.Tab>
  <Tabs.Tab>
    ```shell
    pnpm create ton@latest simple-counter --type tact-counter --contractName SimpleCounter
    ```
  </Tabs.Tab>
  <Tabs.Tab>
    ```shell
    bun create ton@latest simple-counter --type tact-counter --contractName SimpleCounter
    ```
  </Tabs.Tab>
</Tabs>

### That's it! [#start-3]

Your first contract project is written and compiled already! Go check it out by moving into the relevant directory — `cd simple-counter/contracts{:shell}`.

Here's how it would look like:

```tact
import "@stdlib/deploy";

message Add {
    queryId: Int as uint64;
    amount: Int as uint32;
}

contract SimpleCounter with Deployable {
    id: Int as uint32;
    counter: Int as uint32;

    init(id: Int) {
        self.id = id;
        self.counter = 0;
    }

    receive(msg: Add) {
        self.counter += msg.amount;

        // Notify the caller that the receiver was executed and forward remaining value back
        self.notify("Cashback".asComment());
    }

    get fun counter(): Int {
        return self.counter;
    }

    get fun id(): Int {
        return self.id;
    }
}
```

To re-compile or deploy, refer to the commands in the scripts section of `package.json` in the root of this newly created project and to the documentation of [Blueprint](https://github.com/ton-org/blueprint) — this is the tool we've used to create and compile your first simple counter contract in Tact. In fact, Blueprint can do much more than that: including tests, customizations and more.

</Steps>

## Where to go next? [#next]

<Steps>

### Have some blockchain knowledge already? [#next-1]

See the [Tact Cookbook](/cookbook), which is a handy collection of everyday tasks (and solutions) every Tact developer faces during smart contract development. Use it to avoid re-inventing the wheel.

Alternatively, check the following cheatsheets to quickly get started:

<Cards>
  <Cards.Card
    icon="💎 "
    title="Coming from FunC (TON)"
    href="/book/cs/from-func"
  />
  <Cards.Card
    icon="🔷 "
    title="Coming from Solidity (Ethereum)"
    href="/book/cs/from-solidity"
  />
</Cards>

### Want to know more? [#next-2]

For further guidance on compilation, testing and deployment see the respective pages:

* [Testing and debugging](/book/debug) page tells you everything about debugging Tact contracts
* [Deployment](/book/deploy) page shows what deployment looks like and helps you harness the powers of [Blueprint](https://github.com/ton-org/blueprint) for it.

For custom plugins for your favorite editor and other tooling see the [Tools](/ecosystem/tools/overview) page.

Alternatively, take a look at the following broader sections:
* [Book](/book) helps you learn the language step-by-step
* [Cookbook](/cookbook) gives you ready-made recipes of Tact code
* [Reference](/ref) provides a complete glossary of the standard library, grammar and evolution process
* Finally, [Ecosystem](/ecosystem) describes "what's out there" in the Tacts' and TONs' ecosystems

<Cards>
  <Cards.Card
    icon="📚 "
    title="Read the Book of Tact"
    href="/book"
  />
  <Cards.Card
    icon="🍲 "
    title="Grind the Cookbook"
    href="/cookbook"
  />
  <Cards.Card
    icon="🔬 "
    title="Skim the Reference"
    href="/ref"
  />
  <Cards.Card
    icon="🗺️ "
    title="Embrace the Ecosystem"
    href="/ecosystem"
  />
</Cards>

### Feeling a bit uncomfortable? [#next-3]

If you ever get stuck, try searching — the search box is right at the top of the documentation. There is also a handy <kbd>Ctrl</kbd> + <kbd>K</kbd> shortcut to quickly focus and start the search as you type.

If you can't find the answer in the docs, or you've tried to do some local testing and it still didn't help — don't hesitate to reach out to Tact's flourishing community:

<Cards>
  <Cards.Card
    arrow
    icon="✈️ "
    title="Telegram Group"
    href="https://t.me/tactlang"
  />
  <Cards.Card
    arrow
    icon="🐦 "
    title="X/Twitter"
    href="https://twitter.com/tact_language"
  />
</Cards>

Good luck on your coding adventure with ⚡ Tact!

</Steps>


## bounced.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/bounced.mdx)
import { Callout } from 'nextra-theme-docs'

# Bounced messages

When a contract sends a message with a flag `bounce` set to `true{:tact}`, then if the message wasn't processed properly, it would bounce back to the sender. This is useful when you want to make sure that the message was processed properly and if not — revert the changes.

## Caveats

Currently, bounced messages in TON have only 224 usable data bits in the message body and don't have any references. This means that you can't recover much of the data from the bounced message. This is a limitation of the TON blockchain and will be fixed in the future. Tact helps you to check if your message fits the limit and in case it doesn't — suggests using a special type constructor `bounced<T>{:tact}` for the bounced message receiver, that would construct a partial representation of the message that fits into the required limits.

## Bounced message receiver

<Callout type="warning" emoji="⚠️">

  Bounced text messages are not supported yet.

</Callout>

To receive a bounced message, define a `bounced(){:tact}` [receiver function](/book/contracts#receiver-functions) in your [contract](/book/contracts) or a [trait](/book/types#traits):

```tact {2-4}
contract MyContract {
    bounced(msg: bounced<MyMessage>) {
        // ...
    }
}
```

To process bounced messages manually, you can use a fallback definition that handles a raw [`Slice{:tact}`](/book/cells#slices) directly. Note, that such receiver will get **all** the bounced messages produced by your contract:

```tact /rawMsg: Slice/
contract MyContract {
    bounced(rawMsg: Slice) {
        // ...
    }
}
```


## cells.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/cells.mdx)
# Cells, Builders and Slices

import { Callout } from 'nextra/components'

[Cells](#cells), [Builders](#builders) and [Slices](#slices) are low-level [primitives][p] of TON Blockchain. The virtual machine of TON Blockchain, [TVM][tvm], uses cells to represent all data structures in persistent storage, and most in memory.

## Cells

`Cell{:tact}` is a [primitive][p] and a data structure, which [ordinarly](#cells-kinds) consists of up to $1023$ continuously laid out bits and up to $4$ references (refs) to other cells. Circular references are forbidden and cannot be created by the means of [TVM][tvm], which means cells can be viewed as [quadtrees][quadtree] or [directed acyclic graphs (DAGs)](https://en.wikipedia.org/wiki/Directed_acyclic_graph) of themselves. Contract code itself is represented by a tree of cells.

Cells and [cell primitives](#cells-immutability) are bit-oriented, not byte-oriented: [TVM][tvm] regards data kept in cells as sequences (strings or streams) of up to $1023$ bits, not bytes. If necessary, contracts are free to use, say, $21$-bit integer fields serialized into [TVM][tvm] cells, thus using fewer persistent storage bytes to represent the same data.

### Kinds [#cells-kinds]

While the [TVM][tvm] type [`Cell{:tact}`](#cells) refers to all cells, there are different cell kinds with various memory layouts. The one described [earlier](#cells) is commonly referred to as an _ordinary_ (or simple) cell — that's the most simple and most commonly used flavor of cells, which can only contain data. The grand majority of descriptions, guides and [references](/ref/core-cells) to cells and their usage assumes ordinary ones.

Other kinds of cells are collectively called _exotic_ (or special) cells. They sometimes appear in actual representations of blocks and other data structures on TON Blockchain. Their memory layouts and purposes significantly differ from ordinary cells.

Kinds (or subtypes) of all cells are encoded by an integer between $-1$ and $255$. Ordinary cells are encoded by $-1$, while exotic ones can be encoded by any other integer in that range. The subtype of an exotic cell is stored in the first $8$ bits of its data, which means valid exotic cells always have at least $8$ data bits.

[TVM][tvm] currently supports the following exotic cell subtypes:
* [Pruned branch cell][c-pruned], with subtype encoded as $1$ — they represent deleted subtrees of cells.
* [Library reference cell][c-library], with subtype encoded as $2$ — they are used for storing libraries, and usually, in [masterchain](/book/masterchain) contexts.
* [Merkle proof cell][c-mproof], with subtype encoded as $3$ — they are used for verifying that certain portions of other cell's tree data belong to the full tree.
* [Merkle update cell][c-mupdate], with subtype encoded as $4$ — they always have two references and behave like a [Merkle proof][mproof] for both of them.

<Callout>

  **Useful links:**\
  [Pruned branch cells in TON Docs][c-pruned]\
  [Library reference cells in TON Docs][c-library]\
  [Merkle proof cells in TON Docs][c-mproof]\
  [Merkle update cells in TON Docs][c-mupdate]\
  [Simple proof-verifying example in TON Docs][mproof]

</Callout>

[c-pruned]: https://docs.ton.org/develop/data-formats/exotic-cells#pruned-branch
[c-library]: https://docs.ton.org/develop/data-formats/library-cells
[c-mproof]: https://docs.ton.org/develop/data-formats/exotic-cells#merkle-proof
[c-mupdate]: https://docs.ton.org/develop/data-formats/exotic-cells#merkle-update
[mproof]: https://docs.ton.org/develop/data-formats/exotic-cells#simple-proof-verifying-example

### Levels [#cells-levels]

Every cell, being a [quadtree][quadtree], has an attribute called _level_, which is represented by an integer between $0$ and $3$. The level of an [ordinary](#cells-kinds) cell is always equal to the maximum of the levels of all its references. That is, level of an ordinary cell without references is equal to $0$.

[Exotic](#cells-kinds) cells have different rules for determining their level, which are described [on this page in TON Docs](https://docs.ton.org/develop/data-formats/exotic-cells).

### Serialization [#cells-serialization]

Before a cell can be transferred over the network or stored on disk, it must be serialized. There are several common formats, such as [standard `Cell{:tact}` representation](#cells-representation) and [BoC](#cells-boc).

#### Standard representation [#cells-representation]

Standard [`Cell{:tact}`](#cells) representation is a common serialization format for cells first described in the [tvm.pdf](https://docs.ton.org/tvm.pdf). Its algorithm representing cells in octet (byte) sequences begins with serializing the first $2$ bytes called descriptors:

* _Refs descriptor_ is calculated according to this formula: $r + 8 * k + 32 * l$, where $r$ is the number of references contained in the cell (between $0$ and $4$), $k$ is a flag for the cell kind ($0$ for [ordinary](#cells-kinds) and $1$ for [exotic](#cells-kinds)), and $l$ is the [level](#cells-levels) of the cell (between $0$ and $3$).
* _Bits descriptor_ is calculated according to this formula $\lfloor\frac{b}{8}\rfloor + \lceil\frac{b}{8}\rceil$, where $b$ is the number of bits in the cell (between $0$ and $1023$).

Then, the data bits of the cell themselves are serialized as $\lceil\frac{b}{8}\rceil$ $8$-bit octets (bytes). If $b$ is not a multiple of eight, a binary $1$ and up to six binary $0$s are appended to the data bits.

Next, the $2$ bytes store the depth of the refs, i.e. the number of cells between the root of the cell tree (the current cell) and the deepest of the references, including it. For example, a cell containing only one reference and no further references would have a depth of $1$, while the referenced cell would have a depth of $0$.

Finally, for every reference cell the [SHA-256][sha-2] hash of its standard representation is stored, occupying $32$ bytes per each such cell and recursively repeating the said algorithm. Notice, that cyclic cell references are not allowed, so this recursion always ends in a well-defined manner.

If we were to compute the hash of the standard representation of this cell, all the bytes from steps above would be concatenated together and then hashed using [SHA-256][sha-2] hash. This is the algorithm behind [`HASHCU` and `HASHSU` instructions](https://docs.ton.org/learn/tvm-instructions/instructions) of [TVM][tvm] and respective [`Cell.hash(){:tact}`](/ref/core-cells#cellhash) and [`Slice.hash(){:tact}`](/ref/core-cells#slicehash) functions of Tact.

#### Bag of Cells [#cells-boc]

Bag of Cells, or _BoC_ for short, is a format for serializing and de-serializing cells into byte arrays as described in [boc.tlb](https://github.com/ton-blockchain/ton/blob/24dc184a2ea67f9c47042b4104bbb4d82289fac1/crypto/tl/boc.tlb#L25) [TL-B schema][tlb].

Read more about BoC in TON Docs: [Bag of Cells](https://docs.ton.org/develop/data-formats/cell-boc#bag-of-cells).

<Callout>

  Advanced information on [`Cell{:tact}`](#cells) serialization: [Canonical `Cell{:tact}` Serialization](https://docs.ton.org/develop/research-and-development/boc).

</Callout>

### Immutability [#cells-immutability]

Cells are read-only and immutable, but there are two major sets of [ordinary](#cells-kinds) cell manipulation instructions in [TVM][tvm]:

* Cell creation (or serialization) instructions, which are used to construct new cells from previously kept values and cells;
* And cell parsing (or deserialization) instructions, which are used to extract or load data previously stored into cells via serialization instructions.

On top of that, there are instructions specific to [exotic](#cells-kinds) cells to create them and expect their values. However, [ordinary](#cells-kinds) cell parsing instructions can still be used on [exotic](#cells-kinds) ones, in which case they are automatically replaced by [ordinary](#cells-kinds) cells during such deserialization attempts.

All cell manipulation instructions require transforming values of [`Cell{:tact}`](#cells) type to either [`Builder{:tact}`](#builders) or [`Slice{:tact}`](#slices) types before such cells can be modified or inspected.

## Builders

`Builder{:tact}` is a cell manipulation [primitive][p] for using cell creation instructions. They're immutable just like cells are, and allow constructing new cells from previously kept values and cells. Unlike cells, values of type `Builder{:tact}` appear only on [TVM][tvm] stack and cannot be stored in persistent storage. That means, for example, that persistent storage fields with type `Builder{:tact}` would actually be stored as cells under the hood.

`Builder{:tact}` type represents partially composed cells, for which fast operations for appending integers, other cells, references to other cells and many others are defined:

* [`Builder.storeUint(){:tact}` in Core library][b-2]
* [`Builder.storeInt(){:tact}` in Core library][b-3]
* [`Builder.storeBool(){:tact}` in Core library][b-4]
* [`Builder.storeSlice(){:tact}` in Core library][b-5]
* [`Builder.storeCoins(){:tact}` in Core library][b-6]
* [`Builder.storeAddress(){:tact}` in Core library][b-7]
* [`Builder.storeRef(){:tact}` in Core library][b-8]

While you may use them for [manual construction](#cnp-manually) of the cells, it's strongly recommended to use [Structs][struct] instead: [Construction of cells with Structs](#cnp-structs).

## Slices

`Slice{:tact}` is a cell manipulation [primitive][p] for using cell parsing instructions. Unlike cells, they're mutable and allow extracting or loading data previously stored into cells via serialization instructions. Also unlike cells, values of type `Slice{:tact}` appear only on [TVM][tvm] stack and cannot be stored in persistent storage. That means, for example, that persistent storage fields with type `Slice{:tact}` would actually be stored as cells under the hood.

`Slice{:tact}` type represents either the remainder of a partially parsed cell, or a value (subcell) residing inside such a cell and extracted from it by a parsing instruction:

* [`Slice.loadUint(){:tact}` in Core library][s-2]
* [`Slice.loadInt(){:tact}` in Core library][s-3]
* [`Slice.loadBool(){:tact}` in Core library][s-4]
* [`Slice.loadSlice(){:tact}` in Core library][s-5]
* [`Slice.loadCoins(){:tact}` in Core library][s-6]
* [`Slice.loadAddress(){:tact}` in Core library][s-7]
* [`Slice.loadRef(){:tact}` in Core library][s-8]

While you may use them for [manual parsing](#cnp-manually) of the cells, it's strongly recommended to use [Structs][struct] instead: [Parsing of cells with Structs](#cnp-structs).

## Serialization types

Similar to serialization options of [`Int{:tact}`](/book/integers) type, `Cell{:tact}`, `Builder{:tact}` and `Slice{:tact}` also have various representations for encoding their values in the following cases:

* as [storage variables](/book/contracts#variables) of [contracts](/book/contracts) and [traits](/book/types#traits),
* and as fields of [Structs](/book/structs-and-messages#structs) and [Messages](/book/structs-and-messages#messages).

```tact {2-3}
contract SerializationExample {
    someCell: Cell as remaining;
    someSlice: Slice as bytes32;

    // Constructor function,
    // necessary for this example contract to compile
    init() {
        self.someCell = emptyCell();
        self.someSlice = beginCell().storeUint(42, 256).asSlice();
    }
}
```

### `remaining` [#serialization-remaining]

The `remaining{:tact}` serialization option can be applied to values of [`Cell{:tact}`](#cells), [`Builder{:tact}`](#builders) and [`Slice{:tact}`](#slices) types.

It affects the process of constructing and parsing cell values by causing them to be stored and loaded directly rather than as a reference. To draw parallels with [cell manipulation instructions](#cells-immutability), specifying `remaining{:tact}` is like using [`Builder.storeSlice(){:tact}`][b-5] and [`Slice.loadSlice(){:tact}`][s-5] instead of [`Builder.storeRef(){:tact}`][b-8] and [`Slice.loadRef(){:tact}`][s-8], which are to be used by default.

In addition, the [TL-B][tlb] representation produced by Tact changes too:

```tact {3-5, 8-10}
contract SerializationExample {
    // By default
    cRef: Cell;    // ^cell in TL-B
    bRef: Builder; // ^builder in TL-B
    sRef: Slice;   // ^slice in TL-B

    // With `remaining`
    cRem: Cell as remaining;    // remainder<cell> in TL-B
    bRem: Builder as remaining; // remainder<builder> in TL-B
    sRem: Slice as remaining;   // remainder<slice> in TL-B

    // Constructor function,
    // necessary for this example contract to compile
    init() {
        self.cRef = emptyCell();
        self.bRef = beginCell();
        self.sRef = emptySlice();
        self.cRem = emptyCell();
        self.bRem = beginCell();
        self.sRem = emptySlice();
    }
}
```

There, `^cell`, `^builder` and `^slice` in [TL-B][tlb] syntax mean the reference to [`Cell{:tact}`](#cells), [`Builder{:tact}`](#builders) and [`Slice{:tact}`](#slices) values respectively, while the `remainder<…>` of `cell`, `builder` or `slice` tells that the given value would be stored as a `Slice{:tact}` directly and not as a reference.

Now, to give a real-world example, imagine that you need to notice and react to inbound [jetton][jetton] transfers in your smart contract. The appropriate [Message][message] structure for doing so would look something like this:

```tact /remaining/
message(0x7362d09c) JettonTransferNotification {
    queryId: Int as uint64;             // arbitrary request number to prevent replay attacks
    amount: Int as coins;               // amount of jettons transferred
    sender: Address;                    // address of the sender of the jettons
    forwardPayload: Slice as remaining; // optional custom payload
}
```

And the [receiver][recv] in the contract would look like this:

```tact
receive(msg: JettonTransferNotification) {
    // ... you do you ...
}
```

Upon receiving a [jetton][jetton] transfer notification message, its cell body is converted into a [`Slice{:tact}`](#slices) and then parsed as a `JettonTransferNotification{:tact}` [Message][message]. At the end of this process, the `forwardPayload` will have all the remaining data of the original message cell.

Here, it's not possible to violate the [jetton][jetton] standard by placing the `forwardPayload: Slice as remaining` field in any other position in the `JettonTransferNotification{:tact}` [Message][message]. That's because Tact prohibits usage of `as remaining{:tact}` for any but the last field of the [Structs][struct] and [Messages][message] to prevent misuse of the contract storage and reduce gas consumption.

<Callout>

  Note, that the cell serialized via `as remaining{:tact}` cannot be [optional](/book/optional). That is, specifying something like `Cell? as remaining{:tact}`, `Builder? as remaining{:tact}` or `Slice? as remaining{:tact}` would cause a compilation error.

  Also note, that specifying `remaining{:tact}` for the `Cell{:tact}` as the [map](/book/maps) value type is considered an error and it won't compile.

</Callout>

### `bytes32` [#serialization-bytes64]

<Callout>

  To be resolved by [#94](https://github.com/tact-lang/tact-docs/issues/94).

</Callout>

### `bytes64` [#serialization-bytes64]

<Callout>

  To be resolved by [#94](https://github.com/tact-lang/tact-docs/issues/94).

</Callout>

## Operations

### Construct and parse [#operations-cnp]

In Tact, there are at least two ways to construct and parse cells:

* [Manually](#cnp-manually), which involves active use of [`Builder{:tact}`](#builders), [`Slice{:tact}`](#slices) and [relevant methods](/ref/core-cells).
* [Using Structs](#cnp-structs), which is a recommended and much more convenient approach.

#### Manually [#cnp-manually]

Construction via `Builder{:tact}`      | Parsing via `Slice{:tact}`
:------------------------------------- | :-------------------------
[`beginCell(){:tact}`][b-1]            | [`Cell.beginParse(){:tact}`][s-1]
[`.storeUint(42, 7){:tact}`][b-2]      | [`Slice.loadUint(7){:tact}`][s-2]
[`.storeInt(42, 7){:tact}`][b-3]       | [`Slice.loadInt(7){:tact}`][s-3]
[`.storeBool(true){:tact}`][b-4]       | [`Slice.loadBool(true){:tact}`][s-4]
[`.storeSlice(slice){:tact}`][b-5]     | [`Slice.loadSlice(slice){:tact}`][s-5]
[`.storeCoins(42){:tact}`][b-6]        | [`Slice.loadCoins(42){:tact}`][s-6]
[`.storeAddress(address){:tact}`][b-7] | [`Slice.loadAddress(){:tact}`][s-7]
[`.storeRef(cell){:tact}`][b-8]        | [`Slice.loadRef(){:tact}`][s-8]
[`.endCell(){:tact}`][b-9]             | [`Slice.endParse(){:tact}`][s-9]

[b-1]: /ref/core-cells#begincell
[b-2]: /ref/core-cells#builderstoreuint
[b-3]: /ref/core-cells#builderstoreint
[b-4]: /ref/core-cells#builderstorebool
[b-5]: /ref/core-cells#builderstoreslice
[b-6]: /ref/core-cells#builderstorecoins
[b-7]: /ref/core-cells#builderstoreaddress
[b-8]: /ref/core-cells#builderstoreref
[b-9]: /ref/core-cells#builderendcell
[s-1]: /ref/core-cells#cellbeginparse
[s-2]: /ref/core-cells#sliceloaduint
[s-3]: /ref/core-cells#sliceloadint
[s-4]: /ref/core-cells#sliceloadbool
[s-5]: /ref/core-cells#sliceloadslice
[s-6]: /ref/core-cells#sliceloadcoins
[s-7]: /ref/core-cells#sliceloadaddress
[s-8]: /ref/core-cells#sliceloadref
[s-9]: /ref/core-cells#sliceendparse

#### Using Structs (recommended) [#cnp-structs]

[Structs][struct] and [Messages][message] are almost like living [TL-B schemas][tlb]. Which means that they're, essentially, [TL-B schemas][tlb] expressed in maintainable, verifiable and user-friendly Tact code.

It is strongly recommended to use them and their [methods](/book/functions#extension-function) like [`Struct.toCell(){:tact}`][st-tc] and [`Struct.fromCell(){:tact}`][st-fc] instead of manually constructing and parsing cells, as this allows for much more declarative and self-explanatory contracts.

The examples of manual parsing [above](#cnp-manually) could be re-written using [Structs][struct], with descriptive names of fields if one so desires:

```tact /fromCell/ /toCell/
// First Struct
struct Showcase {
    id: Int as uint8;
    someImportantNumber: Int as int8;
    isThatCool: Bool;
    payload: Slice;
    nanoToncoins: Int as coins;
    wackyTacky: Address;
    jojoRef: Adventure; // another Struct
}

// Here it is
struct Adventure {
    bizarre: Bool = true;
    time: Bool = false;
}

fun example() {
    // Basics
    let s = Showcase.fromCell(
        Showcase{
            id: 7,
            someImportantNumber: 42,
            isThatCool: true,
            payload: emptySlice(),
            nanoToncoins: 1330 + 7,
            wackyTacky: myAddress(),
            jojoRef: Adventure{ bizarre: true, time: false },
        }.toCell());
    s.isThatCool; // true
}
```

Note, that Tact's auto-layout algorithm is greedy. For example, `struct Adventure{:tact}` occupies very little space, and it won't be stored as a reference [`Cell{:tact}`](#cells), but will be provided directly as a [`Slice{:tact}`](#slices).

By using [Structs][struct] and [Messages][message] over manual [`Cell{:tact}`](#cells) composition and parsing, those details would be simplified away and won't cause any hassle when the optimized layout changes.

<Callout>

  **Useful links:**\
  [Convert serialization](/book/func#convert-serialization)\
  [`Struct.toCell(){:tact}` in Core library][st-tc]\
  [`Struct.fromCell(){:tact}` in Core library][st-fc]\
  [`Struct.fromSlice(){:tact}` in Core library][st-fs]\
  [`Message.toCell(){:tact}` in Core library][msg-tc]\
  [`Message.fromCell(){:tact}` in Core library][msg-fc]\
  [`Message.fromSlice(){:tact}` in Core library][msg-fs]

</Callout>

[st-tc]: /ref/core-cells#structtocell
[st-fc]: /ref/core-cells#structfromcell
[st-fs]: /ref/core-cells#structfromslice
[msg-tc]: /ref/core-cells#messagetocell
[msg-fc]: /ref/core-cells#messagefromcell
[msg-fs]: /ref/core-cells#messagefromslice

### Check if empty [#operations-empty]

Neither [`Cell{:tact}`](#cells) nor [`Builder{:tact}`](#builders) can be checked for emptiness directly — one needs to convert them to [`Slice{:tact}`](#slices) first.

To check if there are any bits, use [`Slice.dataEmpty(){:tact}`][s-de]. To check if there are any references, use [`Slice.refsEmpty(){:tact}`][s-re]. And to check both at the same time, use [`Slice.empty(){:tact}`][s-e].

To also throw an [exit code 9](/book/exit-codes#9) whenever the [`Slice{:tact}`](#slices) isn't completely empty, use [`Slice.endParse(){:tact}`][s-ep].

```tact
// Preparations
let someCell = beginCell().storeUint(42, 7).endCell();
let someBuilder = beginCell().storeRef(someCell);

// Obtaining our Slices
let slice1 = someCell.asSlice();
let slice2 = someBuilder.asSlice();

// .dataEmpty()
slice1.dataEmpty(); // false
slice2.dataEmpty(); // true

// .refsEmpty()
slice1.refsEmpty(); // true
slice2.refsEmpty(); // false

// .empty()
slice1.empty(); // false
slice2.empty(); // false

// .endParse()
try {
    slice1.endParse();
    slice2.endParse();
} catch (e) {
    e; // 9
}
```

<Callout>

  **Useful links:**\
  [`Cell.asSlice(){:tact}` in Core library](/ref/core-cells#cellasslice)\
  [`Builder.asSlice(){:tact}` in Core library](/ref/core-cells#builderasslice)\
  [`Slice.dataEmpty(){:tact}` in Core library][s-de]\
  [`Slice.refsEmpty(){:tact}` in Core library][s-re]\
  [`Slice.empty(){:tact}` in Core library][s-e]\
  [`Slice.endParse(){:tact}` in Core library][s-ep]

</Callout>

[s-de]: /ref/core-cells#slicedataempty
[s-re]: /ref/core-cells#slicerefsempty
[s-e]: /ref/core-cells#sliceempty
[s-ep]: /ref/core-cells#sliceendparse

### Check if equal [#operations-equal]

Values of type [`Builder{:tact}`](#builders) cannot be compared directly using binary equality [`=={:tact}`][bin-eq] or inequality [`!={:tact}`][bin-eq] operators. However, values of type [`Cell{:tact}`](#cells) and [`Slice{:tact}`](#slices) can.

Direct comparisons:

```tact
let a = beginCell().storeUint(123, 8).endCell();
let aSlice = a.asSlice();

let b = beginCell().storeUint(123, 8).endCell();
let bSlice = b.asSlice();

let areCellsEqual = a == b; // true
let areCellsNotEqual = a != b; // false

let areSlicesEqual = aSlice == bSlice; // true
let areSlicesNotEqual = aSlice != bSlice; // false
```

Note, that direct comparison via `=={:tact}` or `!={:tact}` operators implicitly uses [SHA-256](https://en.wikipedia.org/wiki/SHA-2#Hash_standard) hashes of [standard `Cell{:tact}` representation](#cells-representation) under the hood.

Explicit comparisons using `.hash(){:tact}` are also available:

```tact
let a = beginCell().storeUint(123, 8).endCell();
let aSlice = a.asSlice();

let b = beginCell().storeUint(123, 8).endCell();
let bSlice = b.asSlice();

let areCellsEqual = a.hash() == b.hash(); // true
let areCellsNotEqual = a.hash() != b.hash(); // false

let areSlicesEqual = aSlice.hash() == bSlice.hash(); // true
let areSlicesNotEqual = aSlice.hash() != bSlice.hash(); // false
```

<Callout>

  **Useful links:**\
  [`Cell.hash(){:tact}` in Core library](/ref/core-cells#cellhash)\
  [`Builder.hash(){:tact}` in Core library](/ref/core-cells#builderhash)\
  [`=={:tact}` and `!={:tact}`][bin-eq]

</Callout>

[p]: /book/types#primitive-types
[struct]: /book/structs-and-messages#structs
[message]: /book/structs-and-messages#messages
[recv]: /book/contracts#receiver-functions

[tvm]: https://docs.ton.org/learn/tvm-instructions/tvm-overview
[tlb]: https://docs.ton.org/develop/data-formats/tl-b-language
[jetton]: https://docs.ton.org/develop/dapps/asset-processing/jettons
[sha-2]: https://en.wikipedia.org/wiki/SHA-2#Hash_standard

[quadtree]: https://en.wikipedia.org/wiki/Quadtree
[bin-eq]: /book/operators#binary-equality



## config.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/config.mdx)
# Configuration

import { Callout } from 'nextra/components'

The behavior of Tact compiler can be customized using its configuration file, `tact.config.json` — a JSON file that contains the list of settings according to the specific [schema](#schema).

This page lists all of the configuration options as they're structured in the [schema](#schema). Look for table of contents on the right to easily navigate them.

<Callout>

  The only requirement for that file is to be a valid JSON with [proper fields](#schema), so it can be named arbitrarily. However, naming your config file as `tact.config.json` is a common convention encouraged and supported by all tools working with Tact.

</Callout>

## `$schema` [#schema]

A [JSON schema](https://json-schema.org/) file is available for editors to provide autocompletion and hover hints: [configSchema.json](http://raw.githubusercontent.com/tact-lang/tact/main/schemas/configSchema.json).

Simply add the `$schema` field on top your configuration file:

```json filename="tact.config.json" {2}
{
  "$schema": "http://raw.githubusercontent.com/tact-lang/tact/main/schemas/configSchema.json",
  "projects": []
}
```

## `projects` [#projects]

List of Tact projects with respective compilation options. Each `.tact` file represents its own Tact project.

```json filename="tact.config.json" {3,4}
{
  "projects": [
    { },
    { }
  ]
}
```

### `name` [#projects-name]

Name of the project. All generated files are prefixed with it.

In [Blueprint][bp], `name` refers to the name of the contract itself.

```json filename="tact.config.json" {4,7}
{
  "projects": [
    {
      "name": "some_prefix"
    },
    {
      "name": "ContractUnderBlueprint"
    }
  ]
}
```

### `path` [#projects-path]

Path to the project's Tact file. You can only specify one Tact file per project.

In [Blueprint][bp], `path` is superseded by the `target` field in `wrappers/ContractName.compile.ts`.

```json filename="tact.config.json" {5}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact"
    }
  ]
}
```

### `output` [#projects-output]

Path to the directory where all generated files will be placed.

In [Blueprint][bp], `output` is not used and all generated files are always placed in `build/ProjectName/`.

```json filename="tact.config.json" {6}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output"
    }
  ]
}
```

### `options` [#projects-options]

Compilation options for the project.

In [Blueprint][bp], they act as default unless modified in `wrappers/ContractName.compile.ts`.

```json filename="tact.config.json" {7,11}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "options": {}
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {}
    }
  ]
}
```

#### `debug` [#options-debug]

`false{:json}` by default.

If set to `true{:json}`, enables debug output of a contract and allows usage of [`dump(){:tact}`](/ref/core-debug#dump) function, which is useful for [debugging purposes](/book/debug). With this option enabled, the contract will report that it was compiled in debug mode using the `supported_interfaces` method.

```json filename="tact.config.json" {8,14}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "options": {
        "debug": true
      }
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {
        "debug": true
      }
    }
  ]
}
```

<Callout>

  Read more on the dedicated page: [Debugging](/book/debug).

</Callout>

#### `masterchain` [#options-masterchain]

`false{:json}` by default.

If set to `true{:json}`, enables [masterchain](/book/masterchain) support.

```json filename="tact.config.json" {8,14}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "options": {
        "masterchain": true
      }
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {
        "masterchain": true
      }
    }
  ]
}
```

<Callout>

  Read more on the dedicated page: [Masterchain](/book/masterchain).

</Callout>

#### `external` [#options-external]

`false{:json}` by default.

If set to `true{:json}`, enables support of [external](/book/external) message receivers.

```json filename="tact.config.json" {8,14}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "options": {
        "external": true
      }
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {
        "external": true
      }
    }
  ]
}
```

<Callout>

  Read more on the dedicated page: [External messages](/book/external).

</Callout>

#### `ipfsAbiGetter` [#options-ipfsabigetter]

`false{:json}` by default.

If set to `true{:json}`, enables generation of a [getter](/book/contracts#getter-functions) with IPFS links describing the contract's ABI.

```json filename="tact.config.json" {8,14}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "options": {
        "ipfsAbiGetter": true
      }
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {
        "ipfsAbiGetter": true
      }
    }
  ]
}
```

<Callout>

  Read more on the dedicated page: [OTP-003: Self-ABI reporting](/ref/evolution/OTP-003).

</Callout>

#### `interfacesGetter` [#options-interfacesgetter]

`false{:json}` by default.

If set to `true{:json}`, enables generation of a [getter](/book/contracts#getter-functions) with a list of interfaces provided by the contract.

```json filename="tact.config.json" {8,14}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "options": {
        "interfacesGetter": true
      }
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {
        "interfacesGetter": true
      }
    }
  ]
}
```

<Callout>

  Read more: [Supported interfaces](/book/contracts#interfaces).

</Callout>

#### `experimental` [#options-experimental]

Experimental options that might be removed in the future. Use with caution!

```json filename="tact.config.json" {8,14}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "options": {
        "experimental": {}
      }
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {
        "experimental": {}
      }
    }
  ]
}
```

##### `inline` [#experimental-inline]

`false{:json}` by default.

If set to `true{:json}`, enables inlining of all functions in contracts. This can reduce gas usage at the cost of bigger contracts.

```json filename="tact.config.json" {9,17}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "options": {
        "experimental": {
          "inline": true
        }
      }
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {
        "experimental": {
          "inline": true
        }
      }
    }
  ]
}
```

### `mode` [#projects-mode]

Compilation mode of the project. Valid values are:

Value                            | Description
:------------------------------- | :----------
`"full"{:json}`                  | (default) Runs the whole compilation pipeline and emits FunC code, BoC, and various utility files, including wrappers for TypeScript.
`"fullWithDecompilation"{:json}` | Runs the whole compilation pipeline like `"full"{:json}`, and also decompiles produced binary code in the BoC format.
`"funcOnly"{:json}`              | Only outputs intermediate FunC code, preventing further compilation.
`"checkOnly"{:json}`             | Only performs syntax and type checking, preventing further compilation.

In [Blueprint][bp], `mode` is always set to `"full"{:json}` and cannot be overwritten.

```json filename="tact.config.json" {7,13}
{
  "projects": [
    {
      "name": "some_prefix",
      "path": "./contract.tact",
      "output": "./contract_output",
      "mode": "full"
    },
    {
      "name": "func_only",
      "path": "./contract.tact",
      "output": "./contract_output",
      "mode": "funcOnly"
    }
  ]
}
```

## Full example

```json filename="tact.config.json" copy=false
{
  "$schema": "http://raw.githubusercontent.com/tact-lang/tact/main/schemas/configSchema.json",
  "projects": [
    {
      "name": "basic",
      "path": "./basic.tact",
      "output": "./basic_output",
      "mode": "full"
    },
    {
      "name": "func_only",
      "path": "./basic.tact",
      "output": "./basic_output",
      "mode": "funcOnly"
    },
    {
      "name": "debugPrefix",
      "path": "./contracts/contract.tact",
      "output": "./contracts/output",
      "options": {
        "debug": true
      }
    },
    {
      "name": "ContractUnderBlueprint",
      "options": {
        "debug": false,
        "masterchain": false,
        "external": false,
        "ipfsAbiGetter": true,
        "interfacesGetter": true,
        "experimental": {
          "inline": false
        }
      }
    }
  ]
}
```

[bp]: https://github.com/ton-org/blueprint


## constants.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/constants.mdx)
# Constants

Constants in Tact could be a little bit more advanced than in popular languages: they could be virtual and abstract. Smart contracts often need to implement multiple traits and sometimes you need to configure some of them in compile time. Constructors in traits are prohibited due to their unpredicted behavior. So, we have to use constants and fields instead to pass values to them. It is the job of a main contract to implement values and constants for all traits.

## Simple constant

Let's start with a simple constant. It is a value that is defined in compile time and cannot be changed. You can define a constant on the top level or inside a contract/trait. Let's define a constant on top level:

```tact
const MY_CONSTANT: Int = 42;
```

Similar for traits and contracts:

```tact
trait MyTrait {
    const MY_CONSTANT: Int = 42;
}

contract MyContract {
    const MY_CONSTANT: Int = 42;
}
```

## Virtual and abstract constants

Virtual constants are the constants that could be defined in a trait but changed in a contract. It is useful when you need to configure some of the traits in compile time. Let's define a virtual constant and an abstract one:

```tact
trait MyTrait {
    virtual const MY_FEE: Int = ton("1.0");
}

trait MyAbstractTrait {
    abstract const MY_DEV_FEE: Int;
}
```

Now you can overwrite defaults in the contract:

```tact
contract MyContract with
    MyTrait,
    MyAbstractTrait, // trailing comma is allowed
{
    override const MY_FEE: Int = ton("0.5");
    override const MY_DEV_FEE: Int = ton("1000");
}
```

This could be very useful to help a compiler to have some values in compile time, for example, you can enable and disable features without needing to change the code and not wasting gas.

```tact
trait Treasure {
    virtual const ENABLE_TIMELOCK: Bool = true;

    receive("Execute") {
        if (self.ENABLE_TIMELOCK) {
            //
            // This branch would be removed in compile time if ENABLE_TIMELOCK is false
            //
        }
    }
}

contract MyContract with Treasure {
    override const ENABLE_TIMELOCK: Bool = false;
}
```


## contracts.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/contracts.mdx)
# Contracts

import { Callout } from 'nextra/components'

Contracts in Tact are similar to classes in popular object-oriented languages, except that their instances are deployed on the blockchain and they can't be passed around like [Structs and Messages](/book/structs-and-messages).

## Self-references [#self]

Contracts and [traits][trait] have a built-in [identifier](/book/expressions#identifiers) `self{:tact}`, which is used for referring to their fields (persistent state [variables](#variables) and [constants](#variables)) and methods ([internal functions](#internal-functions)):

```tact
contract Example {
    // persistent state variables
    foo: Int;

    init() {
        self.foo = 42; // <- referencing variable foo through self.
    }
}
```

## Structure

Each contract can contain:

* [Inherited traits](#traits)
* [Supported interfaces](#interfaces)
* [Persistent state variables](#variables)
* [Constructor function `init(){:tact}`](#init-function)
* [Contract constants](#constants)
* [Getter functions](#getter-functions)
* [Receiver functions](#receiver-functions)
* [Internal functions](#internal-functions)

### Inherited traits, `with{:tact}` [#traits]

Contracts can inherit all the declarations and definitions from [traits][trait] and override some of their default behaviours. In addition to that, every contract and trait implicitly inherits the special [`BaseTrait{:tact}` trait](/ref/core-base).

To inherit a [trait][trait], specify its name after the keyword `with{:tact}` in contract's declaration. To inherit multiple traits at once, specify their names in a comma-separated list with an optional trailing comma.

```tact /with/
trait InheritMe {}
trait InheritMeToo {}

// A contract inheriting a single trait
contract Single with InheritMe {}

// A contract inheriting multiple traits
contract Plural with
    InheritMe,
    InheritMeToo, // trailing comma is allowed
{}
```

As [traits][trait] are not allowed to have [`init(){:tact}` function](#init-function), a contract inheriting a trait with any [persistent state variables](#variables) declared must initialize them by providing its own [`init(){:tact}` function](#init-function).

```tact
trait Supe { omelander: Bool }

contract Vot with Supe {
    init() {
        self.omelander = true;
    }
}
```

If declared or defined in a trait, internal functions and constants can be marked as [virtual or abstract](/book/functions#virtual-and-abstract-functions) and overridden in contracts inheriting from the trait.

### Supported interfaces, `@interface(…)` [#interfaces]

It's hard to figure out what a contract does and what [receivers](#receiver-functions) and [getters](#getter-functions) it has without looking at its source code. Sometimes the source is unavailable or inaccessible, and all that's left is to try to disassemble the contract and introspect it that way, which is a very messy and error-prone approach with diminishing returns and no real reproducibility.

In order to resolve this issue, an [OTP-001: Supported Interfaces](/ref/evolution/OTP-001) was created. In accordance to it, Tact contracts [can report](/book/config#options-interfacesgetter) the list of supported interfaces as a return value of a special `supported_interfaces` [getter](#get-functions). That [getter](#getter-functions) is accessible off-chain using any TON Blockchain explorer — one just needs to specify `supported_interfaces` as a method to execute and get a list of hexadecimal values in return.

These hexadecimal values are truncated to the first 128 bit of [SHA-256](https://en.wikipedia.org/wiki/SHA-2#Hash_standard) hashes of the original [`String{:tact}`][p] values of the supported interfaces. The first value in this list **must** be equal to $\mathrm{0x5cec3d5d2cae7b1e84ec39d64a851b66}$ in [hexadecimal notation](/book/integers#hexadecimal), which is the first half of the SHA-256 hash for `"org.ton.introspection.v0"{:tact}`. If the first value is wrong, you must stop trying to introspect the contract, as it doesn't conform to the [Supported Interfaces](/ref/evolution/OTP-001) proposal.

To declare support of a certain interface, add one or more `@interface("…"){:tact}` attributes right before contract and [trait][trait] declarations:

```tact
@interface("His name is")
@interface("John")
contract SeeNah with Misc {
    // ...
}

@interface("name_of_your_org - miscellaneous")
trait Misc {
    // ...
}
```

Tact has a small set of interfaces provided under specific conditions:

* `"org.ton.abi.ipfs.v0"{:tact}`, in accordance to [OTP-003: Self-ABI Reporting](/ref/evolution/OTP-003) — opt-in via [`ipfsAbiGetter`](/book/config#options-ipfsabigetter) config property
* `"org.ton.deploy.lazy.v0"{:tact}`, in accordance to [OTP-005: Argument-addressable contracts](/ref/evolution/OTP-005)
* `"org.ton.debug.v0"{:tact}`, but only if [debug mode](/book/debug#debug-mode) is enabled
* `"org.ton.chain.any.v0"{:tact}` if [masterchain](/book/masterchain) support is enabled, and `"org.ton.chain.workchain.v0"{:tact}` otherwise

Some [traits][trait] in [standard libraries](/ref/standard-libraries) define their interfaces too:

* [`Ownable{:tact}`](/ref/stdlib-ownable#ownable) trait specifies `"org.ton.ownable"{:tact}`
* [`OwnableTransferable{:tact}`](/ref/stdlib-ownable#ownabletransferable) trait specifies `"org.ton.ownable.transferable.v2"{:tact}`
* [`Stoppable{:tact}`](/ref/stdlib-stoppable#stoppable) trait specifies `"org.ton.stoppable"{:tact}`
* [`Resumable{:tact}`](/ref/stdlib-stoppable#resumable) trait specifies `"org.ton.resumable"{:tact}`

To enable `supported_interfaces` [getter](#getter-functions) generation and use `@interface(){:tact}` attribute in your Tact contracts, modify a [`tact.config.json`](/book/config) file in the root of your project (or create it if it didn't exist yet), and [set the `interfacesGetter` property to `true{:json}`](/book/config#options-interfacesgetter).

If you're working on a [Blueprint][bp]-based project, you can enable `supported_interfaces` in the compilation configs of your contracts, which are located in a directory named `wrappers/`:

```typescript filename="wrappers/YourContractName.compile.ts" {7}
import { CompilerConfig } from '@ton/blueprint';

export const compile: CompilerConfig = {
  lang: 'tact',
  target: 'contracts/your_contract_name.tact',
  options: {
    interfacesGetter: true, // ← that's the stuff!
  }
};
```

In addition to that, [`tact.config.json`](/book/config) may still be used in [Blueprint][bp] projects. In such cases values specified in [`tact.config.json`](/book/config) act as default unless modified in the `wrappers/`.

<Callout type="warning" emoji="⚠️">

  Be aware that adding an interface does not guarantee that the contract actually implements any particular functionality, or that it implements it in any particular way. It's just an off-chain, verifiable promise that a contract _might_ have some specific code in it. It's up to you to trust, but verify, such claims.

  In addition, there is no guarantee that there won't be name clashes between different interfaces, although they are unlikely because even the first 128 bits of SHA-256 provide sufficient [collision resistance](https://en.wikipedia.org/wiki/Collision_resistance).

</Callout>

### Persistent state variables [#variables]

Contracts can define state variables that persist between contract calls. Contracts in TON [pay rent](https://docs.ton.org/develop/smart-contracts/fees#storage-fee) in proportion to the amount of persistent space they consume, so [compact representations via serialization](/book/integers#serialization) are encouraged.

```tact
contract Example {
    // persistent state variables
    val: Int;              // Int
    val32: Int as uint32;  // Int serialized to an 32-bit unsigned
    mapVal: map<Int, Int>; // Int keys to Int values
    optVal: Int?;          // Int or null
}
```

State variables must have a default value or initialized in [`init(){:tact}`](#init-function) function, that runs on deployment of the contract. The only exception is persistent state variables of type [`map<K, V>{:tact}`](/book/maps) since they are initialized empty by default.

<Callout>

  Note, that Tact supports local, non-persistent-state variables too, see: [Variable declaration](/book/statements#let).

</Callout>

### Contract constants [#constants]

Unlike [variables](#variables), constants cannot change. Their values are calculated in _compile-time_ and cannot change during execution.

There isn't much difference between constants defined outside of a contract (global constants) and inside the contract (contract constants). Those defined outside can be used by other contracts in your project.

Constant initializations must be relatively simple and only rely on values known during compilation. If you add two numbers for example, the compiler will calculate the result during build and put the result in your compiled code.

You can read constants both in [receivers](#receiver-functions) and in [getters](#getter-functions).

Unlike [contract variables](#variables), **contract constants don't consume space in persistent state**. Their values are stored directly in the code [`Cell{:tact}`](/book/cells#cells) of the contract.

```tact
// global constants are calculated in compile-time and cannot change
const GlobalConst1: Int = 1000 + ton("42") + pow(10, 9);

contract Example {
    // contract constants are also calculated in compile-time and cannot change
    const ContractConst1: Int = 2000 + ton("43") + pow(10, 9);

    // contract constants can be an easy alternative to enums
    const StateUnpaid: Int = 0;
    const StatePaid: Int = 1;
    const StateDelivered: Int = 2;
    const StateDisputed: Int = 3;

    get fun sum(): Int {
        // access constants from anywhere
        return GlobalConst1 + self.ContractConst1 + self.StatePaid;
    }
}
```

Read more about constants on their dedicated page: [Constants](/book/constants).

### Constructor function `init()` [#init-function]

On deployment of the contract, the constructor function `init(){:tact}` is run.

If a contract has any [persistent state variables](#variables) without default values specified, it must initialize them in this function.

```tact
contract Example {
    // persistent state variables
    var1: Int = 0; // initialized with default value 0
    var2: Int;     // must be initialized in the init() function

    // constructor function
    init() {
        self.var2 = 42;
    }
}
```

If a contract doesn't have any persistent state variables, or they all have their default value specified, it may omit the `init(){:tact}` function declaration altogether. That's because unless explicitly declared, the empty `init(){:tact}` function is present by default in all contracts.

The following is an example of a valid empty contract:

```tact
contract IamEmptyAndIKnowIt {}
```

For your convenience, parameter list of `init(){:tact}` can have a trailing comma:

```tact
contract TheySeeMeTrailing {
    init(
        param1: Int,
        param2: Int, // trailing comma is allowed
    ) {
        // ...
    }
}
```

<Callout>

  To obtain initial state of the target contract in [internal functions](#internal-functions), [receivers](#receiver-functions) or [getters](#getter-functions) use [`initOf{:tact}`](/book/expressions#initof) expression.

</Callout>

### Getter functions

[Getter functions](/book/functions#getter-functions) are **not accessible from other contracts and exported only to off-chain world**.

Additionally, **getters cannot modify the contract's state variables**, only read their values and use them in expressions.

```tact
contract HelloWorld {
    foo: Int;

    init() {
        self.foo = 0;
    }

    // getter function with return type Int
    get fun foo(): Int {
        return self.foo; // can't change self.foo here
    }
}
```

Read more about them in their dedicated section: [Getter functions](/book/functions#getter-functions)

### Receiver functions

[Receiver functions](/book/functions#receiver-functions) in Tact can be one of the following three kinds:

* [`receive(){:tact}`](/book/receive), which receive internal messages (from other contracts).
* [`bounced(){:tact}`](/book/bounced), which are called when outgoing message from this contract has bounced back.
* [`external(){:tact}`](/book/external), which don't have a sender and can be sent by anyone in the world.

```tact
message CanBounce {
    counter: Int;
}

contract HelloWorld {
    counter: Int;

    init() {
        self.counter = 0;
    }

    get fun counter(): Int {
        return self.counter;
    }

    // internal message receiver, which responds to a string message "increment"
    receive("increment") {
        self.counter += 1;

        // sending the message back to the sender
        send(SendParameters{
            to: sender(),
            value: 0,
            mode: SendRemainingValue | SendIgnoreErrors,
            body: CanBounce{counter: self.counter}.toCell(),
        });
    }

    // bounced message receiver, which is called when the message bounces back to this contract
    bounced(src: bounced<MsBounced>) {
        self.counter = 0; // reset the counter in case message bounced
    }

    // external message receiver, which responds to off-chain message "hello, it's me"
    external("hello, it's me") {
        // can't be replied to as there's no sender!
        self.counter = 0;
    }
}
```

Naming a parameter of the receiver function with an underscore `_{:tact}` makes its value considered unused and discarded. This is useful when you don't need to inspect the message received and you only want it to convey a specific opcode:

```tact
message(42) UniverseCalls {}

contract Example {
    receive(_: UniverseCalls) {
        // Got a Message with opcode 42
    }
}
```

### Internal functions

These functions behave similarly to private methods in popular object-oriented languages — they're internal to contracts and can be called by prefixing them with a special [identifier `self{:tact}`](#field-access). That's why internal functions can sometimes be referred to as "contract methods".

Internal functions can access the contract's [persistent state variables](#variables) and [constants](#constants).

They can only be called from [receivers](#receiver-functions), [getters](#getter-functions) and other internal functions, but not from other contracts or [`init(){:tact}`](#init-function).

```tact
contract Functions {
    val: Int = 0;

    // this contract method can only be called from within this contract and access its variables
    fun onlyZeros() {
        require(self.val == 0, "Only zeros are permitted!");
    }

    // receiver function, which calls the internal function onlyZeros
    receive("only zeros") {
        self.onlyZeros();
    }
}
```

<Callout>

  Note, that Tact supports other kinds of functions too, see: [Functions](/book/functions).

</Callout>

[p]: /book/types#primitive-types
[trait]: /book/types#traits

[bp]: https://github.com/ton-org/blueprint


## debug.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/debug.mdx)
# Debugging Tact contracts

import { Callout, Steps, Tabs, Cards } from 'nextra/components'

Without fail, the code we write as smart contract developers doesn’t always do what we expected it to do. Sometimes it does something completely different! When the unexpected happens, the next task is to figure out why. To do so, there are various ways to reveal problems or "bugs" in the code. Let's get to *debugging*!

<Cards>
  <Cards.Card
    arrow
    title="General approach"
    href="#approach"
  />
  <Cards.Card
    arrow
    title="Debug mode"
    href="#debug-mode"
  />
  <Cards.Card
    arrow
    title="Structure of tests"
    href="#tests-structure"
  />
  <Cards.Card
    arrow
    title="Dump values"
    href="#tests-dump"
  />
  <Cards.Card
    arrow
    title="Expect certain states"
    href="#tests-errors"
  />
  <Cards.Card
    arrow
    title="Send messages"
    href="#tests-send"
  />
  <Cards.Card
    arrow
    title="Observe fees"
    href="#tests-fees"
  />
  <Cards.Card
    arrow
    title="Expect exit codes"
    href="#tests-errors"
  />
  <Cards.Card
    arrow
    title="Simulate time"
    href="#tests-time"
  />
  <Cards.Card
    arrow
    title="Emit and log messages"
    href="#logging"
  />
  <Cards.Card
    arrow
    title="Handle bounced messages"
    href="#bounced"
  />
  <Cards.Card
    arrow
    title="Experimental lab setup"
    href="#lab"
  />
</Cards>

## General approach [#approach]

At the moment, Tact doesn't have a step-through debugger. Despite that, it's still possible to use the ["printf debugging"](https://en.wikipedia.org/wiki/Debugging#printf_debugging) approach.

It involves actively placing [`dump(){:tact}`][dump] and [`dumpStack(){:tact}`](/ref/core-debug#dumpstack) function calls throughout your code and observing states of variables at a given point of time. Note, that those functions work only in a [debug mode](#debug-mode) and won't be executed otherwise.

<Callout>

  See how to use [`dump(){:tact}`][dump] for debugging: [Debug with `dump(){:tact}`](#tests-dump).

</Callout>

In addition to dumping values, it's often helpful to use assertive functions like [`require(){:tact}`](/ref/core-debug#require), [`nativeThrowIf(){:tact}`](/ref/core-debug#nativethrowif) and [`nativeThrowUnless(){:tact}`](/ref/core-debug#nativethrowunless). They help stating your assumptions clear, and are handy for setting up "trip wires" for catching issues in the future.

And if you didn't find or cannot resolve the cause of your issues, try asking the community in Tact's [Telegram chat][tg] or, if your issue or question is generally related to TON more than it's related to Tact, hop into [TON Dev Telegram chat](https://t.me/tondev_eng).

## Common debugging functions [#debug-functions]

Tact provides a handful amount of various functions useful for debugging: [Core library → Debug](/ref/core-debug).

## Enabling debug mode in compilation options [#debug-mode]

In order to make certain functions like [`dump(){:tact}`][dump] or [`dumpStack(){:tact}`](/ref/core-debug#dumpstack) work, one needs to enable debug mode.

The simplest and recommended approach is to modify a [`tact.config.json`](/book/config) file in the root of your project (or create it if it didn't exist yet), and [set the `debug` property to `true{:json}`](/book/config#options-debug).

If you're working on a [Blueprint][bp]-based project, you can enable debug mode in the compilation configs of your contracts, which are located in a directory named `wrappers/`:

```typescript filename="wrappers/YourContractName.compile.ts" {7}
import { CompilerConfig } from '@ton/blueprint';

export const compile: CompilerConfig = {
  lang: 'tact',
  target: 'contracts/your_contract_name.tact',
  options: {
    debug: true, // ← that's the stuff!
  }
};
```

Note, that versions of [Blueprint][bp] starting with 0.20.0 automatically enable debug mode in `wrappers/` for new contracts.

In addition to that, [`tact.config.json`](/book/config) may still be used in [Blueprint][bp] projects. In such cases values specified in [`tact.config.json`](/book/config) act as default unless modified in the `wrappers/`.

<Callout>

  Read more about configuration and [`tact.config.json`](/book/config) file: [Configuration](/book/config).\
  See how to use [`dump(){:tact}`][dump] for debugging: [Debug with `dump(){:tact}`](#tests-dump).

</Callout>

## Writing tests in Blueprint, with Sandbox and Jest [#tests]

The [Blueprint][bp] is a popular development framework for writing, testing and deploying smart contracts on TON Blockchain.

For testing smart contracts it uses the [Sandbox][sb], a local TON Blockchain emulator and [Jest][jest], a JavaScript testing framework.

Whenever you create a new [Blueprint][bp] project or use `blueprint create` command inside the existing project, it creates a new contract alongside with a test suite file for it.

Those files are placed in `tests/` folder and executed with [Jest][jest]. By default, all tests run, unless you specify specific group or test closure. For other options, refer to the brief documentation in the Jest CLI: `jest --help`.

### Structure of test files [#tests-structure]

Let's say that we have a contract named `Playground`, written in `contracts/playground.tact` file. If we've created that contract through [Blueprint][bp], then it also created a `tests/Playground.spec.ts` test suite file for us.

The test file contains a single `describe(){:typescript}` [Jest][jest] function call, which denotes a test group.

Inside that group, you'll have three variables, available in all tests within:

* `blockchain` — local blockchain instance provided by [Sandbox][sb]
* `deployer` — a TypeScript wrapper used for deploying our `Playground` contract or any other we'd like to be deployed
* `playground` — a TypeScript wrapper for our `Playground` contract

<Callout>

  It's a common mistake to update `.tact` code and run tests without making a build first. That's because tests in [Blueprint][bp] rely on TypeScript wrappers generated by a Tact compiler and work with the latest build made.

  That's why every time you make a change to your Tact code, make sure to also build it with `npx blueprint build` before you execute the test suite. For your convenience, you may unite builds and tests into a single command, as shown in the [experimental lab setup](#lab-4).

</Callout>

Then, a `beforeEach(){:tact}` [Jest][jest] function is called — it specifies all the code to be executed before each of the subsequent test closures.

<Callout>

  It is strongly advised not to modify the contents of `beforeEach(){:tact}`, unless you really need some specific behavior for each test closure or parameters of your [`init(){:tact}`](/book/contracts#init-function) function have changed.

</Callout>

Finally, each test closure is described with a call to `it(){:tact}` [Jest][jest] function — that's where tests are actually written.

A simplest example of the test closure can look like that:

```typescript
it('should deploy', async () => {
  // The check is done inside beforeEach, so this can be empty
});
```

### Debug with `dump()` [#tests-dump]

To see results of [`dump(){:tact}`][dump] function calls and use ["printf debugging"](#approach-3) approach, one has to:

1. Put calls to [`dump(){:tact}`][dump] and other [common debugging functions](#debug-functions) in relevant places of the code.
2. Run [Jest][jest] tests, which would call target functions and send messages to target receivers.

Assuming you've created a [new counter contract project](/#start), let's see how it works in practice.

First, let's place a call to [`dump(){:tact}`][dump] in `contracts/simple_counter.tact`, which would output the `amount` passed in `msg{:tact}` [Struct][struct] to contract's debug console:

```tact filename="contracts/simple_counter.tact" {3}
// ...
receive(msg: Add) {
    dump(msg.amount);
    // ...
}
// ...
```

Next, let's comment out all existing `it(){:typescript}` test closures in `tests/SimpleCounter.spec.ts` file. And then add the following one:

```typescript filename="tests/SimpleCounter.spec.ts"
it('should dump', async () => {
  await playground.send(
    deployer.getSender(),
    { value: toNano('0.5') },
    { $$type: 'Add', queryId: 1n, amount: 1n },
  );
});
```

It sends a message to our contract's `receive(msg: Add){:tact}` [receiver](/book/receive) without storing the [results of such send](#tests-send).

Now, if we build our contract with `yarn build{:shell}` and run our test suite with `yarn test{:shell}`, we'll see the following in the test logs:

```txt
console.log
  #DEBUG#: [DEBUG] File contracts/simple_counter.tact:17:9
  #DEBUG#: 1

    at SmartContract.runCommon (node_modules/@ton/sandbox/dist/blockchain/SmartContract.js:221:21)
```

Which is produced by of our [`dump(){:tact}`][dump] call above.

<Callout>

  Read more about sending messages to contracts in tests: [Send messages to contracts](#tests-send).

</Callout>

### State expectations with `expect()` [#tests-expect]

The integral parts of writing tests is ensuring that your expectations match the observed reality. For that, [Jest][jest] provides a function `expect(){:tact}`, which is used as follows:

1. First, an observed variable is provided.
2. Then, a specific method is called to check a certain property of that variable.

Here's a more involved example, which uses `expect(){:tact}` function to check that counter contract actually properly increases the counter:

```typescript
it('should increase counter', async () => {
  const increaseTimes = 3;
  for (let i = 0; i < increaseTimes; i++) {
    console.log(`increase ${i + 1}/${increaseTimes}`);

    const increaser = await blockchain.treasury('increaser' + i);

    const counterBefore = await simpleCounter.getCounter();
    console.log('counter before increasing', counterBefore);

    const increaseBy = BigInt(Math.floor(Math.random() * 100));
    console.log('increasing by', increaseBy);

    const increaseResult = await simpleCounter.send(
      increaser.getSender(),
      { value: toNano('0.05') },
      { $$type: 'Add', queryId: 0n, amount: increaseBy }
    );

    expect(increaseResult.transactions).toHaveTransaction({
      from: increaser.address,
      to: simpleCounter.address,
      success: true,
    });

    const counterAfter = await simpleCounter.getCounter();
    console.log('counter after increasing', counterAfter);

    expect(counterAfter).toBe(counterBefore + increaseBy);
  }
});
```

<Callout>

  See more test examples in the [Sandbox][sb] documentation:\
  [Testing flow (FunC)](https://github.com/ton-org/sandbox/blob/main/docs/testing-key-points.md)\
  [Writing tests for Tact](https://github.com/ton-org/sandbox/blob/main/docs/tact-testing-examples.md)

</Callout>

### Utility methods [#tests-jest-utils]

Test files generated by [Blueprint][bp] import `@ton/test-utils` library, which provides access to a number of additional helper methods for the result type of `expect(){:typescript}` [Jest][jest] function. Note, that regular methods like `toEqual(){:typescript}` are still there and ready to be used.

#### toHaveTransaction

The method `expect(…).toHaveTransaction(){:typescript}` checks that the list of transactions has a transaction matching certain properties you specify:

```typescript {2}
const res = await yourContractName.send(…);
expect(res.transactions).toHaveTransaction({
  // For example, let's check that a transaction to your contract was successful:
  to: yourContractName.address,
  success: true,
});
```

To know the full list of such properties, look at auto-completion options provided by your editor or IDE.

#### toEqualCell

The method `expect(…).toEqualCell(){:typescript}` checks equality of two [cells](/book/cells#cells):

```typescript {3}
expect(oneCell).toEqualCell(anotherCell);
```

#### toEqualSlice

The method `expect(…).toEqualSlice(){:typescript}` checks equality of two [slices](/book/cells#slices):

```typescript {3}
expect(oneSlice).toEqualSlice(anotherSlice);
```

#### toEqualAddress

The method `expect(…).toEqualAddress(){:typescript}` checks equality of two [addresses](/book/types#primitive-types):

```typescript {3}
expect(oneAddress).toEqualAddress(anotherAddress);
```

### Send messages to contracts [#tests-send]

To send messages to contracts, use `.send(){:typescript}` method on their TypeScript wrappers like so:

```typescript
// It accepts 3 arguments:
await yourContractName.send(
  // 1. sender of the message
  deployer.getSender(), // this is a default treasury, can be replaced

  // 2. value and (optional) bounce, which is true by default
  { value: toNano('0.5'), bounce: false },

  // 3. a message body, if any
  'Look at me!',
);
```

Message body can be a simple string, or an object specifying fields of the [Message](/book/structs-and-messages#messages) type:

```typescript {4-8}
await yourContractName.send(
  deployer.getSender(),
  { value: toNano('0.5') },
  {
    $$type: 'NameOfYourMessageType',
    field1: 0n, // bigint zero
    field2: 'yay',
  },
);
```

More often than not, it's important to store results of such sends, because they contain events occurred, transactions made and external messages sent:

```typescript
const res = await yourContractName.send(…);
// res.events — array of events occurred
// res.externals — array of external-out messages
// res.transactions — array of transactions made
```

With that, we can easily filter or check certain transactions:

```typescript
expect(res.transactions).toHaveTransaction(…);
```

### Observe the fees and values [#tests-fees]

[Sandbox][sb] provides a helper function `printTransactionFees(){:typescript}`, which pretty-prints all the values and fees that went into transactions provided. It is quite handy for observing the flow of [nanoToncoins](/book/integers#nanotoncoin).

To use it, modify imports from `@ton/sandbox` on top of the test file:

```typescript
import { Blockchain, SandboxContract, TreasuryContract, printTransactionFees } from '@ton/sandbox';
//                                                      ^^^^^^^^^^^^^^^^^^^^
```

Then, provide an array of transactions as an argument, like so:

```typescript
printTransactionFees(res.transactions);
```

To work with individual values of total fees or fees from compute and action [phases](https://docs.ton.org/learn/tvm-instructions/tvm-overview#transactions-and-phases), inspect each transaction individually:

```typescript {11,17,21}
// Storing the transaction handled by the receiver in a separate constant
const receiverHandledTx = res.transactions[1];
expect(receiverHandledTx.description.type).toEqual('generic');

// Needed to please TypeScript
if (receiverHandledTx.description.type !== 'generic') {
  throw new Error('Generic transaction expected');
}

// Total fees
console.log('Total fees: ', receiverHandledTx.totalFees);

// Compute fee
const computeFee = receiverHandledTx.description.computePhase.type === 'vm'
  ? receiverHandledTx.description.computePhase.gasFees
  : undefined;
console.log('Compute fee: ', computeFee);

// Action fee
const actionFee = receiverHandledTx.description.actionPhase?.totalActionFees;
console.log('Action fee: ', actionFee);

// Now we can do some involved checks, like limiting the fees to 1 Toncoin
expect(
  (computeFee ?? 0n)
  + (actionFee ?? 0n)
).toBeLessThanOrEqual(toNano('1'));
```

<Callout>

  [Sandbox][sb] has many more utility functions, which are often handy. For example, it provides `prettyLogTransaction(){:typescript}` and `prettyLogTransactions(){:typescript}`, which operate on a single or multiple transactions respectively and pretty-print flow of values between the addresses.

</Callout>

### Transactions with intentional errors [#tests-errors]

Sometimes it's useful to make negative tests, featuring intentional errors and throwing specific [exit codes](/book/exit-codes).

Example of such [Jest][jest] test closure in [Blueprint][bp]:

```typescript filename="tests/YourTestFileHere.spec.ts" {9,15}
it('throws specific exit code', async () => {
  // Send a specific message to our contract and store the results
  const res = await your_contract_name.send(
    deployer.getSender(),
    {
      value: toNano('0.5'), // value in nanoToncoins sent
      bounce: true,         // (default) bounceable message
    },
    'the message your receiver expects', // ← change it to yours
  );

  // Expect the transaction to our contract fail with a certain exit code
  expect(res.transactions).toHaveTransaction({
    to: your_contract_name.address,
    exitCode: 5, // ← change it to yours
  });
});
```

Note, that to track down transactions with a certain exit code, you only need to specify `exitCode` field in `toHaveTransaction(){:typescript}` method of `expect(){:typescript}`.

However, it's useful to narrow the scope by specifying the recipient address `to`, such that Jest would look only at the transaction caused by our message to the contract.

### Simulate passage of time [#tests-time]

The Unix time in local blockchain instances provided by [Sandbox][bp] starts at the moment of the creation of those in `beforeEach(){:typescript}` block.

```typescript {2}
beforeEach(async () => {
  blockchain = await Blockchain.create(); // ← here
  // ...
});
```

Previously, we've been warned not to modify the `beforeEach(){:typescript}` block unless we really need to. And now, to override the time and time travel a little, we do.

Let's add the following line by the end of it, setting `blockchain.now` explicitly to the time when deployment message was handled:
```typescript {3}
beforeEach(async () => {
  // ...
  blockchain.now = deployResult.transactions[1].now;
});
```

Now, we can manipulate time in out test clauses. For example, let's make a transaction one minute after the deployment and another one after two:

```typescript {2,4}
it('your test clause title', async () => {
  blockchain.now += 60; // 60 seconds late
  const res1 = await yourContractName.send(…);
  blockchain.now += 60; // another 60 seconds late
  const res2 = await yourContractName.send(…);
});
```

## Logging via `emit` [#logging]

A [global static function](/book/functions#global-static-functions) [`emit(){:tact}`](/ref/core-common#emit) sends a message to the outer world — it doesn't have a specific recipient.

This function is very handy for logging and analyzing data off-chain — one just has to look at [external messages](/book/external) produced by the contract.

### Logs in local Sandbox tests [#logging-local]

When deploying in the [Sandbox][sb], you may call [`emit(){:tact}`](/ref/core-common#emit) from a [receiver function](/book/contracts#receiver-functions) and then observe the list of sent [external messages](/book/external):

```typescript {9-10}
it('emits', async () => {
  const res = await simpleCounter.send(
    deployer.getSender(),
    { value: toNano('0.05') },
    'emit_receiver', // ← change to the message your receiver handles
  );

  console.log("Address of our contract: " + simpleCounter.address);
  console.log(res.externals); // ← here one would see results of emit() calls,
                              //   and all external messages in general
});
```

### Logs of a deployed contract [#logging-deployed]

Every transaction on TON Blockchain [contains `out_msgs`](https://docs.ton.org/develop/data-formats/transaction-layout#transaction) — a dictionary that holds the list of outgoing messages that were created while executing the transaction.

To see logs from [`emit(){:tact}`](/ref/core-common#emit) in that dictionary, look for external messages without a recipient. In various TON Blockchain explorers, such transactions will be marked as `external-out` with destination specified as `-` or `empty`.

Note, that some explorers deserialize the message body sent for you, while others don't. However, you can always [parse it yourself](#logging-parsing) locally.

### Parsing body of the emitted message [#logging-parsing]

Consider the following example:

```tact
// We have a Struct
struct Ballroom {
    meme: Bool;
    in: Int;
    theory: String;
}

// And a simple contract,
contract Bonanza {
    // which can receive a String message,
    receive("time to emit") {
        // emit a String
        emit("But to the Supes? Absolutely diabolical.".asComment());

        // and a Struct
        emit(Ballroom{meme: true, in: 42, theory: "Duh"}.toCell());
    }
}
```

Now, let's make a simple [test clause](#tests-structure) for the `Bonanza` contract:

```typescript /bonanza/
it('emits', async () => {
  const res = await bonanza.send(
    deployer.getSender(),
    { value: toNano('0.05') },
    'time to emit',
  );
});
```

There, the `res` object would contain the list of sent [external messages](/book/external) as its `externals` field. Let's access it to parse the first message sent via a call to [`emit(){:tact}`](/ref/core-common#emit) in Tact code (or _emitted_ for short):

```typescript /body/
it('emits', async () => {
  // ... prior code ...

  // We'll need only the body of the observed message:
  const firstMsgBody = res.externals[0].body;

  // Now, let's parse it, knowing that it's a text message.
  // NOTE: In a real-world scenario,
  //       you'd want to check that first or wrap this in a try...catch
  const firstMsgText = firstMsgBody.asSlice().loadStringTail();

  // "But to the Supes? Absolutely diabolical."
  console.log(firstMsgText);
});
```

To parse the second emitted message, we could manually use a bunch of `.loadSomething(){:typescript}` functions, but that's way too brittle — if the fields of the `Ballroom{:tact}` [Struct][struct] even change, you'd need to start all over. That could really backfire when you have a lot of tests written in that manner.

Fortunately, Tact compiler auto-generates TypeScript bindings (or wrappers) for the contracts, and it's really easy to re-use them in your test suite. Not only they have a wrapper of the contract you're testing, but they also export a bunch of helper functions to store or load [Structs][struct] and [Messages][message] defined in the contract. The latter will be named just like the [Structs][struct] and [Messages][message] are, but with the `load` prefix in front.

For example, in our case we'll need a function called `loadBallroom(){:typescript}`, for parsing a [`Slice{:tact}`][slice] into the `Ballroom{:tact}` [Struct][struct] in TypeScript. To import it, either type the name and let your IDE suggest auto-importing it for you, or take a look at the top of your test suite file — there should be a similar line:

```typescript
import { Bonanza } from '../wrappers/Bonanza';
//              ^ here you could import loadBallroom
```

With that, let's parse the second emitted message:

```typescript
it('emits', async () => {
  // ... prior code ...

  // We'll need only the body of the observed message:
  const secondMsgBody = res.externals[1].body;

  // Now, let's parse it, knowing that it's the Ballroom Struct.
  // NOTE: In a real-world scenario,
  //       you'd want to check that first or wrap this in a try...catch
  const secondMsgStruct = loadBallroom(secondMsgBody.asSlice());

  // { '$$type': 'Ballroom', meme: true, in: 42n, theory: 'Duh' }
  console.log(secondMsgStruct);
});
```

Mind you, that it's also possible to parse emitted messages of deployed contracts even outside of our test suite. You would just need to obtain the emitted message bodies and then use the auto-generated TypeScript bindings of Tact alongside the `@ton/core` library just like we did in those examples above.

## Handling bounced messages [#bounced]

When [sent](/book/send) with `bounce: true{:tact}`, messages can bounce back in case of errors. Make sure to write relevant [`bounced(){:tact}`](/book/bounced) message [receivers](/book/contracts#receiver-functions) and handle bounced messages gracefully:

```tact
bounced(msg: YourMessage) {
    // ...alright squad, let's bounce!...
}
```

Keep in mind that bounced messages in TON have only $224$ usable data bits in their message body and don't have any references, so one cannot recover much data from it. However, you still get to see whether the message has bounced or not, allowing you to create more robust contracts.

Read more about bounced messages and receivers: [Bounced messages](/book/bounced).

## Experimental lab setup [#lab]

If you're overwhelmed by the testing setup of [Blueprint][bp] or just want to test some things quickly, worry not — there is a way to set up a simple playground as an experimental lab to test your ideas and hypotheses.

<Steps>

### Create a new Blueprint project [#lab-1]

That will prevent pollution of your existing one with arbitrary code and tests.

The new project can be named anything, but I'll name it `Playground` to convey the right intent.

To create it, run the following command:

<Tabs items={['npm', 'yarn', 'pnpm']} defaultIndex="1">
  <Tabs.Tab>
    ```shell
    npm create ton -- tact-playground --type tact-empty --contractName Playground
    ```
  </Tabs.Tab>
  <Tabs.Tab>
    ```shell
    # recommended
    yarn create ton tact-playground --type tact-empty --contractName Playground
    ```
  </Tabs.Tab>
  <Tabs.Tab>
    ```shell
    pnpm create ton tact-playground --type tact-empty --contractName Playground
    ```
  </Tabs.Tab>
</Tabs>

Versions of [Blueprint][bp] starting with 0.20.0 automatically enable debug mode in `wrappers/` for new contracts, so we only have to adjust the testing suite and prepare our `Playground` contract for testing.

### Update the test suite [#lab-2]

Move into the newly created `tact-playground/` project and in the `tests/Playground.spec.ts`, change the `"should deploy"{:tact}` test closure to the following:

```typescript filename="tests/Playground.spec.ts"
it('plays', async () => {
  const res = await playground.send(
    deployer.getSender(),
    { value: toNano('0.5') }, // ← here you may increase the value in nanoToncoins sent
    'plays',
  );

  console.log("Address of our contract: " + playground.address);
  console.log(res.externals); // ← here one would see results of emit() calls
});
```

### Modify the contract [#lab-3]

Replace the code in `contracts/playground.tact` with the following:

```tact filename="contracts/playground.tact" {4-6}
import "@stdlib/deploy";

contract Playground with Deployable {
    receive("plays") {
        // NOTE: write your test logic here!
    }
}
```

The basic idea of this setup is to place the code you want to test into the [receiver function](/book/contracts#receiver-functions) responding to the [string](/book/types#primitive-types) message `"plays"{:tact}`.

Note, that you can still write any valid Tact code outside of that [receiver](/book/contracts#receiver-functions). But in order to test it you'll need to write related test logic inside of it.

### Let's test! [#lab-4]

With that, our experimental lab setup is complete. To execute that single test we've prepared for our `Playground` contract, run the following:

```shell
yarn test -t plays
```

From now on, to test something you only need to modify the contents of the tested [receiver function](/book/contracts#receiver-functions) of your Tact contract file and re-run the command above. Rinse and repeat that process until you've tested what you wanted to test.

For simplicity and cleaner output's sake, you may add a new field to `scripts` in your `package.json`, such that you'll only need to run `yarn lab{:shell}` to build and test in one.

On Linux or macOS, it would look like:

```json filename="package.json" {3}
{
  "scripts": {
    "lab": "blueprint build 1>/dev/null && yarn test -t plays"
  }
}
```

And here's how it may look on Windows:

```json filename="package.json" {3-4}
{
  "scripts": {
    "build": "blueprint build | out-null",
    "lab": "yarn build && yarn test -t plays"
  }
}
```

To run:

```shell
yarn lab
```

</Steps>

[dump]: /ref/core-debug#dump
[struct]: /book/structs-and-messages#structs
[message]: /book/structs-and-messages#messages
[cell]: /book/cells#cells
[slice]: /book/cells#slices

[tg]: https://t.me/tactlang
[bp]: https://github.com/ton-org/blueprint
[sb]: https://github.com/ton-org/sandbox
[jest]: https://jestjs.io


## deploy.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/deploy.mdx)
# Deploy

Tact Deployer is a small library that integrates with [TON Verifier](https://verifier.ton.org) that allows you to deploy your contracts safely using your favorite wallet without needing to manage keys or deploy contracts manually. Tact Deployer also automatically verifies your contract's source code and you can be sure that your compiler is not compromised.

## Requirements

Your contract MUST have the `Deployer` trait from the `@stdlib/deploy` package to be able to use Tact Deployer.

## Installation

To add Tact Deployer to your project, just use `yarn`:

```bash
yarn add @tact-lang/deployer
```

## How to use

When you build your smart contracts using Tact, it produces a package (*.pkg) file that has all the required information about the built smart contract. To deploy your smart contract, you need to create a deployer instance, pass your package file to it and provide initial data for your contract.

```typescript
import * as fs from 'fs';
import * as path from 'path';
import { Address, contractAddress } from "ton";
import { SampleTactContract } from "./output/sample_SampleTactContract";
import { prepareTactDeployment } from "@tact-lang/deployer";

// Parameters
let testnet = true;                                 // Flag for testnet or mainnet
let packageName = 'sample_SampleTactContract.pkg';  // Name of your package to deploy
let outputPath = path.resolve(__dirname, 'output'); // Path to output directory
let owner = Address.parse('<put_address_here>');    // Our sample contract has an owner
let init = await SampleTactContract.init(owner);    // Create initial data for our contract

// Calculations
let address = contractAddress(0, init);     // Calculate contract address. MUST match with the address in the verifier
let data = init.data.toBoc();               // Create init data
let pkg = fs.readFileSync(                  // Read package file
    path.resolve(outputPath, packageName)
);

// Prepare deploy
let link = await prepareTactDeployment({ pkg, data, testnet });

// Present a deployment link and contract address
console.log('Address: ' + address.toString({ testOnly: testnet }));
console.log('Deploy link: ' + link);
```

After following this link you will be able to deploy and verify your smart contract.

## exit-codes.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/exit-codes.mdx)
# Exit Codes

import { Callout } from 'nextra/components'

<Callout type="warning" emoji="⚠️">
  THis page is under re-construction as per [#106](https://github.com/tact-lang/tact-docs/issues/106). All anchor links (`#`) may change in the future!
</Callout>

An exit code is a $16$-bit unsigned integer which ranges between $0$ to $65535$ (or $2_{16} - 1$).

Codes from $0$ to $127$ are allocated for FunC (TVM), $128$ to $255$ for Tact. The range from $256$ to $65535$ is free for developer-defined exit codes.

List of pre-allocated exit codes:

Exit Code  | phase              | Description
:--------- | :----------------- | --------------------------------------------------------------------------------------------------------------------------
$0$        | [Compute phase][c] | Standard successful execution exit code
$2$        | [Compute phase][c] | Stack underflow. Last op-code consumed more elements than there are on the stacks
$3$        | [Compute phase][c] | Stack overflow. More values have been stored on a stack than allowed by this version of TVM
$4$        | [Compute phase][c] | Integer overflow. Integer does not fit into −2<sup>256</sup> ≤ x < 2<sup>256</sup> or a division by zero has occurred
$5$        | [Compute phase][c] | Integer out of expected range
$6$        | [Compute phase][c] | Invalid opcode. Instruction is unknown in the current TVM version
$7$        | [Compute phase][c] | Type check error. An argument to a primitive is of an incorrect value type
$8$        | [Compute phase][c] | Cell overflow. Writing to builder is not possible since after operation there would be more than 1023 bits or 4 references
$9$        | [Compute phase][c] | Cell underflow. Read from slice primitive tried to read more bits or references than there are
$10$       | [Compute phase][c] | Dictionary error. Error during manipulation with dictionary (hashmaps)
$13$       | [Compute phase][c] | Out of gas error. Thrown by TVM when the remaining gas becomes negative
$-14$      | [Compute phase][c] | It means out of gas error, same as $13$. Negative, because it cannot be faked
$32$       | [Action phase][a]  | Action list is invalid. Set during action phase if c5 register after execution contains unparsable object
$34$       | [Action phase][a]  | Action is invalid or not supported. Set during action phase if current action cannot be applied
$37$       | [Action phase][a]  | Not enough TON. Message sends too much TON (or there is not enough TON after deducting fees)
$38$       | [Action phase][a]  | Not enough extra-currencies
$128$      | Tact (Compiler)    | Null reference exception — compiler expects an integer or cell but a null value has been passed
$129$      | Tact (Compiler)    | Invalid serialization prefix — if there is any inconsistency with the previous op-code check, this exit code will be thrown
$130$      | Tact (Compiler)    | Invalid incoming message — no suitable operation is found
$131$      | Tact (Compiler)    | Constraints error
$132$      | Tact (Compiler)    | Access denied — someone other than the owner sent a message to the contract
$133$      | Tact (Compiler)    | Contract stopped — a message has been sent to a stopped contract
$134$      | Tact (Compiler)    | Invalid argument — invalid Base64 string
$135$      | Tact (Compiler)    | Code of a contract was not found — false flag for a dictionary call
$136$      | Tact (Compiler)    | Invalid Address — Non $267$-bit Address or invalid chain id (other than 0 or -1)
$137$      | Tact (Compiler)    | Masterchain support is not enabled for this contract

[c]: https://docs.ton.org/learn/tvm-instructions/tvm-overview#compute-phase
[a]: https://docs.ton.org/learn/tvm-instructions/tvm-overview#transactions-and-phases

Q: **Where to observe the list of all auto-generated exit codes in your project?**\
A: The Tact Compiler collects all exit codes at the end of a *.md file and you can track them in the directory along
the path "./ProjectFolder/build/ProjectName/tact_ProjectName.md"

Q: **How to observe a thrown exit code?**\
A: In Tact, it's not wise to print the transactions to see the results because they are not easy to read. If you want to see the exit code of a transaction,
use the below template in your Typescript local tests:

```typescript
const sender = await blockchain.treasury('sender');
const result = await contractName.send(sender.getSender(), { value: toNano('0.05'), }, { transactionData });

expect(result.transactions).toHaveTransaction(
    { from: sender.address, to: contractName.address, exitCode: YOUR_DESIRED_EXIT_CODE }
);
```
* First line defines the sender.
* Second line sends the transaction.
* In the third line, you check if the result has a transaction from sender to your contract with your desired exit code.

## Compute phase

### $0$: Successful execution [#0]

This exit code means that the Compute phase of the transaction was completed successfully.

### $4$: Integer overflow [#4]

In TVM, integer can be in the range -2<sup>256</sup> < x < 2<sup>256</sup>.
If the value during the calculation went beyond this range, then 4 exit code is thrown.

Example:

```tact
self.id = 1; // force not to ignore it by using storage variables
repeat(256) {
    self.id = 2 * self.id;
}
```

### $5$: Integer out of expected range [#5]

If the integer value went beyond the expected range, then 5 exit code is thrown.
For example, if a negative value was used in the .store_uint() function. In Tact, there are some other new situations such as:\
1- As you know, you can define more limited integers in Tact (integers with less than 257 bits).
If you try to store a number in this kind of integers and the number doesn't fit to this limited range, you will face this exit code.\
2- according to ```storeUint(self: Builder, value: Int, bits: Int)``` function, it's not possible to use ```storeUint(0, 257)``` because ```0 ≤ bits ≤ 256```.

Example:

```tact
// option 1 -> id: Int as uint32
self.id = 1; // force not to ignore it by using storage variables
repeat(32) {
    self.id = 2 * self.id;
}

// option 2 -> according to storeUint(self: Builder, value: Int, bits: Int) function, it's not possible to use storeUint(0, 1024) because 0 ≤ bits ≤ 256
let s: Slice = beginCell().storeUint(0, 257).asSlice();
```

### $8$: Cell overflow [#8]
A cell has the capacity to store 1023 bits of data and 4 references to other cells.
If you try to write more than 1023 bits or more than 4 references, 8 exit code is thrown.

Example:

```tact
// according to storeUint(self: Builder, value: Int, bits: Int) function, it's not possible to use storeUint(0, 1024) because 0 ≤ bits ≤ 256
let s: Slice = beginCell().storeUint(0, 256).storeUint(0, 256).storeUint(0, 256).storeUint(0, 256).asSlice();
```

### $9$: Cell underflow [#9]

If you try to read more data from a slice than it contains, then 9 exit code is thrown.

Example:

```tact
let s: Slice = emptySlice();
self.id = s.loadUint(1); // force not to ignore it by using storage variables
```

### $13$: Out of gas error [#13]

If there isn't enough TON to handle compute phase, this error is thrown.

During processing, the NOT operation is applied to this value, which changes this value to -14. This is done so that this exit code cannot be faked using the throw function, since all such functions accept only positive values for the exit code as it was discussed previously.

Example:

```tact
repeat(10000) {
    self.id += 1;
}
```

## Action phase

### $34$: Action is invalid or not supported [#34]

This exit code is responsible for most of the errors when working with actions: invalid message, incorrect action, and so on.

Example:

```tact
nativeSendMessage(emptyCell(), 0);
```

### $37$: Not enough TON [#37]

It means that there isn't enough TON to send the specified amount of it.

Example:

```tact
send(SendParameters{to: context().sender, value: ton("10")});
```

## Tact (Compiler)

### $130$: Invalid incoming message [#130]

When you send a message to a contract, the first 32 bits of message body is the op code. It determines the operation that must be done.
In FunC, if no op code is found, 0xffff will be thrown. In Tact, 130 exit code will be thrown.

Example:

1. First, define an empty contract like below:

```tact
contract Fireworks {}
```

2. Then, send a message to this contract. Because no suitable operation is found, you will get this exit code.

### $132$: Access denied [#132]

First, you should import and inherit from Ownable Trait. After it, your contract will have an owner.
You can ask for a check by calling ```self.requireOwner();``` in your functions. It will ensure that only the owner can send message to your contract.

Example:

```tact
import "@stdlib/deploy";
import "@stdlib/ownable";

message FakeLaunch {

}

contract Fireworks with
    Deployable,
    Ownable,
{
    owner: Address;

    init(){
        self.owner = sender();
    }

    receive(msg: FakeLaunch){
        self.requireOwner();
    }
}

fun requireOwner() {
        nativeThrowUnless(132, sender() == self.owner);
}
```

### $133$: Contract stopped [#133]

The stoppable trait allows to stop the contract.
If you send a message to a stopped contract, and the contract asks for a check by running ```self.requireNotStopped();```, this exit code will be thrown.
In the current version of Tact, 40368 exit code will be thrown instead of 133.

Example:

```tact
import "@stdlib/deploy";
import "@stdlib/ownable";
import "@stdlib/stoppable";

message FakeLaunch {}

contract Fireworks with
    Deployable,
    Ownable,
    Stoppable,
{
    owner: Address;
    stopped: Bool;

    init() {
        self.owner = sender();
        self.stopped = false;
    }

    receive(msg: FakeLaunch) {
        self.stopped = true;
        self.requireNotStopped();
    }
}

fun requireNotStopped() {
    require(!self.stopped, "Contract stopped");
}
```

### $134$: Invalid argument [#134]

This will be thrown by the below FunC function(in the last part of a bunch of if conditions). This function reads something from Base64.

If the input characters don't fit into base64 chars, you will encounter this exit code.

Example:

```tact
let code: Slice = beginCell().storeUint(0, 8).asSlice().fromBase64();
// 0 is not a valid ASCII code so it cannot be converted to Base64
```

### $135$: Code of a contract was not found [#135]

It will check the return flag of a search on the dictionary keys.

Example:

```tact
// copy & paste the below line in wrapper file(../build/ContractName/tact_ContractName.ts) instead of the second line of ContractName_init() function - this is a dictionary containing another smart contract code which leads to 135 exit code
// const __system = Cell.fromBase64('te6cckECIwEAB1EAAQHAAQEFodSXAgEU/wD0pBP0vPLICwMCAWIPBAIBIA0FAgEgDAYCAUgLBwIBIAkIAHWs3caGrS4MzmdF5eotqc1vCmiu5ihm5iaqaEpGiYzo5syoyYptJmhuDSoKamwmziqo5spNKy0NLapwQAIRrt7tnm2eNijAIAoAAiQAEbCvu1E0NIAAYACVu70YJwXOw9XSyuex6E7DnWSoUbZoJwndY1LStkfLMi068t/fFiOYJwIFXAG4BnY5TOWDquRyWyw4JwnZdOWrNOy3M6DpZtlGbopIAhG+KO7Z5tnjYowgDgACIwN+0AHQ0wMBcbCjAfpAASDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IhUUFMDbwT4YQL4Yts8VRTbPPLggts8IBIQARbI+EMBzH8BygBVQBEA8lBUINdJgQELuvLgiCDXCwoggQT/uvLQiYMJuvLgiM8WWCDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IjPFgEgbpUwcAHLAY4eINdJgQELuvLgiCDXCwoggQT/uvLQiYMJuvLgiM8W4hL0AAHIgQEBzwDJAczJ7VQC9gGSMH/gcCHXScIflTAg1wsf3iCCEIQwhou6jtYw0x8BghCEMIaLuvLggfpAASDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IgBgQEB1wD6QAEg10mBAQu68uCIINcLCiCBBP+68tCJgwm68uCIQzBsE+AgghAF6DTmuhkTAvyO0DDTHwGCEAXoNOa68uCB+kABINdJgQELuvLgiCDXCwoggQT/uvLQiYMJuvLgiAH6QAEg10mBAQu68uCIINcLCiCBBP+68tCJgwm68uCIEmwS4CCCEHKDsbi6jpQw0x8BghByg7G4uvLggdQBMds8f+DAAAHXScEhsJF/4HAXFATw+EFvJBAjXwMkbrOOF4ERTVNxxwWSMX+ZJSBu8tCAWMcF4vL0mSaBEU0CxwXy9OL4ACDIAYIQcoOxuFjLH8zJI9s8kyBus48kICBu8tCAbyIxggkxLQAjfwNwQwNtbds8IG7y0IBvIjBSQNs86FtwgwYmA39VMG1tFh4dFQEE2zweADSBAQH0hG+lwP+dIG7y0IABIG7y0IBvAuBbbQLQNPhBbyQQI18D+ENUECfbPAGBEU0CcFnIcAHLAXMBywFwAcsAEszMyfkAyHIBywFwAcsAEsoHy//J0CDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IgixwXy9ANwgEBwVSBtbW3bPH8YHgDaAtD0BDBtAYIA6ksBgBD0D2+h8uCHAYIA6ksiAoAQ9BfIAcj0AMkBzHABygBAA1kg10mBAQu68uCIINcLCiCBBP+68tCJgwm68uCIzxYBINdJgQELuvLgiCDXCwoggQT/uvLQiYMJuvLgiM8WyQKi+EFvJDAyJ26zjheBEU1ToccFkjF/mSggbvLQgFjHBeLy9JkpgRFNAscF8vTiJYEBASRZ9AxvoZIwbd9ujo8TXwNwgEBwVSBtbW3bPAHjDQF/HhoC+iTBFI72FYEBAVQQNCBulTBZ9FowlEEz9BTiA6QBggr68IChJnAGyFmCEAXoNOZQA8sfASDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IjPFgEg10mBAQu68uCIINcLCiCBBP+68tCJgwm68uCIzxbJQVBDMHABbW3bPOMOHhsD6jBTQds8IG6OhDAk2zzeIG7y0IBvIjFwUEOAQAPIVSCCEIQwhotQBMsfWCDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IjPFoEBAc8AASDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IjPFsl/VTBtbds8AR0cHgA0gQEB9IxvpcD/nSBu8tCAASBu8tCAbwLgW20ANgGBAQH0eG+lwP+dIG7y0IABIG7y0IBvAuBbbQHKyHEBygFQBwHKAHABygJQBSDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IjPFlAD+gJwAcpoI26zkX+TJG6z4pczMwFwAcoA4w0hbrOcfwHKAAEgbvLQgAHMlTFwAcoA4skB+wAfAJh/AcoAyHABygBwAcoAJG6znX8BygAEIG7y0IBQBMyWNANwAcoA4iRus51/AcoABCBu8tCAUATMljQDcAHKAOJwAcoAAn8BygACyVjMArjtRNDUAfhj0gAB4wL4KNcLCoMJuvLgifpAASDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IgB+kABINdJgQELuvLgiCDXCwoggQT/uvLQiYMJuvLgiBIC0QHbPCIhAAgBbW1wAPr6QAEg10mBAQu68uCIINcLCiCBBP+68tCJgwm68uCIAfpAASDXSYEBC7ry4Igg1wsKIIEE/7ry0ImDCbry4IgB+kAh1wsBwwCOHQEg10mBAQu68uCIINcLCiCBBP+68tCJgwm68uCIkjFt4gH0BNQB0IEBAdcAMBUUQzBsFUhhij0=');
let ctx: Context = context();
let fireworks_init: StateInit = initOf Fireworks(0);
```

### $136$: Invalid address [#136]

In TON, all addresses are 267 bits. If you violate this rule, you will face this exit code.

Currently, TON only supports two chain id. 0 for basechain and -1 for masterchain. If you address isn't from basechain, 136 exit code will be thrown.

Example:

```tact
// fun newAddress(chain: Int, hash: Int): Address;
// creates a new address from chain and hash values.
let zeroAddress: Address = newAddress(1, 0); // invalid chain zero address
```

### $137$: Masterchain support is not enabled for this contract [#137]

Currently, TON only supports two chain id. 0 for basechain and -1 for masterchain.

Tact only supports basechain and if you address is from masterchain, 137 exit code will be thrown.

Example:

```tact
// fun newAddress(chain: Int, hash: Int): Address;
// creates a new address from chain and hash values.
let zeroAddress: Address = newAddress(-1, 0); // masterchain zero address
```


## expressions.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/expressions.mdx)
# Expressions

import { Callout } from 'nextra/components'

Every operator in Tact forms an expression, but there's much more to uncover as Tact offers a wide range of expressive options to choose from.

## Literals

Literals represent values in Tact. These are fixed values—not variables—that you _literally_ provide in your code. All literals in Tact are expressions themselves.

You can also call [extension functions](/book/functions#extension-function) defined on certain [primitive types][p] corresponding to literals right on the literal values:

```tact
// Calling toString() defined for Int on a integer literal:
42.toString();

// Calling asComment() defined for String on a string literal:
"Tact is awesome!".asComment();
```

### Integer literals

Integer literals can be written in [decimal](/book/integers#decimal) (base $10$), [hexadecimal](/book/integers#hexadecimal) (base $16$), [octal](/book/integers#octal) (base $8$) and [binary](/book/integers#binary) (base $2$) notations:

* A [_decimal_ integer](/book/integers#decimal) literal is a sequence of digits ($\mathrm{0 - 9}$).

* A leading $\mathrm{0x}$ (or $\mathrm{0X}$) indicates a [hexadecimal integer](/book/integers#hexadecimal) literal. They can include digits ($\mathrm{0 - 9}$) and the letters $\mathrm{a - f}$ and $\mathrm{A - F}$. Note, that the case of a character does not change its value. Therefore: $\mathrm{0xa}$ = $\mathrm{0xA}$ = $10$ and $\mathrm{0xf}$ = $\mathrm{0xF}$ = $15$.

* A leading $\mathrm{0o}$ (or $\mathrm{0O}$) indicates a [octal integer](/book/integers#octal) literals. They can include only the digits $\mathrm{0 - 7}$.

* A leading $\mathrm{0b}$ (or $\mathrm{0B}$) indicates a [binary integer](/book/integers#binary) literal. THey can only include the digits $0$ and $1$.

<Callout type="warning" emoji="⚠️">
  Be wary that in Tact integer literals with a leading $0$ are still considered decimals, unlike in JavaScript/TypeScript where leading $0$ indicates an octal!
</Callout>

Some examples of integer literals:

```tact
// decimal, base 10:
0, 42, 1_000, 020

// hexadecimal, base 16:
0xABC, 0xF, 0x0011

// octal, base 8:
0o777, 0o001

// binary, base 2:
0b01111001_01101111_01110101_00100000_01100001_01110010_01100101_00100000_01100001_01110111_01100101_01110011_01101111_01101101_01100101
```

Read more about integers and [`Int{:tact}`](/book/integers) type on the dedicated page: [Integers](/book/integers).

### Boolean literals

The [`Bool{:tact}`](/book/types#booleans) type has only two literal values: `true{:tact}` and `false{:tact}`.

```tact
true == true;
true != false;
```

Read more about booleans and [`Bool{:tact}`](/book/types#booleans) type in the dedicated chapter: [Booleans](/book/types#booleans).

### String literals

A string literal is zero or more characters enclosed in double (`"`) quotation marks. All string literals are objects of [`String{:tact}`][p] type.

```tact
"foo";
"1234";
```

Tact strings support a range of [escape sequences](https://en.wikipedia.org/wiki/Escape_sequence) starting with a backslash `\\` character:

* `\\{:tact}` — literal backslash
* `\"{:tact}` — double quote
* `\n{:tact}` — newline
* `\r{:tact}` — carriage return
* `\t{:tact}` — tab
* `\v{:tact}` — vertical tab
* `\b{:tact}` — backspace
* `\f{:tact}` — form feed
* `\x00{:tact}` through `\xFF{:tact}` — [code point](https://en.wikipedia.org/wiki/Code_point), must be exactly two hex digits long
* `\u0000{:tact}` through `\uFFFF{:tact}` — [Unicode code point][unicode], must be exactly four hex digits long
* `\u{0}{:tact}` through `\u{FFFFFF}{:tact}` — [Unicode code point][unicode], can be from $1$ to $6$ hex digits long

[unicode]: https://en.wikipedia.org/wiki/Unicode#Codespace_and_code_points

```tact
// \\
"escape \\ if \\ you \\ can \\";

// \"
"this \"literally\" works";

// \n
"line \n another line";

// \r
"Shutters \r Like \r This \r One";

// \t
"spacing \t granted!";

// \v
"those \v words \v are \v aligned";

// \b
"rm\b\bcreate!";

// \f
"form \f feed";

// \x00 - \xFF
"this \x22literally\x22 works"; // \x22 represents a double quote

// \u0000 - \uFFFF
"danger, \u26A1 high voltage \u26A1"; // \u26A1 represents the ⚡ emoji

// \u{0} - \u{FFFFFF}
"\u{1F602} LOL \u{1F602}"; // \u{1F602} represents the 😂 emoji
```

<Callout>

  Read more about strings and [`String{:tact}`][p] type:\
  [Primitive types in the Book][p]\
  [Strings and StringBuilders in the Reference](/ref/core-strings)

</Callout>

### `null` literal

The `null{:tact}` value is written with a `null{:tact}` literal. It's **not** an [identifier](#identifiers) and doesn't refer to any object. It's also **not** an instance of a [primitive type][p]. Instead, `null{:tact}` represents a lack of identification and the intentional absence of any value.

```tact
let var: Int? = null; // variable, which can hold null value
var = 42;
if (var != null) {
    var!! + var!!;
}
```

Read more about working with `null{:tact}` on the dedicated page: [Optionals](/book/optionals).

## Identifiers

An identifier is a sequence of characters in the code that _identifies_ a [variable](/book/statements#let), [constant](/book/constants), [map](/book/maps) and a [function](/book/functions), as well as a [Struct][s], [Message][m], [contract](/book/contracts), [trait](/book/types#traits), or their fields and methods. Identifiers are case-sensitive and not quoted.

In Tact, identifiers can contain latin lowercase letters (`a-z`), latin uppercase letters (`A-Z`), underscores (`_`) and digits ($\mathrm{0 - 9}$), but may not start with a digit. An identifier differs from a [string](#string-literals) in that a string is data, while an identifier is part of the code.

Note, that when identifiers for [primitive types][p] start with an uppercase letter. Used-defined [composite types](/book/types#composite-types), such as [Structs][s] and [Messages][m] also must be capitalized.

## Instantiation

You can create instances of the following types:

* [Structs][s]
* [Messages][m]

```tact
struct StExample {
    fieldInit: Int = 1;
    fieldUninit: Int;
}

fun example() {
    // Instance with default value of fieldInit
    StExample{ fieldUninit: 2 };

    // Instance with both fields set
    StExample{
        fieldInit: 0,
        fieldUninit: 2, // trailing comma is allowed
    };
}
```

## Field access

You can directly access fields of the following types:

* [Structs][s]
* [Messages][m]

```tact
struct StExample {
    fieldInit: Int = 1;
    fieldUninit: Int;
}

fun example(): Int {
    let struct: StExample = StExample{ fieldUninit: 2 }; // instantiation

    struct.fieldInit;          // access a field
    return struct.fieldUninit; // return field value from the function
}
```

## Extension function call

[Extension functions](/book/functions#extension-function) are defined only on specific types. They can be called similar to method calls in many other languages:

```tact
42.toString(); // toString() is a stdlib function that is defined on Int type
```

## Static function call

Anywhere in the function body, a global [static function](/book/functions#global-static-functions) or an internal function of a [contract](/book/contracts) can be called:

```tact
contract ExampleContract {
    receive() {
        now(); // now() is a static function of stdlib
        let expiration: Int = now() + 1000; // operation and variable declaration
        expiration = self.answerQuestion(); // internal function
    }
    fun answerQuestion(): Int {
        return 42;
    }
}
```

## `initOf`

Expression `initOf{:tact}` computes initial state (`StateInit{:tact}`) of a [contract](/book/contracts):

```tact
//                     argument values for the init() function of the contract
//                     ↓   ↓
initOf ExampleContract(42, 100); // returns a Struct StateInit{}
//     ---------------
//     ↑
//     name of the contract
//     ↓
//     ---------------
initOf ExampleContract(
    42,  // first argument
    100, // second argument, trailing comma is allowed
);
```

Where `StateInit{:tact}` is a built-in [Struct][s], that consists of:

Field  | Type               | Description
:----- | :----------------- | :----------
`code` | [`Cell{:tact}`][cell] | initial code of the [contract](/book/contracts) (the compiled bytecode)
`data` | [`Cell{:tact}`][cell] | initial data of the [contract](/book/contracts) (arguments of `init(){:tact}` function of the contract)

[p]: /book/types#primitive-types
[cell]: /book/cells#cells
[s]: /book/structs-and-messages#structs
[m]: /book/structs-and-messages#messages


## external.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/external.mdx)
import { Callout } from "nextra-theme-docs";

# External Messages

<Callout type="warning" emoji="⚠️">
  External message support must be enabled explicitly in the project configuration.
  Without enabling it compilation would fail.
</Callout>

External messages are those that don't have a sender and can be sent by anyone in the world. External messages are good tools for integrating with off-chain systems or for the general maintenance of contracts. Handling external messages is different from handling internal messages. In this section, we will cover how to handle external messages.

## How External Messages are Different

External messages are different from internal messages in the following ways:

### Contracts Pay for Gas Usage Themselves

When processing internal messages, the sender usually pays for gas usage. When processing external messages, the contract pays for gas usage. This means that you need to be careful with gas usage in external messages. You should always test the gas usage of your contracts and verify that everything is working as intended.

### Messages Have to Be Accepted Manually

External messages are not accepted automatically. You need to accept them manually. This is done by calling the `acceptMessage` function. If you don't call the `acceptMessage` function, the message will be rejected. This is done to prevent the spamming of external messages.

### 10k Gas Limit Before Message Acceptance

10k gas is a very small limit, and Tact itself can consume a sizable amount of gas before it even reaches your code. You should always test the gas usage of your contracts and verify that everything is working as intended.

<Callout type="info" emoji="📚️">
  The 10k gas limit for external messages is based on the parameter we set by the
  validator for the whole blockchain of the `gas_limit` field. You can take
  the reference here:
    - https://docs.ton.org/develop/smart-contracts/guidelines/accept#external-messages
    - https://docs.ton.org/develop/howto/blockchain-configs#param-20-and-21

  </Callout>

### Unbounded Gas Usage After Message Acceptance

After you accept the gas, the contract can use as much gas as it wants. This is done to allow the contract to carry out any kind of processing. You should always test the gas usage of your contracts and verify that everything is working as intended, and avoid possible vulnerabilities that could drain the contract balance.

### No Context Available

When processing an external message, the `context` and `sender` functions are not available. This is because there is no context available for external messages. This means that you can't use the `context` and `sender` functions in external messages. You need to carefully test your contract to make sure that it doesn't use the `context` and `sender` functions.

## Enable External Messages Support

To enable external messages support, please enable it in the project configuration file:

```json
{
  "options": {
    "external": true
  }
}
```

## External receivers

External receivers are defined the same way as internal ones, but using the `external` keyword instead of `receive`:

```tact
contract SampleContract {
    external("Check Timeout") {

        // Check for contract timeout
        require(self.timeout > now(), "Not timeouted");

        // Accept message
        acceptMessage();

        // Timeout processing
        self.onTimeouted();
    }
}
```


## func.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/func.mdx)
# Compatibility with FunC

Tact itself compiles to FunC and maps all its entities directly to various FunC and TL-B types.

## Convert types

[Primitive types](/book/types#primitive-types) in Tact are directly mapped to FunC ones.

All rules about copying variables are the same. One of the big differences is that there are no visible mutation operators in Tact and most [`Slice{:tact}`](/book/cells#slices) operations mutate variables in place.

## Convert serialization

Serialization of [Structs](/book/structs-and-messages#structs) and [Messages](/book/structs-and-messages#messages) in Tact is automatic, unlike FunC where you need to define serialization logic manually.

Tact's auto-layout algorithm is greedy. This means that it takes the next variable, calculates its size, and tries to fit it into a current cell. If it doesn't fit, it creates a new cell and continues. All inner structs for auto-layout are flattened before allocation.

All optional types are serialized as `Maybe` in TL-B, except for [`Address{:tact}`](/book/types#primitive-types).

There is no support for `Either` since it does not define what to pick during serialization in some cases.

### Examples

```tact
// _ value1:int257 = SomeValue;
struct SomeValue {
    value1: Int; // Default is 257 bits
}
```

```tact
// _ value1:int256 value2:uint32 = SomeValue;
struct SomeValue {
    value1: Int as int256;
    value2: Int as uint32;
}
```

```tact
// _ value1:bool value2:Maybe bool = SomeValue;
struct SomeValue {
    value1: Bool;
    value2: Bool?;
}
```

```tact
// _ cell:^cell = SomeValue;
struct SomeValue {
    cell: Cell; // Always stored as a reference
}
```

```tact
// _ cell:^slice = SomeValue;
struct SomeValue {
    cell: Slice; // Always stored as a reference
}
```

```tact
// _ value1:int256 value2:int256 value3:int256 ^[value4:int256] = SomeValue;
struct SomeValue {
    value1: Int as int256;
    value2: Int as int256;
    value3: Int as int256;
    value4: Int as int256;
}
```

```tact
// _ value1:int256 value2:int256 value3:int256 ^[value4:int256] flag:bool = SomeValue;
struct SomeValue {
    value1: Int as int256;
    value2: Int as int256;
    value3: Int as int256;
    flag: Bool; // Flag is written before value4 to avoid auto-layout to allocate it to the next cell
    value4: Int as int256;
}
```

```tact
// _ value1:int256 value2:int256 value3:int256 ^[value4:int256 flag:bool] = SomeValue;
struct SomeValue {
    value1: Int as int256;
    value2: Int as int256;
    value3: Int as int256;
    value4: Int as int256;
    flag: Bool;
}
```

```tact
// _ value1:int256 value2:^TailString value3:int256 = SomeValue;
struct SomeValue {
    value1: Int as int256;
    value2: String;
    value3: Int as int256;
}
```

## Convert received messages to `op` operations

Tact generates a unique `op` for every received typed message, but it can be overwritten.

The following code in FunC:

```func
() recv_internal(int msg_value, cell in_msg_cell, slice in_msg) impure {
    ;; incoming message code...

    ;; Receive MessageWithGeneratedOp message
    if (op == 1180414602) {
        ;; code...
    }

    ;; Receive MessageWithOverwrittenOP message
    if (op == 291) {
        ;; code...
    }

}
```

Becomes this in Tact:

```tact
message MessageWithGeneratedOp {
    amount: Int as uint32;
}

message(0x123) MessageWithOverwrittenOP {
    amount: Int as uint32;
}

contract Contract {
    // Contract Body...

    receive(msg: MessageWithGeneratedOp) {
        // code...
    }

    receive(msg: MessageWithOverwrittenOP) {
        // code...
    }

}
```

## Convert `get`-methods

You can express everything except `list-style-lists` in Tact that would be compatible with FunC's `get`-methods.

### Primitive return type

If a `get`-method returns a primitive in FunC, you can implement it the same way in Tact.

The following code in FunC:

```func
int seqno() method_id {
    return 0;
}
```

Becomes this in Tact:

```tact
get fun seqno(): Int {
    return 0;
}
```

### Tensor return types

In FunC there is a difference between tensor type `(int, int){:func}` and `(int, (int)){:func}`, but for TVM there are no differences, they all represent a stack of two integers.

To convert the tensor that returned from a FunC `get`-method, you need to define a [Struct](/book/structs-and-messages#structs) that has the same field types as the tensor and in the same order.

The following code in FunC:

```func
(int, slice, slice, cell) get_wallet_data() method_id {
    return ...;
}
```

Becomes this in Tact:

```tact
struct JettonWalletData {
    balance: Int;
    owner: Address;
    master: Address;
    walletCode: Cell;
}

contract JettonWallet {
    get fun get_wallet_data(): JettonWalletData {
        return ...;
    }
}
```

### Tuple return type

In FunC if you are returning a tuple, instead of a tensor you need to follow the process for a tensor type, but define the return type of a `get`-method as optional.

The following code in FunC:

```func
[int, int] get_contract_state() method_id {
    return ...;
}
```

Becomes this in Tact:

```tact
struct ContractState {
    valueA: Int;
    valueB: Int;
}

contract StatefulContract {
    get fun get_contract_state(): ContractState? {
        return ...;
    }
}
```

### Mixed tuple and tensor return types

When some of the tensors are a tuple, you need to define a struct as in previous steps and the tuple one must be defined as a separate [Struct](/book/structs-and-messages#structs).

The following code in FunC:

```func
(int, [int, int]) get_contract_state() method_id {
    return ...;
}
```

Becomes this in Tact:

```tact
struct ContractStateInner {
    valueA: Int;
    valueB: Int;
}

struct ContractState {
    valueA: Int;
    valueB: ContractStateInner;
}

contract StatefulContract {
    get fun get_contract_state(): ContractState {
        return ...;
    }
}
```

### Arguments mapping

Conversion of `get`-methods arguments is straightforward. Each argument is mapped _as-is_ to FunC one, and each tuple is mapped to a [Struct](/book/structs-and-messages#structs).

The following code in FunC:

```func
(int, [int, int]) get_contract_state(int arg1, [int,int] arg2) method_id {
    return ...;
}
```

Becomes this in Tact:

```tact
struct ContractStateArg2 {
    valueA: Int;
    valueB: Int;
}

struct ContractStateInner {
    valueA: Int;
    valueB: Int;
}

struct ContractState {
    valueA: Int;
    valueB: ContractStateInner;
}

contract StatefulContract {
    get fun get_contract_state(arg1: Int, arg2: ContractStateArg2): ContractState {
        return ContractState{
            valueA: arg1,
            valueB: ContractStateInner{
                valueA: arg2.valueA,
                valueB: arg2.valueB, // trailing comma is allowed
            }, // trailing comma is allowed
        };
    }
}
```


## functions.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/functions.mdx)
# Functions and their types

Functions in Tact could be defined in different ways:

* Global static function
* Extension functions
* Mutable functions
* Native functions
* Receiver functions
* Getter functions

All functions, except for [receiver functions](#receiver-functions) can have a trailing comma in their definitions (parameter lists) and calls (argument lists):

```tact
fun foo(
    a: Int, // trailing comma in parameter lists is allowed
) {}

fun bar() {
    foo(
        5, // trailing comma in argument lists is allowed too!
    );
}
```

## Global static functions

You can define global function anywhere in your program:

```tact
fun customPow(a: Int, c: Int): Int {
  let res: Int = 1;
  repeat(c) {
    res *= a;
  }
  return res;
}
```

## Virtual and abstract functions

You can allow the contract inheriting a [traits](/book/types#traits) to modify an internal function, if it has the `virtual{:tact}` keyword, using `override{:tact}`. The function can be also marked as `abstract{:tact}`, in which case the inheriting contract has to define its implementation:

```tact
trait FilterTrait with Ownable {
    // Virtual functions can be overridden by users of this trait
    virtual fun filterMessage(): Bool {
        return sender() != self.owner;
    }

    abstract fun specialFilter(): Bool;
}

contract Filter with FilterTrait {
    // Overriding default behavior of the FilterTrait
    override fun filterMessage(): Bool {
        return true;
    }

    override fun specialFilter(): Bool {
        return true;
    }
}
````

## Extension function

Extension functions allow you to implement extensions for any possible type.

> **Warning**
> The name of the first argument MUST be named `self` and the type of this argument is the type you are extending.

```tact
extends fun customPow(self: Int, c: Int): Int {
    let res: Int = 1;
    repeat(c) {
        res *= self;
    }
    return res;
}
```

## Mutable functions

Mutable functions are performing mutation of a value replacing it with an execution result. To perform mutation, the function must change the `self` value.

```tact
extends mutates fun customPow(self: Int, c: Int) {
    let res: Int = 1;
    repeat(c) {
        res *= self;
    }
    self = res;
}
```

## Native functions

Native functions are direct bindings of FunC functions:

> **Note**
> Native functions could be also mutable and extension ones.

```tact
@name(store_uint)
native storeUint(s: Builder, value: Int, bits: Int): Builder;

@name(load_int)
extends mutates native loadInt(self: Slice, l: Int): Int;
```

## Receiver functions

Receiver functions are special functions that are responsible for receiving messages in contracts and could be defined only within a contract or trait.

```tact
contract Treasure {
    // This means that this contract can receive the comment "Increment" and this function would be called for such messages
    receive("Increment") {
        self.counter += 1;
    }
}
```

## Getter Functions

Getter functions define getters on smart contracts and can be defined only within a contract or trait.

```tact
contract Treasure {
    get fun counter(): Int {
        return self.counter;
    }
}
```


## import.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/import.mdx)
import { Callout } from 'nextra-theme-docs'

# Importing code

Tact allows you to import Tact and [FunC](https://docs.ton.org/develop/func/overview) code — any given `.tact` or `.fc`/`.func` file can be imported into your project using an `import{:tact}` keyword.

Additionally, Tact compiler has a versatile set of standard libraries, which come bundled in, but not included right away, see [Standard libraries overview](/ref/standard-libraries).

<Callout type="warning" emoji="⚠️">
  NOTE: All imported code is combined together with yours, so it's important to avoid name collisions and always double-check the sources!
</Callout>

## Import Tact code

It's possible to import any Tact code using the `import{:tact}` statement and providing a relative path to the target `.tact` file like so:

```tact
import "./relative/path/to/the/target/tact/file.tact";
```

Specifying parent directories (`../`) is also possible:

```tact
import "../subfolder/imported/file.tact";
```

## Import FunC code

It's possible to import code written in FunC code directly just as it's done with Tact code imports:

```tact
// Relative import
import "./relative/path/to/the/target/func/file.fc";

// Specifying parent directories
import "../subfolder/imported/func/file.fc";
```

But in order to use functions from such file, one has to declare them as `native` functions first. For example, when standard library [@stdlib/dns](/ref/stdlib-dns) uses a `dns.fc` FunC file, it maps FunC functions to Tact ones like so:

```tact
// FunC code located in a file right next to the current Tact one:
import "./dns.fc";

// Mapping function signatures from FunC to Tact:
@name(dns_string_to_internal)
native dnsStringToInternal(str: String): Slice?;
```

## Standard libraries

See [Standard libraries overview](/ref/standard-libraries).


## index.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/index.mdx)
# Book overview

import { Cards, Steps } from 'nextra/components'

Welcome to **The Tact Book** section (or just **The Book**), — an introductory book about the Tact language.

Here are its main contents:

<Steps>

### Cheatsheets

[Cheatsheets](/book/cs/from-func) are quick rundowns on Tact syntax and idioms with comparison to other blockchain languages, such as FunC (also on TON) and Solidity (Ethereum blockchain). Use those to transition to Tact as swiftly as possible.

<Cards>
  <Cards.Card
    arrow
    title="Go to the first cheatsheet"
    href="/book/cs/from-func"
  />
</Cards>

### Book

[**The Tact Book**](/book/types) is a cohesive and streamlined sequence of educational materials about Tact. In general, it assumes that you’re reading it in sequence from front to back. Later parts build on concepts in earlier parts, and earlier parts might not delve into details on a particular topic but will revisit the topic in a later part.

Additionally, there are many references to the Language section of the documentation, where many primitives of the language are described in much more fine detail. Additionally, whenever there's an existing explanation of the broader TON concept in the main TON documentation, this Book tries to reference it as well.

Book also assumes that you’ve written code in another programming language but doesn’t make any assumptions about which one. We’ve tried to make the material broadly accessible to those from a wide variety of programming backgrounds. We don’t spend a lot of time talking about what programming _is_ or how to think about it. If you’re entirely new to programming, you would be better served by reading a book that specifically provides an introduction to programming.

<Cards>
  <Cards.Card
    arrow
    title="Proceed to the Book itself"
    href="/book/types"
  />
</Cards>

</Steps>


## integers.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/integers.mdx)
# Integers

import { Callout } from 'nextra/components'

Arithmetic in smart contracts on TON is always done with integers and never with floating-point numbers since the floats are [unpredictable](https://learn.microsoft.com/en-us/cpp/build/why-floating-point-numbers-may-lose-precision). Therefore, the big accent goes on integers and their handling.

The only primitive number type in Tact is `Int{:tact}`, for $257$-bit signed integers.\
It's capable of storing integers between $-2^{256}$ and $2^{256} - 1.$

## Notation

Tact supports various ways of writing primitive values of `Int{:tact}` as [integer literals](/book/expressions#integer-literals).

Most of the notations allow adding underscores (`_`) in-between digits, except for:
* Representations in strings, as seen in [nano-tons](#nano-tons) case.
* Decimal numbers written with a leading zero $0.$ Their use is generally discouraged, see [below](#decimal).

Additionally, several underscores in a row as in $4\_\_2$, or trailing underscores as in $42\_$ are **not** allowed.

### Decimal

Most common and most used way of representing numbers, using the [decimal numeral system](https://en.wikipedia.org/wiki/Decimal): $123456789.$\
You can use underscores (`_`) to improve readability: $123\_456\_789$ is equal to $123456789.$

<Callout type="warning" emoji="⚠️">
  Alternatively, you can prefix the number with one $0$, which prohibits use of underscores and only allows decimal digits: $0123 = 123.$
  Note, that using this notation with leading zero is **strongly discouraged** due to possible confusion with octal integer literals in TypeScript, which is often used alongside Tact to develop and test contracts.
</Callout>

### Hexadecimal

Represent numbers using [hexadecimal numeral system](https://en.wikipedia.org/wiki/Hexadecimal), denoted by the $\mathrm{0x}$ (or $\mathrm{0X}$) prefix: $\mathrm{0xFFFFFFFFF}.$\
Use underscores (`_`) to improve readability: $\mathrm{0xFFF\_FFF\_FFF}$ is equal to $\mathrm{0xFFFFFFFFF}.$

### Octal

Represent numbers using [octal numeral system](https://en.wikipedia.org/wiki/Octal), denoted by the $\mathrm{0o}$ (or $\mathrm{0O}$) prefix: $\mathrm{0o777777777.}$\
Use underscores (`_`) to improve readability: $\mathrm{0o777\_777\_777}$ is equal to $\mathrm{0o777777777}.$

### Binary

Represent numbers using [binary numeral system](https://en.wikipedia.org/wiki/Binary_number), denoted by the $\mathrm{0b}$ (or $\mathrm{0B}$) prefix: $\mathrm{0b111111111.}$\
Use underscores (`_`) to improve readability: $\mathrm{0b111\_111\_111}$ is equal to $\mathrm{0b111111111}.$

### NanoToncoin

Arithmetic with dollars requires two decimal places after the dot — those are used for the cents value. But how would we represent the number \$$1.25$ if we're only able to work with integers? The solution is to work with _cents_ directly. This way, \$$1.25$ becomes $125$ cents. We simply memorize that the two rightmost digits represent the numbers after the decimal point.

Similarly, working with Toncoin, the main currency of TON Blockchain, requires nine decimal places instead of the two. One can say that nanoToncoin is the $\frac{1}{10^{9}}\mathrm{th}$ of the Toncoin.

Therefore, the amount of $1.25$ Toncoin, which can be represented in Tact as [`ton("1.25"){:tact}`](/ref/core-comptime#ton), is actually the number $1250000000$. We refer to such numbers as _nanoToncoin(s)_ (or _nano-ton(s)_) rather than _cents_.

## Serialization

When encoding `Int{:tact}` values to persistent state (fields of [contracts](/book/contracts) and [traits](/book/types#traits)), it's usually better to use smaller representations than $257$-bits to reduce [storage costs](https://docs.ton.org/develop/smart-contracts/fees#storage-fee). Usage of such representations is also called "serialization" due to them representing the native [TL-B][tlb] types which TON Blockchain operates on.

The persistent state size is specified in every declaration of a state variable after the `as{:tact}` keyword:

```tact
contract SerializationExample {
    // persistent state variables
    oneByte: Int as int8 = 0; // ranges from -128 to 127 (takes 8 bit = 1 byte)
    twoBytes: Int as int16;   // ranges from -32,768 to 32,767 (takes 16 bit = 2 bytes)

    init() {
        // needs to be initialized in the init() because it doesn't have the default value
        self.twoBytes = 55*55;
    }
}
```

Integer serialization is also available for the fields of [Structs](/book/structs-and-messages#structs) and [Messages](/book/structs-and-messages#messages), as well as in key/value types of [maps](/book/maps):

```tact
struct StSerialization {
    martin: Int as int8;
}

message MsgSerialization {
    seamus: Int as int8;
    mcFly: map<Int as int8, Int as int8>;
}
```

Motivation is very simple:
* Storing $1000$ $257$-bit integers in state [costs](https://docs.ton.org/develop/smart-contracts/fees#how-to-calculate-fees) about $0.184$ TON per year.
* Storing $1000$ $32$-bit integers only costs $0.023$ TON per year by comparison.

### Serialization types

Name             | [TL-B][tlb]                 | Inclusive range             | Space taken
:--------------: | :-------------------------: | :-------------------------: | :------------------------:
`uint8{:tact}`   | [`uint8`][tlb-builtin]      | $0$ to $2^{8} - 1$          | $8$ bits = $1$ byte
`uint16{:tact}`  | [`uint16`][tlb-builtin]     | $0$ to $2^{16} - 1$         | $16$ bits = $2$ bytes
`uint32{:tact}`  | [`uint32`][tlb-builtin]     | $0$ to $2^{32} - 1$         | $32$ bits = $4$ bytes
`uint64{:tact}`  | [`uint64`][tlb-builtin]     | $0$ to $2^{64} - 1$         | $64$ bits = $8$ bytes
`uint128{:tact}` | [`uint128`][tlb-builtin]    | $0$ to $2^{128} - 1$        | $128$ bits = $16$ bytes
`uint256{:tact}` | [`uint256`][tlb-builtin]    | $0$ to $2^{256} - 1$        | $256$ bits = $32$ bytes
`int8{:tact}`    | [`int8`][tlb-builtin]       | $-2^{7}$ to $2^{7} - 1$     | $8$ bits = $1$ byte
`int16{:tact}`   | [`int16`][tlb-builtin]      | $-2^{15}$ to $2^{15} - 1$   | $16$ bits = $2$ bytes
`int32{:tact}`   | [`int32`][tlb-builtin]      | $-2^{31}$ to $2^{31} - 1$   | $32$ bits = $4$ bytes
`int64{:tact}`   | [`int64`][tlb-builtin]      | $-2^{63}$ to $2^{63} - 1$   | $64$ bits = $8$ bytes
`int128{:tact}`  | [`int128`][tlb-builtin]     | $-2^{127}$ to $2^{127} - 1$ | $128$ bits = $16$ bytes
`int256{:tact}`  | [`int256`][tlb-builtin]     | $-2^{255}$ to $2^{255} - 1$ | $256$ bits = $32$ bytes
`int257{:tact}`  | [`int257`][tlb-builtin]     | $-2^{256}$ to $2^{256} - 1$ | $257$ bits = $32$ bytes + $1$ bit
`coins{:tact}`   | [`VarUInteger 16`][varuint] | $0$ to $2^{120} - 1$        | between $4$ and $124$ bits, [see below](#serialization-coins)

### Variable `coins` type [#serialization-coins]

In Tact, `coins{:tact}` is an alias to [`VarUInteger 16`][varuint] in [TL-B][tlb] representation, i.e. it takes a variable bit length depending on the optimal number of bytes needed to store the given integer and is commonly used for storing [nanoToncoin](/book/integers#nanotoncoin) amounts.

This serialization format consists of two [TL-B fields](https://docs.ton.org/develop/data-formats/tl-b-language#field-definitions):

* `len`, a $4$-bit unsigned big-endian integer storing the byte length of the value provided
* `value`, a $8 * len$-bit unsigned big-endian representation of the value provided

That is, integers serialized as `coins{:tact}` occupy between $4$ and $124$ bits ($4$ bits for `len` and $0$ to $15$ bytes for `value`) and have values in the inclusive range from $0$ to $2^{120} - 1$.

Examples:

```tact
struct Scrooge {
    // len: 0000, 4 bits (always)
    // value: none!
    // in total: 4 bits
    a: Int as coins = 0; // 0000

    // len: 0001, 4 bits
    // value: 00000001, 8 bits
    // in total: 12 bits
    b: Int as coins = 1; // 0001 00000001

    // len: 0010, 4 bits
    // value: 00000001 00000010, 16 bits
    // in total: 20 bits
    c: Int as coins = 258; // 0010 00000001 00000010

    // len: 1111, 4 bits
    // value: hundred twenty 1's in binary
    // in total: 124 bits
    d: Int as coins = pow(2, 120) - 1; // hundred twenty 1's in binary
}
```

<Callout>

  Read more on serialization here: [Compatibility with FunC](/book/func#convert-serialization)

</Callout>

## Operations

All runtime calculations with numbers are done at 257-bits, so [overflows](https://en.wikipedia.org/wiki/Integer_overflow) are quite rare. Nevertheless, if any math operation overflows, an exception will be thrown, and the transaction will fail. You could say that Tact's math is safe by default.

Note, that there is no problem with mixing variables of [different state sizes](#serialization) in the same calculation. At runtime they are all the same type no matter what — $257$-bit signed, so overflows won't happen then.

However, this can still lead to **errors** in the [compute phase](https://docs.ton.org/learn/tvm-instructions/tvm-overview#compute-phase) of the transaction. Consider the following example:

```tact
import "@stdlib/deploy";

contract ComputeErrorsOhNo with Deployable {
    oneByte: Int as uint8; // persistent state variable, max value is 255

    init() {
        self.oneByte = 255; // initial value is 255, everything fits
    }

    receive("lets break it") {
        let tmp: Int = self.oneByte * 256; // no runtime overflow
        self.oneByte = tmp; // whoops, tmp value is out of the expected range of oneByte
    }
}
```

Here, `oneByte` is serialized as a [`uint8`](#serialization-types), which occupies only one byte and ranges from $0$ to $2^{8} - 1$, which is $255$. And when used in runtime calculations no overflow happens and everything is calculated as a $257$-bit signed integers. But the very moment we decide to store the value of `tmp` back into `oneByte` we get an error with the [exit code 5](/book/exit-codes#5), which states the following: `Integer out of the expected range`.

<Callout type="warning" emoji="⚠️">
  Therefore, be **very** careful with numbers and always double-check calculations when using serialization.
</Callout>

[tlb]: https://docs.ton.org/develop/data-formats/tl-b-language
[tlb-builtin]: https://docs.ton.org/develop/data-formats/tl-b-language#built-in-types
[varuint]: https://docs.ton.org/develop/data-formats/msg-tlb#varuinteger-n


## lifecycle.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/lifecycle.mdx)
# Message Lifecycle

There are several stages of message processing by a contract, there are more of them, but we would focus on the most important ones:

## Receive Phase

This phase combines multiple low-level phases. 

It starts by adding a **message value to the contract balance**. The value of an incoming message is the maximum price that a contract can pay for gas to process this message. The contract can overwrite this limit, but it is not recommended and is suitable only for advanced developers since it could lead to a contract being drained. 1 million of gas is the maximum amount that a contract can spend in a single contract which equals 0.4 TON for basechain (currently). If the message value is zero then execution is aborted.

Then some (usually small) amount of nanotons gets subtracted from the contract balance for storage. This means that you can't perfectly predict balance changes and have to adjust your code to this instability.

Then it deploys a contract if it is not deployed yet and the message contains the init package. If the init package isn't present, it will be ignored.

## Compute Phase

This phase executes the code of a smart contract and produces a list of actions or an exception. Currently, only two types of actions are supported: **send message** and **reserve**.

Sending a message could use a fixed value or a dynamic value like **remaining value of a message** - the remaining value of the incoming message. Sending a message could be with a flag `SendIgnoreErrors` that would ignore errors during message sending and would continue to the next action. This flag is useful if you have multiple actions. When sending a message with some value, it first subtracts this value from the incoming value and only then from the contract balance (before processing).

## Action Phase

Actions are executed in sequence, but bear in mind:
**EXCEPTION DURING PROCESSING ACTIONS WOULDN'T REVERT THE TRANSACTION**

For example, if you subtract 1 ton from a customer's balance and then send an invalid message, that could lead to a situation when the customer's balance is subtracted, but he wouldn't receive it.


## maps.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/maps.mdx)
# Maps

import { Callout } from 'nextra/components'

The [composite type](/book/types#composite-types) `map<K, V>{:tact}` is used as a way to associate keys of type `K{:tact}` with corresponding values of type `V{:tact}`.

For example, `map<Int, Int>{:tact}` uses [`Int{:tact}`][int] type for its keys and values:

```tact
struct IntToInt {
    counters: map<Int, Int>;
}
```

## Allowed types

Allowed key types:

* [`Int{:tact}`][int]
* [`Address{:tact}`][p]

Allowed value types:

* [`Int{:tact}`][int]
* [`Bool{:tact}`](/book/types#booleans)
* [`Cell{:tact}`][cell]
* [`Address{:tact}`][p]
* [Struct](/book/structs-and-messages#structs)
* [Message](/book/structs-and-messages#messages)

## Operations

### Declare, `emptyMap()` [#emptymap]

As a [local variable](/book/statements#let), using `emptyMap(){:tact}` function of standard library:

```tact
let fizz: map<Int, Int> = emptyMap();
let fizz: map<Int, Int> = null; // identical to the previous line, but less descriptive
```

As a [persistent state variable](/book/contracts#variables):

```tact
contract Example {
    fizz: map<Int, Int>; // Int keys to Int values
    init() {
        self.fizz = emptyMap(); // redundant and can be removed!
    }
}
```

Note, that [persistent state variables](/book/contracts#variables) of type `map<K, V>{:tact}` are initialized empty by default and don't need default values or an initialization in the [`init(){:tact}` function](/book/contracts#init-function).

### Set values, `.set()` [#set]

To set or replace the value under a key call the `.set(){:tact}` [method](/book/functions#extension-function), which is accessible for all maps.

```tact
// Empty map
let fizz: map<Int, Int> = emptyMap();

// Setting a couple of values under different keys
fizz.set(7, 7);
fizz.set(42, 42);

// Overriding one of the existing key-value pairs
fizz.set(7, 68); // key 7 now points to value 68
```

### Get values, `.get()` [#get]

To check if a key is found in the map by calling the `.get(){:tact}` [method](/book/functions#extension-function), which is accessible for all maps. This will return `null{:tact}` if the key is missing, or the value if the key is found.

```tact
// Empty map
let fizz: map<Int, Int> = emptyMap();

// Setting a value
fizz.set(68, 0);

// Getting the value by its key
let gotButUnsure: Int? = fizz.get(68);          // returns Int or null, therefore the type is Int?
let mustHaveGotOrErrored: Int = fizz.get(68)!!; // explicitly asserting that the value must not be null,
                                                // which may crush at runtime if the value is, in fact, null

// Alternatively, we can check for the key in the if statement
if (gotButUnsure != null) {
    // Hooray, let's use !! without fear now and cast Int? to Int
    let definitelyGotIt: Int = fizz.get(68)!!;
} else {
    // Do something else...
}
```

### Delete entries, `.del()` [#del]

To delete a single key-value pair (single entry), use the `.del(){:tact}` [method](/book/functions#extension-function). It returns `true{:tact}` in the case of successful deletion and `false{:tact}` otherwise.

```tact
// Empty map
let fizz: map<Int, Int> = emptyMap();

// Setting a couple of values under different keys
fizz.set(7, 123);
fizz.set(42, 321);

// Deleting one of the keys
let deletionSuccess: Bool = fizz.del(7); // true, because map contained the entry under key 7
fizz.del(7);                             // false, because map no longer has an entry under key 7

// Note, that assigning the `null` value to the key when using the `.set()` method
//   is equivalent to calling `.del()`, although such approach is much less descriptive
//   and is generally discouraged:
fizz.set(42, null); // the entry under key 42 is now deleted
```

To delete all the entries from the map, re-assign the map using the `emptyMap(){:tact}` function:

```tact
// Empty map
let fizz: map<Int, Int> = emptyMap();

// Setting a couple of values under different keys
fizz.set(7, 123);
fizz.set(42, 321);

// Deleting all of the entries at once
fizz = emptyMap();
fizz = null; // identical to the previous line, but less descriptive
```

With this approach all previous entries of the map are completely discarded from the contract even if the map was declared as its persistent state variable. As a result, assigning maps to `emptyMap(){:tact}` **does not** inflict any hidden or sudden [storage fees](https://docs.ton.org/develop/smart-contracts/fees#storage-fee).

### Check if empty, `.isEmpty()` [#isempty]

The `.isEmpty(){:tact}` [method](/book/functions#extension-function) on maps returns `true{:tact}` if the map is empty and `false{:tact}` otherwise:

```tact
let fizz: map<Int, Int> = emptyMap();

if (fizz.isEmpty()) {
    dump("Empty maps are empty, duh!");
}

// Note, that comparing the map to `null` behaves the same as `.isEmpty()` method,
// although such direct comparison is much less descriptive and is generally discouraged:
if (fizz == null) {
    dump("Empty maps are null, which isn't obvious");
}
```

### Convert to a `Cell`, `.asCell()` [#ascell]

Use `.asCell(){:tact}` [method](/book/functions#extension-function) on maps to convert all their values to a [`Cell{:tact}`][cell] type. Be mindful, that [`Cell{:tact}`][cell] type is able to store up to 1023 bits, so converting larger maps to the Cell will result in error.

As an example, this method is useful for sending small maps directly in the body of the reply:

```tact
contract Example {
    // Persistent state variables
    fizz: map<Int, Int>; // our map

    // Constructor (initialization) function of the contract
    init() {
        // Setting a bunch of values
        self.fizz.set(0, 3);
        self.fizz.set(1, 14);
        self.fizz.set(2, 15);
        self.fizz.set(3, 926);
        self.fizz.set(4, 5_358_979_323_846);
    }

    // Internal message receiver, which responds to empty messages
    receive() {
        // Here we're converting the map to a Cell and making a reply with it
        self.reply(self.fizz.asCell());
    }
}
```

### Traverse over entries [#traverse]

To iterate over map entries there is a [`foreach{:tact}`](/book/statements#foreach-loop) loop statement:

```tact
// Empty map
let fizz: map<Int, Int> = emptyMap();

// Setting a couple of values under different keys
fizz.set(42, 321);
fizz.set(7, 123);

// Iterating over in a sequential order: from the smallest keys to the biggest ones
foreach (key, value in fizz) {
    dump(key); // will dump 7 on the first iteration, then 42 on the second
}
```

Read more about it: [`foreach{:tact}` loop in Book→Statements](/book/statements#foreach-loop).

Note, that it's also possible to use maps as simple arrays if you define a `map<Int, V>{:tact}` with an [`Int{:tact}`][int] type for the keys, any allowed `V{:tact}` type for values and keep track of the number of items in the separate variable:

```tact
contract Iteration {
    // Persistent state variables
    counter: Int as uint32;    // counter of map entries, serialized as a 32-bit unsigned
    record: map<Int, Address>; // Int to Address map

    // Constructor (initialization) function of the contract
    init() {
        self.counter = 0; // Setting the self.counter to 0
    }

    // Internal message receiver, which responds to a String message "Add"
    receive("Add") {
        // Get the Context Struct
        let ctx: Context = context();
        // Set the entry: counter Int as a key, ctx.sender Address as a value
        self.record.set(self.counter, ctx.sender);
        // Increase the counter
        self.counter += 1;
    }

    // Internal message receiver, which responds to a String message "Send"
    receive("Send") {
        // Loop until the value of self.counter (over all the self.record entries)
        let i: Int = 0; // declare usual i for loop iterations
        while (i < self.counter) {
           send(SendParameters{
                bounce: false,              // do not bounce back this message
                to: self.record.get(i)!!,   // set the sender address, knowing that key i exists in the map
                value: ton("0.0000001"),    // 100 nanoToncoins (nano-tons)
                mode: SendIgnoreErrors,     // send ignoring errors in transaction, if any
                body: "SENDING".asComment() // String "SENDING" converted to a Cell as a message body
            });
            i += 1; // don't forget to increase the i
        }
    }

    // Getter function for obtaining the value of self.record
    get fun map(): map<Int, Address> {
        return self.record;
    }

    // Getter function for obtaining the value of self.counter
    get fun counter(): Int {
        return self.counter;
    }
}
```

It's often useful to set an upper-bound restriction on such maps, so that you [don't hit the limits](#limits-and-drawbacks).

<Callout type="warning" emoji="⚠️">

  Note, that manually keeping track of number of items or checking the length of such map is very error-prone and generally discouraged. Instead, try to wrap your map into the [Struct](/book/structs-and-messages#structs) and define [extension functions](/book/functions#extension-function) on it. See example in the Cookbook: [How to emulate an array using a map wrapped in a Struct](/cookbook/data-structures#array).

</Callout>

<Callout>

  This example was adapted from [howardpen9/while-example-tact](https://github.com/howardpen9/while-example-tact/blob/de5807fcd20dba5f6a3748d112511477fb22bfcc/contracts/awesome.tact#L19C10-L19C10).

  See other examples of map usage in the Cookbook:\
  [How to emulate a stack using a map wrapped in a Struct](/cookbook/data-structures#stack)\
  [How to emulate a circular buffer using a map wrapped in a Struct](/cookbook/data-structures#circular-buffer)

</Callout>

## Serialization

It's possible to do [integer serialization](/book/integers#serialization-types) of map keys, values or both to [preserve space and reduce storage costs](/book/integers#serialization):

```tact
struct SerializedMapInside {
    // Both keys and values here would be serialized as 8-bit unsigned integers,
    // thus preserving the space and reducing storage costs:
    countersButCompact: map<Int as uint8, Int as uint8>;
}
```

<Callout>

  Read about other serialization options: [Compatibility with FunC](/book/func#convert-serialization).

</Callout>

## Limits and drawbacks

While maps can be convenient to work with on a small scale, they cause a number of issues if the number of items is unbounded and map can significantly grow in size:

* As the upper bound of the smart contract state size is around $65\,000$ items of type [`Cell{:tact}`][cell], it constrains the storage limit of maps to be about $30\,000$ key-value pairs for the whole contract.

* The more entries you have in a map, the bigger [compute fees](https://docs.ton.org/develop/howto/fees-low-level#computation-fees) you'll get. Thus, working with large maps makes compute fees tough to predict and manage.

* Using a large map in a single contract doesn't allow to distribute its workload. Hence, it can make the overall performance much worse compared to  using a smaller map and a bunch of interacting smart contracts.

To resolve such issues you can set an upper-bound restriction on a map as a constant and check against it every time you're setting a new value to the map:

```tact
contract Example {
    // Declare a compile-time constant upper-bound for our map
    const MaxMapSize: Int = 42;

    // Persistent state variables
    arr: map<Int, Int>; // "array" of Int values as a map
    arrLength: Int = 0; // length of the "array", defaults to 0

    // Internal function for pushing an item to the end of the "array"
    fun arrPush(item: Int) {
        if (self.arrLength >= self.MaxMapSize) {
            // Do something, stop the operation, for example
        } else {
            // Proceed with adding new item
            self.arr.set(self.arrLength, item);
            self.arrLength += 1;
        }
    }
}
```

If you still need a large map or an unbound (infinitely large) map, it's better to architect your smart contracts according to the [asynchronous and actor-based model of TON blockchain](https://docs.ton.org/learn/overviews/ton-blockchain). That is, to use contract sharding and essentially make the whole blockchain a part of your map(s).

{/*
  TODO: Add reference to sharding page as per: https://github.com/tact-lang/tact-docs/issues/155
*/}

[p]: /book/types#primitive-types
[int]: /book/integers
[cell]: /book/cells#cells


## masterchain.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/masterchain.mdx)
# Masterchain

import { Callout } from 'nextra-theme-docs'

<Callout type="warning" emoji="⚠️">

  Masterchain addresses are treated as invalid unless the `masterchain` option in the [configuration file](/book/config) is set to `true{:json}`.

</Callout>

In TON Blockchain, a special chain called ["masterchain"](https://docs.ton.org/learn/overviews/ton-blockchain#masterchain-blockchain-of-blockchains) is used to synchronize message routing and transaction execution, so that nodes in the network can fix a particular point in a multi-chain state and reach a consensus about that state.

Masterchain stores the [network configuration](/ref/core-advanced#getconfigparam) and the final state of all [workchains](https://docs.ton.org/learn/overviews/ton-blockchain#workchain-blockchain-with-your-own-rules). It carries fundamental protocol information, including current settings, a list of active validators and their stakes, active workchains, and associated [shardchains](https://docs.ton.org/develop/blockchain/shards). Most importantly, it maintains a record of the latest block hashes for all workchains and shardchains, enforcing consensus across the network.

## How contract is protected from masterchain [#protection]

Tact enforces all contracts to use the [basechain](https://docs.ton.org/develop/blockchain/shards), which is the default workchain with ID $0$. This is done to prevent masterchain addresses from being used in the contract.

Any attempts to point to masterchain or otherwise interact with it without [enabling masterchain support](#enable-support) throw an exception with [exit code 137](/book/exit-codes#137): `Masterchain support is not enabled for this contract`.

That is, accidental deployments to the masterchain, receiving messages from masterchain accounts, sending messages to such accounts, and using masterchain addresses or its chain ID ($-1$) are all prohibited by default.

## Enabling masterchain support in compilation options [#support]

<Callout type="warning" emoji="⚠️">

Most contracts don't need to be deployed on a masterchain or have any interactions on a masterchain. That's because the masterchain is primarily used for voting or storing libraries. If you don't need to partake in those things, you don't need to enable masterchain support.

</Callout>

If you really do need masterchain support, the simplest and recommended approach is to modify a [`tact.config.json`](/book/config) file in the root of your project (or create it if it didn't exist yet), and [set the `masterchain` property to `true{:json}`](/book/config#options-masterchain).

If you're working on a [Blueprint][bp]-based project, you can enable masterchain support in the compilation configs of your contracts, which are located in a directory named `wrappers/`:

```typescript filename="wrappers/YourContractName.compile.ts" {7}
import { CompilerConfig } from '@ton/blueprint';

export const compile: CompilerConfig = {
  lang: 'tact',
  target: 'contracts/your_contract_name.tact',
  options: {
    masterchain: true, // ← that's the stuff!
  }
};
```

However, [`tact.config.json`](/book/config) may still be used in [Blueprint][bp] projects. In such cases values specified in [`tact.config.json`](/book/config) act as default unless modified in the `wrappers/`.

[bp]: https://github.com/ton-org/blueprint


## message-mode.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/message-mode.mdx)
import { Callout } from 'nextra/components'

# Message `mode`

As it was previously mentioned, messages are sent with the `mode` param of a struct `SendParameters{:tact}`. It's an [`Int{:tact}`][int] value, which is combined from base modes and optional flags, which are also [`Int{:tact}`][int] values.

It's possible to use raw [`Int{:tact}`][int] values and manually provide them for the `mode`, but for your convenience there's a set of constants which you may use to construct the compound `mode` with ease. Take a look at the following tables for more information on base modes and optional flags.

## Base modes

Mode value | Constant name                 | Description
---------: | :---------------------------- | -----------
$0$        | -                             | Ordinary message (default).
$64$       | `SendRemainingValue{:tact}`   | Carry all the remaining value of the inbound message in addition to the value initially indicated in the new message.
$128$      | `SendRemainingBalance{:tact}` | Carry all the remaining balance of the current smart contract instead of the value originally indicated in the message.

## Optional flags

Flag value | Constant name                   | Description
---------: | :------------------------------ | -----------
$+1$       | `SendPayGasSeparately{:tact}`   | Pay forward fees separately from the message value.
$+2$       | `SendIgnoreErrors{:tact}`       | Ignore any errors arising while processing this message during the action phase.
$+16$      | `SendBounceIfActionFail{:tact}` | Bounce transaction in case of any errors during action phase. Has no effect if flag $+2$, `SendIgnoreErrors{:tact}` is used.
$+32$      | `SendDestroyIfZero{:tact}`      | Current account must be destroyed if its resulting balance is zero (often used with mode $128$, `SendRemainingBalance{:tact}`).

## Combining modes with flags

To make the [`Int{:tact}`][int] value for `mode` field of `SendParameters{:tact}`, you just have to combine base modes with optional flags by applying the [bitwise OR](/book/operators#binary-bitwise-or) operation.

For example, if you want to send a regular message and pay transfer fees separately, use the mode $0$ (default) and a flag $+1$ to get `mode` $= 1$, which is equal to using `SendPayGasSeparately{:tact}` constant.

Alternatively, if you want to send the whole contract balance and destroy it immediately, use the mode $128$ and flag $+32$ to get `mode` $= 160$, which is equal to `SendRemainingBalance | SendDestroyIfZero{:tact}`.

Here's how the latter example would look in code:

```tact
let to: Address = ...;
let value: Int = ton("1");
send(SendParameters{
    to: to,
    value: value,
    mode: SendRemainingBalance | SendDestroyIfZero,
    body: "Hello, World!".asComment(),
});
```

<Callout type="warning" emoji="⚠️">

  Note, that while adding ([`+{:tact}`](/book/operators#binary-add)) base modes together with optional flags is possible, it is discouraged due to the possibility of excess values. Use the bitwise OR ([`|{:tact}`](/book/operators#binary-bitwise-or)) instead, as it's designed to work with such flag and bit manipulations of the `mode`.

</Callout>

<Callout>

  Also note, that there can be only one [base mode](#base-modes), but number of [optional flags](#optional-flags) may vary: you can use them all, none or just some.

</Callout>

[int]: /book/integers


## operators.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/operators.mdx)
# Operators

import { Callout } from 'nextra/components'

Almost every contract operates on data: transforms some values into another. Scope may vary, but operators lay in core of such modifications.

This page lists all the operators in Tact in decreasing order of their [precedence](#precedence), with examples of usage.

<Callout>

  Note, that there are no implicit type conversions in Tact, so operators can't be used to, say, add values of different type or compare them in terms of equality without explicitly casting to the same type. That's done with certain functions from the standard library. See [`Int.toString(){:tact}`](/ref/core-strings#inttostring) for an example of such function.

</Callout>

## Table of operators [#table]

The following table lists operators in order of decreasing [precedence](#precedence): from highest to lowest.

Brief description | Operators
:---------------- | :--------------------------------------------------------------------
Parentheses       | [`(){:tact}`][paren]
Unary postfix     | [`!!{:tact}`][nna]
Unary prefix      | [`+{:tact}`][plus] &nbsp; [`-{:tact}`][neg] &nbsp; [`!{:tact}`][inv] &nbsp; [`~{:tact}`][b-not]
Multiplicative    | [`*{:tact}`][mul] &nbsp; [`/{:tact}`][div] &nbsp; [`%{:tact}`][mod]
Additive          | [`+{:tact}`][add] &nbsp; [`-{:tact}`][sub]
Shift             | [`>>{:tact}`][shr] &nbsp; [`<<{:tact}`][shl]
Relation          | [`>{:tact}`][gt] &nbsp; [`>={:tact}`][ge] &nbsp; [`<{:tact}`][lt] &nbsp; [`<={:tact}`][le]
Equality          | [`=={:tact}`][eq] &nbsp; [`!={:tact}`][eq]
Bitwise AND       | [`&{:tact}`][b-and]
Bitwise XOR       | [`^{:tact}`][b-xor]
Bitwise OR        | [`\|{:tact}`][b-or]
Logical AND       | [`&&{:tact}`][l-and]
Logical OR        | [`\|\|{:tact}`][l-or]
Ternary           | [`?:{:tact}`][ternary]
Assignment        | [`={:tact}`][assign] and [all augmented assignment operators](#augmented-assignment)

[paren]: #parentheses

[nna]: #unary-non-null-assert
[plus]: #unary-plus
[neg]: #unary-negate
[inv]: #unary-inverse
[b-not]: #unary-bitwise-not

[mul]: #binary-multiply
[div]: #binary-divide
[mod]: #binary-modulo

[add]: #binary-add
[sub]: #binary-subtract

[shr]: #binary-bitwise-shift-right
[shl]: #binary-bitwise-shift-left

[gt]: #binary-greater
[ge]: #binary-greater-equal
[lt]: #binary-less
[le]: #binary-less-equal

[eq]: #binary-equality

[b-and]: #binary-bitwise-and
[b-xor]: #binary-bitwise-xor
[b-or]: #binary-bitwise-or

[l-and]: #binary-logical-and
[l-or]: #binary-logical-or

[ternary]: #ternary

[assign]: #assignment

## Precedence

All operators on this page are given in order of decreasing precedence, from highest to lowest. Precedence is used to choose which operator would be considered in a particular situation. Whenever any ambiguity arises, Tact would prefer operators with higher precedence over those with lower.

For example, minus sign (`-{:tact}`) may be considered as a subtraction operator or as a negation operator, which reverses the sign of the expression from plus to minus, or vice-versa. As the latter has the higher precedence over the former in cases of ambiguity between the two Tact will first consider `-{:tact}` as a negation operator. And if that doesn't make sense for the given expression, only then it would consider it as a subtraction operator.

Consider the following code:

```tact
5 + -5; // here, the minus sign would be viewed as a negation operator
5 -5;   // while here it would be viewed as a subtraction operator, despite formatting
```

Even though this example may be simple, neglecting of precedence rules can often lead to confusing situations with operators. The correct order of operations can be ensured by wrapping every operation in [parentheses](#parentheses), since parentheses have the highest precedence of all expressions and operators there is.

## Parentheses, `()` [#parentheses]

Parentheses (also can be called round brackets, `(){:tact}`) are more of a punctuation symbols than actual operators, but their [precedence](#precedence) is higher than precedence of any other operator. Use parentheses to override order of operations:

```tact
5 * 5 - 2;   // 23
5 * (5 - 2); // 15
```

## Unary

Unary here means that they are applied only to one operand of the given expression. All unary operators, except for the [non-null assertion](#unary-non-null-assert), are of the same [precedence](#precedence).

Unary operators can be one of the two types:

* prefix — placed before the expression.
* postfix (or suffix) —  placed after the expression.

### Non-null assert, `!!` [#unary-non-null-assert]

Unary double-exclamation mark (_non-null assertion_) operator `!!{:tact}` is a postfix operator, which enforces non-null values and allows direct access to the value of the optional variable if it's not `null{:tact}`. Raises a compilation error otherwise. Can be applied to any optional variable regardless of its non-null type.

<Callout>

  Read more about optional variables and fields here: [Optionals](/book/optionals)

</Callout>

### Plus, `+` [#unary-plus]

Although unary plus sign operator `+{:tact}` is specified in the grammar of Tact compiler, it only exists as a [binary operator](#binary-plus).

### Negate, `-` [#unary-negate]

Unary minus sign (_negation_) operator `-{:tact}` is a prefix operator, which reverses the sign of the expression. Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let five: Int = 5;
five + -five; // here, the minus sign is a negation operator, not a subtraction operator
-(-1);        // double application gives back the original value, which is 1
--1;          // 1
```

### Inverse, `!` [#unary-inverse]

Unary exclamation mark (_inversion_) operator `!{:tact}` is a prefix operator, which inverts the boolean value of the expression — changes `true{:tact}` to `false{:tact}`, and vice versa. Can only be applied to values of type [`Bool{:tact}`][bool]:

```tact
let iLikeTact: Bool = true;
!iLikeTact; // false
!false;     // true
!(!false);  // false
!!false;    // false
```

### Bitwise NOT, `~` [#unary-bitwise-not]

Unary tilde (_bitwise not_) operator `~{:tact}` is a prefix operator, which inverts or _flips_ each bit in the binary representation of the expression — changes each $1$ to $0$, and vice versa. Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let answer: Int = 42;
~answer;    // -43
~(~answer); // 42
~(~0);      // 0
~~0;        // 0
```

## Binary

Binary operators are split into several subsections, in order of decreasing [precedence](#precedence). Operators within each subsection have the same [precedence](#precedence) as the subsection itself.

### Multiplication [#binary-multiplication]

Multiply, divide or obtain a remainder.

#### Multiply, `*` [#binary-multiply]

Binary asterisk (_multiplication_) operator `*{:tact}` is used for multiplication of two values. Can cause [integer overflows](/book/integers#operations).

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two * two;         // 4
0 * 1_000_000_000; // 0
-1 * 5;            // -5

pow(2, 255) * pow(2, 255); // build error: integer overflow!
```

#### Divide, `/` [#binary-divide]

Binary slash (_division_) operator `/{:tact}` is used for integer division of two values, which truncates towards zero if result is positive, and away from zero if result is negative. This is also called [rounding down](https://en.wikipedia.org/wiki/Rounding#Rounding_down) (or rounding towards $-∞$).

An attempt to divide by zero would result in an error with [exit code 4](/book/exit-codes#4): `Integer overflow`.

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two / 2; // 1
two / 1; // 2
-1 / 5;  // -1
-1 / -5; // 0
1 / -5;  // -1
1 / 5;   // 0
6 / 5;   // 1, rounding down
-6 / 5;  // -2, rounding down (towards -∞)
```

<Callout>

  Note that the following relationship between the division and modulo operators always holds for `Int{:tact}` type:

  ```tact
  a / b * b + a % b == a; // true for any Int values of `a` and `b`,
                          //   except when `b` is equal to 0 and we divide `a` by 0,
                          //   which is an attempt to divide by zero resulting in an error
  ```

</Callout>

#### Modulo, `%` [#binary-modulo]

Binary percent sign (_modulo_) operator `%{:tact}` is used for getting the modulo of an integer division, which must not be confused with getting a remainder. For two values of the same sign, modulo and remainder operations are equivalent, but when the operands are of different signs, the modulo result always has the same sign as the _divisor_ (value on the right), while the remainder has the same sign as the _dividend_ (value on the left), which can make them differ by one unit of the _divisor_.

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two % 2; // 0
two % 1; // 1

1 % 5;   // 1
-1 % 5;  // 4
1 % -5;  // -4
-1 % -5; // -1
```

The simplest way to avoid confusion between the two is to prefer using positive values via [`abs(x: Int){:tact}`](/ref/core-math#abs):

```tact
abs(-1) % abs(-5); // 1
```

<Callout>

  Did you know, that in JavaScript `%{:tact}` works as a _remainder_ operator, but not _modulo_ operator (like in Tact)?\
  [Remainder (%) - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Remainder#description)\
  [Modulo - Wikipedia](https://en.wikipedia.org/wiki/Modulo)

</Callout>

### Addition [#binary-addition]

Add or subtract.

#### Add, `+` [#binary-add]

Binary plus (_addition_) operator `+{:tact}` is used for adding numbers together. Going beyond the maximum value of an [`Int{:tact}`][int] will result in an error with [exit code 4](/book/exit-codes#4): `Integer overflow`.

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two + 2; // 4
-1 + 1;  // 0

pow(2, 254) + pow(2, 254);     // 2 * 2^254
pow(2, 255) + pow(2, 255);     // build error: integer overflow!
pow(2, 255) - 1 + pow(2, 255); // 2^256 - 1, maximal value of any integer in Tact!
```

#### Subtract, `-` [#binary-subtract]

Binary minus (_subtraction_) operator `-{:tact}` is used for subtracting numbers from each other. Going beyond the minimum value of an [`Int{:tact}`][int] will result in an error with [exit code 4](/book/exit-codes#4): `Integer overflow`.

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two - 2; // 0
-1 - 1;  // -2

pow(2, 254) - pow(2, 254); // 0
pow(2, 255) - pow(2, 255); // 0
pow(2, 256) - pow(2, 256); // build error: integer overflow!
```

### Bitwise shifts [#binary-bitwise-shifts]

Shift bits to the left or to the right.

#### Shift right, `>>` [#binary-bitwise-shift-right]

Binary double greater than (_bitwise shift right_) operator `>>{:tact}` returns an integer which binary representation is the _left operand_ value shifted by the _right operand_ number of bits to the right. Excess bits shifted off to the right are discarded, and copies of the leftmost bit are shifted in from the left. This operation is also called "sign-propagating right shift" or "arithmetic right shift", because the sign of the resulting number is the same as the sign of the _left operand_. This is a more effective way to divide the _left operand_ by $2^n$, where $n$ is equal to the _right operand_.

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two >> 1; // 1
4 >> 1;   // 2
5 >> 1;   // 2, due to flooring of integer values

pow(2, 254) >> 254; // 1
```

<Callout>

  [Bit shifts - Wikipedia](https://en.wikipedia.org/wiki/Bitwise_operation#Bit_shifts)\
  [Bit manipulation - Wikipedia](https://en.wikipedia.org/wiki/Bit_manipulation)

</Callout>

#### Shift left, `<<` [#binary-bitwise-shift-left]

Binary double greater than (_bitwise shift left_) operator `<<{:tact}` returns an integer which binary representation is the _left operand_ value shifted by the _right operand_ number of bits to the left. Excess bits shifted off to the left are discarded, and zero bits are shifted in from the right. This is a more effective way to multiply the _left operand_ by $2^n$, where $n$ is equal to the _right operand_. Going beyond the maximum value of an [`Int{:tact}`][int] will result in an error with [exit code 4](/book/exit-codes#4): `Integer overflow`.

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two << 1; // 4
1 << 5;   // 1 * 2^5, which is 32
2 << 5;   // 2 * 2^5, which is 64

pow(2, 254) == (1 << 254); // true
pow(2, 254) == 1 << 254; // true, no parentheses needed due to higher precedence of >> over ==
pow(2, 255) == 1 << 255; // true, but we're very close to overflow here!
```

<Callout>

  [Bit shifts - Wikipedia](https://en.wikipedia.org/wiki/Bitwise_operation#Bit_shifts)\
  [Bit manipulation - Wikipedia](https://en.wikipedia.org/wiki/Bit_manipulation)

</Callout>

### Relation [#binary-relation]

Find bigger, smaller or equal values.

#### Greater than, `>` [#binary-greater]

Binary _greater than_ operator `>{:tact}` returns `true{:tact}` if the left operand is greater than the right operand, and `false{:tact}` otherwise. Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two > 2; // false
-1 > -3; // true
```

#### Greater than or equal to, `>=` [#binary-greater-equal]

Binary _greater than or equal to_ operator `>={:tact}` returns `true{:tact}` if the left operand is greater than or to the right operand, and `false{:tact}` otherwise. Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two >= 2; // true
-1 >= -3; // true
```

#### Less than, `<` [#binary-less]

Binary _less than_ operator `<{:tact}` returns `true{:tact}` if the left operand is less than the right operand, and `false{:tact}` otherwise. Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two < 2; // false
-1 < -3; // false
```

#### Less than or equal to, `<=` [#binary-less-equal]

Binary _less than or equal to_ operator `<={:tact}` returns `true{:tact}` if the left operand is less than or equal to the right operand, and `false{:tact}` otherwise. Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two <= 2; // true
-1 <= -3; // false
```

### Equality and inequality, `==` `!=` [#binary-equality]

Binary equality (_equal_) operator `=={:tact}` checks whether its two operands are _equal_, returning a result of type [`Bool{:tact}`][bool].

Binary inequality (_not equal_) operator `!={:tact}` checks whether its two operands are _not equal_, returning a result of type [`Bool{:tact}`][bool].

Both operators require operands to be of the same type and both don't perform implicit type conversions, except for the [`Cell{:tact}`][cell] and [`Slice{:tact}`][slice] types, which are implicitly compared by their hashes.

Both operators can be applied to the following list of types and values:

* [`Int{:tact}`][int]
* [`Bool{:tact}`][bool]
* [`Address{:tact}`][p]
* [`Cell{:tact}`][cell], implicitly compares via `.hash(){:tact}`
* [`Slice{:tact}`][slice], implicitly compares via `.hash(){:tact}`
* [`String{:tact}`][p]
* [`map<K, V>{:tact}`](/book/maps), but only if their key and value types are identical
* [Optionals and `null{:tact}` value](/book/optionals)

```tact
// Int:
2 == 3; // false
2 != 3; // true

// Bool:
true == true;  // true
false != true; // true

// Address:
myAddress() == myAddress(); // true
myAddress() != myAddress(); // false

// Cell:
emptyCell() == emptyCell(); // true
emptyCell() != emptyCell(); // false

// Slice:
"A".asSlice() == "A".asSlice(); // true
"A".asSlice() != "A".asSlice(); // false

// String:
"A" == "A"; // true
"A" != "A"; // false

// map<K, V>:
let map1: map<Int, Int> = emptyMap();
let map2: map<Int, Int> = emptyMap();
map1 == map2; // true
map1 != map2; // false

// Optionals and null values themselves
let nullable: Int? = null;
nullable == null; // true
null == null;     // true
nullable != null; // false
null != null;     // false

let anotherNullable: Int? = 5;
nullable == anotherNullable; // false
nullable != anotherNullable; // true
```

### Bitwise AND, `&` [#binary-bitwise-and]

Binary ampersand (_bitwise AND_) operator `&{:tact}` applies a [bitwise AND](https://en.wikipedia.org/wiki/Bitwise_operation#AND), which performs the [logical AND](#binary-logical-and) operation on each pair of the corresponding bits of operands. This is useful when we want to clear selected bits off a number, where each bit represents an individual flag or a boolean state, which makes it possible to "store" up to $257$ boolean values per integer, as all integers in Tact are $257$-bit signed.

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two & 1; // 0
4 & 1;   // 0
3 & 1;   // 1
1 & 1;   // 1

255 & 0b00001111;        // 15
0b11111111 & 0b00001111; // 15
```

<Callout>

  [Bitwise AND - Wikipedia](https://en.wikipedia.org/wiki/Bitwise_operation#AND)\
  [Bit manipulation - Wikipedia](https://en.wikipedia.org/wiki/Bit_manipulation)

</Callout>

### Bitwise XOR, `^` [#binary-bitwise-xor]

Binary caret (_bitwise XOR_) operator `^{:tact}` applies a [bitwise XOR](https://en.wikipedia.org/wiki/Bitwise_operation#XOR), which performs the [logical exclusive OR](https://en.wikipedia.org/wiki/Exclusive_or) operation on each pair of the corresponding bits of operands. The result in each position is $1$ if only one of the bits is $1$, but will be $0$ if both are $0$ or both are $1$. In this it performs the comparison of two bits, giving $1$ if the two bits are different, and $0$ if they are the same.

It is useful for inverting selected bits of an operand (also called toggle or flip), as any bit may be toggled by "XORing" it with $1$.

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two ^ 3; // 1
4 ^ 1;   // 0
3 ^ 1;   // 3
1 ^ 1;   // 0

255 ^ 0b00001111;        // 240
0b11111111 ^ 0b00001111; // 240
```

<Callout>

  [Bitwise XOR - Wikipedia](https://en.wikipedia.org/wiki/Bitwise_operation#XOR)\
  [Bit manipulation - Wikipedia](https://en.wikipedia.org/wiki/Bit_manipulation)

</Callout>

### Bitwise OR, `|` [#binary-bitwise-or]

Binary bar (_bitwise OR_) operator `|{:tact}` applies a [bitwise OR](https://en.wikipedia.org/wiki/Bitwise_operation#OR), which performs the [logical OR](#binary-logical-or) operation on each pair of the corresponding bits of operands. This is useful when we want to apply a specific [bitmask](https://en.wikipedia.org/wiki/Mask_(computing)).

For example, _bitwise OR_ is commonly used in Tact to [combine base modes with optional flags](/book/message-mode#combining-modes-with-flags) by masking specific bits to $1$ in order to construct a target [message `mode`](/book/message-mode).

Can only be applied to values of type [`Int{:tact}`][int]:

```tact
let two: Int = 2;
two | 1; // 3
4 | 1;   // 5
3 | 1;   // 3
1 | 1;   // 1

255 | 0b00001111;        // 255
0b11111111 | 0b00001111; // 255
```

<Callout>

  [Bitwise OR - Wikipedia](https://en.wikipedia.org/wiki/Bitwise_operation#OR)\
  [Bit manipulation - Wikipedia](https://en.wikipedia.org/wiki/Bit_manipulation)

</Callout>

### Logical AND, `&&` [#binary-logical-and]

Binary logical AND ([logical conjunction](https://en.wikipedia.org/wiki/Logical_conjunction)) operator `&&{:tact}` returns `true{:tact}` if both operands are `true{:tact}`, and `false{:tact}` otherwise. It's short-circuited, meaning that it would immediately evaluate the whole expression as `false{:tact}` if the left operand is `false{:tact}`, without evaluating the right one.

Can only be applied to values of type [`Bool{:tact}`][bool]:

```tact
let iLikeTact: Bool = true;
iLikeTact && true;  // true, evaluated both operands
iLikeTact && false; // false, evaluated both operands
false && iLikeTact; // false, didn't evaluate iLikeTact
```

### Logical OR, `||` [#binary-logical-or]

Binary logical OR ([logical disjunction](https://en.wikipedia.org/wiki/Logical_disjunction)) operator `||{:tact}` returns `false{:tact}` only if both operands are `false{:tact}`, and `true{:tact}` otherwise. It's short-circuited, meaning that it would immediately evaluate the whole expression as `true{:tact}` if the left operand is `true{:tact}`, without evaluating the right one.

Can only be applied to values of type [`Bool{:tact}`][bool]:

```tact
let iLikeSnails: Bool = false;
iLikeSnails || true;  // true, evaluated both operands
iLikeSnails || false; // false, evaluated both operands
true || iLikeSnails;  // true, didn't evaluate iLikeSnails
```

## Ternary, `?:` [#ternary]

Conditional (_ternary_) operator is the only Tact operator that takes three operands: a condition followed by a question mark (`?{:tact}`), then an expression to execute if the condition is evaluated to `true{:tact}` followed by a colon (`:{:tact}`), and finally the expression to execute if the condition is evaluated to `false{:tact}`. This operator is frequently used as an alternative to an [`if...else{:tact}`](/book/statements#if-else) statement.

Condition must resolve to type [`Bool{:tact}`][bool]:

```tact
// condition
// ↓
true ? "incredibly so" : "absolutely not"; // "incredibly so"
//     ---------------   ----------------
//     ↑                 ↑
//     |                 alternative, when condition is false
//     |
//     consequence, when condition is true

2 + 2 == 4 ? true : false; // true
```

Ternary operator is the only operator with right associativity, besides [assignment-related ones](#assignment). This means that in ambiguous situations Tact would prefer the longest matching sequence. In short, this makes bracket-less nesting of ternary operators possible, but only for alternative cases (the part that comes after the colon sign `:{:tact}`):

```tact
// don't need additional parentheses for alternative cases
false ? 1 : (false ? 2 : 3); // 3
false ? 1 : false ? 2 : 3;   // also 3
false ? 1 : true ? 2 : 3;    // 2

// need additional parentheses for consequence cases (parts in-between ? and :)
false ? (false ? 1 : 2) : 3; // 3
false ? false ? 1 : 2 : 3;   // SYNTAX ERROR!
true  ? (false ? 1 : 2) : 3; // 2
```

## Assignment, `=` [#assignment]

Assignment operator `={:tact}` is used to assign a value to a variable, or to a property of a [Message](/book/structs-and-messages#messages) or a [Struct](/book/structs-and-messages#structs). The assignment is a statement and it doesn't return a value.

```tact
let someVar: Int = 5;    // assignment operator = is used here...
someVar = 4;             // ...and here
someVar = (someVar = 5); // SYNTAX ERROR!
```

### Augmented assignment

Augmented (or compound) assignment operators such as `+={:tact}` combine an operation with an [assignment](#assignment). The augmented assignment is a statement and it doesn't return a value.

Augmented assignments are semantically equivalent to regular assignments, but with an operation:

```tact
let value: Int = 5;

// this:
value += 5;
// is equivalent to this:
value = value + 5;
```

List of augmented assignment operators:

* `+={:tact}`, which uses [addition operator `+{:tact}`](#binary-add). Can only be applied to values of type [`Int{:tact}`][int].
* `-={:tact}`, which uses [subtraction operator `-{:tact}`](#binary-subtract). Can only be applied to values of type [`Int{:tact}`][int].
* `*={:tact}`, which uses [multiplication operator `*{:tact}`](#binary-multiply). Can only be applied to values of type [`Int{:tact}`][int].
* `/={:tact}`, which uses [division operator `/{:tact}`](#binary-divide). Can only be applied to values of type [`Int{:tact}`][int].
* `%={:tact}`, which uses [modulo operator `%{:tact}`](#binary-modulo). Can only be applied to values of type [`Int{:tact}`][int].
* `&={:tact}`, which uses [bitwise AND operator `&{:tact}`](#binary-bitwise-and). Can only be applied to values of type [`Int{:tact}`][int].
* `^={:tact}`, which uses [bitwise XOR operator `^{:tact}`](#binary-bitwise-xor). Can only be applied to values of type [`Int{:tact}`][int].
* `|={:tact}`, which uses [bitwise OR operator `|{:tact}`](#binary-bitwise-or). Can only be applied to values of type [`Int{:tact}`][int].

```tact
let value: Int = 5;

// +=
value + 5;         // adds 5
value = value + 5; // adds 5 and assigns result back
value += 5;        // also adds 5 and assigns result back

// -=
value - 5;         // subtracts 5
value = value - 5; // subtracts 5 and assigns result back
value -= 5;        // also subtracts 5 and assigns result back

// *=
value * 5;         // multiplies by 5
value = value * 5; // multiplies by 5 and assigns result back
value *= 5;        // also multiplies by 5 and assigns result back

// /=
value / 5;         // divides by 5
value = value / 5; // divides by 5 and assigns result back
value /= 5;        // also divides by 5 and assigns result back

// %=
value % 5;         // gets modulo by 5
value = value % 5; // gets modulo by 5 and assigns result back
value %= 5;        // also gets modulo by 5 and assigns result back

// &=
value & 5;         // bitwise ANDs 5
value = value & 5; // bitwise ANDs 5 and assigns result back
value &= 5;        // also bitwise ANDs 5 and assigns result back

// ^=
value ^ 5;         // bitwise XORs 5
value = value ^ 5; // bitwise XORs 5 and assigns result back
value ^= 5;        // also bitwise XORs 5 and assigns result back

// |=
value | 5;         // bitwise ORs 5
value = value | 5; // bitwise ORs 5 and assigns result back
value |= 5;        // also bitwise ORs 5 and assigns result back
```

[p]: /book/types#primitive-types
[bool]: /book/types#booleans
[int]: /book/integers
[cell]: /book/cells#cells
[slice]: /book/cells#slices


## optionals.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/optionals.mdx)
# Optionals

import { Callout } from 'nextra/components'

As it was mentioned in [type system overview](/book/types#optionals), all [primitive types](/book/types#primitive-types), [Structs](/book/structs-and-messages#structs) and [Messages](/book/structs-and-messages#messages) could be nullable. That is, they don't necessarily hold any value, aside from `null{:tact}` — a special value, which represents the intentional absence of any other value.

[Variables](/book/statements#let) or fields of [Structs](/book/structs-and-messages#structs) and [Messages](/book/structs-and-messages#messages) that can hold `null{:tact}` are called "optionals". They're useful to reduce state size when the variable isn't necessarily used.

You can make any variable or a field an optional by adding a question mark (`?{:tact}`) after its type declaration. The only exceptions are [`map<K, V>{:tact}`](/book/maps) and [`bounced<Msg>{:tact}`](/book/bounced#bounced-messages-in-tact), where you can't make them, inner key/value type (in case of a map) or the inner [Message](/book/structs-and-messages#messages) (in case of a bounced) optional.

Optional variables or optional fields that are not defined hold the `null{:tact}` value by default. You cannot access them without checking for `null{:tact}` first. But if you're certain they are not `null{:tact}` at a given moment, use the [non-null assertion operator `!!{:tact}`](/book/operators#unary-non-null-assert) to access their value.

Trying to access the value of an optional variable or an optional field without using [`!!{:tact}`](/book/operators#unary-non-null-assert) or without checking for `null{:tact}` beforehand will result in a compilation error.

Example of optionals:

```tact
struct StOpt {
    opt: Int?; // Int or null
}

message MsOpt {
    opt: StOpt?; // Notice, how the struct StOpt is used in this definition
}

contract Optionals {
    opt: Int?;
    address: Address?;

    init(opt: Int?) { // optionals as parameters
        self.opt = opt;
        self.address = null; // explicit null value
    }

    receive(msg: MsOpt) {
        let opt: Int? = 12; // defining a new variable
        if (self.opt != null) { // explicit check
            self.opt = opt!!; // using !! as we know that opt value isn't null
        }
    }
}
```


## programmatic.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/programmatic.mdx)
import { Callout } from "nextra-theme-docs";

# Programmatic API

You can invoke the Tact compiler from your code in node and browser environments.

<Callout type="warning" emoji="⚠️">
  This API has not been released yet. It will be released in the 1.0.0 version.
</Callout>

## Run compiler in browser

```ts
import { run } from "@tact-lang/compiler";

// Virtual FS
const fs = {
  ["main.tact"]: Buffer.from("...").toString("base64"),
};

const config = {
  projects: [
    {
      name: "Sample",
      path: "main.tact",
      output: "./output",
    },
  ],
};

// Run compiler
let successful = await run({ config, fs });

// NOTE: Output from is written to the same fs object.
```

## Contract verification

You can always verify the compiled package with the `verify` function.

```ts
import { verify } from "@tact-lang/compiler";
const pkg: string = '...';
const res = await verify(pkg);
```

## receive.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/receive.mdx)
# Receive messages

TON is a distributed blockchain which means that communication between contracts is done by sending and receiving messages. The most common type of message is the internal message - a message sent from one contract (or a wallet) to another.

## Receive internal messages

To receive a message of the required type, you need to declare a receiver function, for example, `receive("increment"){:tact}`. This notation means the declaration of a receiver function that will be called when a text with the value `"increment"{:tact}` is sent to the contract. The function body can modify the state of the contract and send messages to other contracts. It is impossible to call a receiver directly. If you need to reuse some logic you can declare a function and call it from the receiver.

There are several receiver functions. All receiver functions are processed in the order they are listed below:

* `receive(){:tact}` - called when an empty message is sent to the contract
* `receive("message"){:tact}` - called when a text message with a specific comment is sent to the contract
* `receive(str: String){:tact}` - called when an arbitrary text message is sent to the contract
* `receive(msg: MyMessage){:tact}` - called when a binary message of type `MyMessage` is sent to the contract
* `receive(msg: Slice){:tact}` - called when binary message of unknown type is sent to the contract

```tact
message MyMessage {
    value: Int;
}

contract MyContract {
    receive() {
        // ...
    }
    receive("message") {
        // ...
    }
    receive(str: String) {
        // ...
    }
    receive(msg: MyMessage) {
        // ...
    }
    receive(msg: Slice) {
        // ...
    }
}
```

Naming a parameter of the receiver function with an underscore `_{:tact}` makes its value considered unused and discarded. This is useful when you don't need to inspect the message received and you only want it to convey a specific opcode:

```tact
message(42) UniverseCalls {}

contract Example {
    receive(_: UniverseCalls) {
        // Got a Message with opcode 42
    }
}
```


## send.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/send.mdx)
# Sending messages

import { Callout } from 'nextra-theme-docs'

TON blockchain is message-based — to communicate with other contracts and to deploy new ones you need to send messages.

Messages in Tact are commonly composed using a built-in [Struct](/book/structs-and-messages#structs) `SendParameters{:tact}`, which consists of:

Field    | Type                   | Description
:------- | :--------------------- | :----------
`bounce` | [`Bool{:tact}`][p]     | When set to `true` (default) message bounces back to the sender if the receiver contract doesn't exist or wasn't able to process the message.
`to`     | [`Address{:tact}`][p]  | Receiver internal [`Address{:tact}`][p] in TON blockchain.
`value`  | [`Int{:tact}`][int]    | The amount of [nanoToncoins][nano] you want to send with the message. This value is usually used to cover [forward fees][fwdfee], unless the optional flag [`SendPayGasSeparately{:tact}`](/book/message-mode#optional-flags) is used.
`mode`   | [`Int{:tact}`][int]    | An 8-bit value that configures how to send a message, defaults to $0$. See: [Message `mode`](/book/message-mode).
`body`   | [`Cell?{:tact}`][cell] | [Optional][opt] message body as a [`Cell{:tact}`][cell]
`code`   | [`Cell?{:tact}`][cell] | [Optional][opt] initial code of the contract (the compiled bytecode)
`data`   | [`Cell?{:tact}`][cell] | [Optional][opt] initial data of the contract (arguments of [`init(){:tact}` function](/book/contracts#init-function) of the contract)

Fields `code` and `data` are what's called an [init package](/book/expressions#initof), which is used in deployments of new contracts.

## Send simple reply

The simplest message is a reply to the incoming message returning all excess value of a message:

```tact
receive() {
    self.reply("Hello, World!".asComment()); // asComment converts a String to a Cell with a comment
}
```

## Send message

If you need more advanced logic you can use the `send(){:tact}` function and `SendParameters{:tact}` [Struct](/book/structs-and-messages#structs) directly.

In fact, the previous example with [`.reply(){:tact}`](#send-simple-reply) can be made using the following call to `send(){:tact}` function:

```tact
receive() {
    send(SendParameters{
        // bounce is set to true by default
        to: sender(), // sending message back to the sender
        value: 0, // don't add Toncoins to the message...
        mode: SendRemainingValue | SendIgnoreErrors, // ...except for ones received from the sender due to SendRemainingValue
        body: "Hello, World".asComment(), // asComment converts a String to a Cell with a comment
    });
}
```

Another example sends a message to the specified [`Address{:tact}`][p] with a `value` of $1$ TON and the `body` of a comment with a [`String{:tact}`][p] `"Hello, World!"{:tact}`:

```tact
let recipient: Address = ...;
let value: Int = ton("1");
send(SendParameters{
    // bounce is set to true by default
    to: recipient,
    value: value,
    mode: SendIgnoreErrors, // will send the message despite any errors
    body: "Hello, World!".asComment(),
});
```

The [optional flag](/book/message-mode#optional-flags) `SendIgnoreErrors{:tact}` means that even when an error occurs during message sending next messages would be sent anyway. **No error during the sending phase would revert a transaction.**

## Send typed message

To send a binary typed message you can use the following code:

```tact
let recipient: Address = ...;
let value: Int = ton("1");
send(SendParameters{
    // bounce is set to true by default
    to: recipient,
    value: value,
    mode: SendIgnoreErrors, // don't stop in case of errors
    body: SomeMessage{arg1: 123, arg2: 1234}.toCell(),
});
```

## Deploy contract

To deploy a contract you need to calculate its address and initial state with [`initOf{:tact}`](/book/expressions#initof), then send them in the initialization message:

```tact
let init: StateInit = initOf SecondContract(arg1, arg2);
let address: Address = contractAddress(init);
let value: Int = ton("1");
send(SendParameters{
    // bounce is set to true by default
    to: address,
    value: value,
    mode: SendIgnoreErrors, // don't stop in case of errors
    code: init.code,
    data: init.data,
    body: "Hello, World!".asComment(), // not necessary, can be omitted
});
```

## Outbound message processing

Each transaction on TON Blockchain consists of [multiple phases][phases]. Outbound messages are evaluated in [compute phase][compute], but are **not** sent in that phase. Instead, they're queued in order of appearance for the [action phase][phases], where all actions listed in [compute phase][compute], like outbound messages or [reserve requests](/ref/core-advanced#nativereserve), are executed.

As all the values are computed in [compute phase][compute], all the fees computed by the end of it, and exceptions do not revert the transaction during [action phase][phases], outbound message sends can fail without bounce due to unsufficient [action fees](https://docs.ton.org/develop/howto/fees-low-level#action-fee) or [forward fees][fwdfee].

Consider the following example:

```tact
// This contract initially has 0 nanoToncoins on the balance
contract FailureIsNothingButAnotherStep {
    // And all the funds it gets are obtained from inbound internal messages
    receive() {
        // 1st outbound message evaluated and queued (but not sent yet)
        send(SendParameters{
            to: sender(),
            value: ton("0.042"), // plus forward fee due to SendPayGasSeparately
            mode: SendIgnoreErrors | SendPayGasSeparately,
        });

        // 2nd outbound message evaluated and queued (but not sent yet, and never will be!)
        send(SendParameters{
            to: sender(),
            value: 0,
            mode: SendRemainingValue | SendIgnoreErrors,
        });
    }
}
```

There, the second message won't actually be sent:

* After finishing the [compute phase][compute], the remaining value $\mathrm{R}$ of the contract is computed.

* During the outbound message processing and assuming that there was enough value provided in the inbound message, the first message leaves $\mathrm{R} - (0.042 + \mathrm{forward\_fees})$ [nanoToncoins](/book/integers#nanotoncoin) on the balance.

* When the second message is processed, contract tries to send $\mathrm{R}$ [nanoToncoins](/book/integers#nanotoncoin), but fails to do so because there is already a smaller amount left.

<Callout>

  Read more about all message sending functions in the Reference:
  * [`send(){:tact}`](/ref/core-common#send)
  * [`emit(){:tact}`](/ref/core-common#emit)
  * [`self.notify(){:tact}`](/ref/core-base#self-notify)
  * [`self.reply(){:tact}`](/ref/core-base#self-reply)
  * [`self.forward(){:tact}`](/ref/core-base#self-forward)
  * [`nativeSendMessage(){:tact}`](/ref/core-advanced#nativesendmessage)

</Callout>

[p]: /book/types#primitive-types
[int]: /book/integers
[cell]: /book/cells#cells
[opt]: /book/optionals

[phases]: https://docs.ton.org/learn/tvm-instructions/tvm-overview#transactions-and-phases
[compute]: https://docs.ton.org/learn/tvm-instructions/tvm-overview#compute-phase
[nano]: /book/integers#nanotoncoin
[fwdfee]: https://docs.ton.org/develop/howto/fees-low-level#forward-fees


## statements.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/statements.mdx)
# Statements

import { Callout } from 'nextra/components'

The following statements can appear anywhere in the [function](/book/functions) body.

## `let` statement [#let]

The `let{:tact}` statement allows local and [block](#block)-scoped variable declaration.

In Tact, declaring a local variable always requires an initial value. However, the type ascription can be omitted and Tact will try to infer it from the initial value:

```tact
let value: Int = 123; // full declaration with type and value
let vInferred = 123;  // inferred type Int

let vExplicitCtx: Context = context(); // explicit type Context, a built-in Struct
let vCtx = context();                  // inferred type Context
```

Note, that initial value of `null{:tact}` can mean both an empty [`map<K, V>{:tact}`](/book/maps) with arbitrary `K{:tact}` and `V{:tact}` types, and the intentional absence of any other value for the [optional](/book/optionals) type. That's why whenever you're declaring an [optional](/book/optionals) or a [`map<K, V>{:tact}`](/book/maps), you'll need to explicitly specify the type as it cannot be inferred:

```tact
let vOptional: Int? = null; // explicit type Int or null
let vOptInt = 42;           // implicit type Int
vOptInt = null;             // COMPILATION ERROR!

let vMap: map<Int, Int> = emptyMap(); // explicit type map<Int, Int>
let vMapWithSerialization: map<Int as uint8, Int as uint8> = emptyMap();
```

Naming a local variable with underscore `_{:tact}` makes its value considered unused and discarded. This is useful when you don't need a return value of some function with side effects, and want to explicitly mark the variable as unused. Note, that such wildcard variable name `_{:tact}` cannot be accessed:

```tact
let _ = someFunctionWithSideEffects(); // with type inference
let _: map<Int, Int> = emptyMap();     // with explicit type

dump(_); // COMPILATION ERROR! Cannot access _
```

## `return` statement [#return]

The `return{:tact}` statement ends [function](/book/functions) execution and specifies a value to be returned to the [function](/book/functions) caller.

```tact
// Simple wrapper over stdlib function now()
fun getTimeFromNow(offset: Int): Int {
    return now() + offset;
}
```

## Block

A block statement is used to group zero or more statements. The block is delimited by a pair of braces ("curly braces", `{}{:tact}`) and contains a list of zero or more statements and declarations.

Some statements, such as [`let{:tact}`](#let) or [`return{:tact}`](#return), must end with a terminating semicolon `;{:tact}`. However, the semicolon of the last statement in the block is optional and may be omitted.

```tact
{ // <- start of the block
    // arbitrary statements:
    let value: Int = 2 + 2;
    dump(value);
} // <- end of the block

{ dump(2 + 2) } // a block with only one statement,
                // omitted the last and only semicolon

{
    let nah = 3 * 3 * 3; // a block with two statements,
    let yay = nah + 42   // but without the last semicolon
}
```

## Expression

An expression statement is an expression used in a place where a statement is expected. The expression is evaluated and its result is discarded — therefore, it makes sense only for expressions that have side effects, such as executing a function or updating a variable.

```tact
dump(2 + 2); // stdlib function
```

## Assignment

Assignment statements use an [assignment operator](/book/operators#assignment) (`={:tact}`) or [augmented assignment operators](/book/operators#augmented-assignment) (assignments combined with an operation):

```tact
let value: Int; // declaration
value = 5;      // assignment
value += 5;     // augmented assignment (one of the many, see below)
```

<Callout>

  Read more about assignment and augmented assignment in their dedicated section: [assignment operators](/book/operators#assignment).

</Callout>

## Branches

Control the flow of the code.

### `if...else` [#if-else]

<Callout type="warning" emoji="⚠️">

  Curly brackets (code blocks) are required!

</Callout>

When executing an `if...else{:tact}` statement, first, the specified condition gets evaluated. If the resulting value is `true{:tact}`, the following statement block gets executed. Otherwise, if the condition evaluates to `false{:tact}`, the optional `else{:tact}` block will be executed. If the `else{:tact}` block is missing, nothing happens and execution continues further.

Regular `if{:tact}` statement:

```tact
// condition
// ↓
if (true) { // consequence, when condition is true
    dump(2 + 2);
}
```

With `else{:tact}` block:

```tact
// condition
// ↓
if (2 + 2 == 4) {
    // consequence, when condition is true
    dump(true);
} else {
    // alternative, when condition is false
    dump(false);
}
```

With nested `if...else{:tact}`:

```tact
// condition
// ↓
if (2 + 2 == 3) {
    // consequence, when condition is true
    dump("3?");
//        condition2
//        ↓
} else if (2 + 2 == 4) {
    // another consequence, when condition2 is true
    dump(true);
} else {
    // alternative, when both condition and condition2 are false
    dump(false);
}
```

<Callout>

  Tact also has a ternary expression `?:{:tact}`, which is described earlier in the Book: [Ternary](/book/operators#ternary).

</Callout>

### `try...catch` [#try-catch]

The `try...catch{:tact}` statement is comprised of a `try{:tact}` block and an optional `catch{:tact}` block, which receives an [`Int{:tact}`][int] [exit code](/book/exit-codes) as its only argument. The code in the `try{:tact}` block is executed first, and if it fails, the code in the `catch{:tact}` block will be executed and changes made in `try{:tact}` block will be rolled back, if possible.

<Callout>

  Note, that some TVM state parameters, such as codepage and gas counters, will not be rolled back. That is, all gas usage in the `try{:tact}` block will be taken into account and the effects of opcodes that change the gas limit will be preserved.

</Callout>

Regular `try{:tact}` statement:

```tact
fun braveAndTrue() {
    // Lets try and do something erroneous
    try {
        nativeThrow(42); // throwing with exit code 42
    }

    // The following will be executed as the erroneous code above was wrapped in a try block
    dump(42);
}
```

With `catch (e){:tact}` block:

```tact
fun niceCatch() {
    // Lets try and do something erroneous
    try {
        nativeThrow(42); // throwing with exit code 42
    } catch (err) {
        dump(err);       // this will dump the exit code caught, which is 42
    }
}
```

With nested `try...catch{:tact}`:

```tact
try {
    // Preparing an x equal to 0, in such a way that Tact compiler won't realize it (yet!)
    let xs: Slice = beginCell().storeUint(0, 1).endCell().beginParse();
    let x: Int = xs.loadUint(1); // 0

    try {
        throw(101);     // 1. throws with exit code 101
    } catch (err) {     // 2. catches the error and captures its exit code (101) as err
        return err / x; // 3. divides err by x, which is zero, throwing with exit code 4
    }

} catch (err) {         // 4. catches the new error and captures its exit code (4) as err
    //   ^^^ this works without name collisions because the previous err
    //       has a different scope and is only visible inside the previous catch block

    dump(err);          // 5. dumps the last caught exit code (4)
}
```

Note, that similar to [`let{:tact}` statement](#let), captured [exit code](/book/exit-codes) in the `catch (){:tact}` clause can be discarded by specifying an underscore `_{:tact}` in its place:

```tact
try {
    throw(42);
} catch (_) {
    dump("I don't know the exit code anymore");
}
```

<Callout>

  Read more about exit codes on the dedicated page: [Exit codes in the Book](/book/exit-codes).

</Callout>

## Loops

Conditionally repeat certain blocks of code multiple times.

### `repeat` [#repeat-loop]

The `repeat{:tact}` loop executes a block of code a specified number of times. The number of repetitions should be given as a positive $32$-bit [`Int{:tact}`][int] in the inclusive range from $1$ to $2^{31} - 1$. If the value is greater, an error with the [exit code 5](/book/exit-codes#5), `Integer out of the expected range` would be thrown.

If the specified number of repetitions is equal to $0$ or any negative number in the inclusive range $-2^{256}$ to $-1$, it is ignored and the code block is not executed at all.

```tact
let twoPow: Int = 1;

// Repeat exactly 10 times
repeat (10) {
    twoPow *= 2;
}

// Skipped
repeat (-1) {
    twoPow *= 3333;
}

twoPow; // 1024
```

### `while` [#while-loop]

The `while{:tact}` loop continues executing the block of code as long as the given condition is `true{:tact}`.

In the following example, the value of `x` is decremented by $1$ on each iteration, so the loop will run $10$ times:

```tact
let x: Int = 10;
while (x > 0) {
    x -= 1;
}
```

### `do...until` [#do-until-loop]

The `do...until{:tact}` loop is a post-test loop that executes the block of code at least once, and then continues to execute it until the given condition becomes `true{:tact}`.

In the following example, the value of `x` is decremented by $1$ on each iteration, so the loop will run $10$ times:

```tact
let x: Int = 10;
do {
    x -= 1;  // executes this code block at least once
} until (x <= 0);
```

### `foreach` [#foreach-loop]

The `foreach{:tact}` loop operates on key-value pairs (entries) of [`map<K, V>{:tact}`](/book/maps) type in sequential order: from the smallest keys of the map to the biggest ones.

This loop executes a block of code for each entry in the given map, capturing the key and value on each iteration. This is handy when you don't know in advance how many items there is in the map or don't want to explicitly look for each of the entry using [`.get(){:tact}`](/book/maps#get) [method](/book/functions#extension-function) of maps.

Note, that the names of captured key and value pair on each iteration are arbitrary and can be any valid Tact identifier, provided that they're new to the current scope. The most common options are: `k` and `v`, or `key` and `value`.

In the following example, map `cells` has $4$ entries, so the loop will run $4$ times:

```tact
// Empty map
let cells: map<Int, Cell> = emptyMap();

// Setting four entries
cells.set(1, beginCell().storeUint(100, 16).endCell());
cells.set(2, beginCell().storeUint(200, 16).endCell());
cells.set(3, beginCell().storeUint(300, 16).endCell());
cells.set(4, beginCell().storeUint(400, 16).endCell());

// A variable for summing up the values
let sum: Int = 0;

// For each key and value pair in cells map, do:
foreach (key, value in cells) { // or just k, v
    let s: Slice = value.beginParse(); // convert Cell to Slice
    sum += s.loadUint(16);             // sum the Slice values
}
dump(sum); // 1000
```

It's also possible to iterate over a map in contract storage, and over maps as members of instances of [Struct](/book/structs-and-messages#structs) or [Message](/book/structs-and-messages#messages) types:

```tact
import "@stdlib/deploy";

struct Fizz { oh_my: map<Int, Int> }
message Buzz { oh_my: map<Int, Int> }

contract Iterated {
    oh_my: map<Int, Int>;

    receive("call to iterate!") {
        let oh_my: map<Int, Int> = emptyMap();
        oh_my.set(0, 42);
        oh_my.set(1, 27);

        self.oh_my = oh_my; // assigning local map to the storage one
        let fizz = Fizz{ oh_my }; // field punning
        let buzz = Buzz{ oh_my }; // field punning

        // Iterating over map in contract storage
        foreach (key, value in self.oh_my) {
            // ...
        }

        // Iterating over map member of a Struct Fizz instance
        foreach (key, value in fizz.oh_my) {
            // ...
        }

        // Iterating over map member of a Message Buzz instance
        foreach (key, value in buzz.oh_my) {
            // ...
        }
    }
}
```

Note, that similar to [`let{:tact}` statement](#let), either of captured key or value (or both) can be discarded by specifying an underscore `_{:tact}` in their place:

```tact
// Empty map
let quartiles: map<Int, Int> = emptyMap();

// Setting some entries
quartiles.set(1, 25);
quartiles.set(2, 50);
quartiles.set(3, 75);

// Discarding captured keys
// without modifying them in the map itself
foreach (_, value in quartiles) {}

// Discarding captured values
// without modifying them in the map itself
foreach (key, _ in quartiles) {}

// Discarding both keys and values
// without modifying them in the map itself
foreach (_, _ in quartiles) {
    // Can't access via _, but can do desired operations
    // n times, where n is the current length of the map
}
```

<Callout type="warning" emoji="⚠️">

  Note, that at the moment `foreach{:tact}` works only with explicitly provided map identifiers and nested identifier constructions, like `foo.bar.targetMap{:tact}` or `self.baz.targetMap{:tact}`. That is, returning a map from a function and trying to iterate over its entries won't work:

  ```tact
  foreach (k, v in emptyMap()) {
  //               ^ this will give the following error message:
  //                 foreach is only allowed over maps that are path expressions,
  //                 i.e. identifiers, or sequences of direct contract/struct/message accesses,
  //                 like "self.foo" or "self.structure.field"
  }
  ```

  Trying to iterate over a map member of a [Struct](/book/structs-and-messages#structs) returned from a function also won't work, because function call is an expression and not an identifier nor a nested identifier access:

  ```tact
  foreach (k, v in genCoolStruct().map) {
  //               ^ this will give the following error message:
  //                 foreach is only allowed over maps that are path expressions,
  //                 i.e. identifiers, or sequences of direct contract/struct/message accesses,
  //                 like "self.foo" or "self.structure.field"
  }
  ```

</Callout>

<Callout>

  For additional loop examples see: [Loops in Tact-By-Example](https://tact-by-example.org/04-loops).

</Callout>

[int]: /book/integers


## structs-and-messages.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/structs-and-messages.mdx)
# Structs and Messages

import { Callout } from 'nextra/components'

Tact supports a number of [primitive data types](/book/types#primitive-types) that are tailored for smart contract use. However, using individual means of storage often becomes cumbersome, so there are [Structs](#structs) and [Messages](#messages) which allow combining types together.

<Callout type="warning" emoji="⚠️">

  **Warning**: Currently circular types are **not** possible. This means that Struct/Message **A** can't have a field of a Struct/Message **B** that has a field of the Struct/Message **A**.

  Therefore, the following code **won't** compile:

  ```tact
  struct A {
      circularFieldA: B;
  }

  struct B {
      impossibleFieldB: A;
  }
  ```

</Callout>

## Structs

Structs can define complex data types that contain multiple fields of different types. They can also be nested.

```tact
struct Point {
    x: Int as int64;
    y: Int as int64;
}

struct Line {
    start: Point;
    end: Point;
}
```

Structs can also contain default fields and define fields of [optional types](/book/optionals). This can be useful if you have a lot of fields, but don't want to keep having to specify common values for them in [new instances](#instantiate).

```tact
struct Params {
    name: String = "Satoshi"; // default value

    age: Int?; // field with an optional type Int?
               // and default value of null

    point: Point; // nested Structs
}
```

Structs are also useful as return values from getters or other internal functions. They effectively allow a single getter to return multiple return values.

```tact
contract StructsShowcase {
    params: Params; // Struct as a contract's persistent state variable

    init() {
        self.params = Params{
            point: Point{
                x: 4,
                y: 2,
            },
        };
    }

    get fun params(): Params {
        return self.params;
    }
}
```

Note, that the last semicolon `;` in Struct declaration is optional and may be omitted:

```tact
struct Mad { ness: Bool }

struct MoviesToWatch {
    wolverine: String;
    redFunnyGuy: String
}
```

The order of fields matters, as it corresponds to the resulting memory layout in [TL-B schemas](https://docs.ton.org/develop/data-formats/tl-b-language). However, unlike some languages with manual memory management, Tact does not have any padding between fields.

## Messages

Messages can hold [Structs](#structs) in them:

```tact
struct Point {
    x: Int;
    y: Int;
}

message Add {
    point: Point; // holds a struct Point
}
```

Messages are almost the same thing as [Structs](#structs) with the only difference that Messages have a 32-bit integer header in their serialization containing their unique numeric id. This allows Messages to be used with [receivers](/book/receive) since the contract can tell different types of messages apart based on this id.

Tact automatically generates those unique ids for every received Message, but this can be manually overwritten:

```tact
// This Message overwrites its unique id with 0x7362d09c
message(0x7362d09c) TokenNotification {
    forwardPayload: Slice as remaining;
}
```

This is useful for cases where you want to handle certain opcodes (operation codes) of a given smart contract, such as [Jetton standard](https://github.com/ton-blockchain/TEPs/blob/master/text/0074-jettons-standard.md). The short-list of opcodes this contract is able to process is [given here in FunC](https://github.com/ton-blockchain/token-contract/blob/main/ft/op-codes.fc). They serve as an interface to the smart contract.

<Callout>

  For more in-depth information on this see:\
  [Convert received messages to `op` operations](/book/func#convert-received-messages-to-op-operations)\
  [Internal message body layout in TON Docs](https://docs.ton.org/develop/smart-contracts/guidelines/internal-messages#internal-message-body)\
  [Messages of the Jetton implementation in Tact](https://github.com/howardpen9/jetton-implementation-in-tact/blob/9eee917877a92af218002874a9f2bd3f9c619229/sources/messages.tact)\
  [Jetton Standard in Tact on Tact-by-Example](https://tact-by-example.org/07-jetton-standard)

</Callout>

## Operations

### Instantiate

Creation of [Struct](#structs) and [Message](#messages) instances resembles [function calls](/book/expressions#static-function-call), but instead of paretheses `(){:tact}` one needs to specify arguments in braces `{}{:tact}` (curly brackets):

```tact
struct StA {
    field1: Int;
    field2: Int;
}

message MsgB {
    field1: String;
    field2: String;
}

fun example() {
    // Instance of a Struct StA
    StA{
        field1: 42,
        field2: 68 + 1, // trailing comma is allowed
    };

    // Instance of a Message MsgB
    MsgB{
        field1: "May the 4th",
        field2: "be with you!", // trailing comma is allowed
    };
}
```

When the name of a variable or constant assigned to a field coincides with the name of such field, Tact provides a handy syntactic shortcut sometimes called field punning. With it, you don't have to type more than it's necessary:

```tact
struct PopQuiz {
    vogonsCount: Int;
    nicestNumber: Int;
}

fun example() {
    // Let's introduce a couple of variables
    let vogonsCount: Int = 42;
    let nicestNumber: Int = 68 + 1;

    // You may instantiate the Struct as usual and assign variables to fields,
    // but that is a bit repetitive and tedious at times
    PopQuiz{ vogonsCount: vogonsCount, nicestNumber: nicestNumber };

    // Let's use field punning and type less,
    // because our variable names happen to be the same as field names
    PopQuiz{
        vogonsCount,
        nicestNumber, // trailing comma is allowed here too!
    };
}
```

<Callout>

  Because instantiation is an expression in Tact, it's also described on the related page: [Instantiation expression](/book/expressions#instantiation).

</Callout>

### Convert to a `Cell`, `.toCell()` [#tocell]

It's possible to convert an arbitrary [Struct](#structs) or [Message](#messages) to the [`Cell{:tact}`][cell] type by using the `.toCell(){:tact}` [extension function](/book/functions#extension-function):

```tact
struct Big {
    f1: Int;
    f2: Int;
    f3: Int;
    f4: Int;
    f5: Int;
    f6: Int;
}

fun conversionFun() {
    dump(Big{
        f1: 10000000000, f2: 10000000000, f3: 10000000000,
        f4: 10000000000, f5: 10000000000, f6: 10000000000,
    }.toCell()); // x{...cell with references...}
}
```

<Callout>

  See those extension functions in the Reference:\
  [`Struct.toCell(){:tact}`](/ref/core-cells#structtocell)\
  [`Message.toCell(){:tact}`](/ref/core-cells#messagetocell)

</Callout>

### Obtain from a `Cell` or `Slice`, `.fromCell()` and `.fromSlice()` [#fromcellslice]

Instead of manually parsing a [`Cell{:tact}`][cell] or [`Slice{:tact}`][slice] via a series of relevant `.loadSomething(){:tact}` function calls, one can use `.fromCell(){:tact}` and `.fromSlice(){:tact}` [extension functions](/book/functions#extension-function) for converting the provided [`Cell{:tact}`][cell] or [`Slice{:tact}`][slice] into the needed [Struct](#structs) or [Message](#messages).

Those extension functions only attempt to parse a [`Cell{:tact}`][cell] or [`Slice{:tact}`][slice] according to the structure of your [Struct](#structs) or [Message](#messages). In case layouts don't match, various exceptions may be thrown — make sure to wrap your code in [`try...catch{:tact}`](/book/statements#try-catch) blocks to prevent unexpected results.

```tact
struct Fizz { foo: Int }
message(100) Buzz { bar: Int }

fun constructThenParse() {
    let fizzCell = Fizz{foo: 42}.toCell();
    let buzzCell = Buzz{bar: 27}.toCell();

    let parsedFizz: Fizz = Fizz.fromCell(fizzCell);
    let parsedBuzz: Buzz = Buzz.fromCell(buzzCell);
}
```

<Callout>

  See those extension functions in the Reference:\
  [`Struct.fromCell(){:tact}`][st-fc]\
  [`Struct.fromSlice(){:tact}`][st-fs]\
  [`Message.fromCell(){:tact}`][msg-fc]\
  [`Message.fromSlice(){:tact}`][msg-fs]

</Callout>

### Conversion laws

Whenever one converts between [`Cell{:tact}`][cell]/[`Slice{:tact}`][slice] and [Struct](#structs)/[Message](#messages) via `.toCell(){:tact}` and `.fromCell(){:tact}` functions, the following laws hold:

* For any instance of type [Struct](#structs)/[Message](#messages), calling `.toCell(){:tact}` on it, then applying `Struct.fromCell(){:tact}` (or `Message.fromCell(){:tact}`) to the result gives back the copy of the original instance:

```tact {8-9,13-14}
struct ArbitraryStruct {}
message(0x2A) ArbitraryMessage {}

fun lawOne() {
    let structInst = ArbitraryStruct{};
    let messageInst = ArbitraryMessage{};

    ArbitraryStruct.fromCell(structInst.toCell());   // = structInst
    ArbitraryMessage.fromCell(messageInst.toCell()); // = messageInst

    // Same goes for Slices, with .toCell().asSlice() and .fromSlice()

    ArbitraryStruct.fromSlice(structInst.toCell().asSlice());   // = structInst
    ArbitraryMessage.fromSlice(messageInst.toCell().asSlice()); // = messageInst
}
```

* For any [`Cell{:tact}`][cell] with the same [TL-B](https://docs.ton.org/develop/data-formats/tl-b-language) layout as a given [Struct](#structs)/[Message](#messages), calling `Struct.fromCell(){:tact}` (or `Message.fromCell(){:tact}`) on it, and then converting the result to a [`Cell{:tact}`][cell] via `.toCell(){:tact}` would give the copy of the original [`Cell{:tact}`][cell]:

```tact {9-10,15-16}
struct ArbitraryStruct { val: Int as uint32 }
message(0x2A) ArbitraryMessage {}

fun lawTwo() {
    // Using 32 bits to store 42 just so this cellInst can be
    // re-used for working with both ArbitraryStruct and ArbitraryMessage
    let cellInst = beginCell().storeUint(42, 32).endCell();

    ArbitraryStruct.fromCell(cellInst).toCell();  // = cellInst
    ArbitraryMessage.fromCell(cellInst).toCell(); // = cellInst

    // Same goes for Slices, with .fromSlice() and .toCell().asSlice()
    let sliceInst = cellInst.asSlice();

    ArbitraryStruct.fromSlice(sliceInst).toCell().asSlice();  // = sliceInst
    ArbitraryMessage.fromSlice(sliceInst).toCell().asSlice(); // = sliceInst
}
```

[st-fc]: /ref/core-cells#structfromcell
[st-fs]: /ref/core-cells#structfromslice
[msg-fc]: /ref/core-cells#messagefromcell
[msg-fs]: /ref/core-cells#messagefromslice

[p]: /book/types#primitive-types
[cell]: /book/cells#cells
[slice]: /book/cells#slices


## types.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/types.mdx)
# Type system overview

import { Callout } from 'nextra/components'

Every variable, item, and value in Tact programs has a type. They can be:

* One of the [primitive types](#primitive-types)
* or [composite types](#composite-types)

Additionally, many of those types [can be made nullable](#optionals).

## Primitive types

Tact supports a number of primitive data types that are tailored for smart contract use:

* [`Int{:tact}`](/book/integers) — all numbers in Tact are $257$-bit signed integers, but [smaller representations](/book/integers#serialization) can be used to reduce storage costs.
* [`Bool{:tact}`](#booleans) — classical boolean with `true{:tact}` and `false{:tact}` values.
* `Address{:tact}` — standard [smart contract address](https://docs.ton.org/learn/overviews/addresses#address-of-smart-contract) in TON Blockchain.
* [`Cell{:tact}`](/book/cells#cells), [`Builder{:tact}`](/book/cells#builders), [`Slice{:tact}`](/book/cells#slices) — low-level primitives of [TVM][tvm].
* `String{:tact}` — immutable text strings.
* `StringBuilder{:tact}` — helper type that allows you to concatenate strings in a gas-efficient way.

[tvm]: https://docs.ton.org/learn/tvm-instructions/tvm-overview

### Booleans [#booleans]

The primitive type `Bool{:tact}` is the classical boolean type, which can hold only the two values: `true{:tact}` and `false{:tact}`. It's convenient for boolean and logical operations, as well as for storing flags.

There are no implicit type conversions in Tact, so addition ([`+{:tact}`](/book/operators#binary-add)) of two boolean values isn't possible. Hovewer, many comparison [operators](/book/statements#operators) are available, such as:

* `&&{:tact}` for [logical AND](/book/operators#binary-logical-and),
* `||{:tact}` for [logical OR](/book/operators#binary-logical-or),
* `!{:tact}` for [logical inversion](/book/operators#unary-inverse),
* `=={:tact}` and `!={:tact}` for checking [equality](/book/operators#binary-equality),
* and `!!{:tact}` for [non-null assertion](/book/optionals).

Persisting bools to state is very space-efficient, as they only take 1-bit. Storing 1000 bools in state [costs](https://ton.org/docs/develop/smart-contracts/fees#how-to-calculate-fees) about $0.00072$ TON per year.

## Composite types

Using individual means of storage often becomes cumbersome, so there are ways to combine multiple [primitive types](#primitive-types) together to create composite types:

* [Maps](#maps) — associations of keys with values.
* [Structs and Messages](#structs-and-messages) — data structures with typed fields.
* [Optionals](#optionals) — `null{:tact}` values for variables or fields of [Structs and Messages](#structs-and-messages).

In addition to the composite types above, Tact provides a special type constructor [`bounced<T>{:tact}`](/book/bounced), which can only be specified in [bounced message receivers](/book/bounced).

Note, while [contracts](#contracts) and [traits](#traits) are also considered a part of the Tacts type system, one can't pass them around like [Structs and Messages](#structs-and-messages). Instead, it's possible to obtain the initial state of the given contract by using the [`initOf{:tact}`](/book/expressions#initof) expression.

### Maps

The type [`map<K, V>{:tact}`][maps] is used as a way to associate keys of type `K{:tact}` with corresponding values of type `V{:tact}`.

Example of a [`map<K, V>{:tact}`][maps]:

```tact
let mapExample: map<Int, Int> = emptyMap(); // empty map with Int keys and values
```

Learn more about them on a dedicated page: [Maps][maps].

[maps]: /book/maps

### Structs and Messages

[Structs][structs] and [Messages][messages] are two main ways of combining multiple [primitive types](#primitive-types) into a composite one.

Example of a [Struct][structs]:

```tact
struct Point {
    x: Int;
    y: Int;
}
```

Example of a [Message][messages]:

```tact
// Custom numeric id of the Message
message(0x11111111) SetValue {
    key: Int;
    value: Int?; // Optional, Int or null
    coins: Int as coins; // Serialization into TL-B types
}
```

Learn more about them on a dedicated page: [Structs and Messages][s-n-m].

[s-n-m]: /book/structs-and-messages
[structs]: /book/structs-and-messages#structs
[messages]: /book/structs-and-messages#messages

### Optionals

All [primitive types](#primitive-types), as well as [Structs and Messages](#structs-and-messages) could be nullable and hold a special `null{:tact}` value.

Example of an [optional][optionals]:

```tact
let opt: Int? = null; // Int or null, with explicitly assigned null
```

Learn more about them on a dedicated page: [Optionals][optionals].

[optionals]: /book/optionals

### Contracts

[Contracts](/book/contracts) in Tact serve as the main entrypoints of smart contracts of TON blockchain. They hold all [functions](/book/functions), [getters](/book/functions#getter-functions), and [receivers](/book/functions#receiver-functions) of a TON contract, and much more.

Example of a [contract](/book/contracts):

```tact
contract HelloWorld {
    // Persistent state variable
    counter: Int;

    // Constructor function init(), where all the variables are initialized
    init() {
        self.counter = 0;
    }

    // Internal message receiver, which responds to a string message "increment"
    receive("increment") {
        self.counter += 1;
    }

    // Getter function with return type Int
    get fun counter(): Int {
        return self.counter;
    }
}
```

Read more about them on the dedicated page: [Contracts](/book/contracts).

### Traits

Tact doesn't support classical class inheritance, but instead introduces the concept of _traits_, which can be viewed as abstract contracts (like abstract classes in popular object-oriented languages). They have the same structure as [contracts](#contracts), but can't [initialize persistent state variables](/book/contracts#init-function).

A trait can also let the contract inheriting it to override the behavior of its [functions](/book/functions#virtual-and-abstract-functions) and the value of its [constants](/book/constants#virtual-and-abstract-constants).

Example of a trait [`Ownable{:tact}`](/ref/stdlib-ownable#ownable) from [`@stdlib/ownable`](/ref/stdlib-ownable):

```tact
trait Ownable {
    // Persistent state variable, which cannot be initialized in the trait
    owner: Address;

    // Internal function
    fun requireOwner() {
        nativeThrowUnless(132, context().sender == self.owner);
    }

    // Getter function with return type Address
    get fun owner(): Address {
        return self.owner;
    }
}
```

And the [contract](#contracts) that uses trait [`Ownable{:tact}`](/ref/stdlib-ownable#ownable):

```tact
contract Treasure with Ownable {
    // Persistent state variable, which MUST be defined in the contract
    owner: Address;

    // Constructor function init(), where all the variables are initialized
    init(owner: Address) {
        self.owner = owner;
    }
}
```


## upgrades.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/upgrades.mdx)
# Contracts upgrades

Tact currently doesn't allow contract upgrades since Tact contracts have a more convoluted nature than the ones in FunC. It is theoretically possible, but the required tools are not here.


## from-func.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/cs/from-func.mdx)
# Coming from FunC

import { Callout } from 'nextra/components'

<Callout emoji="🚨">
  This page awaits implementation in [#54](https://github.com/tact-lang/tact-docs/issues/54)
</Callout>

## from-solidity.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/book/cs/from-solidity.mdx)
# Coming from Solidity

import { Callout } from 'nextra/components'

<Callout emoji="🚨">
  This page awaits implementation in [#67](https://github.com/tact-lang/tact-docs/issues/67)
</Callout>

## access.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/access.mdx)
# Access control

import { Callout } from 'nextra/components'

This page lists common examples of working with privileges, ownership and access control.

## How to check sender privileges using Ownable trait

```tact
// Ownable has to be imported from stdlib, as well as Deployable, for convenience:
import "@stdlib/ownable";
import "@stdlib/deploy";

message FooBarMsg {
    newVal: Int as uint32;
}

// Ownable trait can limit certain actions to the owner only
contract SenderChecker with Deployable, Ownable {
    // Persistent state variables
    owner: Address;     // Ownable trait requires you to add this exact state variable
    val: Int as uint32; // some value

    init() {
        // we can initialize owner to any value we want, the deployer in this case:
        self.owner = sender();
        self.val = 0;
    }

    receive("inc") {
        self.requireOwner(); // throws exit code 132 if the sender isn't an owner
        self.val += 1;
    }

    receive(msg: FooBarMsg) {
        self.requireOwner(); // throws exit code 132 if the sender isn't an owner
        self.val = msg.newVal;
    }
}
```

<Callout>

  **Useful link:**\
  [`trait Ownable{:tact}` in Core library](/ref/stdlib-ownable#ownable)

</Callout>

<Callout type="info" emoji="🤔">

  Didn't find your favorite example of access control? Have cool implementations in mind? [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## algo.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/algo.mdx)
# Algorithms

import { Callout, Steps } from 'nextra/components'

Algorithm is a finite sequence of rigorous instructions, typically used to solve a class of specific problems or to perform a computation.

<Callout emoji="🚨">

  This page is a stub. [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## data-structures.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/data-structures.mdx)
# Data structures

import { Callout, Steps } from 'nextra/components'

Data structures are data organization, management, and storage formats that are usually chosen for efficient access to data. More precisely, a data structure is a collection of data values, the relationships among them, and the functions or operations that can be applied to the data.

This page lists a handy collection of data structures implemented in Tact for your day-to-day needs and beyond.

All of the data structures listed here are made using the built-in [`map<K, V>{:tact}`][map] type. For the description and basic usage of maps see the [dedicated page in the Book][map].

## Array

An [array](https://en.wikipedia.org/wiki/Array_(data_structure)) is a data structure consisting of a continuous block of memory, which represents a collection of elements of same memory size, each identified by at least one array key or _index_.

Following example emulates an array using a [`map<Int, V>{:tact}`][map] wrapped in a [Struct](/book/structs-and-messages#structs), where `V{:tact}` can be any of the [allowed value types](/book/maps#allowed-types) of the map:

```tact
import "@stdlib/deploy"; // for Deployable trait

struct Array {
    m: map<Int as uint16, Int>; // array of Int values as a map of Ints to Ints,
                                // with serialization of its keys to uint16 to save space
    length: Int = 0;            // length of the array, defaults to 0
}

// Compile-time constant upper bound for our map representing an array.
const MaxArraySize: Int = 5_000; // 5,000 entries max, to stay reasonably far from limits

// Extension mutation function for adding new entries to the end of the array
extends mutates fun append(self: Array, item: Int) {
    require(self.length + 1 <= MaxArraySize, "No space in the array left for new items!");

    self.map.set(self.length, item); // set the entry (key-value pair)
    self.length += 1;                // increase the length field
}

// Extension mutation function for inserting new entries at the given index
extends mutates fun insert(self: Array, item: Int, idx: Int) {
    require(self.length + 1 <= MaxArraySize, "No space in the array left for new items!");
    require(idx >= 0, "Index of the item cannot be negative!");
    require(idx < self.length, "Index is out of array bounds!");

    // Move all items from idx to the right
    let i: Int = self.length; // not a typo, as we need to start from the non-existing place
    while (i > idx) {
        // Note, that we use !! operator as we know for sure that the value would be there
        self.map.set(i, self.map.get(i - 1)!!);
        i -= 1;
    }

    // And put the new item in
    self.map.set(idx, item); // set the entry (key-value pair)
    self.length += 1;        // increase the length field
}

// Extension function for getting the value at the given index
extends fun getIdx(self: Array, idx: Int): Int {
    require(self.length > 0, "No items in the array!");
    require(idx >= 0, "Index of the item cannot be negative!");
    require(idx < self.length, "Index is out of array bounds!");

    // Note, that we use !! operator as we know for sure that the value would be there
    return self.map.get(idx)!!;
}

// Extension function for returning the last value
extends fun getLast(self: Array): Int {
    require(self.length > 0, "No items in the array!");

    // Note, that we use !! operator as we know for sure that the value would be there
    return self.map.get(self.length - 1)!!;
}

// Extension mutation function for deleting and entry at the given index and returning its value
extends mutates fun deleteIdx(self: Array, idx: Int): Int {
    require(self.length > 0, "No items in the array to delete!");
    require(idx >= 0, "Index of the item cannot be negative!");
    require(idx < self.length, "Index is out of array bounds!");

    // Remember the value, which is going to be deleted
    let memorized: Int = self.map.get(idx)!!;

    // Move all items from idx and including to the left
    let i: Int = idx;
    while (i + 1 < self.length) {
        // Note, that we use !! operator as we know for sure that the value would be there
        self.map.set(i, self.map.get(i + 1)!!);
        i += 1;
    }

    self.map.set(self.length - 1, null); // delete the last entry
    self.length -= 1;                    // decrease the length field

    return memorized;
}

// Extension mutation function for deleting the last entry and returning its value
extends fun deleteLast(self: Array): Int {
    require(self.length > 0, "No items in the array!");

    // Note, that we use !! operator as we know for sure that the value would be there
    let lastItem: Int = self.map.get(self.length - 1)!!;
    self.map.set(self.length - 1, null); // delete the entry
    self.length -= 1;                    // decrease the length field

    return lastItem;
}

// Extension function for deleting all items in the Array
extends mutates fun deleteAll(self: Array) {
    self.map = emptyMap();
    self.length = 0;
}

// Global static function for creating an empty Array
fun emptyArray(): Array {
    return Array{m: emptyMap(), length: 0}; // length defaults to 0
}

// Contract, with emulating an Array using the map
contract MapAsArray with Deployable {
    // Persistent state variables
    array: Array;

    // Constructor (initialization) function of the contract
    init() {
        self.array = emptyArray();
    }

    // Internal message receiver, which responds to a String message "append"
    receive("append") {
        // Add a new item
        self.array.append(42);
    }

    // Internal message receiver, which responds to a String message "delete_5h"
    receive("delete_5th") {
        // Remove the 5th item if it exists and reply back with its value, or raise an error
        self.reply(self.array.deleteIdx(4).toCoinsString().asComment()); // index offset 0 + 4 gives the 5th item
    }

    // Internal message receiver, which responds to a String message "del_last"
    receive("del_last") {
        // Remove the last item and reply back with its value, or raise an error
        self.reply(self.array.deleteLast().toCoinsString().asComment());
    }

    // Internal message receiver, which responds to a String message "get_last"
    receive("get_last") {
        // Reply back with the latest item in the array if it exists, or raise an error
        self.reply(self.array.getLast().toCoinsString().asComment());
    }

    // Internal message receiver, which responds to a String message "delete_all"
    receive("delete_all") {
        self.array.deleteAll();
    }
}
```

## Stack

A [stack](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)) is a data structure consisting of a collection of elements with two main operations:

* push, which adds an element to the end of the collection
* pop, which removes the most recently added element

Following example emulates a stack using a [`map<Int, V>{:tact}`][map] wrapped in a [Struct](/book/structs-and-messages#structs), where `V{:tact}` can be any of the [allowed value types](/book/maps#allowed-types) of the map:

```tact
import "@stdlib/deploy"; // for Deployable trait

struct Stack {
    m: map<Int as uint16, Int>; // stack of Int values as a map of Ints to Ints,
                                // with serialization of its keys to uint16 to save space
    length: Int = 0;            // length of the stack, defaults to 0
}

// Compile-time constant upper bound for our map representing an stack.
const MaxStackSize: Int = 5_000; // 5,000 entries max, to stay reasonably far from limits

// Extension mutation function for adding new entries to the end of the stack
extends mutates fun push(self: Stack, item: Int) {
    require(self.length + 1 <= MaxStackSize, "No space in the stack left for new items!");

    self.map.set(self.length, item); // set the entry (key-value pair)
    self.length += 1;                // increase the length field
}

// Extension mutation function for deleting the last entry and returning its value
extends mutates fun pop(self: Stack): Int {
    require(self.length > 0, "No items in the stack to delete!");

    // Note, that we use !! operator as we know for sure that the value would be there
    let lastItem: Int = self.map.get(self.length - 1)!!;
    self.map.set(self.length - 1, null); // delete the entry
    self.length -= 1;                    // decrease the length field

    return lastItem;
}

// Extension function for returning the last value
extends fun peek(self: Stack): Int {
    require(self.length > 0, "No items in the stack!");

    // Note, that we use !! operator as we know for sure that the value would be there
    return self.map.get(self.length - 1)!!;
}

// Extension function for deleting all items in the Stack
extends mutates fun deleteAll(self: Stack) {
    self.map = emptyMap();
    self.length = 0;
}

// Global static function for creating an empty Stack
fun emptyStack(): Stack {
    return Stack{m: emptyMap(), length: 0}; // length defaults to 0
}

contract MapAsStack with Deployable {
    // Persistent state variables
    stack: Stack; // our stack, which uses the map

    // Constructor (initialization) function of the contract
    init() {
        self.stack = emptyStack();
    }

    // Internal message receiver, which responds to a String message "push"
    receive("push") {
        // Add a new item
        self.stack.push(42);
    }

    // Internal message receiver, which responds to a String message "pop"
    receive("pop") {
        // Remove the last item and reply with it
        self.reply(self.stack.pop().toCoinsString().asComment());
    }

    // Internal message receiver, which responds to a String message "peek"
    receive("peek") {
        // Reply back with the latest item in the map if it exists, or raise an error
        self.reply(self.stack.peek().toCoinsString().asComment());
    }

    // Internal message receiver, which responds to a String message "delete_all"
    receive("delete_all") {
        self.stack.deleteAll();
    }

    // Getter function for obtaining the stack
    get fun map(): map<Int, Int> {
        return self.stack.map;
    }

    // Getter function for obtaining the current length of the stack
    get fun length(): Int {
        return self.stack.length;
    }
}
```

## Circular buffer

A [circular buffer](https://en.wikipedia.org/wiki/Circular_buffer) (circular queue, cyclic buffer or ring buffer) is a data structure, which uses a single, fixed-size [buffer](https://en.wikipedia.org/wiki/Data_buffer) as it were connected end-to-end.

Following example emulates a circular buffer using a [`map<Int, V>{:tact}`][map] wrapped in a [Struct](/book/structs-and-messages#structs), where `V{:tact}` can be any of the [allowed value types](/book/maps#allowed-types) of the map:

```tact
import "@stdlib/deploy"; // for Deployable trait

struct CircularBuffer {
    m: map<Int as uint8, Int>; // circular buffer of Int values as a map of Ints to Ints,
                               // with serialization of its keys to uint8 to save space
    length: Int = 0;           // length of the circular buffer, defaults to 0
    start: Int = 0;            // current index into the circular buffer, defaults to 0
}

// Compile-time constant upper bound for our map representing a circular buffer.
const MaxCircularBufferSize: Int = 5;

// Extension mutation function for putting new items to the circular buffer
extends mutates fun put(self: CircularBuffer, item: Int) {
    if (self.length < MaxCircularBufferSize) {
        self.map.set(self.length, item); // store the item
        self.length += 1;                // increase the length field
    } else {
        self.map.set(self.start, item);                        // store the item, overriding previous entry
        self.start = (self.start + 1) % MaxCircularBufferSize; // update starting position
    }
}

// Extension mutation function for getting an item from the circular buffer
extends mutates fun getIdx(self: CircularBuffer, idx: Int): Int {
    require(self.length > 0, "No items in the circular buffer!");
    require(idx >= 0, "Index of the item cannot be negative!");

    if (self.length < MaxCircularBufferSize) {
        // Note, that we use !! operator as we know for sure that the value would be there
        return self.map.get(idx % self.length)!!;
    }

    // Return the value rotating around the circular buffer, also guaranteed to be there
    return self.map.get((self.start + idx) % MaxCircularBufferSize)!!;
}

// Extension function for iterating over all items in the circular buffer and dumping them to the console
extends fun printAll(self: CircularBuffer) {
    let i: Int = self.start;
    repeat (self.length) {
        dump(self.map.get(i)!!); // !! tells the compiler this can't be null
        i = (i + 1) % MaxCircularBufferSize;
    }
}

// Extension function for deleting all items in the CircularBuffer
extends mutates fun deleteAll(self: CircularBuffer) {
    self.map = emptyMap();
    self.length = 0;
    self.start = 0;
}

// Global static function for creating an empty CircularBuffer
fun emptyCircularBuffer(): CircularBuffer {
    return CircularBuffer{m: emptyMap(), length: 0, start: 0}; // length and start default to 0
}

// This contract records the last 5 timestamps of when "timer" message was received
contract MapAsCircularBuffer with Deployable {
    // Persistent state variables
    cBuf: CircularBuffer; // our circular buffer, which uses a map

    // Constructor (initialization) function of the contract
    init() {
        self.cBuf = emptyCircularBuffer();
    }

    // Internal message receiver, which responds to a String message "timer"
    // and records the timestamp when it receives such message
    receive("timer") {
        let timestamp: Int = now();
        self.cBuf.put(timestamp);
    }

    // Internal message receiver, which responds to a String message "get_first"
    // and replies with the first item of the circular buffer
    receive("get_first") {
        self.reply(self.cBuf.getIdx(0).toCoinsString().asComment());
    }

    // Internal message receiver, which responds to a String message "print_all"
    receive("print_all") {
        self.cBuf.printAll();
    }

    // Internal message receiver, which responds to a String message "delete_all"
    receive("delete_all") {
        self.cBuf.deleteAll();
    }
}
```

<Callout>

  This example is adapted from [Arrays page in Tact-By-Example](https://tact-by-example.org/04-arrays).

</Callout>

<Callout type="info" emoji="🤔">

  Didn't find your favorite example of working with data structures? Have cool implementations in mind? [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>

[map]: /book/maps


## index.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/index.mdx)
# Cookbook overview

import { Callout, Steps, Cards } from 'nextra/components'
import { OneIcon, FormulaIcon, DiagramIcon, DropperIcon, BoxIcon, IdCardIcon, WarningIcon, StarsIcon, RowsIcon, GearIcon, LightningIcon } from '@components/icons'

The main reason for making the Tact Cookbook is to gather all the experiences of Tact developers in one place so that future developers can use it. This section of the documentation is more focused on everyday tasks that every Tact developer resolves during the development of smart contracts.

Use it as a recipe book for cooking up delightful smart contracts on TON Blockchain without re-inventing the wheel in the process.

<Steps>

### Single contract [#single-contract]

Following pages focus on single-contract examples and cover a wide range of topics:

<Cards>
  <Cards.Card
    icon={<OneIcon />}
    title="Single-contract communication"
    href="/cookbook/single-communication"
  />
  <Cards.Card
    icon={<GearIcon />}
    title="Type conversion"
    href="/cookbook/type-conversion"
  />
  <Cards.Card
    icon={<BoxIcon />}
    title="Data structures"
    href="/cookbook/data-structures"
  />
  <Cards.Card
    icon={<FormulaIcon />}
    title="Algorithms"
    href="/cookbook/algo"
  />
  <Cards.Card
    icon={<RowsIcon />}
    title="Time and date"
    href="/cookbook/time"
  />
  <Cards.Card
    icon={<WarningIcon />}
    title="Access control"
    href="/cookbook/access"
  />
  <Cards.Card
    icon={<StarsIcon />}
    title="Randomness"
    href="/cookbook/random"
  />
  <Cards.Card
    icon={<DropperIcon />}
    title="Miscellaneous"
    href="/cookbook/misc"
  />
</Cards>

### Multiple contracts [#multiple-contracts]

Following pages focus on multi-contract examples, exploring the scalable nature of TON Blockchain:

<Cards>
  <Cards.Card
    icon={<DiagramIcon />}
    title="Multi-contract communication"
    href="/cookbook/multi-communication"
  />
  <Cards.Card
    icon={<LightningIcon />}
    title="Fungible Tokens (Jettons)"
    href="/cookbook/jettons"
  />
  <Cards.Card
    icon={<IdCardIcon />}
    title="Non-Fungible Tokens (NFTs)"
    href="/cookbook/nfts"
  />
</Cards>

Additionally, there are examples of working with popular TON DEXes (Decentralized EXchanges), which often require many contracts and complex logic:

<Cards>
  <Cards.Card
    arrow
    title="DeDust.io"
    href="/cookbook/dexes/dedust"
  />
  <Cards.Card
    arrow
    title="STON.fi"
    href="/cookbook/dexes/stonfi"
  />
</Cards>

</Steps>


## jettons.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/jettons.mdx)
# Fungible Tokens (Jettons)

import { Callout } from 'nextra-theme-docs';

This page lists common examples of working with [jettons](https://docs.ton.org/develop/dapps/asset-processing/jettons).

## Accepting jetton transfer

Transfer notification message have the following structure.

```tact
message(0x7362d09c) JettonTransferNotification {
    queryId: Int as uint64;
    amount: Int as coins;
    sender: Address;
    forwardPayload: Slice as remaining;
}
```

Use [receiver](/book/receive) function to accept token notification message.

<Callout type="warning" emoji="⚠️">

  Sender of transfer notification must be validated!

</Callout>

Validation can be done using jetton wallet state init and calculating jetton address.
Note, that notifications are coming from YOUR contract's jetton wallet, so [`myAddress()`](/ref/core-common#myaddress) should be used in owner address field.
Wallet initial data layout is shown below, but sometimes it can differ.
Note that `myJettonWalletAddress` may also be stored in contract storage to use less gas in every transaction.

```tact
struct JettonWalletData {
    balance: Int as coins;
    ownerAddress: Address;
    jettonMasterAddress: Address;
    jettonWalletCode: Cell;
}

fun calculateJettonWalletAddress(ownerAddress: Address, jettonMasterAddress: Address, jettonWalletCode: Cell): Address {
    let initData = JettonWalletData{
        balance: 0,
        ownerAddress,
        jettonMasterAddress,
        jettonWalletCode,
    };

    return contractAddress(StateInit{code: jettonWalletCode, data: initData.toCell()});
}

contract Sample {
    jettonWalletCode: Cell;
    jettonMasterAddress: Address;

    init(jettonWalletCode: Cell, jettonMasterAddress: Address) {
        self.jettonWalletCode = jettonWalletCode;
        self.jettonMasterAddress = jettonMasterAddress;
    }

    receive(msg: JettonTransferNotification) {
        let myJettonWalletAddress = calculateJettonWalletAddress(myAddress(), self.jettonMasterAddress, self.jettonWalletCode);
        require(sender() == myJettonWalletAddress, "Notification not from your jetton wallet!");

        // your logic of processing token notification
    }
}
```

## Sending jetton transfer

To send jetton transfer use [`send(){:tact}`](/book/send) function.
Note that `myJettonWalletAddress` may also be stored in contract storage to use less gas in every transaction.

```tact
message(0xf8a7ea5) JettonTransfer {
    queryId: Int as uint64;
    amount: Int as coins;
    destination: Address;
    responseDestination: Address?;
    customPayload: Cell? = null;
    forwardTonAmount: Int as coins;
    forwardPayload: Slice as remaining;
}

receive("send") {
    let myJettonWalletAddress = calculateJettonWalletAddress(myAddress(), self.jettonMasterAddress, self.jettonWalletCode);
    send(SendParameters{
        to: myJettonWalletAddress,
        value: ton("0.05"),
        body: JettonTransfer{
            queryId: 42,
            amount: jettonAmount, // jetton amount you want to transfer
            destination: msg.userAddress, // address you want to transfer jettons. Note that this is address of jetton wallet owner, not jetton wallet itself
            responseDestination: msg.userAddress, //  address where to send a response with confirmation of a successful transfer and the rest of the incoming message Toncoins
            customPayload: null, // in most cases will be null and can be omitted. Needed for custom logic on Jetton Wallets itself
            forwardTonAmount: 1, // amount that will be transferred with JettonTransferNotification. Needed for custom logic execution like in example below. If the amount is 0 notification won't be sent
            forwardPayload: rawSlice("F") // precomputed beginCell().storeUint(0xF, 4).endCell().beginParse(). This works for simple transfer, if needed any struct can be used as `forwardPayload`
        }.toCell(),
    });
}
```

## Burning jetton

```tact
message(0x595f07bc) JettonBurn {
    queryId: Int as uint64;
    amount: Int as coins;
    responseDestination: Address?;
    customPayload: Cell? = null;
}

receive("burn") {
    let myJettonWalletAddress = calculateJettonWalletAddress(myAddress(), self.jettonMasterAddress, self.jettonWalletCode);
    send(SendParameters{
        to: myJettonWalletAddress,
        body: JettonBurn{
            queryId: 42,
            amount: jettonAmount, // jetton amount you want to burn
            responseDestination: someAddress, // address where to send a response with confirmation of a successful burn and the rest of the incoming message coins
            customPayload: null, // in most cases will be null and can be omitted. Needed for custom logic on jettons itself
        }.toCell(),
    });
}
```

## USDT jetton operations

Operations with USDT (on TON) remain the same, except that the  `JettonWalletData` will have the following structure:

```tact
struct JettonWalletData {
    status: Ins as uint4;
    balance: Int as coins;
    ownerAddress: Address;
    jettonMasterAddress: Address;
}
```

Function to calculate wallet address will look like this:

```tact
fun calculateJettonWalletAddress(ownerAddress: Address, jettonMasterAddress: Address, jettonWalletCode: Cell): Address {
    let initData = JettonWalletData{
        status: 0,
        balance: 0,
        ownerAddress,
        jettonMasterAddress,
    };

    return contractAddress(StateInit{code: jettonWalletCode, data: initData.toCell()});
}
```

<Callout type="info" emoji="🤔">

  Didn't find your favorite example of a jettons communication? Have cool implementations in mind? [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## misc.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/misc.mdx)
# Miscellaneous

import { Callout } from 'nextra/components'

Various niche examples which don't yet have a dedicated page, but are useful and interesting nonetheless.

## How to throw errors

The `throw(){:tact}` function in a contract is useful when we don't know how often to perform a specific action.

It allows intentional exception or error handling, which leads to the termination of the current transaction and reverts any state changes made during that transaction.

```tact
let number: Int = 198;

// the error will be triggered anyway
throw(36);

// the error will be triggered only if the number is greater than 50
nativeThrowIf(35, number > 50);

// the error will be triggered only if the number is NOT EQUAL to 198
nativeThrowUnless(39, number == 198);
```

<Callout>

  **Useful links:**\
  [`throw(){:tact}` in Core library](/ref/core-debug#throw)\
  [Errors in Tact-By-Example](https://tact-by-example.org/03-errors)

</Callout>

<Callout type="info" emoji="🤔">

  Didn't find your favorite example of working with something niche? Have cool implementations in mind? [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## multi-communication.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/multi-communication.mdx)
# Multi-contract communication

import { Callout } from 'nextra/components'

<Callout emoji="🚨">

  This page is a stub. [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## nfts.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/nfts.mdx)
# Non-Fungible Tokens (NFTs)

import { Callout } from 'nextra/components'

<Callout emoji="🚨">

  This page is a stub. [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## random.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/random.mdx)
# Randomness

import { Callout } from 'nextra/components'

This page lists examples of working with random numbers, uncertainty and randomness in general.

## How to generate a random number

```tact
// Declare a variable to store the random number
let number: Int;

// Generate a new random number, which is an unsigned 256-bit integer
number = randomInt();

// Generate a random number between 1 and 12
number = random(1, 12);
```

<Callout>

  **Useful links:**\
  [`randomInt(){:tact}` in Core library](/ref/core-random#randomInt)\
  [`random(){:tact}` in Core library](/ref/core-random#random)

</Callout>

<Callout type="info" emoji="🤔">

  Didn't find your favorite example of working with randomness? Have cool implementations in mind? [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## single-communication.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/single-communication.mdx)
# Single-contract Communication

import { Callout } from 'nextra/components'

This page lists examples of communication of a single deployed contract with other contracts on blockchain.

For examples of communication between multiple deployed contracts see: [Multi-contract communication](/cookbook/multi-communication).

## How to make a basic reply

```tact
receive() {
    self.reply("Hello, World!".asComment()); // asComment converts a String to a Cell with a comment
}
```

## How to send a simple message

```tact
send(SendParameters{
    bounce: true, // default
    to: destinationAddress,
    value: ton("0.01"), // attached amount of Tons to send
    body: "Hello from Tact!".asComment(), // comment (optional)
});
```

## How to send a message with the entire balance

If we need to send the whole balance of the smart contract, then we should use the `SendRemainingBalance{:tact}` send mode. Alternatively, we can use `mode: 128{:tact}`, which has the same meaning.

```tact
send(SendParameters{
    // bounce = true by default
    to: sender(), // send the message back to the original sender
    value: 0,
    mode: SendRemainingBalance, // or mode: 128
    body: "Hello from Tact!".asComment(), // comment (optional)
});
```

## How to send a message with the remaining value

If we want to make a reply to the same sender, we can use the mode `SendRemainingValue{:tact}` (i.e. `mode: 64{:tact}`), which carries all the remaining value of the inbound message in addition to the value initially indicated in the new message.

```tact
send(SendParameters{
    // bounce = true by default
    to: sender(), // send the message back to the original sender
    value: 0,
    mode: SendRemainingValue,
    body: "Hello from Tact!".asComment(), // comment (optional)
});
```

It's often useful to add the `SendIgnoreErrors{:tact}` flag too, in order to ignore any errors arising while processing this message during the action phaseL

```tact
send(SendParameters{
    // bounce = true by default
    to: sender(), // send the message back to the original sender
    value: 0,
    mode: SendRemainingValue | SendIgnoreErrors, // prefer using | over + for the mode
    body: "Hello from Tact!".asComment(), // comment (optional)
});
```

The latter example is identical to using a [`.reply(){:tact}` function](#how-to-make-a-basic-reply).

## How to send a message with a long text comment

If we need to send a message with a lengthy text comment, we should create a [`String{:tact}`](/book/types#primitive-types) that consists of more than $127$ characters. To do this, we can utilize the [`StringBuilder{:tact}`](/book/types#primitive-types) primitive type and its methods called `beginComment(){:tact}` and `append(){:tact}`. Prior to sending, we should convert this string into a cell using the `toCell(){:tact}` method.

```tact
let comment: StringBuilder = beginComment();
let longString = "..."; // Some string with more than 127 characters.
comment.append(longString);

send(SendParameters{
    // bounce = true by default
    to: sender(),
    value: 0,
    mode: SendIgnoreErrors,
    body: comment.toCell(),
});
```

<Callout>

  **Useful links:**\
  ["Sending messages" in the Book](/book/send#send-message)\
  ["Message `mode`" in the Book](/book/message-mode)\
  [`StringBuilder{:tact}` in the Book](/book/types#primitive-types)\
  [`Cell{:tact}` in Core library](/ref/core-cells)

</Callout>

<Callout type="info" emoji="🤔">

  Didn't find your favorite example of a single-contract communication? Have cool implementations in mind? [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## time.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/time.mdx)
# Time and date

import { Callout } from 'nextra/components'

## How to get the current time

Use the `now(){:tact}` method to obtain the current standard [Unix time](https://en.wikipedia.org/wiki/Unix_time).

If you need to store the time in state or encode it in a message, use the following [serialization](/book/integers#serialization): `Int as uint32{:tact}`.

```tact
let currentTime: Int = now();

if (currentTime > 1672080143) {
    // do something
}
```

<Callout>

  **Useful links:**\
  [`now(){:tact}` in Core library](/ref/core-common#now)\
  ["Current Time" in Tact-By-Example](https://tact-by-example.org/04-current-time)

</Callout>

<Callout type="info" emoji="🤔">

  Didn't find your favorite example of working with time and date? Have cool implementations in mind? [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>


## type-conversion.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/type-conversion.mdx)
# Type conversion

import { Callout, Steps } from 'nextra/components'

This page shows examples of converting between [primitive types][p] and obtaining them from [composite types](/book/types#composite-types).

## `Int` ↔ `String` [#int-string]

### How to convert a `String` to an `Int`

```tact
// Defining a new extension function for type String that returns value of type Int
// Caution: produces unexpected results when String contains non-numeric characters!
extends fun toInt(self: String): Int {
    // Cast the String as a Slice for parsing
    let string: Slice = self.asSlice();

    // A variable to store the accumulated number
    let acc: Int = 0;

    // Loop until the String is empty
    while (!string.empty()) {
        let char: Int = string.loadUint(8); // load 8 bits (1 byte) from the Slice
        acc = (acc * 10) + (char - 48);     // using ASCII table to get numeric value
        // Note, that this approach would produce unexpected results
        //   when the starting String contains non-numeric characters!
    }

    // Produce the resulting number
    return acc;
}

fun runMe() {
    let string: String = "26052021";
    dump(string.toInt());
}
```

### How to convert an `Int` to a `String`

```tact
let number: Int = 261119911;

// Converting the [number] to a String
let numberString: String = number.toString();

// Converting the [number] to a float String,
//   where passed argument 3 is the exponent of 10^(-3) of resulting float String,
//   and it can be any integer between 0 and 76 including both ends
let floatString: String = number.toFloatString(3);

// Converting the [number] as coins to a human-readable String
let coinsString: String = number.toCoinsString();

dump(numberString); // "261119911"
dump(floatString);  // "261119.911"
dump(coinsString);  // "0.261119911"
```

<Callout>

  **Useful links:**\
  [`Int.toString(){:tact}` in Core library](/ref/core-strings#inttostring)\
  [`Int.toFloatString(){:tact}` in Core library](/ref/core-strings#inttofloatstring)\
  [`Int.toCoinsString(){:tact}` in Core library](/ref/core-strings#inttocoinsstring)

</Callout>

## `Struct` or `Message` ↔ `Cell` or `Slice` [#structmessage-cellslice]

### How to convert an arbitrary `Struct` or `Message` to a `Cell` or a `Slice`

```tact {19-20, 22-23}
struct Profit {
    big: String?;
    dict: map<Int, Int as uint64>;
    energy: Int;
}

message(0x45) Nice {
    maybeStr: String?;
}

fun convert() {
    let st = Profit{
        big: null,
        dict: null,
        energy: 42,
    };
    let msg = Nice{ maybeStr: "Message of the day!" };

    st.toCell();
    msg.toCell();

    st.toCell().asSlice();
    msg.toCell().asSlice();
}
```

<Callout>

  **Useful links:**\
  [`Struct.toCell(){:tact}` in Core library](/ref/core-cells#structtocell)\
  [`Message.toCell(){:tact}` in Core library](/ref/core-cells#messagetocell)

</Callout>

### How to convert a `Cell` or a `Slice` to an arbitrary `Struct` or `Message`

```tact {19-20, 22-23}
struct Profit {
    big: String?;
    dict: map<Int, Int as uint64>;
    energy: Int;
}

message(0x45) Nice {
    maybeStr: String?;
}

fun convert() {
    let stCell = Profit{
        big: null,
        dict: null,
        energy: 42,
    }.toCell();
    let msgCell = Nice{ maybeStr: "Message of the day!" }.toCell();

    Profit.fromCell(stCell);
    Nice.fromCell(msgCell);

    Profit.fromSlice(stCell.asSlice());
    Nice.fromSlice(msgCell.asSlice());
}
```

<Callout>

  **Useful links:**\
  [`Struct.fromCell(){:tact}` in Core library](/ref/core-cells#structfromcell)\
  [`Struct.fromSlice(){:tact}` in Core library](/ref/core-cells#structfromslice)\
  [`Message.fromCell(){:tact}` in Core library](/ref/core-cells#messagefromcell)\
  [`Message.fromSlice(){:tact}` in Core library](/ref/core-cells#messagefromslice)

</Callout>

<Callout type="info" emoji="🤔">

  Didn't find your favorite example of type conversion? Have cool implementations in mind? [Contributions are welcome!](https://github.com/tact-lang/tact-docs/issues)

</Callout>

[p]: /book/types#primitive-types


## dedust.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/dexes/dedust.mdx)
# DeDust.io

import { Callout, Steps, Tabs } from 'nextra/components'

{/* See: https://nextra.site/docs/guide/built-ins */}

[DeDust](https://dedust.io) is a decentralized exchange (DEX) and automated market maker (AMM) built natively on [TON Blockchain](https://ton.org) and [DeDust Protocol 2.0](https://docs.dedust.io/reference/tlb-schemes). DeDust is designed with a meticulous attention to user experience (UX), gas efficiency, and extensibility.

<Callout emoji="🚨">

  This page is a stub until it gets new content in [#146](https://github.com/tact-lang/tact-docs/issues/146).

</Callout>


## stonfi.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/cookbook/dexes/stonfi.mdx)
# STON.fi

import { Callout, Steps, Tabs } from 'nextra/components'

{/* See: https://nextra.site/docs/guide/built-ins */}

[STON.fi](https://ston.fi) is a decentralized automated market maker (AMM) built on [TON blockchain](https://ton.org) providing virtually zero fees, low slippage, an extremely easy interface, and direct integration with TON wallets.

<Callout emoji="🚨">

  This page is a stub until it gets new content in [#149](https://github.com/tact-lang/tact-docs/issues/149).

</Callout>


## index.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ecosystem/index.mdx)
# Ecosystem overview

import { Cards, Steps } from 'nextra/components'

Welcome to the **Ecosystem** section — a bird-eye overview of Tact ecosystem, tools and ways you can start contributing to those!

Here are its main contents:

<Steps>

### Tools

[Tools](/ecosystem/tools/overview) sub-section is a list of official and community-made tools made specifically for Tact, or whose that play along with the language and other tools. Each tool has a brief usage details and additional information, which sometimes is missing from the respective docs or is a convenient summary available only in the Tact documentation.

<Cards>
  <Cards.Card
    arrow
    title="Go to tools overview"
    href="/ecosystem/tools/overview"
  />
</Cards>

</Steps>


## jetbrains.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ecosystem/tools/jetbrains.mdx)
# TON Development Plugin for JetBrains IDEs

Supports highlighting Tact's syntax in JetBrains IDEs versioned **2023.** and later. Note, that besides support for Tact, it also includes a rich support of FunC and Fift languages of TON Blockchain, as well as TL-B schemas.

Plugin on the JetBrains Marketplace: [TON Development Plugin](https://plugins.jetbrains.com/plugin/23382-ton)

## Installation manual

1. Open your JetBrains IDE (IntelliJ IDEA, PyCharm, WebStorm, etc.)
2. Navigate to the **Plugin Marketplace** by selecting `File > Settings/Preferences > Plugins`
3. In the Plugin Marketplace's search bar, type "TON Development". You will see a dropdown with the extension provided by `TON Foundation`.
4. Click the **Install** button next to the plugin name. Wait for the installation to complete.
5. Once the plugin is installed, you will be prompted to restart your JetBrains IDE. Click the **Restart** button to apply changes.
6. After restarting, the TON Development plugin should now be successfully installed in your JetBrains IDE.

## Troubleshooting

If you encounter issues during the installation process, please consult the [plugin's GitHub repository](https://github.com/ton-blockchain/intellij-ton) for solutions and further information.

## References and Resources

- [Plugin on GitHub](https://github.com/ton-blockchain/intellij-ton)
- [Plugin on the JetBrains Marketplace](https://plugins.jetbrains.com/plugin/23382-ton)

## misti.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ecosystem/tools/misti.mdx)
# Misti

[Misti](https://nowarp.github.io/tools/misti/) is a static program analysis tool that supports Tact.

## What is Misti?

* **Static Program Analysis**: Misti analyzes code without executing it, scanning for [bugs and security flaws](https://nowarp.github.io/tools/misti/docs/detectors) by examining the structure and syntax. This approach catches issues early, preventing them from reaching production.
* **Custom Detectors**: Customize Misti to your specific needs by creating [custom detectors](https://nowarp.github.io/tools/misti/docs/hacking/custom-detector). This helps identify vulnerabilities that generic tools might miss, ensuring a thorough review of your code.
* **CI/CD Integration**: [Integrate](https://nowarp.github.io/tools/misti/docs/tutorial/ci-cd) Misti into your CI/CD pipeline to ensure continuous code quality checks, catching issues before they make it to production.

## Resources

* [Github](https://github.com/nowarp/misti)
* [Telegram Community](https://t.me/misti_dev)
* [Misti Documentation](https://nowarp.github.io/docs/misti/)
* [Misti API Reference](https://nowarp.github.io/docs/misti/api)


## overview.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ecosystem/tools/overview.mdx)
# Tools Overview

import { Cards } from 'nextra/components'

This sub-section contains a list of official and community-made tools made specifically for Tact, or whose that play along with the language and other tools. Each tool has a brief usage details and additional information, which sometimes is missing from the respective docs or is a convenient summary available only in the Tact documentation.

<Cards>
  <Cards.Card
    arrow
    title="Typescript"
    href="/ecosystem/tools/typescript"
  />
  <Cards.Card
    arrow
    title="Misti Static Analyzer"
    href="/ecosystem/tools/misti"
  />
  <Cards.Card
    arrow
    title="VS Code Extension"
    href="/ecosystem/tools/vscode"
  />
  <Cards.Card
    arrow
    title="JetBrains IDEs Plugin"
    href="/ecosystem/tools/jetbrains"
  />
</Cards>


## typescript.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ecosystem/tools/typescript.mdx)
# TypeScript Libraries

The Tact language has built-in support for the [@ton/ton](https://github.com/ton-org/ton) and [@ton/core](https://github.com/ton-org/ton-core) TypeScript libraries. The compiler automatically generates code for these libraries, so you can use [@tact-lang/emulator](https://github.com/tact-lang/tact-emulator) or [@ton/sandbox](https://github.com/ton-org/sandbox), that work on top of them.

## Tact contract in TypeScript

The compiler generates files named `{project}_{contract}.ts` for each contract in your [project](/book/config#projects), which contain ready-to-use strongly typed wrappers for working with it in any TypeScript-powered environment: for [testing](/book/debug), [deployments](/book/deploy), etc.


## vscode.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ecosystem/tools/vscode.mdx)
# VS Code Extension

Provides extensive support for Tact language in the Visual Studio Code:

* Syntax highlighting
* Error highlighting
* Snippets
* Information on hover
* Code completion for all variables, functions, global parameters and unique types of Tact
* Code completion for all contracts / libraries in the current file and all referenced imports
* Formatting

Extension on the VS Code Marketplace: [Tact Language Support for TON blockchain](https://marketplace.visualstudio.com/items?itemName=KonVik.tact-lang-vscode)

## Installation manual

1. Open Visual Studio Code (shortly referred to as VS Code).
2. Navigate to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window. It looks like a square within a square.
3. In the Extensions view input box, type "Tact Language". You should see a dropdown with the extension "Tact Language" provided by KonVik. Probably, you would see the similar extension provided by TON Community, but that one is deprecated and **we should use KonVik's one instead**.
4. Click on the install button next to the extension name. Wait until the installation is complete.
5. Once the extension is installed, you might need to reload VS Code. If necessary, there will be a Reload button next to the extension. Click on this button if it appears.
6. The Tact Language extension should now be installed on your VS Code.

## Enabling `Format on Save` [#format-on-save]

This guide will provide instructions on how to enable the Format on Save feature for the Tact Language extension in VS Code using the Command Palette and editing the JSON settings file.

1. Type `Preferences: Open Settings (JSON)` in the command palette. This will open your `settings.json` file.
2. Editing JSON Settings

   - You'll see a JSON object. We're going to add some properties to this object to enable format on save for the Tact Language extension.
   - Add the following lines inside the JSON object:

     ```json
     {
     	"[tact]": {
     		"editor.formatOnSave": true,
     		"editor.defaultFormatter": "KonVik.tact-lang-vscode"
     	}
     }
     ```

   - This will enable format on save (`"editor.formatOnSave": true`) and set the default formatter for Tact files (`"[tact]": {"editor.defaultFormatter": "KonVik.tact-lang-vscode"}`) to the Tact Language extension.

3. Saving and Closing Settings
   - Save your `settings.json` file after adding these lines (You can press `Ctrl+S` to save).
   - Close the `settings.json` tab or press `Ctrl+W`.

Your Tact Language VS Code extension should now automatically format your files when you save them. If you don't see these changes take effect immediately, you might need to reload VS Code.

## References and Resources

- [Extension on GitHub](https://github.com/tact-lang/tact-vscode)
- [Extension on the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=KonVik.tact-lang-vscode)

## core-advanced.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-advanced.mdx)
# Advanced

import { Callout } from 'nextra/components'

Various niche, dangerous or unstable features which can produce unexpected results and are meant to be used by the more experienced users.

<Callout type="warning" emoji="⚠️">

  Proceed with caution.

</Callout>

## Context.readForwardFee

```tact
extends fun readForwardFee(self: Context): Int
```

Extension function for the [`Context{:tact}`](/ref/core-common#context).

Reads [forward fee](https://docs.ton.org/develop/smart-contracts/guidelines/processing) and returns it as [`Int{:tact}`][int] amount of [nanoToncoins](book/integers#nanotoncoin).

Usage example:

```tact
let fwdFee: Int = context().readForwardFee();
```

## getConfigParam

```tact
fun getConfigParam(id: Int): Cell?;
```

Loads a [configuration parameter](https://docs.ton.org/develop/howto/blockchain-configs) of TON Blockchain by its `id` number.

Usage examples:

```tact
// Parameter 0, address of a special smart contract that stores the blockchain's configuration
let configAddrAsCell: Cell = getConfigParam(0)!!;

// Parameter 18, configuration for determining the prices for data storage
let dataStorageFeeConfig: Cell = getConfigParam(18)!!;
```

<Callout>

  Standard library [`@stdlib/config`](/ref/stdlib-config) provides two related helper functions:\
  [`getConfigAddress(){:tact}`](/ref/stdlib-config#getconfigaddress) for retrieving config [`Address{:tact}`][p]\
  [`getElectorAddress(){:tact}`](/ref/stdlib-config#getconfigaddress) for retrieving elector [`Address{:tact}`][p]

  Read more about other parameters: [Config Parameters in TON Docs](https://docs.ton.org/develop/howto/blockchain-configs).

</Callout>

## acceptMessage

```tact
fun acceptMessage();
```

Agrees to buy some gas to finish the current transaction. This action is required to process external messages, which bring no value (hence no gas) with themselves.

Usage example:

```tact {10}
contract Timeout {
    timeout: Int;

    init() {
        self.timeout = now() + 5 * 60; // 5 minutes from now
    }

    external("timeout") {
        if (now() > self.timeout) {
            acceptMessage(); // start accepting external messages once timeout went out
        }
    }
}
```

<Callout>

  For more details, see: [Accept Message Effects in TON Docs](https://docs.ton.org/develop/smart-contracts/guidelines/accept).

</Callout>

## commit

```tact
fun commit();
```

Commits the current state of [registers](https://docs.ton.org/learn/tvm-instructions/tvm-overview#control-registers) `c4` ("persistent data") and `c5` ("actions"), so that the current execution is considered "successful" with the saved values even if an exception in compute phase is thrown later.

Usage example:

```tact {1}
commit();  // now, transaction is considered "successful"
throw(42); // and this won't fail it
```

## nativePrepareRandom

```tact
fun nativePrepareRandom();
```

Prepares a random number generator by using [`nativeRandomizeLt(){:tact}`](#nativerandomizelt). Automatically called by [`randomInt(){:tact}`](/ref/core-random#randomint) and [`random(){:tact}`](/ref/core-random#random) functions.

Usage example:

```tact
nativePrepareRandom(); // prepare the RNG
// ... do your random things ...
```

## nativeRandomize

```tact
fun nativeRandomize(x: Int);
```

Randomizes the pseudo-random number generator with the specified seed `x`.

Usage example:

```tact
nativeRandomize();          // now, random numbers are less predictable
let idk: Int = randomInt(); // ???, it's random!
```

## nativeRandomizeLt

```tact
fun nativeRandomizeLt();
```

Randomizes the random number generator with the current [logical time](https://docs.ton.org/develop/smart-contracts/guidelines/message-delivery-guarantees#what-is-a-logical-time).

Usage example:

```tact
nativeRandomizeLt();        // now, random numbers are unpredictable for users,
                            // but still may be affected by validators or collators
                            // as they determine the seed of the current block.
let idk: Int = randomInt(); // ???, it's random!
```

## nativeRandom

```tact
fun nativeRandom(): Int;
```

Generates and returns an $256$-bit random number just like [`randomInt(){:tact}`](/ref/core-random#randomint), but doesn't initialize the random generator with [`nativePrepareRandom(){:tact}`](#nativepreparerandom) beforehand.

<Callout>

  Don't use this function directly, and prefer using [`randomInt(){:tact}`](/ref/core-random#randomint) instead.

</Callout>

## nativeRandomInterval

```tact
fun nativeRandomInterval(max: Int): Int;
```

Generates and returns a $256$-bit random number in the range from $0$ to `max` similar to [`random(){:tact}`](/ref/core-random#random), but doesn't initialize the random generator with [`nativePrepareRandom(){:tact}`](#nativepreparerandom) beforehand.

<Callout>

  Don't use this function directly, and prefer using [`random(){:tact}`](/ref/core-random#random) instead.

</Callout>

## nativeSendMessage

```tact
fun nativeSendMessage(cell: Cell, mode: Int);
```

[Queues the message](/book/send#outbound-message-processing) to be sent by specifying the complete `cell` and the [message `mode`](/book/message-mode).

<Callout>

  Prefer using a much more common and user-friendly [`send(){:tact}`](/ref/core-common#send) function unless you have a complex logic that can't be expressed otherwise.

</Callout>

## nativeReserve

```tact
fun nativeReserve(amount: Int, mode: Int);
```

Calls native `raw_reserve` function with specified amount and mode. The `raw_reserve` is a function that creates an output action to reserve a specific amount of [nanoToncoins](book/integers#nanotoncoin) from the remaining balance of the account.

It has the following signature in FunC:

```func
raw_reserve(int amount, int mode) impure asm "RAWRESERVE";
```

The function takes two arguments:
* `amount`: The number of [nanoToncoins](book/integers#nanotoncoin) to reserve.
* `mode`: Determines the reservation behavior.

Function `raw_reserve` is roughly equivalent to creating an outbound message carrying the specified `amount` of [nanoToncoins](book/integers#nanotoncoin) (or `b` $-$ `amount` [nanoToncoins](book/integers#nanotoncoin), where `b` is the remaining balance) to oneself. This ensures that subsequent output actions cannot spend more money than the remainder.

It's possible to use raw [`Int{:tact}`][int] values and manually provide them for the `mode`, but for your convenience there's a set of constants which you may use to construct the compound `mode` with ease. Take a look at the following tables for more information on base modes and optional flags.

<Callout type="warning" emoji="⚠️">

  Currently, `amount` must be a non-negative integer, and `mode` must be in the range $0..31$, inclusive.

</Callout>

### Base modes [#nativereserve-base-modes]

The resulting `mode` value can have the following base modes:

Mode value | Constant name                 | Description
---------: | :---------------------------- | -----------
$0$        | `ReserveExact{:tact}`         | Reserves exactly the specified `amount` of [nanoToncoins](book/integers#nanotoncoin).
$1$        | `ReserveAllExcept{:tact}`     | Reserves all, but the specified `amount` of [nanoToncoins](book/integers#nanotoncoin).
$2$        | `ReserveAtMost{:tact}`        | Reserves at most the specified `amount` of [nanoToncoins](book/integers#nanotoncoin).

### Optional flags [#nativereserve-optional-flags]

Additionally, the resulting `mode` can have the following optional flags added:

Flag value | Constant name                      | Description
---------: | :--------------------------------- | -----------
$+4$       | `ReserveAddOriginalBalance{:tact}` | Increases the `amount` by the original balance of the current account (before the compute phase), including all extra currencies.
$+8$       | `ReserveInvertSign{:tact}`         | Negates the `amount` value before performing the reservation.
$+16$      | `ReserveBounceIfActionFail{:tact}` | Bounces the transaction if reservation fails.

### Combining modes with flags [#nativereserve-combining-modes-with-flags]

To make the [`Int{:tact}`][int] value for `mode` parameter, you just have to combine base modes with optional flags by applying the [bitwise OR](/book/operators#binary-bitwise-or) operation:

```tact
nativeReserve(ton("0.1"), ReserveExact | ReserveBounceIfActionFail);
//            ----------  ----------------------------------------
//            ↑           ↑
//            |           mode, which would bounce the transaction if exact reservation would fail
//            amount of nanoToncoins to reserve
```

[p]: /book/types#primitive-types
[bool]: /book/types#booleans
[int]: /book/integers


## core-base.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-base.mdx)
# Base trait

import { Callout } from 'nextra-theme-docs'

Every [contract](/book/contracts) and [trait](/book/types#traits) in Tact implicitly [inherits](/book/contracts#traits) the `BaseTrait{:tact}` trait, which contains a number of the most useful [internal functions](/book/contracts#internal-functions) for any kind of contract, and a constant `self.storageReserve{:tact}` aimed at advanced users of Tact.

## Constants

### self.storageReserve [#self-storagereserve]

```tact
virtual const storageReserve: Int = 0;
```

Usage example:

```tact
contract AllYourStorageBelongsToUs {
    // This would change the behavior of self.forward() function,
    // causing it to try reserving this amount of nanoToncoins before
    // forwarding a message with SendRemainingBalance mode
    override const storageReserve: Int = ton("0.1");
}
```

## Functions

### self.reply [#self-reply]

```tact
virtual fun reply(body: Cell?);
```

An alias to calling the [`self.forward(){:tact}`](#self-forward) function with the following arguments:

```tact
self.forward(sender(), body, true, null);
//           ↑         ↑     ↑     ↑
//           |         |     |     init: StateInit?
//           |         |     bounce: Bool
//           |         body: Cell?
//           to: Address
```

Usage example:

```tact
// This message can bounce back to us!
self.reply("Beware, this is my reply to you!".asComment());
```

### self.notify [#self-notify]

```tact
virtual fun notify(body: Cell?);
```

An alias to calling the [`self.forward(){:tact}`](#self-forward) function with the following arguments:

```tact
self.forward(sender(), body, false, null);
//           ↑         ↑     ↑      ↑
//           |         |     |      init: StateInit?
//           |         |     bounce: Bool
//           |         body: Cell?
//           to: Address
```

Usage example:

```tact
// This message won't bounce!
self.notify("Beware, this is my reply to you!".asComment());
```

### self.forward [#self-forward]

```tact
virtual fun forward(to: Address, body: Cell?, bounce: Bool, init: StateInit?);
```

[Queues the message](/book/send#outbound-message-processing) (bounceable or non-bounceable) to be sent to the specified address `to`. Optionally, you may provide a `body` of the message and the [`init` package](/book/expressions#initof).

When [`self.storageReserve{:tact}`](#self-storagereserve) constant is overwritten to be $> 0$, before sending a message it also tries to reserve the `self.storageReserve{:tact}` amount of [nanoToncoins][nano] from the remaining balance before making the send in the [`SendRemainingBalance{:tact}`](https://docs.tact-lang.org/book/message-mode#base-modes) ($128$) mode.

In case reservation attempt fails and in the default case without the attempt, the message is sent with the [`SendRemainingValue{:tact}`](https://docs.tact-lang.org/book/message-mode#base-modes) ($64$) mode instead.

<Callout>

  Note, that `self.forward(){:tact}` never sends additional [nanoToncoins][nano] on top of what's available on the balance.\
  To be able to send more [nanoToncoins][nano] with a single message, use the the [`send(){:tact}`](/ref/core-common#send) function.

</Callout>

Usage example:

```tact
import "@stdlib/ownable";

message PayoutOk {
    address: Address;
    value: Int as coins;
}

contract Payout with Ownable {
    completed: Bool;
    owner: Address;

    init(owner: Address) {
        self.owner = owner;
        self.completed = false;
    }

    // ... some actions there ...

    // Bounced receiver function, which is called when the specified outgoing message bounces back
    bounced(msg: bounced<PayoutOk>) {
        // Reset completed flag if our message bounced
        self.completed = false;

        // Send a notification that the payout failed using the remaining funds for processing this send
        self.forward(self.owner, "Payout failed".asComment(), false, null);
    }
}
```

[nano]: /book/integers#nanotoncoin


## core-cells.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-cells.mdx)
# Cells, Builders and Slices

import { Callout } from 'nextra-theme-docs'

[`Cell{:tact}`][cell] is a low-level [primitive][p] that represents data in TON Blockchain. Cells consist of $1023$ bits of data with up to $4$ references to another cells. They are read-only and immutable, and cannot have cyclic references.

[`Builder{:tact}`][builder] is an immutable [primitive][p] to construct cells, and [`Slice{:tact}`][slice] is a mutable [primitive][p] to parse them.

<Callout>

  Be very careful when constructing and parsing cells manually, and always make sure to document their desired layout: a strict order of values and types for serialization and deserialization.

  To do so, advanced users are recommended to use [Type Language - Binary (TL-B) schemas][tlb].

  And every user is recommended to use [Structs][struct] and their [methods](/book/functions#extension-function) like [`Struct.toCell(){:tact}`](structtocell) and [`Struct.fromCell(){:tact}`](structfromcell) instead of manually constructing and parsing cells, because [Structs][struct] and [Messages][message] are closest to being the [living TL-B schemas of your contracts](/book/cells#cnp-structs).

</Callout>

## beginCell

```tact
fun beginCell(): Builder
```

Creates a new empty [`Builder{:tact}`][builder].

Usage example:

```tact
let fizz: Builder = beginCell();
```

## emptyCell

```tact
fun emptyCell(): Cell;
```

Creates and returns an empty [`Cell{:tact}`][cell] (without data and references). Alias to `beginCell().endCell(){:tact}`.

Usage example:

```tact
let fizz: Cell = emptyCell();
let buzz: Cell = beginCell().endCell();

fizz == buzz; // true
```

## emptySlice

```tact
fun emptySlice(): Slice;
```

Creates and returns an empty [`Slice{:tact}`][slice] (without data and references). Alias to `emptyCell().asSlice(){:tact}`.

Usage example:

```tact
let fizz: Slice = emptySlice();
let buzz: Slice = emptyCell().asSlice();

fizz == buzz; // true
```

## Cell.beginParse

```tact
extends fun beginParse(self: Cell): Slice;
```

Extension function for the [`Cell{:tact}`][cell].

Opens the [`Cell{:tact}`][cell] for parsing and returns it as a [`Slice{:tact}`][slice].

Usage example:

```tact
let c: Cell = emptyCell();
let fizz: Slice = c.beginParse();
```

## Cell.hash

```tact
extends fun hash(self: Cell): Int;
```

Extension function for the [`Cell{:tact}`][cell].

Calculates and returns an [`Int{:tact}`][int] value of the [SHA-256][sha-2] hash of the [standard `Cell{:tact}` representation][std-repr] of the given [`Cell{:tact}`][cell].

Usage example:

```tact
let c: Cell = emptyCell();
let fizz: Int = c.hash();
```

## Cell.asSlice

```tact
extends fun asSlice(self: Cell): Slice;
```

Extension function for the [`Cell{:tact}`][cell].

Converts the Cell to a [`Slice{:tact}`][slice] and returns it. Alias to `self.beginParse(){:tact}`.

Usage example:

```tact
let c: Cell = emptyCell();
let fizz: Slice = c.asSlice();
```

## Builder.endCell

```tact
extends fun endCell(self: Builder): Cell;
```

Extension function for the [`Builder{:tact}`][builder].

Converts a [`Builder{:tact}`][builder] into an ordinary [`Cell{:tact}`][cell].

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Cell = b.endCell();
```

## Builder.storeUint

```tact
extends fun storeUint(self: Builder, value: Int, bits: Int): Builder;
```

Extension function for the [`Builder{:tact}`][builder].

Stores an unsigned `bits`-bit `value` into the copy of the [`Builder{:tact}`][builder] for $0 ≤$ `bits` $≤ 256$. Returns that copy.

Attempts to store a negative `value` or provide an insufficient or out-of-bounds `bits` number throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Builder = b.storeUint(42, 6);
```

## Builder.storeInt

```tact
extends fun storeInt(self: Builder, value: Int, bits: Int): Builder;
```

Extension function for the [`Builder{:tact}`][builder].

Stores a signed `bits`-bit `value` into the copy of the [`Builder{:tact}`][builder] for $0 ≤$ `bits` $≤ 257$. Returns that copy.

Attempts to provide an insufficient or out-of-bounds `bits` number throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Builder = b.storeUint(42, 7);
```

## Builder.storeBool

```tact
extends fun storeBool(self: Builder, value: Bool): Builder;
```

Extension function for the [`Builder{:tact}`][builder].

Stores a [`Bool{:tact}`][bool] `value` into the copy of the [`Builder{:tact}`][builder]. Writes $1$ as a single bit if `value` is `true{:tact}`, and writes $0$ otherwise. Returns that copy of the [`Builder{:tact}`][builder].

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Builder = b.storeBool(true);  // writes 1
let buzz: Builder = b.storeBool(false); // writes 0
```

## Builder.storeSlice

```tact
extends fun storeSlice(self: Builder, cell: Slice): Builder;
```

Extension function for the [`Builder{:tact}`][builder].

Stores a [`Slice{:tact}`][slice] `cell` into the copy of the [`Builder{:tact}`][builder]. Returns that copy.

Usage example:

```tact
let b: Builder = beginCell();
let s: Slice = emptyCell().asSlice();
let fizz: Builder = b.storeSlice(s);
```

## Builder.storeCoins

```tact
extends fun storeCoins(self: Builder, value: Int): Builder;
```

Extension function for the [`Builder{:tact}`][builder].

Stores (serializes) an unsigned [`Int{:tact}`][int] `value` in the range $0 .. 2^{120} − 1$ into the copy of the [`Builder{:tact}`][builder]. The serialization of `value` consists of a $4$-bit unsigned big-endian integer $l$, which is the smallest integer $l ≥ 0$, such that `value` $< 2^{8 * l}$, followed by an $8 * l$-bit unsigned big-endian representation of `value`. Returns that copy of the [`Builder{:tact}`][builder].

Attempts to store an out-of-bounds `value` throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

This is the most common way of storing [nanoToncoins](/book/integers#nanotoncoin).

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Builder = b.storeCoins(42);
```

<Callout>

  **Useful links:**\
  [Special `coins` serialization type](/book/integers#serialization-coins)

</Callout>

## Builder.storeAddress

```tact
extends fun storeAddress(self: Builder, address: Address): Builder;
```

Extension function for the [`Builder{:tact}`][builder].

Stores the `address` in the copy of the [`Builder{:tact}`][builder]. Returns that copy.

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Builder = b.storeAddress(myAddress());
```

## Builder.storeRef

```tact
extends fun storeRef(self: Builder, cell: Cell): Builder;
```

Extension function for the [`Builder{:tact}`][builder].

Stores a reference `cell` into the copy of the [`Builder{:tact}`][builder]. Returns that copy.

As a single [`Cell{:tact}`][cell] can store up to $4$ references, attempts to store more throw an exception with [exit code 8](/book/exit-codes#8): `Cell overflow`.

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Builder = b.storeRef(emptyCell());
```

## Builder.refs

```tact
extends fun refs(self: Builder): Int;
```

Extension function for the [`Builder{:tact}`][builder].

Returns the number of cell references already stored in the [`Builder{:tact}`][builder] as an [`Int{:tact}`][int].

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Int = b.refs(); // 0
```

## Builder.bits

```tact
extends fun bits(self: Builder): Int;
```

Extension function for the [`Builder{:tact}`][builder].

Returns the number of data bits already stored in the [`Builder{:tact}`][builder] as an [`Int{:tact}`][int].

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Int = b.bits(); // 0
```

## Builder.asSlice

```tact
extends fun asSlice(self: Builder): Slice;
```

Extension function for the [`Builder{:tact}`][builder].

Converts the [`Builder{:tact}`][builder] to a [`Slice{:tact}`][slice] and returns it. Alias to `self.endCell().beginParse(){:tact}`.

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Slice = b.asSlice();
```

## Builder.asCell

```tact
extends fun asCell(self: Builder): Cell;
```

Extension function for the [`Builder{:tact}`][builder].

Converts the [`Builder{:tact}`][builder] to a [`Cell{:tact}`][cell] and returns it. Alias to `self.endCell(){:tact}`.

Usage example:

```tact
let b: Builder = beginCell();
let fizz: Cell = b.asCell();
```

## Slice.loadUint

```tact
extends mutates fun loadUint(self: Slice, l: Int): Int;
```

Extension mutation function for the [`Slice{:tact}`][slice].

Loads and returns an unsigned `l`-bit [`Int{:tact}`][int] from the [`Slice{:tact}`][slice] for $0 ≤$ `l` $≤ 256$.

Attempts to specify an out-of-bounds `l` value throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Attempts to load more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeInt(42, 7).asSlice();
let fizz: Int = s.loadUint(7);
```

## Slice.preloadUint

```tact
extends fun preloadUint(self: Slice, l: Int): Int;
```

Extension function for the [`Slice{:tact}`][slice].

Preloads and returns an unsigned `l`-bit [`Int{:tact}`][int] from the [`Slice{:tact}`][slice] for $0 ≤$ `l` $≤ 256$. Doesn't modify the [`Slice{:tact}`][slice].

Attempts to specify an out-of-bounds `l` value throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Attempts to preload more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeInt(42, 7).asSlice();
let fizz: Int = s.preloadUint(7);
```

## Slice.loadInt

```tact
extends mutates fun loadInt(self: Slice, l: Int): Int;
```

Extension mutation function for the [`Slice{:tact}`][slice].

Loads and returns a signed `l`-bit [`Int{:tact}`][int] from the [`Slice{:tact}`][slice] for $0 ≤$ `l` $≤ 257$.

Attempts to specify an out-of-bounds `l` value throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Attempts to load more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeInt(42, 7).asSlice();
let fizz: Int = s.loadInt(7);
```

## Slice.preloadInt

```tact
extends fun preloadInt(self: Slice, l: Int): Int;
```

Extension function for the [`Slice{:tact}`][slice].

Preloads and returns a signed `l`-bit [`Int{:tact}`][int] from the [`Slice{:tact}`][slice] for $0 ≤$ `l` $≤ 257$. Doesn't modify the [`Slice{:tact}`][slice].

Attempts to specify an out-of-bounds `l` value throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Attempts to preload more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeInt(42, 7).asSlice();
let fizz: Int = s.preloadInt(7);
```

## Slice.loadBits

```tact
extends mutates fun loadBits(self: Slice, l: Int): Slice;
```

Extension mutation function for the [`Slice{:tact}`][slice].

Loads $0 ≤$ `l` $≤ 1023$ bits from the [`Slice{:tact}`][slice], and returns them as a separate [`Slice{:tact}`][slice].

Attempts to specify an out-of-bounds `l` value throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Attempts to load more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeInt(42, 7).asSlice();
let fizz: Slice = s.loadBits(7);
```

## Slice.preloadBits

```tact
extends fun preloadBits(self: Slice, l: Int): Slice;
```

Extension function for the [`Slice{:tact}`][slice].

Preloads $0 ≤$ `l` $≤ 1023$ bits from the [`Slice{:tact}`][slice], and returns them as a separate [`Slice{:tact}`][slice]. Doesn't modify the original [`Slice{:tact}`][slice].

Attempts to specify an out-of-bounds `l` value throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Attempts to preload more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeInt(42, 7).asSlice();
let fizz: Slice = s.preloadBits(7);
```

## Slice.skipBits

```tact
extends mutates fun skipBits(self: Slice, l: Int);
```

Extension mutation function for the [`Slice{:tact}`][slice].

Loads all but the first $0 ≤$ `l` $≤ 1023$ bits from the [`Slice{:tact}`][slice].

Attempts to specify an out-of-bounds `l` value throw an exception with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Attempts to load more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeInt(42, 7).asSlice();
s.skipBits(5);                   // all but first 5 bits
let fizz: Slice = s.loadBits(1); // load only 1 bit
```

## Slice.loadBool

```tact
extends mutates fun loadBool(self: Slice): Bool;
```

Extension mutation function for the [`Slice{:tact}`][slice].

Loads a single bit and returns a [`Bool{:tact}`][bool] value from the [`Slice{:tact}`][slice]. Reads `true{:tact}` if the loaded bit is equal to $1$, and reads `false{:tact}` otherwise.

Attempts to load such [`Bool{:tact}`][bool] when [`Slice{:tact}`][slice] doesn't contain it throw an exception with [exit code 8](/book/exit-codes#8): `Cell overflow`.

Attempts to load more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeBool(true).asSlice();
let fizz: Bool = s.loadBool(); // true
```

## Slice.loadCoins

```tact
extends mutates fun loadCoins(self: Slice): Int;
```

Extension mutation function for the [`Slice{:tact}`][slice].

Loads and returns [serialized](#builderstorecoins) an unsigned [`Int{:tact}`][int] value in the range $0 .. 2^{120} - 1$ from the [`Slice{:tact}`][slice]. This value usually represents the amount in [nanoToncoins](/book/integers#nanotoncoin).

Attempts to load such [`Int{:tact}`][int] when [`Slice{:tact}`][slice] doesn't contain it throw an exception with [exit code 8](/book/exit-codes#8): `Cell overflow`.

Attempts to load more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeCoins(42).asSlice();
let fizz: Int = s.loadCoins();
```

<Callout>

  **Useful links:**\
  [Special `coins` serialization type](/book/integers#serialization-coins)

</Callout>

## Slice.loadAddress

```tact
extends mutates fun loadAddress(self: Slice): Address;
```

Extension mutation function for the [`Slice{:tact}`][slice].

Loads and returns an [`Address{:tact}`][p] from the [`Slice{:tact}`][slice].

Attempts to load such [`Address{:tact}`][p] when [`Slice{:tact}`][slice] doesn't contain it throw an exception with [exit code 8](/book/exit-codes#8): `Cell overflow`.

Attempts to load more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage example:

```tact
let s: Slice = beginCell().storeAddress(myAddress()).asSlice();
let fizz: Address = s.loadAddress();
```

## Slice.loadRef

```tact
extends mutates fun loadRef(self: Slice): Cell;
```

Extension mutation function for the [`Slice{:tact}`][slice].

Loads the next reference from the [`Slice{:tact}`][slice] as a [`Cell{:tact}`][cell].

Attempts to load such reference [`Cell{:tact}`][cell] when [`Slice{:tact}`][slice] doesn't contain it throw an exception with [exit code 8](/book/exit-codes#8): `Cell overflow`.

Attempts to load more data than [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage examples:

```tact
let s: Slice = beginCell().storeRef(emptyCell()).asSlice();
let fizz: Cell = s.loadRef();

let s: Slice = beginCell()
    .storeRef(emptyCell())
    .storeRef(emptyCell())
    .asSlice();
let ref1: Cell = s.loadRef();
let ref2: Cell = s.loadRef();
```

## Slice.refs

```tact
extends fun refs(self: Slice): Int;
```

Extension function for the [`Slice{:tact}`][slice].

Returns the number of references in the [`Slice{:tact}`][slice] as an [`Int{:tact}`][int].

Usage example:

```tact
let s: Slice = beginCell().storeRef(emptyCell()).asSlice();
let fizz: Int = s.refs();
```

## Slice.bits

```tact
extends fun bits(self: Slice): Int;
```

Extension function for the [`Slice{:tact}`][slice].

Returns the number of data bits in the [`Slice{:tact}`][slice] as an [`Int{:tact}`][int].

Usage example:

```tact
let s: Slice = beginCell().storeRef(emptyCell()).asSlice();
let fizz: Int = s.bits();
```

## Slice.empty

```tact
extends fun empty(self: Slice): Bool;
```

Extension function for the [`Slice{:tact}`][slice].

Checks whether the [`Slice{:tact}`][slice] is empty (i.e., contains no bits of data and no cell references). Returns `true{:tact}` if it's empty, `false{:tact}` otherwise.

Usage example:

```tact
let s: Slice = beginCell().storeRef(emptyCell()).asSlice();
let fizz: Bool = s.empty();                     // false
let buzz: Bool = beginCell().asSlice().empty(); // true
```

<Callout>

  Unlike [`Slice.endParse(){:tact}`](#sliceendparse), this function doesn't throw any exceptions even when the [`Slice{:tact}`][slice] is empty.

</Callout>

## Slice.dataEmpty

```tact
extends fun dataEmpty(slice: Slice): Bool;
```

Extension function for the [`Slice{:tact}`][slice].

Checks whether the [`Slice{:tact}`][slice] has no bits of data. Returns `true{:tact}` if it has no data, `false{:tact}` otherwise.

Usage example:

```tact
let s: Slice = beginCell().storeRef(emptyCell()).asSlice();
let fizz: Bool = s.dataEmpty();  // true

let s2: Slice = beginCell().storeInt(42, 7).asSlice();
let buzz: Bool = s2.dataEmpty(); // false
```

## Slice.refsEmpty

```tact
extends fun refsEmpty(slice: Slice): Bool;
```

Extension function for the [`Slice{:tact}`][slice].

Checks whether the [`Slice{:tact}`][slice] has no references. Returns `true{:tact}` if it has no references, `false{:tact}` otherwise.

Usage example:

```tact
let s: Slice = beginCell().storeRef(emptyCell()).asSlice();
let fizz: Bool = s.refsEmpty();                     // false
let buzz: Bool = beginCell().asSlice().refsEmpty(); // true
```

## Slice.endParse

```tact
extends fun endParse(self: Slice);
```

Extension function for the [`Slice{:tact}`][slice].

Checks whether the [`Slice{:tact}`][slice] is empty (i.e., contains no bits of data and no cell references). If it's not, throws an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage examples:

```tact {2,6}
let emptyOne: Slice = emptySlice();
emptyOne.endParse(); // nothing, as it's empty

let paul: Slice = "Fear is the mind-killer".asSlice();
try {
    paul.endParse(); // throws exit code 9
}
```

## Slice.hash

```tact
extends fun hash(self: Slice): Int;
```

Extension function for the [`Slice{:tact}`][slice].

Calculates and returns an [`Int{:tact}`][int] value of the [SHA-256][sha-2] hash of the [standard `Cell{:tact}` representation][std-repr] of the given [`Slice{:tact}`][slice].

Usage example:

```tact
let s: Slice = beginCell().asSlice();
let fizz: Int = s.hash();
```

## Slice.asCell

```tact
extends fun asCell(self: Slice): Cell;
```

Extension function for the [`Slice{:tact}`][slice].

Converts the [`Slice{:tact}`][slice] to a [`Cell{:tact}`][cell] and returns it. Alias to `beginCell().storeSlice(self).endCell(){:tact}`.

Usage example:

```tact
let s: Slice = beginCell().asSlice();
let fizz: Cell = s.asCell();
let buzz: Cell = beginCell().storeSlice(s).endCell();

fizz == buzz; // true
```

## Address.asSlice

```tact
extends fun asSlice(self: Address): Slice;
```

Extension function for the [`Address{:tact}`][p].

Converts the [`Address{:tact}`][p] to a [`Slice{:tact}`][slice] and returns it. Alias to `beginCell().storeAddress(self).asSlice(){:tact}`.

Usage example:

```tact
let a: Address = myAddress();
let fizz: Slice = a.asSlice();
let buzz: Slice = beginCell().storeAddress(a).asSlice();

fizz == buzz; // true
```

## Struct.toCell

```tact
extends fun toCell(self: Struct): Cell;
```

Extension function for any structure type [Struct][struct].

Converts the [Struct][struct] to a [`Cell{:tact}`][cell] and returns it.

Usage example:

```tact
struct GuessCoin {
    probably: Int as coins;
    nothing: Int as coins;
}

fun coinCell(): Cell {
    let s: GuessCoin = GuessCoin{ probably: 42, nothing: 27 };
    let fizz: Cell = s.toCell();

    return fizz; // "x{12A11B}"
}
```

## Struct.fromCell

```tact
extends fun fromCell(self: Struct, cell: Cell): Struct;
```

Extension function for any structure type [Struct][struct].

Converts a [`Cell{:tact}`][cell] into the specified [Struct][struct] and returns that [Struct][struct].

Attempts to pass a [`Cell{:tact}`][cell] with layout different from the specified [Struct][struct] or to load more data than a [`Cell{:tact}`][cell] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage examples:

```tact
struct GuessCoin {
    probably: Int as coins;
    nothing: Int as coins;
}

fun directParse(payload: Cell): GuessCoin {
    return GuessCoin.fromCell(payload);
}

fun cautiousParse(payload: Cell): GuessCoin? {
    let coin: GuessCoin? = null;
    try {
        coin = GuessCoin.fromCell(payload);
    } catch (e) {
        dump("Cell payload doesn't match GuessCoin Struct!");
    }
    return coin;
}
```

## Struct.fromSlice

```tact
extends fun fromSlice(self: Struct, cell: Slice): Struct;
```

Extension function for any structure type [Struct][struct].

Converts a [`Slice{:tact}`][slice] into the specified [Struct][struct] and returns that [Struct][struct].

Attempts to pass a [`Slice{:tact}`][slice] with layout different from the specified [Struct][struct] or to load more data than a [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage examples:

```tact
struct GuessCoin {
    probably: Int as coins;
    nothing: Int as coins;
}

fun directParse(payload: Slice): GuessCoin {
    return GuessCoin.fromSlice(payload);
}

fun cautiousParse(payload: Slice): GuessCoin? {
    let coin: GuessCoin? = null;
    try {
        coin = GuessCoin.fromSlice(payload);
    } catch (e) {
        dump("Slice payload doesn't match GuessCoin Struct!");
    }
    return coin;
}
```

## Message.toCell

```tact
extends fun toCell(self: Message): Cell;
```

Extension function for any message type [Message][message].

Converts the [Message][message] to a [`Cell{:tact}`][cell] and returns it.

Usage example:

```tact
message GuessCoin {
    probably: Int as coins;
    nothing: Int as coins;
}

fun coinCell(): Cell {
    let s: GuessCoin = GuessCoin{ probably: 42, nothing: 27 };
    let fizz: Cell = s.toCell();

    return fizz; // "x{AB37107712A11B}"
}
```

## Message.fromCell

```tact
extends fun fromCell(self: Message, cell: Cell): Message;
```

Extension function for any message type [Message][message].

Converts a [`Cell{:tact}`][cell] into the specified [Message][message] and returns that [Message][message].

Attempts to pass a [`Cell{:tact}`][cell] with layout different from the specified [Message][message] or to load more data than a [`Cell{:tact}`][cell] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage examples:

```tact
message(0x777) TripleAxe {
    prize: Int as uint32;
}

fun directParse(payload: Cell): TripleAxe {
    return TripleAxe.fromCell(payload);
}

fun cautiousParse(payload: Cell): TripleAxe? {
    let coin: TripleAxe? = null;
    try {
        coin = TripleAxe.fromCell(payload);
    } catch (e) {
        dump("Cell payload doesn't match TripleAxe Message!");
    }
    return coin;
}
```

## Message.fromSlice


```tact
extends fun fromSlice(self: Message, cell: Slice): Message;
```

Extension function for any message type [Message][message].

Converts a [`Slice{:tact}`][slice] into the specified [Message][message] and returns that [Message][message].

Attempts to pass a [`Slice{:tact}`][slice] with layout different from the specified [Message][message] or to load more data than a [`Slice{:tact}`][slice] contains throw an exception with [exit code 9](/book/exit-codes#9): `Cell underflow`.

Usage examples:

```tact
message(0x777) TripleAxe {
    prize: Int as uint32;
}

fun directParse(payload: Slice): TripleAxe {
    return TripleAxe.fromSlice(payload);
}

fun cautiousParse(payload: Slice): TripleAxe? {
    let coin: TripleAxe? = null;
    try {
        coin = TripleAxe.fromSlice(payload);
    } catch (e) {
        dump("Slice payload doesn't match TripleAxe Message!");
    }
    return coin;
}
```

[p]: /book/types#primitive-types
[bool]: /book/types#booleans
[int]: /book/integers
[cell]: /book/cells#cells
[builder]: /book/cells#builders
[slice]: /book/cells#slices
[map]: /book/maps
[struct]: /book/structs-and-messages#structs
[message]: /book/structs-and-messages#messages

[std-repr]: /book/cells#cells-representation

[tlb]: https://docs.ton.org/develop/data-formats/tl-b-language
[sha-2]: https://en.wikipedia.org/wiki/SHA-2#Hash_standard


## core-common.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-common.mdx)
# Common

import { Callout } from 'nextra-theme-docs'

List of the most commonly used built-in [global static functions](/book/functions#global-static-functions).

## Contextual

### now

```tact
fun now(): Int
```

Returns the current [Unix time](https://en.wikipedia.org/wiki/Unix_time).

Usage example:

```tact
let timeOffset: Int = now() + 1000; // thousand seconds from now()
```

### myBalance

```tact
fun myBalance(): Int;
```

Returns the [nanoToncoin](/book/integers#nanotoncoin) balance of the smart contract as it was at the start of the [compute phase](https://docs.ton.org/learn/tvm-instructions/tvm-overview#compute-phase) of the current transaction.

Usage example:

```tact
let iNeedADolla: Int = myBalance();
```

<Callout type="warning" emoji="⚠️">

  Beware, that [all message sending functions](/book/send) of Tact can change the _actual_ contract's balance, but they _won't_ update the value returned by this function.

</Callout>

### myAddress

```tact
fun myAddress(): Address;
```

Returns the address of the current smart contract as an [`Address{:tact}`][p].

Usage example:

```tact
let meMyselfAndI: Address = myAddress();
```

### sender

```tact
fun sender(): Address;
```

Returns the [`Address{:tact}`][p] of the sender of the current message.

Usage example:

```tact
receive() {
    let whoSentMeMessage: Address = sender();
}
```

<Callout type="warning" emoji="⚠️">

  Behavior is undefined for [getter functions](/book/contracts#getter-functions), as they cannot have a sender nor they can send messages.

</Callout>

<Callout>

  In order to reduce gas usage, prefer using this function over calling [`context().sender{:tact}`](#context) when you only need to know the sender of the message.

</Callout>

### context

```tact
fun context(): Context;
```

Returns `Context{:tact}` [Struct](/book/structs-and-messages#structs), that consists of:

Field     | Type                  | Description
:-------- | :-------------------- | :----------
`bounced` | [`Bool{:tact}`][bool] | [Bounced](https://ton.org/docs/learn/overviews/addresses#bounceable-vs-non-bounceable-addresses) flag of the incoming message.
`sender`  | [`Address{:tact}`][p] | Internal address of the sender on the TON blockchain.
`value`   | [`Int{:tact}`][int]   | Amount of [nanoToncoins](/book/integers#nanotoncoin) in a message.
`raw`     | [`Slice{:tact}`][slice]   | The remainder of the message as a [`Slice{:tact}`][slice]. It follows [internal message layout](https://docs.ton.org/develop/smart-contracts/messages#message-layout) of TON starting from the destination [`Address{:tact}`][p] (`dest:MsgAddressInt ` in [TL-B notation](https://docs.ton.org/develop/data-formats/tl-b-language)).

Usage example:

```tact
let ctx: Context = context();
require(ctx.value != 68 + 1, "Invalid amount of nanoToncoins, bye!");
```

<Callout>

  Note, that if you only need to know who sent the message, use the [`sender(){:tact}`](#sender) function, as it's less gas-consuming.

</Callout>

## Addressing

### newAddress

```tact
fun newAddress(chain: Int, hash: Int): Address;
```

Creates a new [`Address{:tact}`][p] based on the [`chain` id](https://ton-blockchain.github.io/docs/#/overviews/TON_blockchain_overview) and the [SHA-256](/ref/stdlib-math#sha256) encoded [`hash` value](https://docs.ton.org/learn/overviews/addresses#account-id).

This function tries to resolve constant values in [compile-time](/ref/core-comptime) whenever possible.

Usage example:

```tact
let oldTonFoundationAddr: Address =
    newAddress(0, 0x83dfd552e63729b472fcbcc8c45ebcc6691702558b68ec7527e1ba403a0f31a8);
    //         ↑  ------------------------------------------------------------------
    //         |  ↑
    //         |  sha-256 hash of contract's init package (StateInit)
    //         chain id: 0 is a workchain, -1 is a masterchain
```

<Callout type="warning" emoji="⚠️">

  This method throws an error with [exit code 136](/book/exit-codes#136) if `chain` is invalid or with [exit code 137](/book/exit-codes#137) if `chain` points to the masterchain ($-1$) without [masterchain support](/book/masterchain) enabled.

</Callout>

<Callout>

  **Useful links:**\
  [`chain` (Workchain ID) in TON Docs](https://docs.ton.org/learn/overviews/addresses#workchain-id)\
  [`hash` (Account ID) in TON Docs](https://docs.ton.org/learn/overviews/addresses#account-id)\
  [Contract's init package (`StateInit{:tact}`)](/book/expressions#initof)

</Callout>

### contractAddress

```tact
fun contractAddress(s: StateInit): Address;
```

Computes smart contract's [`Address{:tact}`][p] in a workchain $0$ based on its [`StateInit{:tact}`](/book/expressions#initof).

Usage example:

```tact
let foundMeSome: Address = contractAddress(initOf SomeContract());
```

### contractAddressExt

```tact
fun contractAddressExt(chain: Int, code: Cell, data: Cell): Address;
```

Computes smart contract's [`Address{:tact}`][p] based on the `chain` id, contract's `code` and contract's initial state `data`. Use [`initOf{:tact}`](/book/expressions#initof) expression to obtain initial `code` and initial `data` of a given contract.

Usage example:

```tact
let initPkg: StateInit = initOf SomeContract();
let hereBeDragons: Address = contractAddressExt(0, initPkg.code, initPkg.data);
```

<Callout type="warning" emoji="⚠️">

  This method throws an error with [exit code 136](/book/exit-codes#136) if `chain` is invalid or with [exit code 137](/book/exit-codes#137) if `chain` points to the masterchain ($-1$) without [masterchain support](/book/masterchain) enabled.

</Callout>

<Callout>

  For this function to work, the compiler option `debug` has to be set to `true{:tact}` for the current project in the [configuration file](/book/config).\
  Read more about debugging on the dedicated page: [Debugging](/book/debug).

</Callout>

## Communication

### send

```tact
fun send(params: SendParameters);
```

[Queues the message](/book/send#outbound-message-processing) to be sent using a [`SendParameters{:tact}`](/book/send) [Struct](/book/structs-and-messages#structs).

Usage example:

```tact
send(SendParameters{
    to: sender(),    // back to the sender,
    value: ton("1"), // with 1 Toncoin (1_000_000_000 nanoToncoin),
                     // and no message body
});
```

<Callout>

  **Useful links:**\
  [Sending messages in the Book](/book/send)\
  [Message `mode` in the Book](/book/message-mode)\
  [Single-contract communication in the Cookbook](/cookbook/single-communication)

</Callout>

### emit

```tact
fun emit(body: Cell);
```

[Queues the message](/book/send#outbound-message-processing) `body` to be sent to the outer world with the purpose of logging and analyzing it later off-chain. The message does not have a recipient and is gas-efficient compared to using any other message sending functions of Tact.

Usage example:

```tact
emit("Catch me if you can, Mr. Holmes".asComment()); // asComment() converts a String to a Cell
```

<Callout>

  To analyze `emit(){:tact}` calls, one has to look at [external messages](/book/external) produced by the contract.

  Read more: [Logging via `emit(){:tact}`](/book/debug#logging).

</Callout>

[p]: /book/types#primitive-types
[bool]: /book/types#booleans
[int]: /book/integers
[slice]: /book/cells#slices


## core-comptime.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-comptime.mdx)
# Compile-time

import { Callout } from 'nextra-theme-docs'

This page lists all the built-in [global static functions](/book/functions#global-static-functions), which are evaluated at the time of building the Tact project and cannot work with non-constant, run-time data. These functions are commonly referred to as "compile-time functions".

## address

```tact
fun address(s: String): Address;
```

A compile-time function that converts a [`String{:tact}`][p] with an address into the [`Address{:tact}`][p] type.

Usage example:

```tact
contract Example {
    // Persistent state variables
    addr: Address =
        address("EQCD39VS5jcptHL8vMjEXrzGaRcCVYto7HUn4bpAOg8xqB2N"); // works at compile-time!
}
```

## cell

```tact
fun cell(bocBase64: String): Cell;
```

A compile-time function that embeds a base64-encoded [BoC](https://docs.ton.org/develop/data-formats/cell-boc#bag-of-cells) `bocBase64` as a [`Cell{:tact}`][cell] into the contract.

Usage example:

```tact
contract Example {
    // Persistent state variables
    storedCell: Cell =
        // Init package for Wallet V3R1 as a base64-encoded BoC
        cell("te6cckEBAQEAYgAAwP8AIN0gggFMl7qXMO1E0NcLH+Ck8mCDCNcYINMf0x/TH/gjE7vyY+1E0NMf0x/T/9FRMrryoVFEuvKiBPkBVBBV+RDyo/gAkyDXSpbTB9QC+wDo0QGkyMsfyx/L/8ntVD++buA="); // works at compile-time!
}
```

<Callout>

  **Useful links:**\
  [Bag of Cells in TON Docs](https://docs.ton.org/develop/data-formats/cell-boc#bag-of-cells)

</Callout>

## ton

```tact
fun ton(value: String): Int;
```

A compile-time function that converts the given Toncoins `value` from a human-readable format [`String{:tact}`][p] to the [nanoToncoin](/book/integers#nanotoncoin) [`Int{:tact}`][int] format.

Usage example:

```tact
contract Example {
    // Persistent state variables
    one: Int = ton("1");            // 10^9 nanoToncoins, which is equal to one Toncoin
    pointOne: Int = ton("0.1");     // 10^8 nanoToncoins, which is equal to 0.1 Toncoin
    nano: Int = ton("0.000000001"); // 1 nanoToncoin, which is equal to 10^-9 Toncoins
                                    // works at compile-time!
}
```

[p]: /book/types#primitive-types
[bool]: /book/types#booleans
[int]: /book/integers
[cell]: /book/cells#cells


## core-debug.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-debug.mdx)
# Debug

import { Callout } from 'nextra-theme-docs'

List of functions commonly used for debugging smart contracts in Tact.

<Callout>

  Read more about debugging on the dedicated page: [Debugging](/book/debug).

</Callout>

## require

```tact
fun require(condition: Bool, error: String);
```

Checks the `condition` and throws an error with an [exit code](/book/exit-codes) generated from the `error` message if the `condition` is `false{:tact}`. Does nothing otherwise.

The algorithm for generating the exit code works as follows:

* First, the [SHA-256](https://en.wikipedia.org/wiki/SHA-2#Hash_standard) hash of `error` message [`String{:tact}`][p] is obtained.
* Then, its value is read as a 32-bit [big-endian](https://en.wikipedia.org/wiki/Endianness) number modulo $63000$ plus $1000$, in that order.
* Finally, it's put into the `.md` compilation report file, which resides with the other compilation artifacts in your project's `outputs/` or `build/` directories.

The generated exit code is guaranteed to be outside the common $0 - 255$ range reserved for TVM and Tact contract errors, which makes it possible to distinguish exit codes from `require(){:tact}` and any other [standard exit codes](/book/exit-codes).

Usage examples:

```tact
// now() has to return a value greater than 1000, otherwise an error message will be thrown
require(now() > 1000, "We're in the first 1000 seconds of 1 January 1970!");

try {
    // The following will never be true, so this require would always throw
    require(now() < -1, "Time is an illusion. Lunchtime doubly so.");
} catch (e) {
    // e will be outside of range 0-255
    dump(e);
}
```

## dump

```tact
fun dump(arg);
```

Prints the argument `arg` to the contract's debug console. Evaluated only if the `debug` option in the [configuration file](/book/config) is set to `true{:json}`, otherwise does nothing.

Can be applied to the following list of types and values:

* [`Int{:tact}`][int]
* [`Bool{:tact}`][bool]
* [`Address{:tact}`][p]
* [`Cell{:tact}`][cell], [`Builder{:tact}`][builder] or [`Slice{:tact}`][slice]
* [`String{:tact}`][p] or [`StringBuilder{:tact}`][p]
* [`map<K, V>{:tact}`](/book/maps)
* [Optionals and `null{:tact}` value](/book/optionals)
* `void`, which is implicitly returned when a function doesn't have return value defined

Usage examples:

```tact
// Int
dump(42);

// Bool
dump(true);
dump(false);

// Address
dump(myAddress());

// Cell, Builder or Slice
dump(emptyCell());  // Cell
dump(beginCell());  // Builder
dump(emptySlice()); // Slice

// String or StringBuilder
dump("Hello, my name is..."); // String
dump(beginTailString());      // StringBuilder

// Maps
let m: map<Int, Int> = emptyMap();
m.set(2 + 2, 4);
dump(m);

// Special values
dump(null);
dump(emit("msg".asComment())); // As emit() function doesn't return a value, dump() would print #DEBUG#: void.
```

## dumpStack

```tact
fun dumpStack();
```

Prints all the values of [persistent state variables](/book/contracts#variables) to the contract's debug console. Evaluated only if `debug` option is set in the [configuration file](/book/config), otherwise does nothing.

Usage example:

```tact {6}
contract DumpsterFire {
    var1: Int = 0;
    var2: Int = 5;

    receive() {
        dumpStack(); // would print 0 5
    }
}
```

## throw

```tact
fun throw(code: Int);
```

An alias to [`nativeThrow(){:tact}`](#nativethrow).

## nativeThrow

```tact
fun nativeThrow(code: Int);
````

Throws an exception with an error code equal to `code`. Execution of the current context stops (the statements after `nativeThrow` won't be executed) and control will be passed to the first [`try...catch{:tact}` block](/book/statements#try-catch) in the call stack. If no `try{:tact}` or `try...catch{:tact}` block exists among caller functions, [TVM](https://docs.ton.org/learn/tvm-instructions/tvm-overview) will terminate the transaction.

Usage examples:

```tact {2,7}
fun thisWillTerminate() {
    nativeThrow(42); // throwing with exit code 42
}

fun butThisDoesNot() {
    try {
        nativeThrow(42); // throwing with exit code 42
    }

    // ... follow-up logic ...
}
```

## nativeThrowIf

```tact
fun nativeThrowIf(code: Int, condition: Bool);
```

Similar to [`nativeThrow(){:tact}`](#nativethrow), but throws an exception conditionally, when `condition` is equal to `true{:tact}`. Doesn't throw otherwise.

Usage examples:

```tact {2,7}
fun thisWillTerminate() {
    nativeThrowIf(42, true); // throwing with exit code 42
}

fun butThisDoesNot() {
    try {
        nativeThrowIf(42, true); // throwing with exit code 42
    }
    // ... follow-up logic ...
}
```

## nativeThrowUnless

```tact
fun nativeThrowUnless(code: Int, condition: Bool);
```

Similar to [`nativeThrow(){:tact}`](#nativethrow), but throws an exception conditionally, when `condition` is equal to `false{:tact}`. Doesn't throw otherwise.

Usage examples:

```tact {2,7}
fun thisWillTerminate() {
    nativeThrowUnless(42, false); // throwing with exit code 42
}

fun butThisDoesNot() {
    try {
        nativeThrowUnless(42, false); // throwing with exit code 42
    }
    // ... follow-up logic ...
}
```

[p]: /book/types#primitive-types
[bool]: /book/types#booleans
[int]: /book/integers
[cell]: /book/cells#cells
[builder]: /book/cells#builders
[slice]: /book/cells#slices


## core-math.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-math.mdx)
# Math

import { Callout } from 'nextra-theme-docs'

Various math helper functions.

## min

```tact
fun min(x: Int, y: Int): Int;
```

Computes and returns the [minimum](https://en.wikipedia.org/wiki/Maximum_and_minimum) of two [`Int{:tact}`][int] values `x` and `y`.

Usage examples:

```tact
min(1, 2);        // 1
min(2, 2);        // 2
min(007, 3);      // 3
min(0x45, 3_0_0); // 69, nice
//  ↑     ↑
//  69    300
```

## max

```tact
fun max(x: Int, y: Int): Int;
```

Computes and returns the [maximum](https://en.wikipedia.org/wiki/Maximum_and_minimum) of two [`Int{:tact}`][int] values `x` and `y`.

Usage examples:

```tact
max(1, 2);        // 2
max(2, 2);        // 2
max(007, 3);      // 7
max(0x45, 3_0_0); // 300
//  ↑     ↑
//  69    300
```

## abs

```tact
fun abs(x: Int): Int
```

Computes and returns the [absolute value](https://en.wikipedia.org/wiki/Absolute_value) of the [`Int{:tact}`][int] value `x`.

Usage examples:

```tact
abs(42);        // 42
abs(-42);       // 42
abs(-(-(-42))); // 42
```

## log

```tact
fun log(num: Int, base: Int): Int;
```

Computes and returns the [logarithm](https://en.wikipedia.org/wiki/Logarithm) of a number `num` $> 0$ to the base `base` $≥ 1$. Results are [rounded down](https://en.wikipedia.org/wiki/Rounding#Rounding_down). Passing a non-positive `num` value or a `base` less than $1$ throws an error with [exit code 5](/book/exit-codes#5): `Integer out of expected range`.

Usage examples:

```tact
log(1000, 10); // 3, as 10^3 is 1000
//  ↑     ↑             ↑       ↑
//  num   base          base    num

log(1001, 10);  // 3
log(999, 10);   // 2
try {
  log(-1000, 10); // throws exit code 5 because of the non-positive num
}
log(1024, 2);   // 10
try {
  log(1024, -2);  // throws exit code 5 because of the base less than 1
}
```

<Callout>

  Note, that if you only need to obtain logarithms to the base $2$, use the [`log2(){:tact}`](#log2) function, as it's more gas-efficient.

</Callout>

## log2

```tact
fun log2(num: Int): Int;
```

Similar to [`log(){:tact}`](#log), but sets the `base` to $2$.

Usage example:

```tact
log2(1024); // 10, as 2^10 is 1024
//   ↑                ↑       ↑
//   num              base₂   num
```

<Callout>

  In order to reduce gas usage, prefer using this function over calling [`log(){:tact}`](#log) when you only need to obtain logarithms to the base $2$.

</Callout>

## pow

```tact
fun pow(base: Int, exp: Int): Int;
```

Computes and returns the [exponentiation](https://en.wikipedia.org/wiki/Exponentiation) involving two numbers: the `base` and the exponent (or _power_) `exp`. Exponent `exp` must be non-negative, otherwise an error with [exit code 5](/book/exit-codes#5) will be thrown: `Integer out of expected range`.

Note, that this function works both at run-time and at [compile-time](/ref/core-comptime).

Usage example:

```tact
contract Example {
    // Persistent state variables
    p23: Int = pow(2, 3); // raises 2 to the 3rd power, which is 8
    one: Int = pow(5, 0); // raises 5 to the power 0, which always produces 1
                          // works at compile-time!

    // Internal message receiver, which accepts message ExtMsg
    receive() {
        pow(self.p23, self.one + 1); // 64, works at run-time too!
        pow(0, -1);                  // ERROR! Exit code 5: Integer out of expected range
    }
}
```

<Callout>

  Note, that if you only need to obtain powers of $2$, use the [`pow2(){:tact}`](#pow2) function, as it's more gas-efficient.

</Callout>

<Callout>

  List of functions, that only work at compile-time: [API Comptime](/ref/core-comptime).

</Callout>

## pow2

```tact
fun pow2(exp: Int): Int;
```

Similar to [`pow(){:tact}`](#pow), but sets the `base` to $2$. Works both at run-time and at [compile-time](/ref/core-comptime).

Usage examples:

```tact
contract Example {
    // Persistent state variables
    p23: Int = pow2(3); // raises 2 to the 3rd power, which is 8
    one: Int = pow2(0); // raises 2 to the power 0, which always produces 1
                        // works at compile-time!

    // Internal message receiver, which accepts message ExtMsg
    receive() {
        pow2(self.one + 1); // 4, works at run-time too!
        pow2(-1);           // ERROR! Exit code 5: Integer out of expected range
    }
}
```

<Callout>

  In order to reduce gas usage, prefer using this function over calling [`pow(){:tact}`](#pow) when you only need to obtain powers of $2$.

</Callout>

<Callout>

  List of functions, that only work at compile-time: [API Comptime](/ref/core-comptime).

</Callout>

## checkSignature

```tact
fun checkSignature(hash: Int, signature: Slice, public_key: Int): Bool;
```

Checks the [Ed25519][ed] `signature` of the $256$-bit unsigned [`Int{:tact}`][int] `hash` using a `public_key`, represented by a $256$-bit unsigned [`Int{:tact}`][int] too. The signature must contain at least $512$ bits of data, but only the first $512$ bits are used.

Returns `true{:tact}` if the signature is valid, `false{:tact}` otherwise.

Usage example:

```tact {19-24}
message ExtMsg {
    signature: Slice;
    data: Cell;
}

contract Showcase {
    // Persistent state variables
    pub: Int as uint256; // public key as an 256-bit unsigned Int

    // Constructor function init(), where all the variables are initialized
    init(pub: Int) {
        self.pub = pub; // storing the public key upon contract initialization
    }

    // External message receiver, which accepts message ExtMsg
    external(msg: ExtMsg) {
        let hash: Int = beginCell().storeRef(msg.data).endCell().hash();
        let check: Bool = checkSignature(hash, msg.signature, self.pub);
        //                               ----  -------------  --------
        //                               ↑     ↑              ↑
        //                               |     |              public_key, stored in our contract
        //                               |     signature, obtained from the received message
        //                               hash, calculated using the data from the received message
        // ... follow-up logic ...
    }
}
```

## checkDataSignature

```tact
fun checkDataSignature(data: Slice, signature: Slice, public_key: Int): Bool;
```

Checks the [Ed25519][ed] `signature` of the `data` using a `public_key`, similar to [`checkSignature(){:tact}`](#checksignature). If the bit length of `data` is not divisible by $8$, this functions throws an error with [exit code 9](/book/exit-codes#9): `Cell underflow`. Verification itself is being done indirectly: on a [SHA-256][sha-2] hash of the `data`.

Returns `true{:tact}` if the signature is valid, `false{:tact}` otherwise.

Usage example:

```tact
let data: Slice = ...;
let signature: Slice = ...;
let publicKey: Int = ...;

let check: Bool = checkSignature(data, signature, publicKey);
```

## sha256

```tact
fun sha256(data: Slice): Int;
fun sha256(data: String): Int;
```

Computes and returns the [SHA-256][sha-2] hash as an $256$-bit unsigned [`Int{:tact}`][int] from a passed [`Slice{:tact}`][slice] or [`String{:tact}`][p] `data`.

In case `data` is a [`String{:tact}`][p] it should have a number of bits divisible by $8$, and in case it's a [`Slice{:tact}`][slice] it must **also** have no references (i.e. only up to 1023 bits of data in total).

This function tries to resolve constant string values in [compile-time](/ref/core-comptime) whenever possible.

Usage examples:

```tact
sha256(beginCell().asSlice());
sha256("Hello, world!"); // will be resolved in compile-time
sha256(someVariableElsewhere); // will try to resolve at compile-time,
                               // and fallback to run-time evaluation
```

[p]: /book/types#primitive-types
[bool]: /book/types#booleans
[int]: /book/integers
[slice]: /book/cells#slices

[ed]: https://en.wikipedia.org/wiki/EdDSA#Ed25519
[sha-2]: https://en.wikipedia.org/wiki/SHA-2#Hash_standard


## core-random.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-random.mdx)
# Random number generation

import { Callout } from 'nextra-theme-docs'

Random number generation for Tact smart contracts.

## random

```tact
fun random(min: Int, max: Int): Int;
```

Generates and returns a new pseudo-random unsigned [`Int{:tact}`][int] value `x` in the provided semi-closed interval: `min` $≤$ `x` $<$ `max` or `min` $≥$ `x` $>$ `max`, if both `min` and `max` are negative. Note, that `max` value is never included in the interval.

Usage examples:

```tact
random(42, 43); // 42, always
random(0, 42);  // 0-41, but never a 42
```

## randomInt

```tact
fun randomInt(): Int;
```

Generates and returns a new pseudo-random unsigned $256$-bit [`Int{:tact}`][int] value `x`.

The algorithm works as follows: if `r` is the old value of the random seed considered a $32$-byte array (by constructing the big-endian representation of an unsigned $256$-bit [`Int{:tact}`][int]), then its `sha512(r){:tact}` is computed. The first $32$ bytes of this hash are stored as the new value `r'` of the random seed, and the remaining $32$ bytes are returned as the next random value `x`.

Usage example:

```tact
let allYourRandomBelongsToUs: Int = randomInt(); // ???, it's random :)
```

<Callout type="warning" emoji="⚠️">

  Advanced functions for working with random numbers are listed on a specialized page: [Advanced APIs](/ref/core-advanced).

</Callout>

[int]: /book/integers


## core-strings.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/core-strings.mdx)
# Strings and StringBuilders

import { Callout } from 'nextra-theme-docs'

Strings are immutable sequences of characters, which means that once a [`String{:tact}`][p] is created, it cannot be changed. Strings are useful to store text, and so they can be converted to [`Cell{:tact}`][cell] type to be used as message bodies.

To be able to concatenate strings in a gas-efficient way, use a [`StringBuilder{:tact}`][p].

To use [`String{:tact}`][p] literals directly, see: [String literals](/book/expressions#string-literals).

## beginString

```tact
fun beginString(): StringBuilder;
```

Creates and returns an empty [`StringBuilder{:tact}`][p].

Usage example:

```tact
let fizz: StringBuilder = beginString();
```

## beginComment

```tact
fun beginComment(): StringBuilder;
```

Creates and returns an empty [`StringBuilder{:tact}`][p] for building a comment string, which prefixes the resulting [`String{:tact}`][p] with four null bytes. This format is used for passing text comments as message bodies.

Usage example:

```tact
let fizz: StringBuilder = beginComment();
```

## beginTailString

```tact
fun beginTailString(): StringBuilder;
```

Creates and returns an empty [`StringBuilder{:tact}`][p] for building a tail string, which prefixes the resulting [`String{:tact}`][p] with a single null byte. This format is used in various standards like NFT or Jetton.

Usage example:

```tact
let fizz: StringBuilder = beginTailString();
```

## beginStringFromBuilder

```tact
fun beginStringFromBuilder(b: StringBuilder): StringBuilder;
```

Creates and returns a new [`StringBuilder{:tact}`][p] from existing [`StringBuilder{:tact}`][p] `b`. Useful when you need to serialize an existing [`String{:tact}`][p] to a [`Cell{:tact}`][cell] with some other data.

Usage example:

```tact
let fizz: StringBuilder = beginStringFromBuilder(beginString());
```

## StringBuilder.append

```tact
extends mutates fun append(self: StringBuilder, s: String);
```

Extension mutation function for the [`StringBuilder{:tact}`][p].

Appends a [`String{:tact}`][p] `s` to the [`StringBuilder{:tact}`][p].

Usage example:

```tact
let fizz: StringBuilder = beginString();
fizz.append("oh");
fizz.append("my");
fizz.append("Tact!");
```

## StringBuilder.concat

```tact
extends fun concat(self: StringBuilder, s: String): StringBuilder;
```

Extension function for the [`StringBuilder{:tact}`][p].

Returns a new [`StringBuilder{:tact}`][p] after concatinating it with a [`String{:tact}`][p] `s`. Can be chained, unlike [`StringBuilder.append(){:tact}`](#stringbuilderappend).

Usage example:

```tact
let fizz: StringBuilder = beginString()
    .concat("oh")
    .concat("my")
    .concat("Tact!");
```

## StringBuilder.toString

```tact
extends fun toString(self: StringBuilder): String;
```

Extension function for the [`StringBuilder{:tact}`][p].

Returns a built [`String{:tact}`][p] from a [`StringBuilder{:tact}`][p].

Usage example:

```tact
let fizz: StringBuilder = beginString();
let buzz: String = fizz.toString();
```

## StringBuilder.toCell

```tact
extends fun toCell(self: StringBuilder): Cell;
```

Extension function for the [`StringBuilder{:tact}`][p].

Returns an assembled [`Cell{:tact}`][cell] from a [`StringBuilder{:tact}`][p].

Usage example:

```tact
let fizz: StringBuilder = beginString();
let buzz: Cell = fizz.toCell();
```

## StringBuilder.toSlice

```tact
extends fun toSlice(self: StringBuilder): Slice;
```

Extension function for the [`StringBuilder{:tact}`][p].

Returns an assembled [`Cell{:tact}`][cell] as a [`Slice{:tact}`][slice] from a [`StringBuilder{:tact}`][p]. Alias to [`self.toCell().asSlice(){:tact}`](/ref/core-cells#cellasslice).

Usage example:

```tact
let s: StringBuilder = beginString();
let fizz: Slice = s.toSlice();
let buzz: Slice = s.toCell().asSlice();

fizz == buzz; // true
```

## String.asSlice

```tact
extends fun asSlice(self: String): Slice;
```

Extension function for the [`String{:tact}`][p].

Returns a [`Slice{:tact}`][slice] from a [`String{:tact}`][p] by trying to pack all of its bits into a continuous list of [Cells][p], each referencing the next one and opening them all for future parsing.

Note, that there's no indication of how many bytes a particular character could take in the [`Slice{:tact}`][slice] or how deep the list of references is going to be, so use this function only if you know what you're doing.

Usage example:

```tact
let s: String = "It's alive! It's alive!!!";
let fizz: Slice = s.asSlice();
let buzz: Slice = s.asSlice().asString().asSlice();

fizz == buzz; // true, but be careful as it's not always the case
```

<Callout>

  See how `String.asSlice{:tact}` function can be used in practice: [How to convert a `String` to an `Int`](/cookbook/type-conversion#how-to-convert-a-string-to-an-int).

</Callout>

## String.asComment

```tact
extends fun asComment(self: String): Cell;
```

Extension function for the [`String{:tact}`][p].

Returns a [`Cell{:tact}`][cell] from a [`String{:tact}`][p] by prefixing the latter with four null bytes. This format is used for passing text comments as message bodies.

Usage example:

```tact
let s: String = "When life gives you lemons, call them 'yellow oranges' and sell them for double the price.";
let fizz: Cell = s.asComment();

let b: StringBuilder = beginComment();
b.append(s);
let buzz: Cell = b.toCell();

fizz == buzz; // true
```

## String.fromBase64

```tact
extends fun fromBase64(self: String): Slice;
```

Extension function for the [`String{:tact}`][p].

Returns a [`Slice{:tact}`][slice] out of the decoded [Base64](https://en.wikipedia.org/wiki/Base64) [`String{:tact}`][p]. Alias to `self.asSlice().fromBase64(){:tact}`.

Note, that this function is limited and only takes the first $1023$ bits of data from the given [`String{:tact}`][p], without throwing an exception when the [`String{:tact}`][p] is larger (i.e. contains more than $1023$ bits of data).

Usage example:

```tact
let s: String = "SGVyZSdzIEpvaG5ueSE=";
let fizz: Slice = s.fromBase64();
let buzz: Slice = s.asSlice().fromBase64();

fizz == buzz; // true
```

## Slice.asString

```tact
extends fun asString(self: Slice): String;
```

Extension function for the [`Slice{:tact}`][slice].

Returns a [`String{:tact}`][p] from a [`Slice{:tact}`][slice] by trying to load all of its bits without looking for its references, if any.

Note, that this function doesn't look at the references at all and is truncates its output to $1023$ bits, so use it only if you know what you're doing.

Usage example:

```tact
let s: String = "Keep your Slices close, but your Strings closer.";
let fizz: String = s;
let buzz: String = s.asSlice().asString();

fizz == buzz; // true, but be careful as it's not always the case
```

## Slice.fromBase64

```tact
extends fun fromBase64(self: Slice): Slice;
```

Extension function for the [`Slice{:tact}`][slice].

Returns a new [`Slice{:tact}`][slice] out of the decoded [Base64](https://en.wikipedia.org/wiki/Base64) [`Slice{:tact}`][slice].

Note, that this function is limited and only takes the first $1023$ bits of data from the given [`Slice{:tact}`][slice], without throwing an exception if the [`Slice{:tact}`][slice] has more data (i.e., when it has any references).

Usage example:

```tact
let s: Slice = "SSBhbSBHcm9vdC4=".asSlice();
let fizz: Slice = s.fromBase64();
```

## Int.toString

```tact
extends fun toString(self: Int): String;
```

Extension function for the [`Int{:tact}`][int].

Returns a [`String{:tact}`][p] from an [`Int{:tact}`][int] value.

Usage example:

```tact
let fizz: String = (84 - 42).toString();
```

## Int.toFloatString

```tact
extends fun toFloatString(self: Int, digits: Int): String;
```

Extension function for the [`Int{:tact}`][int].

Returns a [`String{:tact}`][p] from an [`Int{:tact}`][int] value using a [fixed-point representation](https://en.wikipedia.org/wiki/Fixed-point_arithmetic) of a fractional number, where `self` is a significant part of the number and `digits` is a number of digits in the fractional part.

More precisely, `digits` is an exponentiation parameter of $10^{-\mathrm{digits}}$ expression, which gives the represented fractional number when multiplied by the actual [`Int{:tact}`][int] value. Parameter `digits` is required to be in the semi-closed interval: $0 <=$ `digits` $< 78$, otherwise an exception with [exit code 134](/book/exit-codes#134) will be thrown: `Invalid argument`.

Usage example:

```tact
let fizz: String = (42).toFloatString(9); // "0.000000042"
```

## Int.toCoinsString

```tact
extends fun toCoinsString(self: Int): String;
```

Extension function for the [`Int{:tact}`][int].

Returns a [`String{:tact}`][p] from an [`Int{:tact}`][int] value using a [fixed-point representation](https://en.wikipedia.org/wiki/Fixed-point_arithmetic) of a fractional number. Alias to `self.toFloatString(9){:tact}`.

This is used to represent [nanoToncoin](book/integers#nanotoncoin) [`Int{:tact}`][int] values using strings.

Usage example:

```tact
let nanotons: Int = 42;
let fizz: String = nanotons.toCoinsString();
let buzz: String = nanotons.toFloatString(9);

fizz == buzz; // true, both store "0.000000042"
```

## Address.toString

```tact
extends fun toString(self: Address): String;
```

Extension function for the [`Address{:tact}`][p].

Returns a [`String{:tact}`][p] from an [`Address{:tact}`][p].

Usage example:

```tact
let community: Address = address("UQDpXLZKrkHsOuE_C1aS69C697wE568vTnqSeRfBXZfvmVOo");
let fizz: String = community.toString();
```

[p]: /book/types#primitive-types
[bool]: /book/types#booleans
[int]: /book/integers
[cell]: /book/cells#cells
[slice]: /book/cells#slices


## index.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/index.mdx)
# Reference overview

import { Cards, Steps } from 'nextra/components'

Welcome to the **Reference** section of Tact documentation — a place for discovering the Tact's standard library, grammar specification and evolution process.

Here are its main contents:

<Steps>

### Core library

[Core library](/ref/core-base) gives a comprehensive list of auto-included functions, traits and other constructs with examples of their usage.

<Cards>
  <Cards.Card
    arrow
    title="Go to the Core library"
    href="/ref/core-base"
  />
</Cards>

### Standard libraries

[Standard libraries](/ref/standard-libraries) sub-section explains how to use the bundled libraries, lists all their contents with examples of their usage.

<Cards>
  <Cards.Card
    arrow
    title="Go to Standard libraries"
    href="/ref/standard-libraries"
  />
</Cards>

### Specification

[Specification](/ref/spec) page provides full Tact grammar written in Ohm language, which is used in the Tact's compiler. Aimed at more experienced programmers, but generally can still be very handy to quickly grasp all of the possible syntax in the language.

<Cards>
  <Cards.Card
    arrow
    title="Go to the Specification"
    href="/ref/spec"
  />
</Cards>

### Evolution

Finally, [Evolution](/ref/evolution/overview) sub-section gives insight on important decisions about language semantics, Tact's future and links to the up-to-date changelog of Tact updates.

<Cards>
  <Cards.Card
    arrow
    title="Go to the Evolution"
    href="/ref/evolution/overview"
  />
</Cards>

</Steps>


## spec.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/spec.mdx)
# Tact Specification

import { Callout } from 'nextra/components'

<Callout emoji="🚨">
  This page is mostly a stub until it's implemented in [#76](https://github.com/tact-lang/tact-docs/issues/76)
</Callout>

Tact grammar used in its compiler is written in an [Ohm language](https://ohmjs.org), which is based on [parsing expression grammars](http://en.wikipedia.org/wiki/Parsing_expression_grammar) (PEGs), which are a formal way of describing syntax, similar to regular expressions and context-free grammars.

{/*
    This is a comment and it's hidden from the page.

    Shiki does a bad job of highlighting Ohm via TextMate grammar, although it works well in VSCode. I think the reason may be either due to Shiki highlighting line by line or that it uses a different RegEx engine. I'm not sure what's the issue there, so until it's fixed it's better to use tree-sitter-ohm and generate ANSI sequences using its `highlight` command. Then Shiki does the rest:
*/}

```ansi
[38;5;23mTact[0m [38;5;239m{[0m

    [3;38;5;245m// Starting point of the program[0m
    [38;5;26mProgram[0m [1;38;5;239m=[0m [38;5;26mProgramItem[0m[1;38;5;239m*[0m
    [38;5;26mProgramItem[0m [1;38;5;239m=[0m [38;5;26mStruct[0m
                [1;38;5;239m|[0m [38;5;26mContract[0m
                [1;38;5;239m|[0m [38;5;26mPrimitive[0m
                [1;38;5;239m|[0m [38;5;26mStaticFunction[0m
                [1;38;5;239m|[0m [38;5;26mNativeFunction[0m
                [1;38;5;239m|[0m [38;5;26mProgramImport[0m
                [1;38;5;239m|[0m [38;5;26mTrait[0m
                [1;38;5;239m|[0m [38;5;26mConstant[0m
    [38;5;26mProgramImport[0m [1;38;5;239m=[0m [38;5;26mimport[0m [38;5;26mstringLiteral[0m [38;5;28m";"[0m

    [3;38;5;245m// Built-in declarations[0m
    [38;5;26mPrimitive[0m [1;38;5;239m=[0m [38;5;28m"primitive"[0m [38;5;26mType[0m [38;5;28m";"[0m

    [3;38;5;245m// Static function[0m
    [38;5;26mStaticFunction[0m [1;38;5;239m=[0m [38;5;26mFunction[0m
    [38;5;26mNativeFunction[0m [1;38;5;239m=[0m [38;5;26mnameAttribute[0m [38;5;28m"("[0m [38;5;26mfuncId[0m [38;5;28m")"[0m [38;5;26mFunctionAttribute[0m[1;38;5;239m*[0m [38;5;26mnative[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mFunctionArg[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m [38;5;28m";"[0m [3;38;5;124m--withVoid[0m
                   [1;38;5;239m|[0m [38;5;26mnameAttribute[0m [38;5;28m"("[0m [38;5;26mfuncId[0m [38;5;28m")"[0m [38;5;26mFunctionAttribute[0m[1;38;5;239m*[0m [38;5;26mnative[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mFunctionArg[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;28m";"[0m [3;38;5;124m--withType[0m

    [3;38;5;245m// Field declarations[0m
    [38;5;26mType[0m [1;38;5;239m=[0m [38;5;26mtypeLiteral[0m [38;5;28m"?"[0m [3;38;5;124m--optional[0m
         [1;38;5;239m|[0m [38;5;26mtypeLiteral[0m [3;38;5;124m--required[0m
         [1;38;5;239m|[0m [38;5;28m"map"[0m [38;5;28m"<"[0m [38;5;26mtypeLiteral[0m [38;5;239m([0m[38;5;26mas[0m [38;5;26mid[0m[38;5;239m)[0m[1;38;5;239m?[0m [38;5;28m","[0m [38;5;26mtypeLiteral[0m [38;5;239m([0m[38;5;26mas[0m [38;5;26mid[0m[38;5;239m)[0m[1;38;5;239m?[0m [38;5;28m">"[0m [3;38;5;124m--map[0m
         [1;38;5;239m|[0m [38;5;28m"bounced"[0m [38;5;28m"<"[0m [38;5;26mtypeLiteral[0m [38;5;28m">"[0m [3;38;5;124m--bounced[0m
    [38;5;26mField[0m [1;38;5;239m=[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;28m";"[0m [3;38;5;124m--default[0m
          [1;38;5;239m|[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;28m"="[0m [38;5;26mExpression[0m [38;5;28m";"[0m [3;38;5;124m--defaultWithInit[0m
          [1;38;5;239m|[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;26mas[0m [38;5;26mid[0m [38;5;28m";"[0m [3;38;5;124m--withSerialization[0m
          [1;38;5;239m|[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;26mas[0m [38;5;26mid[0m [38;5;28m"="[0m [38;5;26mExpression[0m [38;5;28m";"[0m [3;38;5;124m--withSerializationAndInit[0m

    [3;38;5;245m// Constant[0m
    [38;5;26mConstantAttribute[0m [1;38;5;239m=[0m [38;5;26mvirtual[0m    [3;38;5;124m--virtual[0m
                      [1;38;5;239m|[0m [38;5;26moverride[0m   [3;38;5;124m--override[0m
                      [1;38;5;239m|[0m [38;5;26mabstract[0m   [3;38;5;124m--abstract[0m
    [38;5;26mConstant[0m [1;38;5;239m=[0m [38;5;26mConstantAttribute[0m[1;38;5;239m*[0m [1;38;5;239m~[0m[38;5;26mfun[0m [38;5;26mconst[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;28m"="[0m [38;5;26mExpression[0m [38;5;28m";"[0m [3;38;5;124m--withValue[0m
             [1;38;5;239m|[0m [38;5;26mConstantAttribute[0m[1;38;5;239m*[0m [1;38;5;239m~[0m[38;5;26mfun[0m [38;5;26mconst[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;28m";"[0m                [3;38;5;124m--withEmpty[0m

    [3;38;5;245m// Struct[0m
    [38;5;26mStruct[0m [1;38;5;239m=[0m [38;5;28m"struct"[0m [38;5;26mtypeLiteral[0m [38;5;28m"{"[0m [38;5;26mStructBody[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--originary[0m
           [1;38;5;239m|[0m [38;5;28m"message"[0m [38;5;26mtypeLiteral[0m [38;5;28m"{"[0m [38;5;26mStructBody[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--message[0m
           [1;38;5;239m|[0m [38;5;28m"message"[0m [38;5;28m"("[0m [38;5;26mintegerLiteral[0m [38;5;28m")"[0m [38;5;26mtypeLiteral[0m [38;5;28m"{"[0m [38;5;26mStructBody[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--messageWithId[0m
    [38;5;26mStructBody[0m [1;38;5;239m=[0m [38;5;26mField[0m

    [3;38;5;245m// Contract[0m
    [38;5;26mContract[0m [1;38;5;239m=[0m [38;5;26mContractAttribute[0m[1;38;5;239m*[0m [38;5;26mcontract[0m [38;5;26mid[0m [38;5;28m"{"[0m [38;5;26mContractBody[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--simple[0m
             [1;38;5;239m|[0m [38;5;26mContractAttribute[0m[1;38;5;239m*[0m [38;5;26mcontract[0m [38;5;26mid[0m [38;5;26mwith[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mid[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m"{"[0m [38;5;26mContractBody[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--withTraits[0m
    [38;5;26mContractInit[0m [1;38;5;239m=[0m [38;5;28m"init"[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mFunctionArg[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m
    [38;5;26mContractBody[0m [1;38;5;239m=[0m [38;5;26mField[0m
                 [1;38;5;239m|[0m [38;5;26mContractInit[0m
                 [1;38;5;239m|[0m [38;5;26mReceiveFunction[0m
                 [1;38;5;239m|[0m [38;5;26mFunction[0m
                 [1;38;5;239m|[0m [38;5;26mConstant[0m

    [3;38;5;245m// Trait[0m
    [38;5;26mTrait[0m [1;38;5;239m=[0m [38;5;26mContractAttribute[0m[1;38;5;239m*[0m [38;5;26mtrait[0m [38;5;26mid[0m [38;5;28m"{"[0m [38;5;26mTraitBody[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--originary[0m
          [1;38;5;239m|[0m [38;5;26mContractAttribute[0m[1;38;5;239m*[0m [38;5;26mtrait[0m [38;5;26mid[0m [38;5;26mwith[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mid[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m"{"[0m [38;5;26mTraitBody[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--withTraits[0m
    [38;5;26mTraitBody[0m [1;38;5;239m=[0m [38;5;26mField[0m
              [1;38;5;239m|[0m [38;5;26mReceiveFunction[0m
              [1;38;5;239m|[0m [38;5;26mFunction[0m
              [1;38;5;239m|[0m [38;5;26mConstant[0m

    [3;38;5;245m// Contract attributes[0m
    [38;5;26mContractAttribute[0m [1;38;5;239m=[0m [38;5;28m"@interface"[0m [38;5;28m"("[0m [38;5;26mstringLiteral[0m [38;5;28m")"[0m [3;38;5;124m--interface[0m

    [3;38;5;245m// Function[0m
    [38;5;26mFunctionAttribute[0m [1;38;5;239m=[0m [38;5;28m"get"[0m     [3;38;5;124m--getter[0m
                      [1;38;5;239m|[0m [38;5;26mmutates[0m   [3;38;5;124m--mutates[0m
                      [1;38;5;239m|[0m [38;5;26mextends[0m   [3;38;5;124m--extends[0m
                      [1;38;5;239m|[0m [38;5;26mvirtual[0m   [3;38;5;124m--virtual[0m
                      [1;38;5;239m|[0m [38;5;26moverride[0m  [3;38;5;124m--override[0m
                      [1;38;5;239m|[0m [38;5;26minline[0m    [3;38;5;124m--inline[0m
                      [1;38;5;239m|[0m [38;5;26mabstract[0m  [3;38;5;124m--abstract[0m
    [38;5;26mFunction[0m [1;38;5;239m=[0m [38;5;26mFunctionAttribute[0m[1;38;5;239m*[0m [38;5;26mfun[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mFunctionArg[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--withVoid[0m
             [1;38;5;239m|[0m [38;5;26mFunctionAttribute[0m[1;38;5;239m*[0m [38;5;26mfun[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mFunctionArg[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--withType[0m
             [1;38;5;239m|[0m [38;5;26mFunctionAttribute[0m[1;38;5;239m*[0m [38;5;26mfun[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mFunctionArg[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m [38;5;28m";"[0m [3;38;5;124m--abstractVoid[0m
             [1;38;5;239m|[0m [38;5;26mFunctionAttribute[0m[1;38;5;239m*[0m [38;5;26mfun[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mFunctionArg[0m[38;5;239m,[0m[38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;28m";"[0m [3;38;5;124m--abstractType[0m
    [38;5;26mFunctionArg[0m [1;38;5;239m=[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mType[0m

    [38;5;26mReceiveFunction[0m [1;38;5;239m=[0m [38;5;28m"receive"[0m [38;5;28m"("[0m [38;5;26mFunctionArg[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--simple[0m
                    [1;38;5;239m|[0m [38;5;28m"receive"[0m [38;5;28m"("[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--empty[0m
                    [1;38;5;239m|[0m [38;5;28m"receive"[0m [38;5;28m"("[0m [38;5;26mstringLiteral[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--comment[0m
                    [1;38;5;239m|[0m [38;5;28m"bounced"[0m [38;5;28m"("[0m [38;5;26mFunctionArg[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--bounced[0m
                    [1;38;5;239m|[0m [38;5;28m"external"[0m [38;5;28m"("[0m [38;5;26mFunctionArg[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--externalSimple[0m
                    [1;38;5;239m|[0m [38;5;28m"external"[0m [38;5;28m"("[0m [38;5;26mstringLiteral[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--externalComment[0m
                    [1;38;5;239m|[0m [38;5;28m"external"[0m [38;5;28m"("[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--externalEmpty[0m

    [3;38;5;245m// Statements[0m
    [38;5;26mStatement[0m [1;38;5;239m=[0m [38;5;26mStatementLet[0m
              [1;38;5;239m|[0m [38;5;26mStatementBlock[0m
              [1;38;5;239m|[0m [38;5;26mStatementReturn[0m
              [1;38;5;239m|[0m [38;5;26mStatementExpression[0m
              [1;38;5;239m|[0m [38;5;26mStatementAssign[0m
              [1;38;5;239m|[0m [38;5;26mStatementAugmentedAssign[0m
              [1;38;5;239m|[0m [38;5;26mStatementCondition[0m
              [1;38;5;239m|[0m [38;5;26mStatementWhile[0m
              [1;38;5;239m|[0m [38;5;26mStatementRepeat[0m
              [1;38;5;239m|[0m [38;5;26mStatementUntil[0m
    [38;5;26mStatementBlock[0m [1;38;5;239m=[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m
    [38;5;26mStatementLet[0m [1;38;5;239m=[0m [38;5;26mlet[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mType[0m [38;5;28m"="[0m [38;5;26mExpression[0m [38;5;28m";"[0m
    [38;5;26mStatementReturn[0m [1;38;5;239m=[0m [38;5;26mreturn[0m [38;5;26mExpression[0m [38;5;28m";"[0m [3;38;5;124m--withExpression[0m
                    [1;38;5;239m|[0m [38;5;26mreturn[0m [38;5;28m";"[0m [3;38;5;124m--withoutExpression    [0m
    [38;5;26mStatementExpression[0m [1;38;5;239m=[0m [38;5;26mExpression[0m [38;5;28m";"[0m
    [38;5;26mStatementAssign[0m [1;38;5;239m=[0m [38;5;26mLValue[0m [38;5;28m"="[0m [38;5;26mExpression[0m [38;5;28m";"[0m
    [38;5;26mStatementAugmentedAssign[0m [1;38;5;239m=[0m [38;5;26mStatementAugmentedAssignAdd[0m
                             [1;38;5;239m|[0m [38;5;26mStatementAugmentedAssignSub[0m
                             [1;38;5;239m|[0m [38;5;26mStatementAugmentedAssignMul[0m
                             [1;38;5;239m|[0m [38;5;26mStatementAugmentedAssignDiv[0m
                             [1;38;5;239m|[0m [38;5;26mStatementAugmentedAssignRem[0m
    [38;5;26mStatementAugmentedAssignAdd[0m [1;38;5;239m=[0m [38;5;26mLValue[0m [38;5;28m"+="[0m [38;5;26mExpression[0m [38;5;28m";"[0m
    [38;5;26mStatementAugmentedAssignSub[0m [1;38;5;239m=[0m [38;5;26mLValue[0m [38;5;28m"-="[0m [38;5;26mExpression[0m [38;5;28m";"[0m
    [38;5;26mStatementAugmentedAssignMul[0m [1;38;5;239m=[0m [38;5;26mLValue[0m [38;5;28m"*="[0m [38;5;26mExpression[0m [38;5;28m";"[0m
    [38;5;26mStatementAugmentedAssignDiv[0m [1;38;5;239m=[0m [38;5;26mLValue[0m [38;5;28m"/="[0m [38;5;26mExpression[0m [38;5;28m";"[0m
    [38;5;26mStatementAugmentedAssignRem[0m [1;38;5;239m=[0m [38;5;26mLValue[0m [38;5;28m"%="[0m [38;5;26mExpression[0m [38;5;28m";"[0m
    [38;5;26mStatementCondition[0m [1;38;5;239m=[0m [38;5;26mif[0m [38;5;26mExpression[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [1;38;5;239m~[0m[38;5;26melse[0m [3;38;5;124m--simple[0m
                       [1;38;5;239m|[0m [38;5;26mif[0m [38;5;26mExpression[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [38;5;26melse[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [3;38;5;124m--withElse[0m
                       [1;38;5;239m|[0m [38;5;26mif[0m [38;5;26mExpression[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [38;5;26melse[0m [38;5;26mStatementCondition[0m [3;38;5;124m--withElseIf[0m
    [38;5;26mStatementWhile[0m [1;38;5;239m=[0m [38;5;26mwhile[0m [38;5;28m"("[0m [38;5;26mExpression[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m
    [38;5;26mStatementRepeat[0m [1;38;5;239m=[0m [38;5;26mrepeat[0m [38;5;28m"("[0m [38;5;26mExpression[0m [38;5;28m")"[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m
    [38;5;26mStatementUntil[0m [1;38;5;239m=[0m [38;5;26mdo[0m [38;5;28m"{"[0m [38;5;26mStatement[0m[1;38;5;239m*[0m [38;5;28m"}"[0m [38;5;26muntil[0m [38;5;28m"("[0m [38;5;26mExpression[0m [38;5;28m")"[0m [38;5;28m";"[0m

    [3;38;5;245m// L-value[0m
    [38;5;26mLValue[0m [1;38;5;239m=[0m [38;5;26mid[0m [38;5;28m"."[0m [38;5;26mLValue[0m [3;38;5;124m--more[0m
           [1;38;5;239m|[0m [38;5;26mid[0m [3;38;5;124m--single[0m

    [3;38;5;245m// Expressions[0m
    [38;5;26mExpression[0m [1;38;5;239m=[0m [38;5;26mExpressionConditional[0m
    [38;5;26mExpressionConditional[0m [1;38;5;239m=[0m [38;5;26mExpressionOr[0m [38;5;28m"?"[0m [38;5;26mExpressionOr[0m [38;5;28m":"[0m [38;5;26mExpressionConditional[0m [3;38;5;124m--ternary[0m
                          [1;38;5;239m|[0m [38;5;26mExpressionOr[0m
    [38;5;26mExpressionOr[0m [1;38;5;239m=[0m [38;5;26mExpressionOr[0m [38;5;28m"||"[0m [38;5;26mExpressionAnd[0m [3;38;5;124m--or[0m
                 [1;38;5;239m|[0m [38;5;26mExpressionAnd[0m
    [38;5;26mExpressionAnd[0m [1;38;5;239m=[0m [38;5;26mExpressionAnd[0m [38;5;28m"&&"[0m [38;5;26mExpressionCompare[0m [3;38;5;124m--and[0m
                  [1;38;5;239m|[0m [38;5;26mExpressionCompare[0m
    [38;5;26mExpressionCompare[0m [1;38;5;239m=[0m [38;5;26mExpressionCompare[0m [38;5;28m"!="[0m [38;5;26mExpressionBinary[0m [3;38;5;124m--not[0m
                      [1;38;5;239m|[0m [38;5;26mExpressionCompare[0m [38;5;28m"=="[0m [38;5;26mExpressionBinary[0m [3;38;5;124m--eq[0m
                      [1;38;5;239m|[0m [38;5;26mExpressionCompare[0m [38;5;28m">"[0m [38;5;26mExpressionBinary[0m [3;38;5;124m--gt[0m
                      [1;38;5;239m|[0m [38;5;26mExpressionCompare[0m [38;5;28m">="[0m [38;5;26mExpressionBinary[0m [3;38;5;124m--gte[0m
                      [1;38;5;239m|[0m [38;5;26mExpressionCompare[0m [38;5;28m"<"[0m [38;5;26mExpressionBinary[0m [3;38;5;124m--lt[0m
                      [1;38;5;239m|[0m [38;5;26mExpressionCompare[0m [38;5;28m"<="[0m [38;5;26mExpressionBinary[0m [3;38;5;124m--lte[0m
                      [1;38;5;239m|[0m [38;5;26mExpressionBinary[0m
    [38;5;26mExpressionBinary[0m [1;38;5;239m=[0m [38;5;26mExpressionBinary[0m [38;5;28m">>"[0m [38;5;26mExpressionAdd[0m [3;38;5;124m--shr[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionBinary[0m [38;5;28m"<<"[0m [38;5;26mExpressionAdd[0m [3;38;5;124m--shl[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionBinary[0m [38;5;28m"&"[0m [38;5;26mExpressionAdd[0m [3;38;5;124m--bin_and[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionBinary[0m [38;5;28m"|"[0m [38;5;26mExpressionAdd[0m [3;38;5;124m--bin_or[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionAdd[0m
    [38;5;26mExpressionAdd[0m [1;38;5;239m=[0m [38;5;26mExpressionAdd[0m [38;5;28m"+"[0m [1;38;5;239m~[0m[38;5;28m"+"[0m [38;5;26mExpressionMul[0m [3;38;5;124m--add[0m
                  [1;38;5;239m|[0m [38;5;26mExpressionAdd[0m [38;5;28m"-"[0m [1;38;5;239m~[0m[38;5;28m"-"[0m [38;5;26mExpressionMul[0m [3;38;5;124m--sub[0m
                  [1;38;5;239m|[0m [38;5;26mExpressionMul[0m
    [38;5;26mExpressionMul[0m [1;38;5;239m=[0m [38;5;26mExpressionMul[0m [38;5;28m"*"[0m [38;5;26mExpressionUnary[0m [3;38;5;124m--mul[0m
                  [1;38;5;239m|[0m [38;5;26mExpressionMul[0m [38;5;28m"/"[0m [38;5;26mExpressionUnary[0m [3;38;5;124m--div[0m
                  [1;38;5;239m|[0m [38;5;26mExpressionMul[0m [38;5;28m"%"[0m [38;5;26mExpressionUnary[0m [3;38;5;124m--rem[0m
                  [1;38;5;239m|[0m [38;5;26mExpressionUnary[0m
    [38;5;26mExpressionUnary[0m [1;38;5;239m=[0m [38;5;28m"-"[0m [38;5;26mExpressionUnarySuffix[0m [3;38;5;124m--neg[0m
                    [1;38;5;239m|[0m [38;5;28m"+"[0m [38;5;26mExpressionUnarySuffix[0m [3;38;5;124m--add[0m
                    [1;38;5;239m|[0m [38;5;28m"!"[0m [38;5;26mExpressionUnarySuffix[0m [3;38;5;124m--not[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionUnarySuffix[0m
    [38;5;26mExpressionUnarySuffix[0m [1;38;5;239m=[0m [38;5;26mExpressionValue[0m [38;5;28m"!!"[0m [3;38;5;124m--notNull[0m
                          [1;38;5;239m|[0m [38;5;26mExpressionValue[0m
    [38;5;26mExpressionBracket[0m [1;38;5;239m=[0m [38;5;28m"("[0m [38;5;26mExpression[0m [38;5;28m")"[0m

    [3;38;5;245m// Order is important[0m
    [38;5;26mExpressionValue[0m [1;38;5;239m=[0m [38;5;26mExpressionCall[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionField[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionStaticCall[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionBracket[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionNew[0m
                    [1;38;5;239m|[0m [38;5;26mintegerLiteral[0m
                    [1;38;5;239m|[0m [38;5;26mboolLiteral[0m
                    [1;38;5;239m|[0m [38;5;26mid[0m
                    [1;38;5;239m|[0m [38;5;26mnull[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionInitOf[0m
                    [1;38;5;239m|[0m [38;5;26mExpressionString[0m
    [38;5;26mExpressionString[0m [1;38;5;239m=[0m [38;5;26mstringLiteral[0m
    [38;5;26mExpressionField[0m [1;38;5;239m=[0m [38;5;26mExpressionValue[0m [38;5;28m"."[0m [38;5;26mid[0m [1;38;5;239m~[0m[38;5;28m"("[0m
    [38;5;26mExpressionCall[0m [1;38;5;239m=[0m [38;5;26mExpressionValue[0m [38;5;28m"."[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mExpression[0m[38;5;239m,[0m [38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m
    [38;5;26mExpressionNew[0m [1;38;5;239m=[0m [38;5;26mid[0m [38;5;28m"{"[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mNewParameter[0m[38;5;239m,[0m [38;5;28m","[0m[38;5;239m>[0m [38;5;28m"}"[0m
    [38;5;26mNewParameter[0m [1;38;5;239m=[0m [38;5;26mid[0m [38;5;28m":"[0m [38;5;26mExpression[0m
    [38;5;26mExpressionStaticCall[0m [1;38;5;239m=[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mExpression[0m[38;5;239m,[0m [38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m
    [38;5;26mExpressionInitOf[0m [1;38;5;239m=[0m [38;5;26minitOf[0m [38;5;26mid[0m [38;5;28m"("[0m [1;38;5;26mListOf[0m[38;5;239m<[0m[38;5;26mExpression[0m[38;5;239m,[0m [38;5;28m","[0m[38;5;239m>[0m [38;5;28m")"[0m

    [3;38;5;245m// Type Literal[0m
    [38;5;26mtypeLiteral[0m [1;38;5;239m=[0m [38;5;26mletterAsciiUC[0m [38;5;26mtypeLiteralPart[0m[1;38;5;239m*[0m
    [38;5;26mtypeLiteralPart[0m [1;38;5;239m=[0m [38;5;26mletterAscii[0m [1;38;5;239m|[0m [1;38;5;26mdigit[0m [1;38;5;239m|[0m [38;5;28m"_"[0m

    [3;38;5;245m// Integer Literal[0m
    [3;38;5;245m// hexDigit defined in Ohm's built-in rules (otherwise: hexDigit = "0".."9" | "a".."f" | "A".."F")[0m
    [3;38;5;245m// digit defined in Ohm's built-in rules (otherwise: digit = "0".."9")[0m
    [38;5;26mintegerLiteral[0m [1;38;5;239m=[0m [38;5;26mintegerLiteralHex[0m [1;38;5;239m|[0m [38;5;26mintegerLiteralBin[0m [1;38;5;239m|[0m [38;5;26mintegerLiteralOct[0m [1;38;5;239m|[0m [38;5;26mintegerLiteralDec[0m [3;38;5;245m// Order is important[0m
    [38;5;26mintegerLiteralDec[0m [1;38;5;239m=[0m [38;5;26mnonZeroDigit[0m [38;5;239m([0m[38;5;28m"_"[0m[1;38;5;239m?[0m [1;38;5;26mdigit[0m[38;5;239m)[0m[1;38;5;239m*[0m  [3;38;5;124m--nonZeroIntegerLiteralDec[0m
                      [1;38;5;239m|[0m [38;5;28m"0"[0m [1;38;5;26mdigit[0m[1;38;5;239m*[0m                  [3;38;5;124m--integerLiteralWithLeadingZero[0m
    [38;5;26mintegerLiteralHex[0m [1;38;5;239m=[0m [38;5;239m([0m[38;5;28m"0x"[0m [1;38;5;239m|[0m [38;5;28m"0X"[0m[38;5;239m)[0m [1;38;5;26mhexDigit[0m [38;5;239m([0m[38;5;28m"_"[0m[1;38;5;239m?[0m [1;38;5;26mhexDigit[0m[38;5;239m)[0m[1;38;5;239m*[0m
    [38;5;26mintegerLiteralBin[0m [1;38;5;239m=[0m [38;5;239m([0m[38;5;28m"0b"[0m [1;38;5;239m|[0m [38;5;28m"0B"[0m[38;5;239m)[0m [38;5;26mbinDigit[0m [38;5;239m([0m[38;5;28m"_"[0m[1;38;5;239m?[0m [38;5;26mbinDigit[0m[38;5;239m)[0m[1;38;5;239m*[0m
    [38;5;26mintegerLiteralOct[0m [1;38;5;239m=[0m [38;5;239m([0m[38;5;28m"0o"[0m [1;38;5;239m|[0m [38;5;28m"0O"[0m[38;5;239m)[0m [38;5;26moctDigit[0m [38;5;239m([0m[38;5;28m"_"[0m[1;38;5;239m?[0m [38;5;26moctDigit[0m[38;5;239m)[0m[1;38;5;239m*[0m
    [38;5;26mbinDigit[0m [1;38;5;239m=[0m [38;5;28m"0"[0m [1;38;5;239m|[0m [38;5;28m"1"[0m
    [38;5;26moctDigit[0m [1;38;5;239m=[0m [38;5;28m"0"[0m[1;38;5;239m..[0m[38;5;28m"7"[0m
    [38;5;26mnonZeroDigit[0m [1;38;5;239m=[0m [38;5;28m"1"[0m[1;38;5;239m..[0m[38;5;28m"9"[0m

    [3;38;5;245m// Letters[0m
    [38;5;26mletterAsciiLC[0m [1;38;5;239m=[0m [38;5;28m"a"[0m[1;38;5;239m..[0m[38;5;28m"z"[0m
    [38;5;26mletterAsciiUC[0m [1;38;5;239m=[0m [38;5;28m"A"[0m[1;38;5;239m..[0m[38;5;28m"Z"[0m
    [38;5;26mletterAscii[0m [1;38;5;239m=[0m [38;5;26mletterAsciiLC[0m [1;38;5;239m|[0m [38;5;26mletterAsciiUC[0m
    [38;5;26mletterComment[0m [1;38;5;239m=[0m [38;5;26mletterAsciiLC[0m [1;38;5;239m|[0m [38;5;26mletterAsciiUC[0m [1;38;5;239m|[0m [1;38;5;26mdigit[0m [1;38;5;239m|[0m [38;5;28m"_"[0m

    [3;38;5;245m// ID Literal[0m
    [38;5;26midStart[0m [1;38;5;239m=[0m [38;5;26mletterAscii[0m [1;38;5;239m|[0m [38;5;28m"_"[0m
    [38;5;26midPart[0m [1;38;5;239m=[0m [38;5;26mletterAscii[0m [1;38;5;239m|[0m [1;38;5;26mdigit[0m [1;38;5;239m|[0m [38;5;28m"_"[0m
    [38;5;26mid[0m [1;38;5;239m=[0m [1;38;5;239m~[0m[38;5;26mreservedWord[0m [1;38;5;239m#[0m[38;5;26midStart[0m [1;38;5;239m#[0m[38;5;239m([0m[38;5;26midPart[0m[1;38;5;239m*[0m[38;5;239m)[0m

    [3;38;5;245m// FunC id[0m
    [38;5;26mfuncLetter[0m [1;38;5;239m=[0m [38;5;26mletterAscii[0m [1;38;5;239m|[0m [38;5;28m"_"[0m [1;38;5;239m|[0m [38;5;28m"'"[0m [1;38;5;239m|[0m [38;5;28m"?"[0m [1;38;5;239m|[0m [38;5;28m"!"[0m [1;38;5;239m|[0m [38;5;28m"::"[0m [1;38;5;239m|[0m [38;5;28m"&"[0m
    [38;5;26mfuncId[0m [1;38;5;239m=[0m [38;5;26mfuncLetter[0m [1;38;5;239m#[0m[38;5;239m([0m[38;5;26mfuncLetter[0m [1;38;5;239m|[0m [1;38;5;26mdigit[0m[38;5;239m)[0m[1;38;5;239m*[0m

    [3;38;5;245m// Bool Literal[0m
    [38;5;26mboolLiteral[0m [1;38;5;239m=[0m [38;5;239m([0m[38;5;28m"true"[0m [1;38;5;239m|[0m [38;5;28m"false"[0m[38;5;239m)[0m [1;38;5;239m~[0m[38;5;26midPart[0m

    [3;38;5;245m// String literal[0m
    [38;5;26mstringLiteralCharacter[0m [1;38;5;239m=[0m [1;38;5;239m~[0m[38;5;239m([0m[38;5;28m"[0m[38;5;30m\"[0m[38;5;28m"[0m [1;38;5;239m|[0m [38;5;28m"[0m[38;5;30m\\[0m[38;5;28m"[0m [1;38;5;239m|[0m [38;5;26mlineTerminator[0m[38;5;239m)[0m [1;38;5;26many[0m
    [38;5;26mstringLiteral[0m [1;38;5;239m=[0m [38;5;28m"[0m[38;5;30m\"[0m[38;5;28m"[0m [38;5;26mstringLiteralCharacter[0m[1;38;5;239m*[0m [38;5;28m"[0m[38;5;30m\"[0m[38;5;28m"[0m

    [3;38;5;245m// Keywords[0m
    [3;38;5;245m// NOTE Order is important[0m
    [38;5;26mkeyword[0m [1;38;5;239m=[0m [38;5;26mfun[0m
            [1;38;5;239m|[0m [38;5;26mlet[0m
            [1;38;5;239m|[0m [38;5;26mreturn[0m
            [1;38;5;239m|[0m [38;5;26mextend[0m
            [1;38;5;239m|[0m [38;5;26mnative[0m
            [1;38;5;239m|[0m [38;5;26mpublic[0m
            [1;38;5;239m|[0m [38;5;26mnull[0m
            [1;38;5;239m|[0m [38;5;26mif[0m
            [1;38;5;239m|[0m [38;5;26melse[0m
            [1;38;5;239m|[0m [38;5;26mwhile[0m
            [1;38;5;239m|[0m [38;5;26mrepeat[0m
            [1;38;5;239m|[0m [38;5;26mdo[0m
            [1;38;5;239m|[0m [38;5;26muntil[0m
            [1;38;5;239m|[0m [38;5;26mas[0m
            [1;38;5;239m|[0m [38;5;26mmutates[0m
            [1;38;5;239m|[0m [38;5;26mextends[0m
            [1;38;5;239m|[0m [38;5;26mimport[0m
            [1;38;5;239m|[0m [38;5;26mwith[0m
            [1;38;5;239m|[0m [38;5;26mtrait[0m
            [1;38;5;239m|[0m [38;5;26minitOf[0m
            [1;38;5;239m|[0m [38;5;26moverride[0m
            [1;38;5;239m|[0m [38;5;26mabstract[0m
            [1;38;5;239m|[0m [38;5;26mvirtual[0m
            [1;38;5;239m|[0m [38;5;26minline[0m
            [1;38;5;239m|[0m [38;5;26mconst[0m
    [38;5;26mcontract[0m [1;38;5;239m=[0m [38;5;28m"contract"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mlet[0m [1;38;5;239m=[0m [38;5;28m"let"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mfun[0m [1;38;5;239m=[0m [38;5;28m"fun"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mreturn[0m [1;38;5;239m=[0m [38;5;28m"return"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mextend[0m [1;38;5;239m=[0m [38;5;28m"extend"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mnative[0m [1;38;5;239m=[0m [38;5;28m"native"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mpublic[0m [1;38;5;239m=[0m [38;5;28m"public"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mnull[0m [1;38;5;239m=[0m [38;5;28m"null"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mif[0m [1;38;5;239m=[0m [38;5;28m"if"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26melse[0m [1;38;5;239m=[0m [38;5;28m"else"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mwhile[0m [1;38;5;239m=[0m [38;5;28m"while"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mrepeat[0m [1;38;5;239m=[0m [38;5;28m"repeat"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mdo[0m [1;38;5;239m=[0m [38;5;28m"do"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26muntil[0m [1;38;5;239m=[0m [38;5;28m"until"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mas[0m [1;38;5;239m=[0m [38;5;28m"as"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mmutates[0m [1;38;5;239m=[0m [38;5;28m"mutates"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mextends[0m [1;38;5;239m=[0m [38;5;28m"extends"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mimport[0m [1;38;5;239m=[0m [38;5;28m"import"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mwith[0m [1;38;5;239m=[0m [38;5;28m"with"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mtrait[0m [1;38;5;239m=[0m [38;5;28m"trait"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26minitOf[0m [1;38;5;239m=[0m [38;5;28m"initOf"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mvirtual[0m [1;38;5;239m=[0m [38;5;28m"virtual"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26moverride[0m [1;38;5;239m=[0m [38;5;28m"override"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26minline[0m [1;38;5;239m=[0m [38;5;28m"inline"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mconst[0m [1;38;5;239m=[0m [38;5;28m"const"[0m [1;38;5;239m~[0m[38;5;26midPart[0m
    [38;5;26mabstract[0m [1;38;5;239m=[0m [38;5;28m"abstract"[0m [1;38;5;239m~[0m[38;5;26midPart[0m

    [3;38;5;245m// Attributes[0m
    [38;5;26mnameAttribute[0m [1;38;5;239m=[0m [38;5;28m"@name"[0m

    [3;38;5;245m// Reserved[0m
    [38;5;26mreservedWord[0m [1;38;5;239m=[0m [38;5;26mkeyword[0m

    [3;38;5;245m// Comments[0m
    [38;5;26mspace[0m [1;38;5;239m+=[0m [38;5;26mcomment[0m [1;38;5;239m|[0m [38;5;26mlineTerminator[0m
    [38;5;26mcomment[0m [1;38;5;239m=[0m [38;5;26mmultiLineComment[0m [1;38;5;239m|[0m [38;5;26msingleLineComment[0m
    [38;5;26mlineTerminator[0m [1;38;5;239m=[0m [38;5;28m"[0m[38;5;30m\n[0m[38;5;28m"[0m [1;38;5;239m|[0m [38;5;28m"[0m[38;5;30m\r[0m[38;5;28m"[0m [1;38;5;239m|[0m [38;5;28m"[0m[38;5;30m\u2028[0m[38;5;28m"[0m [1;38;5;239m|[0m [38;5;28m"[0m[38;5;30m\u2029[0m[38;5;28m"[0m
    [38;5;26mmultiLineComment[0m [1;38;5;239m=[0m [38;5;28m"/*"[0m [38;5;239m([0m[1;38;5;239m~[0m[38;5;28m"*/"[0m [1;38;5;26many[0m[38;5;239m)[0m[1;38;5;239m*[0m [38;5;28m"*/"[0m
    [38;5;26msingleLineComment[0m [1;38;5;239m=[0m [38;5;28m"//"[0m [38;5;239m([0m[1;38;5;239m~[0m[38;5;26mlineTerminator[0m [1;38;5;26many[0m[38;5;239m)[0m[1;38;5;239m*[0m
[38;5;239m}[0m
```

## standard-libraries.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/standard-libraries.mdx)
# Standard libraries overview

import { Callout } from 'nextra-theme-docs'

Some libraries (also referred to as standard libraries or stdlibs) come bundled with Tact compiler, but aren't automatically included to your project until explicitly made to.

To import any standard library, use the [`import{:tact}` keyword](/book/import) followed by the name of that library in a [string][p], like so:

```tact
// This would include everything from @stdlib/deploy into your codebase:
import "@stdlib/deploy";
```

## List of standard libraries: [#list]

Library                  | Description                                                      | Commonly used APIs
:----------------------- | :--------------------------------------------------------------- | :-----------------
[`@stdlib/config`][1]    | Config and elector address retrieval.                            | [`getConfigAddress(){:tact}`][gca], [`getElectorAddress(){:tact}`][gea]
[`@stdlib/content`][2]   | Encoding off-chain link [strings][p] to a [`Cell{:tact}`][cell]. | [`createOffchainContent(){:tact}`][coff]
[`@stdlib/deploy`][3]    | Unified mechanism for deployments.                               | [`Deployable{:tact}`][dep], [`FactoryDeployable{:tact}`][fcd]
[`@stdlib/dns`][4]       | Resolution of [DNS][dns] names.                                  | [`DNSResolver{:tact}`][dnsr], [`dnsInternalVerify(){:tact}`][dnsi]
[`@stdlib/ownable`][5]   | Traits for ownership management.                                 | [`Ownable{:tact}`][own], [`OwnableTransferable{:tact}`][ownt]
[`@stdlib/stoppable`][6] | Traits that allow contract stops. Requires [@stdlib/ownable][5]. | [`Stoppable{:tact}`][stp], [`Resumable{:tact}`][res]

[1]: /ref/stdlib-config
[gca]: /ref/stdlib-config#getconfigaddress
[gea]: /ref/stdlib-config#getelectoraddress

[2]: /ref/stdlib-content
[coff]: /ref/stdlib-content#createoffchaincontent

[3]: /ref/stdlib-deploy
[dep]: /ref/stdlib-deploy#deployable
[fcd]: /ref/stdlib-deploy#factorydeployable

[4]: /ref/stdlib-dns
[dnsr]: /ref/stdlib-dns#dnsresolver
[dnsi]: /ref/stdlib-dns#dnsinternalverify

[5]: /ref/stdlib-ownable
[own]: /ref/stdlib-ownable#ownable
[ownt]: /ref/stdlib-ownable#ownabletransferable

[6]: /ref/stdlib-stoppable
[stp]: /ref/stdlib-stoppable#stoppable
[res]: /ref/stdlib-stoppable#resumable

[p]: /book/types#primitive-types
[cell]: /book/cells#cells
[dns]: https://docs.ton.org/participate/web3/dns


## stdlib-config.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/stdlib-config.mdx)
# @stdlib/config

Provides functions for config and elector Address retrieval.

To use this library, import `@stdlib/config`:

```tact
import "@stdlib/config";
```

## Functions

### getConfigAddress

```tact
fun getConfigAddress(): Address;
```

Retrieves config parameter $0$ as an [`Address{:tact}`][p].

Source code:

```tact
fun getConfigAddress(): Address {
    let cell: Cell = getConfigParam(0)!!;
    let sc: Slice = cell.beginParse();
    return newAddress(-1, sc.loadUint(256));
}
```

### getElectorAddress

```tact
fun getElectorAddress(): Address;
```

Retrieves config parameter $1$ as an [`Address{:tact}`][p].

Source code:

```tact
fun getElectorAddress(): Address {
    let cell: Cell = getConfigParam(1)!!;
    let sc: Slice = cell.beginParse();
    return newAddress(-1, sc.loadUint(256));
}
```

## Sources

* [config.tact](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/config.tact)

[p]: /book/types#primitive-types


## stdlib-content.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/stdlib-content.mdx)
# @stdlib/content

Provides a function for encoding an off-chain link from a [`String{:tact}`][p] to a [`Cell{:tact}`][cell].

To use this library, import `@stdlib/content`:

```tact
import "@stdlib/content";
```

## Functions

### createOffchainContent

```tact
fun createOffchainContent(link: String): Cell;
```

Encodes an off-chain `link` from a [`String{:tact}`][p] to a [`Cell{:tact}`][cell].

Source code:

```tact
fun createOffchainContent(link: String): Cell {
    let builder: StringBuilder = beginStringFromBuilder(beginCell().storeUint(0x01, 8));
    builder.append(link);
    return builder.toCell();
}
```

## Sources

* [content.tact](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/content.tact)

[p]: /book/types#primitive-types
[cell]: /book/cells#cells


## stdlib-deploy.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/stdlib-deploy.mdx)
# @stdlib/deploy

Provides unified mechanisms for deployments.

To use this library, import `@stdlib/deploy`:

```tact
import "@stdlib/deploy";
```

## Messages

### Deploy

```tact
message Deploy {
    queryId: Int as uint64;
}
```

### DeployOk

```tact
message DeployOk {
    queryId: Int as uint64;
}
```

### FactoryDeploy

```tact
message FactoryDeploy {
    queryId: Int as uint64;
    cashback: Address;
}
```

## Traits

### Deployable

Simplest trait `Deployable{:tact}` that provides a handy unified mechanism for deployments by implementing a simple receiver for the [Deploy](#deploy) message.

All contracts are deployed by sending them a message. While any message can be used for this purpose, best practice is to use the special [Deploy](#deploy) message.

This message has a single field, `queryId`, provided by the deployer (usually set to zero). If the deployment succeeds, the contract will reply with a [DeployOk](#deployok) message and echo the same `queryId` in the response.

Source code:

```tact
trait Deployable {
    receive(deploy: Deploy) {
        self.notify(DeployOk{queryId: deploy.queryId}.toCell());
    }
}
```

Usage example:

```tact /Deployable/
import "@stdlib/deploy";

contract ExampleContract with Deployable {
    // Now, this contract has a receiver for Deploy message
}
```

### FactoryDeployable

Trait `FactoryDeployable{:tact}` provides a handy unified mechanism for chained deployments.

Source code:

```tact
trait FactoryDeployable  {
    receive(deploy: FactoryDeploy) {
        self.forward(deploy.cashback, DeployOk{queryId: deploy.queryId}.toCell(), false, null);
    }
}
```

Usage example:

```tact /FactoryDeployable/
import "@stdlib/deploy";

contract ExampleContract with FactoryDeployable {
    // Now, this contract has a receiver for FactoryDeploy message
}
```

## Sources

* [deploy.tact](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/deploy.tact)


## stdlib-dns.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/stdlib-dns.mdx)
# @stdlib/dns

Provides means for resolution of [DNS](https://docs.ton.org/participate/web3/dns) names.

To use this library, import `@stdlib/dns`:

```tact
import "@stdlib/dns";
```

## Structs

### DNSResolveResult

```tact
struct DNSResolveResult {
    prefix: Int;
    record: Cell?;
}
```

## Functions

### dnsStringToInternal

```tact
@name(dns_string_to_internal)
native dnsStringToInternal(str: String): Slice?;
```

Converts a DNS string to a [`Slice{:tact}`][slice] or [`null{:tact}`](/book/optionals), if it's impossible.

Source code (FunC): [dns.fc#L1](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/dns.fc#L1)

### dnsInternalNormalize

```tact
@name(dns_internal_normalize)
native dnsInternalNormalize(src: Slice): Slice;
```

Normalizes the internal DNS representation of the [`Slice{:tact}`][slice].

Source code (FunC): [dns.fc#L125](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/dns.fc#L125)

### dnsInternalVerify

```tact
@name(dns_internal_verify)
native dnsInternalVerify(subdomain: Slice): Bool;
```

Verifies the internal DNS representation of the subdomain [`Slice{:tact}`][slice].

Source code (FunC): [dns.fc#L81](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/dns.fc#L81)

### dnsExtractTopDomainLength

```tact
fun dnsExtractTopDomainLength(subdomain: Slice): Int;
```

Calculates length of a top domain in the `subdomain` [`Slice{:tact}`][slice].

Source code:

```tact
fun dnsExtractTopDomainLength(subdomain: Slice): Int {
    let i: Int = 0;
    let needBreak: Bool = false;
    do {
        let char: Int = subdomain.loadUint(8); // we do not check domain.length because it MUST contain \0 character
        needBreak = char == 0;
        if (!needBreak) {
            i += 8;
        }
    } until (needBreak);
    require(i != 0, "Invalid DNS name");
    return i;
}
```

### dnsExtractTopDomain

```tact
fun dnsExtractTopDomain(subdomain: Slice): Slice;
```

Extracts top domain from a `subdomain` [`Slice{:tact}`][slice].

Source code:

```tact
fun dnsExtractTopDomain(subdomain: Slice): Slice {
    let len: Int = dnsExtractTopDomainLength(subdomain);
    return subdomain.loadBits(len);
}
```

### dnsResolveNext

```tact
fun dnsResolveNext(address: Address): Cell;
```

Resolves an `address` [`Address{:tact}`][p] into a [`Cell{:tact}`][cell].

Source code:

```tact
fun dnsResolveNext(address: Address): Cell {
    return beginCell()
        .storeUint(0xba93, 16)
        .storeAddress(address)
        .endCell();
}
```

### dnsResolveWallet

```tact
fun dnsResolveWallet(address: Address): Cell;
```

Resolves a wallet `address` [`Address{:tact}`][p] into a [`Cell{:tact}`][cell].

Source code:

```tact
fun dnsResolveWallet(address: Address): Cell {
    return beginCell()
        .storeUint(0x9fd3, 16)
        .storeAddress(address)
        .storeUint(0, 8)
        .endCell();
}
```

## Traits

### DNSResolver

Trait `DNSResolver` provides two helper functions for DNS resolution:

1. [getter function](/book/functions#getter-functions) `dnsresolve(){:tact}`, which corresponds to its [FunC variant](https://docs.ton.org/develop/howto/subresolvers#dnsresolve-code).
2. virtual function `doResolveDNS(){:tact}`, which creates a struct [DNSResolveResult](#dnsresolveresult) out of subdomain [`Slice{:tact}`][slice] bits.

Source code:

```tact
trait DNSResolver {
    get fun dnsresolve(subdomain: Slice, category: Int): DNSResolveResult {
        // Normalize
        let delta: Int = 0;
        if (subdomain.preloadUint(8) == 0) {
            subdomain.loadUint(8); // Skip first byte
            delta += 8;
        }

        // Checks correctness
        require(dnsInternalVerify(subdomain), "Invalid DNS name");

        // Resolve
        let res: DNSResolveResult = self.doResolveDNS(subdomain, category);
        return DNSResolveResult{prefix: res.prefix + delta, record: res.record};
    }
    virtual fun doResolveDNS(subdomain: Slice, category: Int): DNSResolveResult {
        return DNSResolveResult{prefix: subdomain.bits(), record: null};
    }
}
```

Usage example:

```tact
import "@stdlib/dns";

contract ExampleContract with DNSResolver {
    // Now, this contract has a:
    // 1. dnsresolve getter function
    // 2. doResolveDNS virtual function
}
```

## Sources

* [dns.tact](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/dns.tact)
* [dns.fc](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/dns.fc)

[p]: /book/types#primitive-types
[cell]: /book/cells#cells
[slice]: /book/cells#slices


## stdlib-ownable.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/stdlib-ownable.mdx)
# @stdlib/ownable

Provides [traits](/book/types#composite-types) for ownable contracts. This is most commonly used trait that is required by most other traits.

To use this library, import `@stdlib/ownable`:

```tact
import "@stdlib/ownable";
```

## Messages

### ChangeOwner

```tact
message ChangeOwner {
    queryId: Int as uint64;
    newOwner: Address;
}
```

### ChangeOwnerOk

```tact
message ChangeOwnerOk {
    queryId: Int as uint64;
    newOwner: Address;
}
```

## Traits

### Ownable

[Trait](/book/types#composite-types) `Ownable{:tact}` declares an owner (non-editable) of a [contract](/book/contracts) and provides a helper function `requireOwner(){:tact}` that checks that a message was sent by an owner.

This [trait](/book/types#composite-types) requires a field `owner: Address{:tact}` to be declared and exposes a [getter function](/book/functions#getter-functions) `owner(){:tact}`, which reads it from the [contract](/book/contracts).

Source code:

```tact
@interface("org.ton.ownable")
trait Ownable {
    owner: Address;

    fun requireOwner() {
        nativeThrowUnless(132, sender() == self.owner);
    }

    get fun owner(): Address {
        return self.owner;
    }
}
```

Usage example:

```tact /Ownable/
import "@stdlib/ownable";

contract ExampleContract with Ownable {
    owner: Address;

    init(owner: Address) {
        self.owner = owner;
    }
}
```

### OwnableTransferable

`OwnableTransferable{:tact}` is an extension of an [`Ownable{:tact}`](#ownable) that allows to transfer ownership of a contract to another address. It provides a secure handle [Message](/book/structs-and-messages#messages) [`ChangeOwner{:tact}`](#changeowner) that could be called by an owner to transfer ownership.

If the owner transfer request succeeds, the contract will reply with a [`ChangeOwnerOk{:tact}`](#changeownerok) [Message](/book/structs-and-messages#messages).

Source code:

```tact
@interface("org.ton.ownable.transferable.v2")
trait OwnableTransferable with Ownable {
    owner: Address;

    receive(msg: ChangeOwner) {
        // Check if the sender is the owner
        self.requireOwner();

        // Update owner
        self.owner = msg.newOwner;

        // Reply result
        self.reply(ChangeOwnerOk{ queryId: msg.queryId, newOwner: msg.newOwner }.toCell());
    }
}
```

Usage example:

```tact /OwnableTransferable/
import "@stdlib/ownable";

contract ExampleContract with OwnableTransferable {
    owner: Address;

    init(owner: Address) {
        self.owner = owner;
    }
}
```

## Sources

* [ownable.tact](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/ownable.tact)


## stdlib-stoppable.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/stdlib-stoppable.mdx)
# @stdlib/stoppable

Provides [traits](/book/types#composite-types) that allow to stop a [contract](/book/contracts). Useful for emergency or maintenance modes. Requires an [`Ownable{:tact}`](/ref/stdlib-ownable#ownable) trait from [`@stdlib/ownable`](/ref/stdlib-ownable). This trait just manages a single flag `stopped` in the contract and handling stopped state have to be done in the contract itself.

To use this library, import `@stdlib/stoppable`:

```tact
import "@stdlib/stoppable"; // this would automatically import @stdlib/ownable too!
```

## Traits

### Stoppable

[Trait](/book/types#composite-types) `Stoppable{:tact}` implements receiver for the [Message](/book/structs-and-messages#messages) [string](/book/types#primitive-types) "Stop" that can be sent by owner, implements `stopped(){:tact}` [getter function](/book/functions#getter-functions) that returns `true{:tact}` if contract is stopped (or `false{:tact}` otherwise) and provides private (non-getter) functions `requireNotStopped(){:tact}` and `requireStopped(){:tact}`.

Source code:

```tact
@interface("org.ton.stoppable")
trait Stoppable with Ownable {
    stopped: Bool;
    owner: Address;

    fun requireNotStopped() {
        require(!self.stopped, "Contract stopped");
    }

    fun requireStopped() {
        require(self.stopped, "Contract not stopped");
    }

    receive("Stop") {
        self.requireOwner();
        self.requireNotStopped();
        self.stopped = true;
        self.reply("Stopped".asComment());
    }

    get fun stopped(): Bool {
        return self.stopped;
    }
}
```

Usage example:

```tact /Stoppable/
import "@stdlib/ownable";
import "@stdlib/stoppable";

contract MyContract with Stoppable {
    owner: Address;
    stopped: Bool;

    init(owner: Address) {
        self.owner = owner;
        self.stopped = false;
    }
}
```

### Resumable

`Resumable{:tact}` [trait](/book/types#composite-types) extends [`Stoppable{:tact}`](#stoppable) trait and allows to resume [contract](/book/contracts) execution.

Source code:

```tact
@interface("org.ton.resumable")
trait Resumable with Stoppable {
    stopped: Bool;
    owner: Address;

    receive("Resume") {
        self.requireOwner();
        self.requireStopped();
        self.stopped = false;
        self.reply("Resumed".asComment());
    }
}
```

Usage example:

```tact /Resumable/
import "@stdlib/ownable";
import "@stdlib/stoppable";

contract MyContract with Resumable {
    owner: Address;
    stopped: Bool;

    init(owner: Address) {
        self.owner = owner;
        self.stopped = false;
    }
}
```

## Sources

* [stoppable.tact](https://github.com/tact-lang/tact/blob/61541b7783098e1af669faccd7d2334c10981c72/stdlib/libs/stoppable.tact)


## OTP-001.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/evolution/OTP-001.mdx)
---
title: "OTP-001: Supported Interfaces"
---

# OTP-001: Supported Interfaces

This proposal recommends a way to introspect smart contracts and find out what interfaces they support.

## Motivation

Right now it is impossible to guess what a user wants to do with a contract or can't figure out what the transaction is about because there is no clear way to find what a contract is about. Humans need to remember or guess what this was about in most ways.

## Guide

When human tries to sign a transaction, they need to understand clearly what they are doing: minting, token transfer, staking, DAO voting. While Ethereum wallets support signing arbitrary structures it is still not clear what are you signing and what's the implications of doing so. In the same way, explorers can't show what's going on in a nice form.

The start of a working with specific contract is a performing introspection - figuring out what the contract declares about itself. When the app knows what this contract is about it could build a good UI, show transaction history, and verify what a human tries to sign.

This proposal describes a way to report what interfaces the contract supports.

Interfaces are defined in a free-form specification. Unlike most of the other approaches, this proposal defines interface as not only the technical interface of a contract (get methods, internal messages, etc) but also a description of its behavior. Attaching a hash of the representation of a technical interface of a contract could cause conflicts between different standards and because of this proposal defines interfaces loosely. Also, it allows an interface to be more fluid, for example token that couldn't be transferred could be just a contract that will have to get the method `can_transfer` that returns `false` and this would mean that this token doesn't support transfers at all without the need to implement this method.

Interface IDs are hashes of reverse domain names (like packages in Java), this avoids clashes of names between different teams if they want to build something just for themselves.

## Specification

In order to support the introspection contract MUST implement the supports_interface GET method:

```(int...) supported_interfaces()```
Which returns a list of supported interface codes. The first value MUST be `hash("org.ton.introspection.v0")` = `123515602279859691144772641439386770278`.
If the first value is incorrect app MUST stop attempting to introspect the contract.
Example
```func
_ supported_interfaces() method_id {
    return (123515602279859691144772641439386770278);
}
```

The hash of an interface is defined as truncated to 128 bits SHA256.

## Drawbacks

This proposal doesn't guarantee that the contract would behave correctly to an interface, also it doesn't provide a guaranteed way to avoid name clashes between different interfaces. This is a non-goal for this proposal.

This proposal isn't tied to a specific technical interface. This could lead to multiple interfaces that do the same thing but with different IDs. This is a non-goal for this proposal since a centralized registry would be very useful for existing interfaces and a custom one would be used mostly in-house.

## Rationale and alternatives

- Why 128 bit? We are looking at a global namespace that we need to keep without conflicts, we can't use anything much smaller since the probability of conflicts would be much higher. We are looking at UUID-like entropy that is exactly 128-bit and is time-proven. More than 128 is too wasteful.
- Why freeform? As mentioned before, it is easier just to define some ID to start work early and then eventually build a standard. Also interfaces (like ERC20) usually not just a technical interface, but also a number of rules on how to work with it.
- Why not find out what contract supports by decompiling? Explicit is always better than implicit in open-world scenarios. We can't rely on our "disassembling" capabilities to perform introspections, even small errors could be fatal.
- Why not hash of representation? Right now there are no compilers that support that, also this proposal is future-proof. If anyone would want to build something more automated they could easily build their own hashes by their own rules keeping everything the same for external observers.

## Prior art

[Ethereum Interface Detection](https://eips.ethereum.org/EIPS/eip-165)


## OTP-002.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/evolution/OTP-002.mdx)
---
title: "OTP-002: Contract ABI"
---

# OTP-002: Contract ABI

ABI defines how to communicate with smart contracts. It contains information about the contract's receivers, data structures, etc.

## Motivation

ABI is an essential tool that allows developers to generate handy bindings, UIs, etc. One of the best consumer usages would be using a DAO and being able to confirm what exactly it is trying to do before signing a transaction.

## Guide

This OTP is based on types that are defined in TLB+ and it is advised to know them before reading this OTP.

## Specification

ABI is a JSON file:

```json
{
  "name": "MyContract",
  "types": [
    {
      "name": "MyRequest",
      "header": 12315123,
      "fields": [
        {
          "name": "queryId",
          "type": {
            "kind": "simple",
            "type": "int",
            "optional": false,
            "format": "uint256"
          }
        }
      ]
    }
  ],
  "receivers": [
    { "type": "binary", "kind": "internal", "name": "MyRequest" },
    { "type": "binary", "kind": "internal" },
    { "type": "comment", "kind": "internal", "comment": "Vote!" },
    { "type": "comment", "kind": "internal" },
    { "type": "empty", "kind": "internal" }
  ],
  "getters": [
    { "name": "getOwner", "type": "address", "args": [] },
    {
      "name": "getBalance",
      "type": "coins",
      "args": [
        {
          "name": "invested",
          "type": {
            "kind": "simple",
            "type": "uint",
            "format": "coins"
          }
        }
      ]
    }
  ],
  "errors": {
    "123": "Error description",
    "124": "Division by zero"
  }
}
```

## Drawbacks

- Binary and compact representation of ABI could be better, but it is not critical for now.

## Prior art

- OTP-001, that is complimentary to this OTP.


## OTP-003.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/evolution/OTP-003.mdx)
---
title: "OTP-003: Self-ABI reporting"
---

# OTP-003: Self-ABI reporting

This proposal defines how to report the contract's ABI using the IPFS link.

## Motivation

Usually, ABI is supplied separately using a third-party service or via some repository on GitHub. This proposal suggests adding a new self-reporting of the contract's ABI using a link to an IPFS. This would allow us to avoid any third-party dependency and allow anyone to build tools that rely on ABI such as explorers, wallets, etc.

## Specification

To support this proposal, the contract should implement OTP-001 and report an interface `org.ton.abi.ipfs.v0`. Then implement a get method `get_abi_ipfs` that returns a string with an IPFS link to the ABI file. The link should be in the format `ipfs://<hash>`.

## Drawbacks

- No way to upgrade ABI without updating a contract. This is a drawback exists only for hardcoded links.


## OTP-004.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/evolution/OTP-004.mdx)
---
title: "OTP-004: Auto Encoder"
---

# OTP-004: Auto Encoder

This proposal defines a way to automatically build a serialization layout for a given structure.

## Motivation

Designing a serialization layout in TLB is a very risky task. Developers have to take care of the size limitations of cells and remember how many bits are used by each field. This is a very error-prone task and it is very easy to make a mistake. This proposal aims to solve this problem by providing a way to automatically build a serialization layout for a given structure.

## Specification

We define auto-encoder as an eager algorithm that builds a serialization layout for a given structure. The algorithm is defined as follows:

```text
Define available references and bits in a current cell 
   as `available_references` and `available_bits` respectively.
   NOTE: there must be at least one reference reserved for the serialization tail and one 
         bit for an optional flag. Depending on context more references or bits may be reserved. 

For each field in A:
    (size_bits, size_ref) = get_field_max_size(field);
    if (available_bits >= size_bits && available_references >= size_ref) {
        Push field to a current cell
    } else {
        available_references = (1023 - 1);
        available_bits = (4 - 1);
        Allocate a new tail and continue from the current field
    }
```

## Drawbacks

- This is an implicit algorithm. It is not clear results of this allocator have to be checked to make compatible serialization.

## OTP-005.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/evolution/OTP-005.mdx)
---
title: "OTP-005: Argument-addressable contracts"
---

# OTP-005: Argument-addressable contracts

This proposal defines a way to address contracts by their arguments instead of their initial data.

## Motivation

Init data could be very different from the arguments. This allows us to avoid executing untrusted code from another contract in the context of a current one or executing TVM code off-chain for deployment that could be risky in some cases.

## Specification

This specification defines a way to write arguments to an init data cell to be read by the contract code during deployment.

### Prefix

The prefix is defined by a smart contract itself, but by default, it is assumed as a `single zero bit`. Prefix is used by the contract code to distinguish between deployed and not-deployed state.

### Arguments encoding

Arguments are encoded using [Auto Encoder](/ref/evolution/OTP-004).

### Contract Requirements

- Contract MUST expose `lazy_deployment_completed` get method that returns `true` if the contract is deployed and `false` otherwise.
- Contract MUST expose `org.ton.deploy.lazy.v0` interface.

## Drawbacks

- Contracts could be in a semi-deployed state
- There are multiple ways to write arguments that would end up in a different init data and a different address
- You can deploy a pre-initialized contract and it would have a different address while being fully functional
- Unpredictable gas usage on deployment. Deployments are usually expensive, but this proposal makes it even more expensive.


## OTP-006.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/evolution/OTP-006.mdx)
---
title: "OTP-006: Contract Package"
---

# OTP-006: Contract Package

This proposal defines a way to package compile contracts, their dependencies, and all related metadata into a single file.

## Motivation

A unified package format is needed to simplify the process of deploying and upgrading contracts using various tools without the need to configure them.

## Specification

The package file has an extension `.pkg` and is a JSON file:

```json
{
  "name": "My Contract",
  "code": "... boc of code ...",
  "abi": "ABI string to be uploaded as is to IPFS or Ton Storage",
  "init": {
    "kind": "direct", // Means that this contract can be deployed as is
    "args": {
      // ... Arguments in ABI format
    },
    "prefix": {
      // Optional prefix for contract init state
      "bits": 0, // Number of bits in prefix
      "value": 0 // Value of prefix
    },
    "deployment": {
      "kind": "system-cell", // Means that this contract can be deployed as is
      "system": "... boc of system cell ..."
    }
  },
  "sources": {
    "file.ton": "... base64 encoded source file ..."
  },
  "compiler": {
    "name": "func",
    "version": "0.4.1",
    "parameters": "..." // Optional string parameters
  }
}
```

## Drawbacks

None


## Reference
- Bags of Cells(BOC): https://docs.ton.org/develop/data-formats/cell-boc#packing-a-bag-of-cells


## overview.mdx (https://github.com/tact-lang/tact/blob/main/tact-docs-main/pages/ref/evolution/overview.mdx)
# Evolution overview

import { Cards } from 'nextra/components'

This sub-section contains all standards that are defined by the Tact Foundation and are used in the evolution process of the Tact and TON ecosystem.
Additionally, it features TEPs (TON Enhancement Proposals) and the up-to-date changelog of Tact updates.

## Open Tact Proposals (OTPs)

<Cards>
  <Cards.Card
    arrow
    title="OTP-001"
    href="/ref/evolution/OTP-001"
  />
  <Cards.Card
    arrow
    title="OTP-002"
    href="/ref/evolution/OTP-002"
  />
  <Cards.Card
    arrow
    title="OTP-003"
    href="/ref/evolution/OTP-003"
  />
  <Cards.Card
    arrow
    title="OTP-004"
    href="/ref/evolution/OTP-004"
  />
  <Cards.Card
    arrow
    title="OTP-005"
    href="/ref/evolution/OTP-005"
  />
  <Cards.Card
    arrow
    title="OTP-006"
    href="/ref/evolution/OTP-006"
  />
</Cards>

## TON Enhancement Protocols (TEPs)

The main goal of TON Enhancement Proposals is to provide a convenient and formal way to propose changes to TON Blockchain and standardize ways of interaction between different parts of ecosystem. Proposal management is done using GitHub pull requests, the process is described formally in [TEP-1](https://github.com/ton-blockchain/TEPs/blob/master/text/0001-tep-lifecycle.md).

List of [merged TEPs](https://github.com/ton-blockchain/TEPs#merged-teps).

## Changelog

All notable changes to the main Tact repository are documented in the [CHANGELOG.md](https://github.com/tact-lang/tact/blob/main/CHANGELOG.md).
