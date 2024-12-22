### Post ID: [6](https://t.me/tact_kitchen/6)
**Date:** 2024-06-08T13:40:41

⚡️ Probably a navigation post, cooking it up!

---
### Post ID: [8](https://t.me/tact_kitchen/8)
**Date:** 2024-06-08T15:09:41

🗿 Where am I? What's Tact Kitchen?

🧑‍🍳 Welcome, fellow chef! Here we bring you tech updates from the Tact team in a digestible form. Read notes on things guaranteed to make it into future releases: from compiler news to plugin enhancements, all ready to be served.

❓ Why, you might ask? Sure, you can subscribe to any repository under github.com/tact-lang and get email notifications right away.

❗️ But if you do it too much, the sheer amount of updates will definitely keep your inbox busy. That's why we've made this channel — to make things nice and simple for you ❤️

📍 Now, to navigation!

Main repositories on GitHub:
• Compiler
• Documentation
• Awesome Tact, the place to collect all community creations
• …and the whole tact-lang, nothing is minor 😎

Community:
• Telegram chat, for tech Q&As 🛠
• X/Twitter profile
• and Tact Kitchen — you're here, chef 🤌

🍲 Let's cook with Tact!
♨️ @tact_kitchen

---
### Post ID: [10](https://t.me/tact_kitchen/10)
**Date:** 2024-06-12T19:27:27

⚡️ Debugging page just got a massive update: Yay! 

Very narrowed table of contents (there's more!):
1️⃣ Description of general debugging approaches for Tact smart contracts
2️⃣ Reference to commonly used debugging functions of Tact
3️⃣ How-to: enable debug mode
4️⃣ How-to: write tests in Blueprint, with Sandbox and Jest
5️⃣ How-to: log via emit()
6️⃣ How-to: handle bounced messages
7️⃣ Experimental lab setup

🍲 Chef's Kiss
♨️ @tact_kitchen

---
### Post ID: [11](https://t.me/tact_kitchen/11)
**Date:** 2024-06-12T19:56:03

Comments have been activated. Health inspectors are invited to make their observations ⚕️

---
### Post ID: [12](https://t.me/tact_kitchen/12)
**Date:** 2024-06-12T22:24:03

⚡️ Remember those weird lvalue expected before ~load_int errors?

Like, when you tried to write this:

beginCell().storeInt(42, 7).asSlice().loadInt(7);

Or something similar, but still got that error?

✅ Well, not anymore!

Now you can freely use .load() or any other extension function on Slices and compile your code successfully!

🧑‍🍳 Contributor: Gusarich
👉 Released in: v1.3.1
🆙 To upgrade your projects, use npm upgrade, or a similar command in other Node.js package managers.

🍲 Gotta Stay Cookin'
♨️ @tact_kitchen

---
### Post ID: [13](https://t.me/tact_kitchen/13)
**Date:** 2024-06-13T19:04:44

⚡️ 0. Cleared invalid return type from Slice.skipBits()

If you've previously tried to assign it's results somewhere, it failed with an unwieldy FunC error. But now, the return type is cleared, so one more unreadable error got out of the way!

If you need its return value for some reason, take a look at Slice.preloadBits()

🧑‍🍳 Contributor: Gusarich
🐙 Implementation: #388
🍽 To be released in: v1.4.0


⚡️ 1. Added bitwise NOT ~ operator

// Let's flip some bits! (~˘▾˘)~
let nice: Int = ~~~~42 + ~~~~27;

// ~(˘▾˘~)
dump(nice);

🧑‍🍳 Contributor: Gusarich
🐙 Implementation: #337
🍽 To be released in: v1.4.0


⚡️ 2. Added &=, |= and ^= operators

They combine operations (&, |, ^)  with an assignment, so that you can move from this:

a = a & 01000101; // bitwise AND
b = b | 01000101; // bitwise OR
c = c ^ 01000101; // bitwise XOR

To this:

a &= 01000101;
b |= 01000101;
c ^= 01000101;

🧑‍🍳🎉 Community contributor: Alejandbel
🐙 Implementation: #350
🍽 To be released in: v1.4.0

🍲 When cooking, make sure not to leave the trail of bits
♨️ @tact_kitchen

---
### Post ID: [14](https://t.me/tact_kitchen/14)
**Date:** 2024-06-15T08:30:44

⚡️ Made last semicolon optional in Struct and Message field declarations

// This now works:
struct You { likeJazz: Bool }

// And that works too:
message GuessCoin {
    probably: Int as coins;
    nothing: Int as coins
    // no trailing semicolon above!
}

🧑‍🍳 Contributor: anton-trunov
🐙 Implementation: #395
🍽 To be released in: v1.4.0

🍲 The more you shave away, the clearer things become
♨️ @tact_kitchen

---
### Post ID: [15](https://t.me/tact_kitchen/15)
**Date:** 2024-06-17T23:37:08

⚡️ Added local type inference for let statements

It's a fancy way of saying that let statements can now be used without specifying a type after the colon. Tact will infer the type from the value of expression on the right.

// Now you can omit the obvious:
let a = 42;
let b = 27;
let c = a + b; // nice

// Explicit approach continues to work:
let d: Int = a + b; // also nice

🧑‍🍳 Contributor: Gusarich
🐙 Implementation: #198
🍽 To be released in: v1.4.0

🍲 Hey, that's my type!
♨️ @tact_kitchen

---
### Post ID: [16](https://t.me/tact_kitchen/16)
**Date:** 2024-06-19T12:01:19

⚡️ 0. Added a Slice.loadBool() function to the core library

It nicely mirrors the existing Builder.storeBool() function, loading a single bit as a signed Int and producing true if it's 1 in binary, and false otherwise.

let slice = beginCell().storeBool(true).asSlice();
let dice = slice.loadBool(); // true

💡 Inspired by a discussion with a community member
🧑‍🍳 Contributor: Gusarich
🐙 Implementation: #412
🍽 To be released in: v1.4.0


⚡️ 1. Fixed a compilation failure with as coins serialization in maps

Previously, if you've tried to compile the following (or similar):

import "@stdlib/deploy";

contract WhatCoin with Deployable {
    c: map<Address, Int as coins>; // ← 👀
}

It produced a compilation error, telling you that coins is unsupported in map values. But that wasn't right, coins serialization format for Ints as map keys and values should've been supported!

✅ And now it is, so the snippet above compiles just fine.

⁉️ Reported by: howardpen9
🧑‍🍳 Fixed by: Gusarich 
🐙 Implementation: #413
🍽 To be released in: v1.4.0

🍲 Gimme, gimme, gimme your bugs after midnight
♨️ @tact_kitchen

---
### Post ID: [17](https://t.me/tact_kitchen/17)
**Date:** 2024-06-19T12:30:01

💡 Both those things are somewhat small, but in no way are they minor. That's because they were a direct result of community discussions in Tact chat and elsewhere.

👀 We, as Tact devs, keep an eye on every message left in that chat. And even if they don't get an answer from us or other community members sometimes, their existence provides a great fuel and reference for future improvements, fixes and documentation updates.

❤️ Keep your quality questions and feedback coming, and cool stuff won't have to wait!

🍲 Cooking with great care
♨️ @tact_kitchen

---
### Post ID: [18](https://t.me/tact_kitchen/18)
**Date:** 2024-06-20T20:17:10

⚡️ Added extension functions Struct.fromCell() and Struct.fromSlice()

Got tired of parsing Cells and you're certain of their structure?

Now you'll be able to call YourStruct.fromCell() and automagically get your Cells parsed! And it also works on Slices, with YourStruct.fromSlice()

Note, that those functions throw exceptions when the layout of a given Cell or Slice doesn't match the Struct's one.

Let's see them in action:

struct Profit {
    big: String?;
    dict: map<Int, Int as uint64>;
    energy: Int;
}

contract MilkMoney with Deployable {
    // 100% sure here
    get fun gotProfit(src: Cell): Profit {
        let profit = Profit.fromCell(src);
        return profit;
    }
    
    // not 100% sure here,
    // being cautious for good reasons
    get fun gotProfitSlice(src: Slice): Profit? {
        let profit: Profit? = null;
        try {
            profit = Profit.fromSlice(src);
        catch (e) {
            dump("Slice doesn't match Profit!");
        }
        return profit;
    }
}
🧑‍🍳 Contributor: Gusarich
🐙 Implementation: #418
🍽 To be released in: v1.4.0 (right around the corner!)

🍲 You shall just parse!
♨️ @tact_kitchen

---
### Post ID: [19](https://t.me/tact_kitchen/19)
**Date:** 2024-06-21T20:05:59

⚡️ hey, pssst, look what they got on the chef's table: https://www.npmjs.com/package/@tact-lang/compiler/v/1.4.0

👉 Some uncooked release notes

🤐 Have a taste, but don’t tell anyone just yet
♨️ @tact_kitchen

---
### Post ID: [20](https://t.me/tact_kitchen/20)
**Date:** 2024-06-25T23:52:46

⚡️ Introduced underscores _ as unused variable identifiers in foreach and let statements, as well as in catch () clauses 

try {
    // If you don't need the return value
    let _ = myReturnIsUseless();

    // If you found yourself looking for map length,
    // and don't care about neither keys nor values
    let counter = 0;
    foreach (_, _ in map) {
        counter += 1;
    }

// If you never wanted that exit code anyways
catch (_) { }

🧑‍🍳 Contributor: Gusarich
🐙 Implementation: #338
🍣 Released in: v1.4.0

🍲 mic value drop
♨️ @tact_kitchen

---
### Post ID: [21](https://t.me/tact_kitchen/21)
**Date:** 2024-07-12T21:44:35

⚡️ Added Mermaid diagrams of trait inheritance and contract dependencies to the compilation report

Did you know, that Tact produces a report of each compilation in markdown format? If not, take a quick look at what it offers:

• Resulting BoC size of the contract in bytes
• TL-B schemes of all Structs and Messages alongside with their Tact signatures
• List of all getter functions
• List of exit codes, both default and produced by calls to require()

And now, Tact also automatically generates neat Mermaid diagrams of trait inheritance and contract dependencies, and puts them in that .md file! Check your build folders once in a while, it's definitely worth it.

🧑‍🍳 Contributor: Gusarich
🐙 Implementation: #560
🍽 To be released in: v1.4.1

🍲 Look at this photograph
♨️ @tact_kitchen

---
### Post ID: [22](https://t.me/tact_kitchen/22)
**Date:** 2024-07-26T19:40:55

🎉 Tact 1.4.1 has just landed on NPM!

🐞 We fixed a gazillion bugs reported by the TON builders and TOL hackathon participants

❤️‍🔥 Thanks so much for your helpful feedback! It means so much to have such a vibrant community of Tacticians

🍳 Now that bug squashing is out of the way, we are on to adding more exciting features (and inevitably introducing some more bugs along the way). Tact 1.5.0 ingredients are out of the fridge and into the pan. 

— The Tact team

🍲 Don’t let update bit rot, go get it!
♨️ @tact_kitchen

---
### Post ID: [23](https://t.me/tact_kitchen/23)
**Date:** 2024-08-01T13:46:02

Hey Tacticians, we are hungry for your honest opinion  ⚡️

---
### Post ID: [24](https://t.me/tact_kitchen/24)
**Date:** 2024-08-01T13:46:03

Attention Developers!

We need your valuable insights to make the TON & Telegram Apps platform even better! 🚀

As a token of our appreciation, every developer who completes our questionnaire will receive an exclusive SBT from TON Society! 🎁

Your feedback is crucial in shaping the future of our ecosystem. Take a few minutes to share your thoughts and experiences with us.

👉 Start the Questionnaire Now

Thank you for being a vital part of our community and helping us build a stronger, more vibrant platform!

---
### Post ID: [25](https://t.me/tact_kitchen/25)
**Date:** 2024-08-06T17:20:13

🐞 Misti – TON Static Program Analyzer

The first release of Misti – a static program analyzer for the TON blockchain has landed!

🐛 Detect Vulnerabilities: Identify and fix potential security flaws early in the development cycle.

🛠 Create Custom Detectors: Solve specific problems in your code or provide a thorough security review if you are an auditor.

📄 Improve Code Quality: Maintain high standards by catching bugs and enforcing best practices automatically.

🚀 Streamline Development: Integrate Misti into your CI/CD pipeline to ensure continuous code quality checks.

💎 Language Support: Tact ⚡ is supported; FunC support is planned.


- GitHub: https://github.com/nowarp/misti, contributions are very welcome!
- Documentation: https://nowarp.github.io/tools/misti/docs
- Telegram Group: @misti_dev

---
### Post ID: [26](https://t.me/tact_kitchen/26)
**Date:** 2024-08-13T19:04:40

🎉 Tact 1.4.2 has just landed on NPM!

🐞 We fixed a few type-checking and code generation bugs. One of the most important fixes is that getters again return flattened types for structs as it used to be. We broke it while trying to allow structs with more than 15 fields. Please give it a try and let us know if the issue is gone now — all your bug reports are really appreciated.

🛠 A bunch of the other changes include improved support for the misti static smart-contract analyzer — give it a try, it’s in early stage of development but already found some issues in soon-to-be released projects.

— The Tact team

♨️ @tact_kitchen

---
### Post ID: [27](https://t.me/tact_kitchen/27)
**Date:** 2024-08-15T20:36:47

🎉 Tact 1.4.3 has just landed on NPM!

🐞 We fixed a couple more issues and provided a fix for a special case of optional types in getter return types. Happy hacking, Tacticians!

— The Tact team

♨️ @tact_kitchen

---
### Post ID: [28](https://t.me/tact_kitchen/28)
**Date:** 2024-08-18T05:36:11

🎉 Tact 1.4.4 has just landed on NPM!

Fixed a few bugs and added AST equality comparison API mostly for third-party tools, like the misti static smart-contract analyzer. The API also be used to compare contracts without taking into account whitespace, comments or even order of definitions and declarations.

More details as always can be found in the changelog.

— The Tact team

♨️ @tact_kitchen

---
### Post ID: [29](https://t.me/tact_kitchen/29)
**Date:** 2024-08-22T14:00:04

🎉 Misti 0.2 has just landed on NPM!

🔍 Five New Tact Detectors: Сonstant Address, Branch Duplicate, `dump` Is Used, Field Initialized Twice, Prefer Augmented Assignment.

🛠 Blueprint Support: Introducing the new Blueprint Plugin.

🔧 Fixes & Enhancements: More configuration options and various fixes. Check out the full changelog.

♨️ @tact_kitchen

---
### Post ID: [30](https://t.me/tact_kitchen/30)
**Date:** 2024-08-31T14:34:13

ASMR asm-functions are coming in the future Tact v1.5.0 release, so you can tap into the power of TVM directly.

This will be valid Tact code⚡️:

asm fun keccak256(s: Slice): Int {
    1 INT HASHEXT_KECCAK256
}

// … more stuff …

let h = keccak256(yourSlice);
— The Tact team

♨️ @tact_kitchen

---
### Post ID: [31](https://t.me/tact_kitchen/31)
**Date:** 2024-09-15T18:46:54

🎉 Tact v1.5.0 has just been released

The new Tact release v1.5.0 just landed on NPM! Here are the highlights of the most important features.

🛠 New Tact features

asm functions allow you to access the deep dark corners of TVM for more features or better performance: 


asm fun keccak256(s: Slice): Int {
    1 INT HASHEXT_KECCAK256
}


asm functions have some limitations at this point and the Tact team will make them even more powerful in the next releases.

- A wider range of serialization options for integers can now be used, not just 8, 16, 32, 64, 128 and 256-bit integers, but anything in between: uint1 through uint256 and int1 through int257. For instance, a 48-bit timestamp can be defined now if you'd like to build contracts that can work after the year 2038:


contract Contract {
    timestamp: Int as uint48
}


- Constant definitions now support calls to user-defined functions and references to other constants:


const CONSTANT: Int =
    myFunction(OTHER_CONSTANT)


👩‍💻 New builtin and stdlib functions and methods

- The exists method for the Map type: m.exists(key) which is equivalent to m.get(key) != null.

- The deepEquals method for the Map type: m1.deepEquals(m2) -- you can now easily compare two maps with the same key-value pairs and get true as the result, even if their internal representations are different, so the hash-based == comparison would return false.

- The toSlice method for structs and messages: struct.toSlice().

- The new slice, rawSlice, ascii and crc32 built-in compile-time functions to help you define constant integers and slices more conveniently.

- The new stdlib functions to help with fee calculations: gasConsumed, getComputeFee, getStorageFee, getForwardFee, getSimpleComputeFee, getSimpleForwardFee, getOriginalFwdFee, myStorageDue. This brings you access to the TVM instructions from 2023.07 and 2024.04 upgrades.

- The parseStdAddress and parseVarAddress stdlib functions allow you to parse slices into structured addresses.

🐞 The new release also includes a bunch of bugfixes. Thanks to all the Tacticians for all the issues you open!

📜 Full changelog for Tact v1.5.0: https://github.com/tact-lang/tact/blob/main/CHANGELOG.md#150---2024-09-15

---
### Post ID: [32](https://t.me/tact_kitchen/32)
**Date:** 2024-09-22T20:08:50

🎉 Misti 0.3 has just landed on NPM!

⚡️Tact 1.5 Support

🔍 Five New Tact Detectors: String Receivers Overlap, Asm Is Used, Preferred Stdlib API, Inherited State Mutation, Argument Copy Mutation.

🔧 Fixes & Enhancements: More configuration options, optimization and API improvements. Check out the full changelog.

♨️ @tact_kitchen

---
### Post ID: [34](https://t.me/tact_kitchen/34)
**Date:** 2024-09-25T19:35:17

🎉 Tact 1.5.2 has just landed on NPM!

Remember, that we've introduced asm functions in version 1.5.0 for you to write TVM assembly right in your Tact code?


asm fun keccak256(s: Slice): Int {
    1 INT HASHEXT_KECCAK256
}

🐞 With this bugfix release, you now can use full* range of its syntax just like you could in similar asm functions of FunC. Just don't do anything too crazy, like trying to shadow (re-define) { or }, or using char } inside your newly defined instructions.

Other than that, have it your way. Note, that support of full Fift+TVM syntax is highly experimental, and will be reworked in future releases, in particular the following works now, but most likely won’t work at some point:

fun onchainSha256(data: String): Int {
    _onchainShaPush(data);
    while (_onchainShaShouldProceed()) {
        _onchainShaOperate();
    }
    return _onchainShaHashExt();
}

// Helper assembly functions,
// each manipulating the stack in their own ways
// in different parts of the `onchainSha256()` function
asm fun _onchainShaPush(data: String) { ONE }
asm fun _onchainShaShouldProceed(): Bool {
    OVER SREFS 0 NEQINT
}
asm fun _onchainShaOperate() {
    OVER LDREF s0 POP CTOS s0 s1 XCHG INC
}
asm fun _onchainShaHashExt(): Int {
    HASHEXT_SHA256
}

🐞 Additionally, all new installations of @tact-lang/compiler or @ton/blueprint via npm should work as expected. All other package managers continue to work fine, so create more awesome projects! We'll handle the rest ❤️

👀 And keep an eye on the docs, something big might happen very soon!

🍲 every contract is open source if you can read bytecode
♨️ @tact_kitchen

---
### Post ID: [35](https://t.me/tact_kitchen/35)
**Date:** 2024-10-02T01:02:26

👏 Huge 👏 Revamp 👏 of Tact 👏 Docs 👏

There were a lot of things we just couldn't do nicely with the previous documentation library, Nextra. Granted, it's very good and has a lot going for it, but its rigidity in important places, as well as its overall pull towards Next.js and Vercel make some features like i18n almost impossible to implement while keeping the static build and not doing the server-side rendering.

It is finally time to move to a more flexible solution: Starlight, a documentation library powered by Astro that allows for great extensibility and bundles (among other things): advanced i18n support via i18next, site navigation, search, SEO, easy-to-read typography, code highlighting, dark mode and more. It's also very lightweight and snappy.

This move brought a lot of enhancements, here's a very short list (there's more!):

0️⃣ Translating the docs to another language (i18n) is super easy now. Just take the original English page, translate it, and put the file in the appropriate folder. That's it, the next deployments would feature your translated page as if it was always there ✨

1️⃣ The search via Ctrl + K (fuzzy full-site search) has been greatly improved. In addition, since all the pages are located in the sidebar, you now can use Ctrl + F (content search) to quickly find the page in any of the sections: Book, Cookbook,  and Ecosystem!

2️⃣ Fixed issues with highlighting of code blocks in the light mode. The similar change for inline code highlighting will follow in the future too!

3️⃣ tact-docs repo has been merged into the Tact compiler one, which means that all new feature and standard library updates will arrive in docs much faster than before! Besides, you'll see badges like "Since version X.Y.Z" under each new feature, so that you'll know when to expect things and which Tact version to use for them :)

Things that didn't make the list include updates that are mostly relevant to the team and maintainers of the docs. For example:

1. It's much easier to influence the SEO of each page with good descriptions and image covers where needed
2. It's super easy to customize the docs with: CSS styles, JS scripts, Markdown pre-processing plugins, HTML pre-processing and post-processing plugins, ...
3. ...and so on and so forth

🧑‍🍳 Contributor: Novus Nota
🐙 Implementation: #880
✈️ Delivered: docs.tact-lang.org

🍲 sparkle! sunshine!
♨️ @tact_kitchen

---
### Post ID: [36](https://t.me/tact_kitchen/36)
**Date:** 2024-10-10T18:25:49

TON Studio is hiring!

TON Studio team is seeking for Lead Developer (smart contracts & audits).

You will work with both FunC and Tact smart contracts to develop highly optimized, secure, and efficient DApps, leveraging your understanding of Fift, TVM, and gas optimizations. 

You can find more details about the job opening and apply here: https://jobs.ton.org/companies/ton-studio/jobs/41178106-lead-developer-smart-contracts-audits#content

We invite builders to post vacancies in the TON Jobs channel. To do this, you need to write to support @tonjobs_support

---
### Post ID: [37](https://t.me/tact_kitchen/37)
**Date:** 2024-10-18T18:52:05

⚡️ Added destructuring statements

It's a concise way to unpack Structs and Messages into distinct variables, which mirrors the instantiation syntax:

// Definition of Example
struct Example { number: Int }

fun basic() {
    // Basic syntax of destructuring assignment
    // is shown on the left of "=":
    let Example { number } =
        Example { number: 42 };

    // The syntax above is roughly equivalent
    // to the following statements:
    let example = Example { number: 42 };
    let number = example.number;
}

One can also create bindings under different variable names or ignore some of the fields. Note, that the order doesn't matter:

// "first" goes first, then goes "second"
struct Two { first: Int; second: String }

// a helper function
fun makeTwo(): Two {
    return Two {
        first: 42,
        second: "yee-haw",
    };
}

// 👀
fun totalDestruction() {
    // The "first" field is ignored,
    // while the value of "second"
    // is bound under the "cowboy"
    // variable from now on:

    let Two {
        second: cowboy,
        first: _,
    } = makeTwo();
}

🧑‍🍳 Contributors: Gusarich, Novus Nota (docs)
🐙 Implementation: #856
🍽 To be released in: v1.6.0

🍲 everyone within a 100 mile radius after you eat a taco
♨️ @tact_kitchen

---
### Post ID: [38](https://t.me/tact_kitchen/38)
**Date:** 2024-10-30T13:32:36

⚡️ Added automatic links to Web IDE from code blocks in Cookbook section of the docs

Did you know, that just like the Remix for Ethereum, TON has an official Web IDE? If not, take a quick look at what it offers:

• Tact and FunC project creation
• Code highlighting and snippets for Tact and FunC
• Semi-automatic Build → Deploy pipeline on every save
• Convenient buttons to call getters and send messages to deployed contracts
• Deploy to Sandbox, testnet and mainnet
• Share button ↗️ on every file in a file tree
• ...plus a lot more!

And now any code samples from the Cookbook are right at your fingertips — just press the "Open in Web IDE" button, and the contents of the code block would automagically transfer to Web IDE!

🧑‍🍳 Contributor: Novus Nota
🐙 Implementation: #994
✈️ Delivered: docs.tact-lang.org/cookbook

🍲 «What's the TTP of Web IDE?»
♨️ @tact_kitchen

---
### Post ID: [39](https://t.me/tact_kitchen/39)
**Date:** 2024-10-31T20:11:19

🎉 Misti 0.5 has just landed on NPM!

🔍 More Tact Detectors: Covered Tact-specific issues like CellOverflow, SuspiciousMessageMode, UnboundMap achieving totally 25 detectors.

⚠️ Warning Suppressions: Suppress specific warnings using // @misti:suppress DetectorName comments.

💡 Usability Enhancements: Install Misti with a single command and run it on the directory containing your contracts—no extra configuration required:
npm install -g @nowarp/misti
misti path/to/src/contracts

🔧 Fixes & Enhancements: More configuration options, optimization and improvements. Check out the full changelog.

♨️ @tact_kitchen

---
### Post ID: [40](https://t.me/tact_kitchen/40)
**Date:** 2024-11-02T21:30:17

⚡️ Watch Tact & DevTools talk from 2nd day of TON Gateway
🌀 It's a whirlwind tour of progress made in Tact and ecosystem, plus the plans for the future!

🎞 If loading the video on Telegram is too much, start watching at the timestamp on YouTube
👀 For more, see the full recording of TON Gateway | Day 2

🍲 tactical advantage, strategic dominance
♨️ @tact_kitchen

---
### Post ID: [41](https://t.me/tact_kitchen/41)
**Date:** 2024-11-12T01:00:11

❤️ A warm welcome to listeners of good podcasts @tonpizdev
♨️ @tact_kitchen

---
### Post ID: [42](https://t.me/tact_kitchen/42)
**Date:** 2024-11-17T11:42:01

⚡️ Heads-up: there are more than 2100 Tact source files on GitHub, not counting forks and the tact-lang organization!

It would be nice to get Tact code highlighted there, don't you think? That's why we've made a PR to Linguist, a language detection and highlighting library from Github.

Here's how you can help:
1. Go to the PR
2. Leave your 👍 without writing any comments, to keep PR clean
3. Keep writing nice open source contracts in Tact 🙌
4. Wait for the best 🤞

This is not a drill. I repeat: this is not a drill.
This is the beginning of the story.

UPD: ❤

🍲 our story, actually
♨️ @tact_kitchen

---
### Post ID: [43](https://t.me/tact_kitchen/43)
**Date:** 2024-11-18T14:23:10

❤️ Thanks, folks! We really appreciate that!

🍲 melting hearts
♨️ @tact_kitchen

---
### Post ID: [44](https://t.me/tact_kitchen/44)
**Date:** 2024-11-27T23:55:54

⚡️ Added a page on security best practices to the documentation

There are several anti-patterns and potential attack vectors that Tact smart contract developers should be aware of. These can affect the security, efficiency, and correctness of the contracts.

With the help of community contributors, we've discussed the do's and don'ts specific to writing and maintaining secure Tact smart contracts, and written a cohesive page for you!

🧑‍🍳🎉 Community contributors: PixelPlex and Aliaksandr Bahdanau
🐙 Implementation: #1070
✈️ Delivered: docs.tact-lang.org/book/security-best-practices

🍲 where did the bad actor go? they ran somewhere
♨️ @tact_kitchen

---
### Post ID: [45](https://t.me/tact_kitchen/45)
**Date:** 2024-11-28T23:51:54

⚡️ Added DeDust and STON.fi cookbooks to the documentation

Ever wondered how to build your own Decentralized EXchange? Neither have I!

However, documentation on how to interact with existing DEXes from Tact was highly requested — and, with the help of community contributors, we wrote it. Read how to swap Toncoins for Jettons, Jettons for Jettons, and provide liquidity to pools of DeDust and STON.fi, all with ⚡️ Tact.

🧑‍🍳🎉 Community contributors: PixelPlex and Aliaksandr Bahdanau
🐙 Implementations: #954, #956
✈️ Delivered: DeDust, STON.fi

🍲 decentralized surprise liquidity provision
♨️ @tact_kitchen

---
### Post ID: [46](https://t.me/tact_kitchen/46)
**Date:** 2024-12-03T10:30:36

⚡️ Completely overhauled exit codes page in the documentation

Sometimes pages in the Tact documentation are more detailed than you'll find elsewhere. The exit codes page is a case in point.

Not only do you get a comprehensive description of what exit codes are, how they are defined, and which ones are reserved, but you also get a handy table of them with short descriptions and quick navigation to each exit code in the table of contents. Since each of the exit codes has its own headings, linking to a specific exit code is easier than ever!

In addition, all descriptions of compute phase exit codes show examples of how you might encounter them. And sometimes even help you to anticipate and avoid them.

By the way, for exit code 50 (not listed anywhere else), we've also described the current limits on config param 43 related to account state, max number of bits and cells in messages, and much more.

🧑‍🍳 Contributor: Novus Nota
🐙 Implementation: #978
✈️ Delivered: docs.tact-lang.org/book/exit-codes

🍲 code: dismissed
♨️ @tact_kitchen

---
### Post ID: [47](https://t.me/tact_kitchen/47)
**Date:** 2024-12-04T13:37:12

⚡️ GitHub supports Tact!

Now that you've clicked, let me clarify — thanks to our efforts, your support and all of you writing lots of smart contracts, Tact now has syntax highlighting all across GitHub!

— Files with a .tact extension? Boom, colored.
— Blocks of code in markdown that specify tact as their language? Got you covered.

❤️ Thanks everyone for your support and love! Without you, there would be nothing. Literally.

✈️ We're continuing to ship awesome stuff for you — expect many shiny things this December.

🍲 growth is inevitable
♨️ @tact_kitchen

---
### Post ID: [48](https://t.me/tact_kitchen/48)
**Date:** 2024-12-05T16:35:01

📣 Hey, folks! The Tact dev team kindly asks you to share some feedback regarding your experienced with smart-contract programming in Tact.

Our mission is to develop a high quality programming language that can be used for every single project on TON and make code easy to write, understand and audit.

The survey covers 4 topics and will only take about 5-8 minutes of your time. 

Thank you for your contribution!

👉https://paperform.co/edit/h02jnxtq

---
### Post ID: [49](https://t.me/tact_kitchen/49)
**Date:** 2024-12-12T20:01:50

📖 Secure Smart Contract Programming in Tact: Avoiding Pitfalls in the TON Ecosystem

As The Open Network evolves, its innovative features and the Tact programming language unlock new possibilities for developers. However, common mistakes can lead to vulnerabilities.

CertiK’s latest blog post highlights critical issues like data serialization, concurrency, and gas management, offering actionable insights to optimize security in Tact smart contracts. Whether you’re new to TON or a seasoned developer, these best practices are essential for building robust and secure applications.

🔗 https://www.certik.com/resources/blog/secure-smart-contract-programming-in-tact-popular-mistakes-in-the-ton

---
### Post ID: [51](https://t.me/tact_kitchen/51)
**Date:** 2024-12-22T17:00:06

🎉 Misti 0.6 has just landed on NPM!

🔍 More Tact Detectors: CellBounds which covers both CellOverflow and CellUnderflow, ExitCodeUsage, EtaLikeSimplifications and ShortCircuitCondition.

⚙️ More Tools: Added Callgraph that tracks function effects and is useful for auditing contracts.

🌐 Better Integrability: Misti can run in browser environments.

🔧 Fixes & Enhancements: Check out the full changelog.

♨️ @tact_kitchen

---
### Post ID: [52](https://t.me/tact_kitchen/52)
**Date:** 2024-12-22T19:05:45

⚡️ Added an assembly functions page to the documentation

👉 Covering all your needs and going beyond:
▪️ Eh, what are TVM instructions anyways?
▪️ Sure, they're used in asm functions of Tact, but what's the syntax and stuff?
▪️ Stack registers, what's that?
▪️ Fine, but what if I want to re-arrange parameters or return values?
▪️ Limitations? Caveats?
▪️ How would I debug all that?
▪️ Can I apply some attributes?
▪️ Got any examples?

🧑‍🍳 Contributor: Novus Nota
🐙 Implementation: #1061
✈️ Delivered: docs.tact-lang.org/book/assembly-functions

🍲 there are 11 types of programmers: ROT, -ROT and BRAINROT
♨️ @tact_kitchen

---
