

## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/.prettierrc.json
{
    "printWidth": 120,
    "tabWidth": 4,
    "useTabs": false
}

## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/ChangeLog.md
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Original goal is followed [Tact Compiler Changelog](https://github.com/tact-lang/tact/tree/main), and keep this project in sync. Enjoy! ❤️❤️❤️

## [1.1.0] - 2024-02-12

-   Change the parameters in NFT Item `init()`

## [1.0.0] - 2023-12-30

### Fixed

-   The testcase in test file
-   Add the `debug` method in `tact.config.json` file


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/README.md
# NFT Standard in Tact

<a href="https://star-history.com/#Ton-Dynasty/tondynasty-contracts&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=howardpen9/nft-template-in-tact&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=howardpen9/nft-template-in-tact&type=Date" />
    <img alt="Star History Chart!!!" src="https://api.star-history.com/svg?repos=howardpen9/nft-template-in-tact&type=Date" />
  </picture>
</a>

This GitHub repository is dedicated to an NFT standard ([TEP-62](https://github.com/ton-blockchain/TEPs/blob/master/text/0062-nft-standard.md)), which provides a set of guidelines and specifications for creating and managing non-fungible tokens (NFTs) on blockchain platforms.

> The repository contains a comprehensive collection of code files, documentation, and resources that developers can utilize to implement the standard in their NFT projects. It offers a well-defined structure and functionality for NFT contracts, including features like token metadata, ownership transfers, and token enumeration.
>
> The repository also includes sample code and examples to help developers understand and implement the NFT standard more easily. Collaborators and contributors actively maintain and update the repository, ensuring it remains up-to-date with the latest advancements and best practices in the NFT ecosystem.

-   https://github.com/ton-blockchain/TEPs/blob/master/text/0062-nft-standard.md
-   https://github.com/ton-blockchain/TEPs/blob/master/text/0064-token-data-standard.md
-   https://github.com/ton-blockchain/TEPs/blob/master/text/0066-nft-royalty-standard.md

## How to use

```bash
yarn build # To build contract
yarn test # To run test cases
yarn deploy # To deploy contract
yarn read # The way to read the smart contract data after your deployed the code
```

> [!WARNING]
> Remember to change the parameter in `contract.deploy.ts` file before you run `yarn deploy`

![Alt text](./images/image.png)

---

![alt text](./images/image-1.png) - once you run `yarn deploy` you will get the address of the deployed contract. You can use this address to interact with the contract.

## More

For more information about this GitHub repository, or if you have any questions related to Tact, feel free to visit:

-   https://t.me/ton101
-   https://t.me/tactlang

If you have more specific questions related to the Tact Language, please refer to:

-   https://tact-lang.org
-   https://tact-by-example.org


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/package-lock.json
{
  "name": "tact-nft-standard",
  "lockfileVersion": 2,
  "requires": true,
  "packages": {
    "": {
      "dependencies": {
        "@orbs-network/ton-access": "^2.2.2",
        "@types/jest": "^29.2.4",
        "@types/node": "^18.11.14",
        "@types/qs": "^6.9.7",
        "base64url": "^3.0.1",
        "enquirer": "^2.3.6",
        "jest": "^29.3.1",
        "open": "^8.4.0",
        "prando": "^6.0.1",
        "prettier": "^2.5.1",
        "qs": "^6.11.0",
        "ton": "^13.3.0",
        "ton-core": "^0.47.1",
        "ton-crypto": "^3.2.0",
        "ton-emulator": "^1.3.0",
        "ton-tact": "^0.9.0",
        "ts-jest": "^29.0.3",
        "ts-node": "^10.9.1",
        "typescript": "^4.9.4"
      }
    },
    "node_modules/@ampproject/remapping": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/@ampproject/remapping/-/remapping-2.2.0.tgz",
      "integrity": "sha512-qRmjj8nj9qmLTQXXmaR1cck3UXSRMPrbsLJAasZpF+t3riI71BXed5ebIOYwQntykeZuhjsdweEc9BxH5Jc26w==",
      "license": "Apache-2.0",
      "dependencies": {
        "@jridgewell/gen-mapping": "^0.1.0",
        "@jridgewell/trace-mapping": "^0.3.9"
      },
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/@ampproject/remapping/node_modules/@jridgewell/gen-mapping": {
      "version": "0.1.1",
      "resolved": "https://registry.npmjs.org/@jridgewell/gen-mapping/-/gen-mapping-0.1.1.tgz",
      "integrity": "sha512-sQXCasFk+U8lWYEe66WxRDOE9PjVz4vSM51fTu3Hw+ClTpUSQb718772vH3pyS5pShp6lvQM7SxgIDXXXmOX7w==",
      "license": "MIT",
      "dependencies": {
        "@jridgewell/set-array": "^1.0.0",
        "@jridgewell/sourcemap-codec": "^1.4.10"
      },
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/@assemblyscript/loader": {
      "version": "0.9.4",
      "resolved": "https://registry.npmjs.org/@assemblyscript/loader/-/loader-0.9.4.tgz",
      "integrity": "sha512-HazVq9zwTVwGmqdwYzu7WyQ6FQVZ7SwET0KKQuKm55jD0IfUpZgN0OPIiZG3zV1iSrVYcN0bdwLRXI/VNCYsUA==",
      "license": "Apache-2.0"
    },
    "node_modules/@babel/code-frame": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/code-frame/-/code-frame-7.18.6.tgz",
      "integrity": "sha512-TDCmlK5eOvH+eH7cdAFlNXeVJqWIQ7gW9tY1GJIpUtFb6CmjVyq2VM3u71bOyR8CRihcCgMUYoDNyLXao3+70Q==",
      "license": "MIT",
      "dependencies": {
        "@babel/highlight": "^7.18.6"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/compat-data": {
      "version": "7.20.14",
      "resolved": "https://registry.npmjs.org/@babel/compat-data/-/compat-data-7.20.14.tgz",
      "integrity": "sha512-0YpKHD6ImkWMEINCyDAD0HLLUH/lPCefG8ld9it8DJB2wnApraKuhgYTvTY1z7UFIfBTGy5LwncZ+5HWWGbhFw==",
      "license": "MIT",
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/core": {
      "version": "7.20.12",
      "resolved": "https://registry.npmjs.org/@babel/core/-/core-7.20.12.tgz",
      "integrity": "sha512-XsMfHovsUYHFMdrIHkZphTN/2Hzzi78R08NuHfDBehym2VsPDL6Zn/JAD/JQdnRvbSsbQc4mVaU1m6JgtTEElg==",
      "license": "MIT",
      "dependencies": {
        "@ampproject/remapping": "^2.1.0",
        "@babel/code-frame": "^7.18.6",
        "@babel/generator": "^7.20.7",
        "@babel/helper-compilation-targets": "^7.20.7",
        "@babel/helper-module-transforms": "^7.20.11",
        "@babel/helpers": "^7.20.7",
        "@babel/parser": "^7.20.7",
        "@babel/template": "^7.20.7",
        "@babel/traverse": "^7.20.12",
        "@babel/types": "^7.20.7",
        "convert-source-map": "^1.7.0",
        "debug": "^4.1.0",
        "gensync": "^1.0.0-beta.2",
        "json5": "^2.2.2",
        "semver": "^6.3.0"
      },
      "engines": {
        "node": ">=6.9.0"
      },
      "funding": {
        "type": "opencollective",
        "url": "https://opencollective.com/babel"
      }
    },
    "node_modules/@babel/generator": {
      "version": "7.20.14",
      "resolved": "https://registry.npmjs.org/@babel/generator/-/generator-7.20.14.tgz",
      "integrity": "sha512-AEmuXHdcD3A52HHXxaTmYlb8q/xMEhoRP67B3T4Oq7lbmSoqroMZzjnGj3+i1io3pdnF8iBYVu4Ilj+c4hBxYg==",
      "license": "MIT",
      "dependencies": {
        "@babel/types": "^7.20.7",
        "@jridgewell/gen-mapping": "^0.3.2",
        "jsesc": "^2.5.1"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-compilation-targets": {
      "version": "7.20.7",
      "resolved": "https://registry.npmjs.org/@babel/helper-compilation-targets/-/helper-compilation-targets-7.20.7.tgz",
      "integrity": "sha512-4tGORmfQcrc+bvrjb5y3dG9Mx1IOZjsHqQVUz7XCNHO+iTmqxWnVg3KRygjGmpRLJGdQSKuvFinbIb0CnZwHAQ==",
      "license": "MIT",
      "dependencies": {
        "@babel/compat-data": "^7.20.5",
        "@babel/helper-validator-option": "^7.18.6",
        "browserslist": "^4.21.3",
        "lru-cache": "^5.1.1",
        "semver": "^6.3.0"
      },
      "engines": {
        "node": ">=6.9.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0"
      }
    },
    "node_modules/@babel/helper-compilation-targets/node_modules/lru-cache": {
      "version": "5.1.1",
      "resolved": "https://registry.npmjs.org/lru-cache/-/lru-cache-5.1.1.tgz",
      "integrity": "sha512-KpNARQA3Iwv+jTA0utUVVbrh+Jlrr1Fv0e56GGzAFOXN7dk/FviaDW8LHmK52DlcH4WP2n6gI8vN1aesBFgo9w==",
      "license": "ISC",
      "dependencies": {
        "yallist": "^3.0.2"
      }
    },
    "node_modules/@babel/helper-compilation-targets/node_modules/yallist": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/yallist/-/yallist-3.1.1.tgz",
      "integrity": "sha512-a4UGQaWPH59mOXUYnAG2ewncQS4i4F43Tv3JoAM+s2VDAmS9NsK8GpDMLrCHPksFT7h3K6TOoUNn2pb7RoXx4g==",
      "license": "ISC"
    },
    "node_modules/@babel/helper-environment-visitor": {
      "version": "7.18.9",
      "resolved": "https://registry.npmjs.org/@babel/helper-environment-visitor/-/helper-environment-visitor-7.18.9.tgz",
      "integrity": "sha512-3r/aACDJ3fhQ/EVgFy0hpj8oHyHpQc+LPtJoY9SzTThAsStm4Ptegq92vqKoE3vD706ZVFWITnMnxucw+S9Ipg==",
      "license": "MIT",
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-function-name": {
      "version": "7.19.0",
      "resolved": "https://registry.npmjs.org/@babel/helper-function-name/-/helper-function-name-7.19.0.tgz",
      "integrity": "sha512-WAwHBINyrpqywkUH0nTnNgI5ina5TFn85HKS0pbPDfxFfhyR/aNQEn4hGi1P1JyT//I0t4OgXUlofzWILRvS5w==",
      "license": "MIT",
      "dependencies": {
        "@babel/template": "^7.18.10",
        "@babel/types": "^7.19.0"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-hoist-variables": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/helper-hoist-variables/-/helper-hoist-variables-7.18.6.tgz",
      "integrity": "sha512-UlJQPkFqFULIcyW5sbzgbkxn2FKRgwWiRexcuaR8RNJRy8+LLveqPjwZV/bwrLZCN0eUHD/x8D0heK1ozuoo6Q==",
      "license": "MIT",
      "dependencies": {
        "@babel/types": "^7.18.6"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-module-imports": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/helper-module-imports/-/helper-module-imports-7.18.6.tgz",
      "integrity": "sha512-0NFvs3VkuSYbFi1x2Vd6tKrywq+z/cLeYC/RJNFrIX/30Bf5aiGYbtvGXolEktzJH8o5E5KJ3tT+nkxuuZFVlA==",
      "license": "MIT",
      "dependencies": {
        "@babel/types": "^7.18.6"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-module-transforms": {
      "version": "7.20.11",
      "resolved": "https://registry.npmjs.org/@babel/helper-module-transforms/-/helper-module-transforms-7.20.11.tgz",
      "integrity": "sha512-uRy78kN4psmji1s2QtbtcCSaj/LILFDp0f/ymhpQH5QY3nljUZCaNWz9X1dEj/8MBdBEFECs7yRhKn8i7NjZgg==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-environment-visitor": "^7.18.9",
        "@babel/helper-module-imports": "^7.18.6",
        "@babel/helper-simple-access": "^7.20.2",
        "@babel/helper-split-export-declaration": "^7.18.6",
        "@babel/helper-validator-identifier": "^7.19.1",
        "@babel/template": "^7.20.7",
        "@babel/traverse": "^7.20.10",
        "@babel/types": "^7.20.7"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-plugin-utils": {
      "version": "7.20.2",
      "resolved": "https://registry.npmjs.org/@babel/helper-plugin-utils/-/helper-plugin-utils-7.20.2.tgz",
      "integrity": "sha512-8RvlJG2mj4huQ4pZ+rU9lqKi9ZKiRmuvGuM2HlWmkmgOhbs6zEAw6IEiJ5cQqGbDzGZOhwuOQNtZMi/ENLjZoQ==",
      "license": "MIT",
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-simple-access": {
      "version": "7.20.2",
      "resolved": "https://registry.npmjs.org/@babel/helper-simple-access/-/helper-simple-access-7.20.2.tgz",
      "integrity": "sha512-+0woI/WPq59IrqDYbVGfshjT5Dmk/nnbdpcF8SnMhhXObpTq2KNBdLFRFrkVdbDOyUmHBCxzm5FHV1rACIkIbA==",
      "license": "MIT",
      "dependencies": {
        "@babel/types": "^7.20.2"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-split-export-declaration": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/helper-split-export-declaration/-/helper-split-export-declaration-7.18.6.tgz",
      "integrity": "sha512-bde1etTx6ZyTmobl9LLMMQsaizFVZrquTEHOqKeQESMKo4PlObf+8+JA25ZsIpZhT/WEd39+vOdLXAFG/nELpA==",
      "license": "MIT",
      "dependencies": {
        "@babel/types": "^7.18.6"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-string-parser": {
      "version": "7.19.4",
      "resolved": "https://registry.npmjs.org/@babel/helper-string-parser/-/helper-string-parser-7.19.4.tgz",
      "integrity": "sha512-nHtDoQcuqFmwYNYPz3Rah5ph2p8PFeFCsZk9A/48dPc/rGocJ5J3hAAZ7pb76VWX3fZKu+uEr/FhH5jLx7umrw==",
      "license": "MIT",
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-validator-identifier": {
      "version": "7.19.1",
      "resolved": "https://registry.npmjs.org/@babel/helper-validator-identifier/-/helper-validator-identifier-7.19.1.tgz",
      "integrity": "sha512-awrNfaMtnHUr653GgGEs++LlAvW6w+DcPrOliSMXWCKo597CwL5Acf/wWdNkf/tfEQE3mjkeD1YOVZOUV/od1w==",
      "license": "MIT",
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helper-validator-option": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/helper-validator-option/-/helper-validator-option-7.18.6.tgz",
      "integrity": "sha512-XO7gESt5ouv/LRJdrVjkShckw6STTaB7l9BrpBaAHDeF5YZT+01PCwmR0SJHnkW6i8OwW/EVWRShfi4j2x+KQw==",
      "license": "MIT",
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/helpers": {
      "version": "7.20.13",
      "resolved": "https://registry.npmjs.org/@babel/helpers/-/helpers-7.20.13.tgz",
      "integrity": "sha512-nzJ0DWCL3gB5RCXbUO3KIMMsBY2Eqbx8mBpKGE/02PgyRQFcPQLbkQ1vyy596mZLaP+dAfD+R4ckASzNVmW3jg==",
      "license": "MIT",
      "dependencies": {
        "@babel/template": "^7.20.7",
        "@babel/traverse": "^7.20.13",
        "@babel/types": "^7.20.7"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/highlight": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/highlight/-/highlight-7.18.6.tgz",
      "integrity": "sha512-u7stbOuYjaPezCuLj29hNW1v64M2Md2qupEKP1fHc7WdOA3DgLh37suiSrZYY7haUB7iBeQZ9P1uiRF359do3g==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-validator-identifier": "^7.18.6",
        "chalk": "^2.0.0",
        "js-tokens": "^4.0.0"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/highlight/node_modules/ansi-styles": {
      "version": "3.2.1",
      "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-3.2.1.tgz",
      "integrity": "sha512-VT0ZI6kZRdTh8YyJw3SMbYm/u+NqfsAxEpWO0Pf9sq8/e94WxxOpPKx9FR1FlyCtOVDNOQ+8ntlqFxiRc+r5qA==",
      "license": "MIT",
      "dependencies": {
        "color-convert": "^1.9.0"
      },
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/@babel/highlight/node_modules/chalk": {
      "version": "2.4.2",
      "resolved": "https://registry.npmjs.org/chalk/-/chalk-2.4.2.tgz",
      "integrity": "sha512-Mti+f9lpJNcwF4tWV8/OrTTtF1gZi+f8FqlyAdouralcFWFQWF2+NgCHShjkCb+IFBLq9buZwE1xckQU4peSuQ==",
      "license": "MIT",
      "dependencies": {
        "ansi-styles": "^3.2.1",
        "escape-string-regexp": "^1.0.5",
        "supports-color": "^5.3.0"
      },
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/@babel/highlight/node_modules/color-convert": {
      "version": "1.9.3",
      "resolved": "https://registry.npmjs.org/color-convert/-/color-convert-1.9.3.tgz",
      "integrity": "sha512-QfAUtd+vFdAtFQcC8CCyYt1fYWxSqAiK2cSD6zDB8N3cpsEBAvRxp9zOGg6G/SHHJYAT88/az/IuDGALsNVbGg==",
      "license": "MIT",
      "dependencies": {
        "color-name": "1.1.3"
      }
    },
    "node_modules/@babel/highlight/node_modules/color-name": {
      "version": "1.1.3",
      "resolved": "https://registry.npmjs.org/color-name/-/color-name-1.1.3.tgz",
      "integrity": "sha512-72fSenhMw2HZMTVHeCA9KCmpEIbzWiQsjN+BHcBbS9vr1mtt+vJjPdksIBNUmKAW8TFUDPJK5SUU3QhE9NEXDw==",
      "license": "MIT"
    },
    "node_modules/@babel/highlight/node_modules/escape-string-regexp": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/escape-string-regexp/-/escape-string-regexp-1.0.5.tgz",
      "integrity": "sha512-vbRorB5FUQWvla16U8R/qgaFIya2qGzwDrNmCZuYKrbdSUMG6I1ZCGQRefkRVhuOkIGVne7BQ35DSfo1qvJqFg==",
      "license": "MIT",
      "engines": {
        "node": ">=0.8.0"
      }
    },
    "node_modules/@babel/highlight/node_modules/has-flag": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/has-flag/-/has-flag-3.0.0.tgz",
      "integrity": "sha512-sKJf1+ceQBr4SMkvQnBDNDtf4TXpVhVGateu0t918bl30FnbE2m4vNLX+VWe/dpjlb+HugGYzW7uQXH98HPEYw==",
      "license": "MIT",
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/@babel/highlight/node_modules/supports-color": {
      "version": "5.5.0",
      "resolved": "https://registry.npmjs.org/supports-color/-/supports-color-5.5.0.tgz",
      "integrity": "sha512-QjVjwdXIt408MIiAqCX4oUKsgU2EqAGzs2Ppkm4aQYbjm+ZEWEcW4SfFNTr4uMNZma0ey4f5lgLrkB0aX0QMow==",
      "license": "MIT",
      "dependencies": {
        "has-flag": "^3.0.0"
      },
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/@babel/parser": {
      "version": "7.20.13",
      "resolved": "https://registry.npmjs.org/@babel/parser/-/parser-7.20.13.tgz",
      "integrity": "sha512-gFDLKMfpiXCsjt4za2JA9oTMn70CeseCehb11kRZgvd7+F67Hih3OHOK24cRrWECJ/ljfPGac6ygXAs/C8kIvw==",
      "license": "MIT",
      "bin": {
        "parser": "bin/babel-parser.js"
      },
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/@babel/plugin-syntax-async-generators": {
      "version": "7.8.4",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-async-generators/-/plugin-syntax-async-generators-7.8.4.tgz",
      "integrity": "sha512-tycmZxkGfZaxhMRbXlPXuVFpdWlXpir2W4AMhSJgRKzk/eDlIXOhb2LHWoLpDF7TEHylV5zNhykX6KAgHJmTNw==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.8.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-bigint": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-bigint/-/plugin-syntax-bigint-7.8.3.tgz",
      "integrity": "sha512-wnTnFlG+YxQm3vDxpGE57Pj0srRU4sHE/mDkt1qv2YJJSeUAec2ma4WLUnUPeKjyrfntVwe/N6dCXpU+zL3Npg==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.8.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-class-properties": {
      "version": "7.12.13",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-class-properties/-/plugin-syntax-class-properties-7.12.13.tgz",
      "integrity": "sha512-fm4idjKla0YahUNgFNLCB0qySdsoPiZP3iQE3rky0mBUtMZ23yDJ9SJdg6dXTSDnulOVqiF3Hgr9nbXvXTQZYA==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.12.13"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-import-meta": {
      "version": "7.10.4",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-import-meta/-/plugin-syntax-import-meta-7.10.4.tgz",
      "integrity": "sha512-Yqfm+XDx0+Prh3VSeEQCPU81yC+JWZ2pDPFSS4ZdpfZhp4MkFMaDC1UqseovEKwSUpnIL7+vK+Clp7bfh0iD7g==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.10.4"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-json-strings": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-json-strings/-/plugin-syntax-json-strings-7.8.3.tgz",
      "integrity": "sha512-lY6kdGpWHvjoe2vk4WrAapEuBR69EMxZl+RoGRhrFGNYVK8mOPAW8VfbT/ZgrFbXlDNiiaxQnAtgVCZ6jv30EA==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.8.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-jsx": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-jsx/-/plugin-syntax-jsx-7.18.6.tgz",
      "integrity": "sha512-6mmljtAedFGTWu2p/8WIORGwy+61PLgOMPOdazc7YoJ9ZCWUyFy3A6CpPkRKLKD1ToAesxX8KGEViAiLo9N+7Q==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.18.6"
      },
      "engines": {
        "node": ">=6.9.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-logical-assignment-operators": {
      "version": "7.10.4",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-logical-assignment-operators/-/plugin-syntax-logical-assignment-operators-7.10.4.tgz",
      "integrity": "sha512-d8waShlpFDinQ5MtvGU9xDAOzKH47+FFoney2baFIoMr952hKOLp1HR7VszoZvOsV/4+RRszNY7D17ba0te0ig==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.10.4"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-nullish-coalescing-operator": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-nullish-coalescing-operator/-/plugin-syntax-nullish-coalescing-operator-7.8.3.tgz",
      "integrity": "sha512-aSff4zPII1u2QD7y+F8oDsz19ew4IGEJg9SVW+bqwpwtfFleiQDMdzA/R+UlWDzfnHFCxxleFT0PMIrR36XLNQ==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.8.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-numeric-separator": {
      "version": "7.10.4",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-numeric-separator/-/plugin-syntax-numeric-separator-7.10.4.tgz",
      "integrity": "sha512-9H6YdfkcK/uOnY/K7/aA2xpzaAgkQn37yzWUMRK7OaPOqOpGS1+n0H5hxT9AUw9EsSjPW8SVyMJwYRtWs3X3ug==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.10.4"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-object-rest-spread": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-object-rest-spread/-/plugin-syntax-object-rest-spread-7.8.3.tgz",
      "integrity": "sha512-XoqMijGZb9y3y2XskN+P1wUGiVwWZ5JmoDRwx5+3GmEplNyVM2s2Dg8ILFQm8rWM48orGy5YpI5Bl8U1y7ydlA==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.8.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-optional-catch-binding": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-optional-catch-binding/-/plugin-syntax-optional-catch-binding-7.8.3.tgz",
      "integrity": "sha512-6VPD0Pc1lpTqw0aKoeRTMiB+kWhAoT24PA+ksWSBrFtl5SIRVpZlwN3NNPQjehA2E/91FV3RjLWoVTglWcSV3Q==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.8.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-optional-chaining": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-optional-chaining/-/plugin-syntax-optional-chaining-7.8.3.tgz",
      "integrity": "sha512-KoK9ErH1MBlCPxV0VANkXW2/dw4vlbGDrFgz8bmUsBGYkFRcbRwMh6cIJubdPrkxRwuGdtCk0v/wPTKbQgBjkg==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.8.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-top-level-await": {
      "version": "7.14.5",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-top-level-await/-/plugin-syntax-top-level-await-7.14.5.tgz",
      "integrity": "sha512-hx++upLv5U1rgYfwe1xBQUhRmU41NEvpUvrp8jkrSCdvGSnM5/qdRMtylJ6PG5OFkBaHkbTAKTnd3/YyESRHFw==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.14.5"
      },
      "engines": {
        "node": ">=6.9.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/plugin-syntax-typescript": {
      "version": "7.20.0",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-typescript/-/plugin-syntax-typescript-7.20.0.tgz",
      "integrity": "sha512-rd9TkG+u1CExzS4SM1BlMEhMXwFLKVjOAFFCDx9PbX5ycJWDoWMcwdJH9RhkPu1dOgn5TrxLot/Gx6lWFuAUNQ==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.19.0"
      },
      "engines": {
        "node": ">=6.9.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0-0"
      }
    },
    "node_modules/@babel/template": {
      "version": "7.20.7",
      "resolved": "https://registry.npmjs.org/@babel/template/-/template-7.20.7.tgz",
      "integrity": "sha512-8SegXApWe6VoNw0r9JHpSteLKTpTiLZ4rMlGIm9JQ18KiCtyQiAMEazujAHrUS5flrcqYZa75ukev3P6QmUwUw==",
      "license": "MIT",
      "dependencies": {
        "@babel/code-frame": "^7.18.6",
        "@babel/parser": "^7.20.7",
        "@babel/types": "^7.20.7"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/traverse": {
      "version": "7.20.13",
      "resolved": "https://registry.npmjs.org/@babel/traverse/-/traverse-7.20.13.tgz",
      "integrity": "sha512-kMJXfF0T6DIS9E8cgdLCSAL+cuCK+YEZHWiLK0SXpTo8YRj5lpJu3CDNKiIBCne4m9hhTIqUg6SYTAI39tAiVQ==",
      "license": "MIT",
      "dependencies": {
        "@babel/code-frame": "^7.18.6",
        "@babel/generator": "^7.20.7",
        "@babel/helper-environment-visitor": "^7.18.9",
        "@babel/helper-function-name": "^7.19.0",
        "@babel/helper-hoist-variables": "^7.18.6",
        "@babel/helper-split-export-declaration": "^7.18.6",
        "@babel/parser": "^7.20.13",
        "@babel/types": "^7.20.7",
        "debug": "^4.1.0",
        "globals": "^11.1.0"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@babel/types": {
      "version": "7.20.7",
      "resolved": "https://registry.npmjs.org/@babel/types/-/types-7.20.7.tgz",
      "integrity": "sha512-69OnhBxSSgK0OzTJai4kyPDiKTIe3j+ctaHdIGVbRahTLAT7L3R9oeXHC2aVSuGYt3cVnoAMDmOCgJ2yaiLMvg==",
      "license": "MIT",
      "dependencies": {
        "@babel/helper-string-parser": "^7.19.4",
        "@babel/helper-validator-identifier": "^7.19.1",
        "to-fast-properties": "^2.0.0"
      },
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/@bcoe/v8-coverage": {
      "version": "0.2.3",
      "resolved": "https://registry.npmjs.org/@bcoe/v8-coverage/-/v8-coverage-0.2.3.tgz",
      "integrity": "sha512-0hYQ8SB4Db5zvZB4axdMHGwEaQjkZzFjQiN9LVYvIFB2nSUHW9tYpxWriPrWDASIxiaXax83REcLxuSdnGPZtw==",
      "license": "MIT"
    },
    "node_modules/@cspotcode/source-map-support": {
      "version": "0.8.1",
      "resolved": "https://registry.npmjs.org/@cspotcode/source-map-support/-/source-map-support-0.8.1.tgz",
      "integrity": "sha512-IchNf6dN4tHoMFIn/7OE8LWZ19Y6q/67Bmf6vnGREv8RSbBVb9LPJxEcnwrcwX6ixSvaiGoomAUvu4YSxXrVgw==",
      "license": "MIT",
      "dependencies": {
        "@jridgewell/trace-mapping": "0.3.9"
      },
      "engines": {
        "node": ">=12"
      }
    },
    "node_modules/@cspotcode/source-map-support/node_modules/@jridgewell/trace-mapping": {
      "version": "0.3.9",
      "resolved": "https://registry.npmjs.org/@jridgewell/trace-mapping/-/trace-mapping-0.3.9.tgz",
      "integrity": "sha512-3Belt6tdc8bPgAtbcmdtNJlirVoTmEb5e2gC94PnkwEW9jI6CAHUeoG85tjWP5WquqfavoMtMwiG4P926ZKKuQ==",
      "license": "MIT",
      "dependencies": {
        "@jridgewell/resolve-uri": "^3.0.3",
        "@jridgewell/sourcemap-codec": "^1.4.10"
      }
    },
    "node_modules/@ipld/dag-pb": {
      "version": "2.1.18",
      "resolved": "https://registry.npmjs.org/@ipld/dag-pb/-/dag-pb-2.1.18.tgz",
      "integrity": "sha512-ZBnf2fuX9y3KccADURG5vb9FaOeMjFkCrNysB0PtftME/4iCTjxfaLoNq/IAh5fTqUOMXvryN6Jyka4ZGuMLIg==",
      "license": "(Apache-2.0 AND MIT)",
      "dependencies": {
        "multiformats": "^9.5.4"
      }
    },
    "node_modules/@istanbuljs/load-nyc-config": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@istanbuljs/load-nyc-config/-/load-nyc-config-1.1.0.tgz",
      "integrity": "sha512-VjeHSlIzpv/NyD3N0YuHfXOPDIixcA1q2ZV98wsMqcYlPmv2n3Yb2lYP9XMElnaFVXg5A7YLTeLu6V84uQDjmQ==",
      "license": "ISC",
      "dependencies": {
        "camelcase": "^5.3.1",
        "find-up": "^4.1.0",
        "get-package-type": "^0.1.0",
        "js-yaml": "^3.13.1",
        "resolve-from": "^5.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/@istanbuljs/load-nyc-config/node_modules/camelcase": {
      "version": "5.3.1",
      "resolved": "https://registry.npmjs.org/camelcase/-/camelcase-5.3.1.tgz",
      "integrity": "sha512-L28STB170nwWS63UjtlEOE3dldQApaJXZkOI1uMFfzf3rRuPegHaHesyee+YxQ+W6SvRDQV6UrdOdRiR153wJg==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/@istanbuljs/schema": {
      "version": "0.1.3",
      "resolved": "https://registry.npmjs.org/@istanbuljs/schema/-/schema-0.1.3.tgz",
      "integrity": "sha512-ZXRY4jNvVgSVQ8DL3LTcakaAtXwTVUxE81hslsyD2AtoXW/wVob10HkOJ1X/pAlcI7D+2YoZKg5do8G/w6RYgA==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/@jest/console": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/console/-/console-29.4.1.tgz",
      "integrity": "sha512-m+XpwKSi3PPM9znm5NGS8bBReeAJJpSkL1OuFCqaMaJL2YX9YXLkkI+MBchMPwu+ZuM2rynL51sgfkQteQ1CKQ==",
      "license": "MIT",
      "dependencies": {
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "jest-message-util": "^29.4.1",
        "jest-util": "^29.4.1",
        "slash": "^3.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/core": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/core/-/core-29.4.1.tgz",
      "integrity": "sha512-RXFTohpBqpaTebNdg5l3I5yadnKo9zLBajMT0I38D0tDhreVBYv3fA8kywthI00sWxPztWLD3yjiUkewwu/wKA==",
      "license": "MIT",
      "dependencies": {
        "@jest/console": "^29.4.1",
        "@jest/reporters": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "ansi-escapes": "^4.2.1",
        "chalk": "^4.0.0",
        "ci-info": "^3.2.0",
        "exit": "^0.1.2",
        "graceful-fs": "^4.2.9",
        "jest-changed-files": "^29.4.0",
        "jest-config": "^29.4.1",
        "jest-haste-map": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-regex-util": "^29.2.0",
        "jest-resolve": "^29.4.1",
        "jest-resolve-dependencies": "^29.4.1",
        "jest-runner": "^29.4.1",
        "jest-runtime": "^29.4.1",
        "jest-snapshot": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-validate": "^29.4.1",
        "jest-watcher": "^29.4.1",
        "micromatch": "^4.0.4",
        "pretty-format": "^29.4.1",
        "slash": "^3.0.0",
        "strip-ansi": "^6.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "peerDependencies": {
        "node-notifier": "^8.0.1 || ^9.0.0 || ^10.0.0"
      },
      "peerDependenciesMeta": {
        "node-notifier": {
          "optional": true
        }
      }
    },
    "node_modules/@jest/environment": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/environment/-/environment-29.4.1.tgz",
      "integrity": "sha512-pJ14dHGSQke7Q3mkL/UZR9ZtTOxqskZaC91NzamEH4dlKRt42W+maRBXiw/LWkdJe+P0f/zDR37+SPMplMRlPg==",
      "license": "MIT",
      "dependencies": {
        "@jest/fake-timers": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "jest-mock": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/expect": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/expect/-/expect-29.4.1.tgz",
      "integrity": "sha512-ZxKJP5DTUNF2XkpJeZIzvnzF1KkfrhEF6Rz0HGG69fHl6Bgx5/GoU3XyaeFYEjuuKSOOsbqD/k72wFvFxc3iTw==",
      "license": "MIT",
      "dependencies": {
        "expect": "^29.4.1",
        "jest-snapshot": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/expect-utils": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/expect-utils/-/expect-utils-29.4.1.tgz",
      "integrity": "sha512-w6YJMn5DlzmxjO00i9wu2YSozUYRBhIoJ6nQwpMYcBMtiqMGJm1QBzOf6DDgRao8dbtpDoaqLg6iiQTvv0UHhQ==",
      "license": "MIT",
      "dependencies": {
        "jest-get-type": "^29.2.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/fake-timers": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/fake-timers/-/fake-timers-29.4.1.tgz",
      "integrity": "sha512-/1joI6rfHFmmm39JxNfmNAO3Nwm6Y0VoL5fJDy7H1AtWrD1CgRtqJbN9Ld6rhAkGO76qqp4cwhhxJ9o9kYjQMw==",
      "license": "MIT",
      "dependencies": {
        "@jest/types": "^29.4.1",
        "@sinonjs/fake-timers": "^10.0.2",
        "@types/node": "*",
        "jest-message-util": "^29.4.1",
        "jest-mock": "^29.4.1",
        "jest-util": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/globals": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/globals/-/globals-29.4.1.tgz",
      "integrity": "sha512-znoK2EuFytbHH0ZSf2mQK2K1xtIgmaw4Da21R2C/NE/+NnItm5mPEFQmn8gmF3f0rfOlmZ3Y3bIf7bFj7DHxAA==",
      "license": "MIT",
      "dependencies": {
        "@jest/environment": "^29.4.1",
        "@jest/expect": "^29.4.1",
        "@jest/types": "^29.4.1",
        "jest-mock": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/reporters": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/reporters/-/reporters-29.4.1.tgz",
      "integrity": "sha512-AISY5xpt2Xpxj9R6y0RF1+O6GRy9JsGa8+vK23Lmzdy1AYcpQn5ItX79wJSsTmfzPKSAcsY1LNt/8Y5Xe5LOSg==",
      "license": "MIT",
      "dependencies": {
        "@bcoe/v8-coverage": "^0.2.3",
        "@jest/console": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@jridgewell/trace-mapping": "^0.3.15",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "collect-v8-coverage": "^1.0.0",
        "exit": "^0.1.2",
        "glob": "^7.1.3",
        "graceful-fs": "^4.2.9",
        "istanbul-lib-coverage": "^3.0.0",
        "istanbul-lib-instrument": "^5.1.0",
        "istanbul-lib-report": "^3.0.0",
        "istanbul-lib-source-maps": "^4.0.0",
        "istanbul-reports": "^3.1.3",
        "jest-message-util": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-worker": "^29.4.1",
        "slash": "^3.0.0",
        "string-length": "^4.0.1",
        "strip-ansi": "^6.0.0",
        "v8-to-istanbul": "^9.0.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "peerDependencies": {
        "node-notifier": "^8.0.1 || ^9.0.0 || ^10.0.0"
      },
      "peerDependenciesMeta": {
        "node-notifier": {
          "optional": true
        }
      }
    },
    "node_modules/@jest/schemas": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/@jest/schemas/-/schemas-29.4.0.tgz",
      "integrity": "sha512-0E01f/gOZeNTG76i5eWWSupvSHaIINrTie7vCyjiYFKgzNdyEGd12BUv4oNBFHOqlHDbtoJi3HrQ38KCC90NsQ==",
      "license": "MIT",
      "dependencies": {
        "@sinclair/typebox": "^0.25.16"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/source-map": {
      "version": "29.2.0",
      "resolved": "https://registry.npmjs.org/@jest/source-map/-/source-map-29.2.0.tgz",
      "integrity": "sha512-1NX9/7zzI0nqa6+kgpSdKPK+WU1p+SJk3TloWZf5MzPbxri9UEeXX5bWZAPCzbQcyuAzubcdUHA7hcNznmRqWQ==",
      "license": "MIT",
      "dependencies": {
        "@jridgewell/trace-mapping": "^0.3.15",
        "callsites": "^3.0.0",
        "graceful-fs": "^4.2.9"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/test-result": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/test-result/-/test-result-29.4.1.tgz",
      "integrity": "sha512-WRt29Lwt+hEgfN8QDrXqXGgCTidq1rLyFqmZ4lmJOpVArC8daXrZWkWjiaijQvgd3aOUj2fM8INclKHsQW9YyQ==",
      "license": "MIT",
      "dependencies": {
        "@jest/console": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/istanbul-lib-coverage": "^2.0.0",
        "collect-v8-coverage": "^1.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/test-sequencer": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/test-sequencer/-/test-sequencer-29.4.1.tgz",
      "integrity": "sha512-v5qLBNSsM0eHzWLXsQ5fiB65xi49A3ILPSFQKPXzGL4Vyux0DPZAIN7NAFJa9b4BiTDP9MBF/Zqc/QA1vuiJ0w==",
      "license": "MIT",
      "dependencies": {
        "@jest/test-result": "^29.4.1",
        "graceful-fs": "^4.2.9",
        "jest-haste-map": "^29.4.1",
        "slash": "^3.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/transform": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/transform/-/transform-29.4.1.tgz",
      "integrity": "sha512-5w6YJrVAtiAgr0phzKjYd83UPbCXsBRTeYI4BXokv9Er9CcrH9hfXL/crCvP2d2nGOcovPUnlYiLPFLZrkG5Hg==",
      "license": "MIT",
      "dependencies": {
        "@babel/core": "^7.11.6",
        "@jest/types": "^29.4.1",
        "@jridgewell/trace-mapping": "^0.3.15",
        "babel-plugin-istanbul": "^6.1.1",
        "chalk": "^4.0.0",
        "convert-source-map": "^2.0.0",
        "fast-json-stable-stringify": "^2.1.0",
        "graceful-fs": "^4.2.9",
        "jest-haste-map": "^29.4.1",
        "jest-regex-util": "^29.2.0",
        "jest-util": "^29.4.1",
        "micromatch": "^4.0.4",
        "pirates": "^4.0.4",
        "slash": "^3.0.0",
        "write-file-atomic": "^5.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jest/transform/node_modules/convert-source-map": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/convert-source-map/-/convert-source-map-2.0.0.tgz",
      "integrity": "sha512-Kvp459HrV2FEJ1CAsi1Ku+MY3kasH19TFykTz2xWmMeq6bk2NU3XXvfJ+Q61m0xktWwt+1HSYf3JZsTms3aRJg==",
      "license": "MIT"
    },
    "node_modules/@jest/types": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/types/-/types-29.4.1.tgz",
      "integrity": "sha512-zbrAXDUOnpJ+FMST2rV7QZOgec8rskg2zv8g2ajeqitp4tvZiyqTCYXANrKsM+ryj5o+LI+ZN2EgU9drrkiwSA==",
      "license": "MIT",
      "dependencies": {
        "@jest/schemas": "^29.4.0",
        "@types/istanbul-lib-coverage": "^2.0.0",
        "@types/istanbul-reports": "^3.0.0",
        "@types/node": "*",
        "@types/yargs": "^17.0.8",
        "chalk": "^4.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/@jridgewell/gen-mapping": {
      "version": "0.3.2",
      "resolved": "https://registry.npmjs.org/@jridgewell/gen-mapping/-/gen-mapping-0.3.2.tgz",
      "integrity": "sha512-mh65xKQAzI6iBcFzwv28KVWSmCkdRBWoOh+bYQGW3+6OZvbbN3TqMGo5hqYxQniRcH9F2VZIoJCm4pa3BPDK/A==",
      "license": "MIT",
      "dependencies": {
        "@jridgewell/set-array": "^1.0.1",
        "@jridgewell/sourcemap-codec": "^1.4.10",
        "@jridgewell/trace-mapping": "^0.3.9"
      },
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/@jridgewell/resolve-uri": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/@jridgewell/resolve-uri/-/resolve-uri-3.1.0.tgz",
      "integrity": "sha512-F2msla3tad+Mfht5cJq7LSXcdudKTWCVYUgw6pLFOOHSTtZlj6SWNYAp+AhuqLmWdBO2X5hPrLcu8cVP8fy28w==",
      "license": "MIT",
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/@jridgewell/set-array": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/@jridgewell/set-array/-/set-array-1.1.2.tgz",
      "integrity": "sha512-xnkseuNADM0gt2bs+BvhO0p78Mk762YnZdsuzFV018NoG1Sj1SCQvpSqa7XUaTam5vAGasABV9qXASMKnFMwMw==",
      "license": "MIT",
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/@jridgewell/sourcemap-codec": {
      "version": "1.4.14",
      "resolved": "https://registry.npmjs.org/@jridgewell/sourcemap-codec/-/sourcemap-codec-1.4.14.tgz",
      "integrity": "sha512-XPSJHWmi394fuUuzDnGz1wiKqWfo1yXecHQMRf2l6hztTO+nPru658AyDngaBe7isIxEkRsPR3FZh+s7iVa4Uw==",
      "license": "MIT"
    },
    "node_modules/@jridgewell/trace-mapping": {
      "version": "0.3.17",
      "resolved": "https://registry.npmjs.org/@jridgewell/trace-mapping/-/trace-mapping-0.3.17.tgz",
      "integrity": "sha512-MCNzAp77qzKca9+W/+I0+sEpaUnZoeasnghNeVc41VZCEKaCH73Vq3BZZ/SzWIgrqE4H4ceI+p+b6C0mHf9T4g==",
      "license": "MIT",
      "dependencies": {
        "@jridgewell/resolve-uri": "3.1.0",
        "@jridgewell/sourcemap-codec": "1.4.14"
      }
    },
    "node_modules/@multiformats/murmur3": {
      "version": "1.1.3",
      "resolved": "https://registry.npmjs.org/@multiformats/murmur3/-/murmur3-1.1.3.tgz",
      "integrity": "sha512-wAPLUErGR8g6Lt+bAZn6218k9YQPym+sjszsXL6o4zfxbA22P+gxWZuuD9wDbwL55xrKO5idpcuQUX7/E3oHcw==",
      "license": "(Apache-2.0 AND MIT)",
      "dependencies": {
        "multiformats": "^9.5.4",
        "murmurhash3js-revisited": "^3.0.0"
      }
    },
    "node_modules/@orbs-network/ton-access": {
      "version": "2.2.2",
      "resolved": "https://registry.npmjs.org/@orbs-network/ton-access/-/ton-access-2.2.2.tgz",
      "integrity": "sha512-ygcbNxqZez2CpDMFhMTgbNAm7MGoDCbF1Zbp/liUAWqrKjytUDAoAAVXIWulhl0exWaacn7YWI75GNt8ouxjwA==",
      "dependencies": {
        "isomorphic-fetch": "^3.0.0"
      }
    },
    "node_modules/@protobufjs/aspromise": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/@protobufjs/aspromise/-/aspromise-1.1.2.tgz",
      "integrity": "sha512-j+gKExEuLmKwvz3OgROXtrJ2UG2x8Ch2YZUxahh+s1F2HZ+wAceUNLkvy6zKCPVRkU++ZWQrdxsUeQXmcg4uoQ==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@protobufjs/base64": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/@protobufjs/base64/-/base64-1.1.2.tgz",
      "integrity": "sha512-AZkcAA5vnN/v4PDqKyMR5lx7hZttPDgClv83E//FMNhR2TMcLUhfRUBHCmSl0oi9zMgDDqRUJkSxO3wm85+XLg==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@protobufjs/codegen": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/@protobufjs/codegen/-/codegen-2.0.4.tgz",
      "integrity": "sha512-YyFaikqM5sH0ziFZCN3xDC7zeGaB/d0IUb9CATugHWbd1FRFwWwt4ld4OYMPWu5a3Xe01mGAULCdqhMlPl29Jg==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@protobufjs/eventemitter": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/eventemitter/-/eventemitter-1.1.0.tgz",
      "integrity": "sha512-j9ednRT81vYJ9OfVuXG6ERSTdEL1xVsNgqpkxMsbIabzSo3goCjDIveeGv5d03om39ML71RdmrGNjG5SReBP/Q==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@protobufjs/fetch": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/fetch/-/fetch-1.1.0.tgz",
      "integrity": "sha512-lljVXpqXebpsijW71PZaCYeIcE5on1w5DlQy5WH6GLbFryLUrBD4932W/E2BSpfRJWseIL4v/KPgBFxDOIdKpQ==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "@protobufjs/aspromise": "^1.1.1",
        "@protobufjs/inquire": "^1.1.0"
      }
    },
    "node_modules/@protobufjs/float": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/@protobufjs/float/-/float-1.0.2.tgz",
      "integrity": "sha512-Ddb+kVXlXst9d+R9PfTIxh1EdNkgoRe5tOX6t01f1lYWOvJnSPDBlG241QLzcyPdoNTsblLUdujGSE4RzrTZGQ==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@protobufjs/inquire": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/inquire/-/inquire-1.1.0.tgz",
      "integrity": "sha512-kdSefcPdruJiFMVSbn801t4vFK7KB/5gd2fYvrxhuJYg8ILrmn9SKSX2tZdV6V+ksulWqS7aXjBcRXl3wHoD9Q==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@protobufjs/path": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/@protobufjs/path/-/path-1.1.2.tgz",
      "integrity": "sha512-6JOcJ5Tm08dOHAbdR3GrvP+yUUfkjG5ePsHYczMFLq3ZmMkAD98cDgcT2iA1lJ9NVwFd4tH/iSSoe44YWkltEA==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@protobufjs/pool": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/pool/-/pool-1.1.0.tgz",
      "integrity": "sha512-0kELaGSIDBKvcgS4zkjz1PeddatrjYcmMWOlAuAPwAeccUrPHdUqo/J6LiymHHEiJT5NrF1UVwxY14f+fy4WQw==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@protobufjs/utf8": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/utf8/-/utf8-1.1.0.tgz",
      "integrity": "sha512-Vvn3zZrhQZkkBE8LSuW3em98c0FwgO4nxzv6OdSxPKJIEKY2bGbHn+mhGIPerzI4twdxaP8/0+06HBpwf345Lw==",
      "license": "BSD-3-Clause"
    },
    "node_modules/@scarf/scarf": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/@scarf/scarf/-/scarf-1.1.1.tgz",
      "integrity": "sha512-VGbKDbk1RFIaSmdVb0cNjjWJoRWRI/Weo23AjRCC2nryO0iAS8pzsToJfPVPtVs74WHw4L1UTADNdIYRLkirZQ==",
      "hasInstallScript": true,
      "license": "Apache-2.0"
    },
    "node_modules/@sinclair/typebox": {
      "version": "0.25.21",
      "resolved": "https://registry.npmjs.org/@sinclair/typebox/-/typebox-0.25.21.tgz",
      "integrity": "sha512-gFukHN4t8K4+wVC+ECqeqwzBDeFeTzBXroBTqE6vcWrQGbEUpHO7LYdG0f4xnvYq4VOEwITSlHlp0JBAIFMS/g==",
      "license": "MIT"
    },
    "node_modules/@sinonjs/commons": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/@sinonjs/commons/-/commons-2.0.0.tgz",
      "integrity": "sha512-uLa0j859mMrg2slwQYdO/AkrOfmH+X6LTVmNTS9CqexuE2IvVORIkSpJLqePAbEnKJ77aMmCwr1NUZ57120Xcg==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "type-detect": "4.0.8"
      }
    },
    "node_modules/@sinonjs/fake-timers": {
      "version": "10.0.2",
      "resolved": "https://registry.npmjs.org/@sinonjs/fake-timers/-/fake-timers-10.0.2.tgz",
      "integrity": "sha512-SwUDyjWnah1AaNl7kxsa7cfLhlTYoiyhDAIgyh+El30YvXs/o7OLXpYH88Zdhyx9JExKrmHDJ+10bwIcY80Jmw==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "@sinonjs/commons": "^2.0.0"
      }
    },
    "node_modules/@tsconfig/node10": {
      "version": "1.0.9",
      "resolved": "https://registry.npmjs.org/@tsconfig/node10/-/node10-1.0.9.tgz",
      "integrity": "sha512-jNsYVVxU8v5g43Erja32laIDHXeoNvFEpX33OK4d6hljo3jDhCBDhx5dhCCTMWUojscpAagGiRkBKxpdl9fxqA==",
      "license": "MIT"
    },
    "node_modules/@tsconfig/node12": {
      "version": "1.0.11",
      "resolved": "https://registry.npmjs.org/@tsconfig/node12/-/node12-1.0.11.tgz",
      "integrity": "sha512-cqefuRsh12pWyGsIoBKJA9luFu3mRxCA+ORZvA4ktLSzIuCUtWVxGIuXigEwO5/ywWFMZ2QEGKWvkZG1zDMTag==",
      "license": "MIT"
    },
    "node_modules/@tsconfig/node14": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/@tsconfig/node14/-/node14-1.0.3.tgz",
      "integrity": "sha512-ysT8mhdixWK6Hw3i1V2AeRqZ5WfXg1G43mqoYlM2nc6388Fq5jcXyr5mRsqViLx/GJYdoL0bfXD8nmF+Zn/Iow==",
      "license": "MIT"
    },
    "node_modules/@tsconfig/node16": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/@tsconfig/node16/-/node16-1.0.3.tgz",
      "integrity": "sha512-yOlFc+7UtL/89t2ZhjPvvB/DeAr3r+Dq58IgzsFkOAvVC6NMJXmCGjbptdXdR9qsX7pKcTL+s87FtYREi2dEEQ==",
      "license": "MIT"
    },
    "node_modules/@types/babel__core": {
      "version": "7.20.0",
      "resolved": "https://registry.npmjs.org/@types/babel__core/-/babel__core-7.20.0.tgz",
      "integrity": "sha512-+n8dL/9GWblDO0iU6eZAwEIJVr5DWigtle+Q6HLOrh/pdbXOhOtqzq8VPPE2zvNJzSKY4vH/z3iT3tn0A3ypiQ==",
      "license": "MIT",
      "dependencies": {
        "@babel/parser": "^7.20.7",
        "@babel/types": "^7.20.7",
        "@types/babel__generator": "*",
        "@types/babel__template": "*",
        "@types/babel__traverse": "*"
      }
    },
    "node_modules/@types/babel__generator": {
      "version": "7.6.4",
      "resolved": "https://registry.npmjs.org/@types/babel__generator/-/babel__generator-7.6.4.tgz",
      "integrity": "sha512-tFkciB9j2K755yrTALxD44McOrk+gfpIpvC3sxHjRawj6PfnQxrse4Clq5y/Rq+G3mrBurMax/lG8Qn2t9mSsg==",
      "license": "MIT",
      "dependencies": {
        "@babel/types": "^7.0.0"
      }
    },
    "node_modules/@types/babel__template": {
      "version": "7.4.1",
      "resolved": "https://registry.npmjs.org/@types/babel__template/-/babel__template-7.4.1.tgz",
      "integrity": "sha512-azBFKemX6kMg5Io+/rdGT0dkGreboUVR0Cdm3fz9QJWpaQGJRQXl7C+6hOTCZcMll7KFyEQpgbYI2lHdsS4U7g==",
      "license": "MIT",
      "dependencies": {
        "@babel/parser": "^7.1.0",
        "@babel/types": "^7.0.0"
      }
    },
    "node_modules/@types/babel__traverse": {
      "version": "7.18.3",
      "resolved": "https://registry.npmjs.org/@types/babel__traverse/-/babel__traverse-7.18.3.tgz",
      "integrity": "sha512-1kbcJ40lLB7MHsj39U4Sh1uTd2E7rLEa79kmDpI6cy+XiXsteB3POdQomoq4FxszMrO3ZYchkhYJw7A2862b3w==",
      "license": "MIT",
      "dependencies": {
        "@babel/types": "^7.3.0"
      }
    },
    "node_modules/@types/graceful-fs": {
      "version": "4.1.6",
      "resolved": "https://registry.npmjs.org/@types/graceful-fs/-/graceful-fs-4.1.6.tgz",
      "integrity": "sha512-Sig0SNORX9fdW+bQuTEovKj3uHcUL6LQKbCrrqb1X7J6/ReAbhCXRAhc+SMejhLELFj2QcyuxmUooZ4bt5ReSw==",
      "license": "MIT",
      "dependencies": {
        "@types/node": "*"
      }
    },
    "node_modules/@types/istanbul-lib-coverage": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/@types/istanbul-lib-coverage/-/istanbul-lib-coverage-2.0.4.tgz",
      "integrity": "sha512-z/QT1XN4K4KYuslS23k62yDIDLwLFkzxOuMplDtObz0+y7VqJCaO2o+SPwHCvLFZh7xazvvoor2tA/hPz9ee7g==",
      "license": "MIT"
    },
    "node_modules/@types/istanbul-lib-report": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/@types/istanbul-lib-report/-/istanbul-lib-report-3.0.0.tgz",
      "integrity": "sha512-plGgXAPfVKFoYfa9NpYDAkseG+g6Jr294RqeqcqDixSbU34MZVJRi/P+7Y8GDpzkEwLaGZZOpKIEmeVZNtKsrg==",
      "license": "MIT",
      "dependencies": {
        "@types/istanbul-lib-coverage": "*"
      }
    },
    "node_modules/@types/istanbul-reports": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/@types/istanbul-reports/-/istanbul-reports-3.0.1.tgz",
      "integrity": "sha512-c3mAZEuK0lvBp8tmuL74XRKn1+y2dcwOUpH7x4WrF6gk1GIgiluDRgMYQtw2OFcBvAJWlt6ASU3tSqxp0Uu0Aw==",
      "license": "MIT",
      "dependencies": {
        "@types/istanbul-lib-report": "*"
      }
    },
    "node_modules/@types/jest": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/@types/jest/-/jest-29.4.0.tgz",
      "integrity": "sha512-VaywcGQ9tPorCX/Jkkni7RWGFfI11whqzs8dvxF41P17Z+z872thvEvlIbznjPJ02kl1HMX3LmLOonsj2n7HeQ==",
      "license": "MIT",
      "dependencies": {
        "expect": "^29.0.0",
        "pretty-format": "^29.0.0"
      }
    },
    "node_modules/@types/long": {
      "version": "4.0.2",
      "resolved": "https://registry.npmjs.org/@types/long/-/long-4.0.2.tgz",
      "integrity": "sha512-MqTGEo5bj5t157U6fA/BiDynNkn0YknVdh48CMPkTSpFTVmvao5UQmm7uEF6xBEo7qIMAlY/JSleYaE6VOdpaA==",
      "license": "MIT"
    },
    "node_modules/@types/node": {
      "version": "18.11.18",
      "resolved": "https://registry.npmjs.org/@types/node/-/node-18.11.18.tgz",
      "integrity": "sha512-DHQpWGjyQKSHj3ebjFI/wRKcqQcdR+MoFBygntYOZytCqNfkd2ZC4ARDJ2DQqhjH5p85Nnd3jhUJIXrszFX/JA==",
      "license": "MIT"
    },
    "node_modules/@types/prettier": {
      "version": "2.7.2",
      "resolved": "https://registry.npmjs.org/@types/prettier/-/prettier-2.7.2.tgz",
      "integrity": "sha512-KufADq8uQqo1pYKVIYzfKbJfBAc0sOeXqGbFaSpv8MRmC/zXgowNZmFcbngndGk922QDmOASEXUZCaY48gs4cg==",
      "license": "MIT"
    },
    "node_modules/@types/qs": {
      "version": "6.9.7",
      "resolved": "https://registry.npmjs.org/@types/qs/-/qs-6.9.7.tgz",
      "integrity": "sha512-FGa1F62FT09qcrueBA6qYTrJPVDzah9a+493+o2PCXsesWHIn27G98TsSMs3WPNbZIEj4+VJf6saSFpvD+3Zsw==",
      "license": "MIT"
    },
    "node_modules/@types/stack-utils": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/@types/stack-utils/-/stack-utils-2.0.1.tgz",
      "integrity": "sha512-Hl219/BT5fLAaz6NDkSuhzasy49dwQS/DSdu4MdggFB8zcXv7vflBI3xp7FEmkmdDkBUI2bPUNeMttp2knYdxw==",
      "license": "MIT"
    },
    "node_modules/@types/tmp": {
      "version": "0.2.3",
      "resolved": "https://registry.npmjs.org/@types/tmp/-/tmp-0.2.3.tgz",
      "integrity": "sha512-dDZH/tXzwjutnuk4UacGgFRwV+JSLaXL1ikvidfJprkb7L9Nx1njcRHHmi3Dsvt7pgqqTEeucQuOrWHPFgzVHA==",
      "license": "MIT"
    },
    "node_modules/@types/yargs": {
      "version": "17.0.22",
      "resolved": "https://registry.npmjs.org/@types/yargs/-/yargs-17.0.22.tgz",
      "integrity": "sha512-pet5WJ9U8yPVRhkwuEIp5ktAeAqRZOq4UdAyWLWzxbtpyXnzbtLdKiXAjJzi/KLmPGS9wk86lUFWZFN6sISo4g==",
      "license": "MIT",
      "dependencies": {
        "@types/yargs-parser": "*"
      }
    },
    "node_modules/@types/yargs-parser": {
      "version": "21.0.0",
      "resolved": "https://registry.npmjs.org/@types/yargs-parser/-/yargs-parser-21.0.0.tgz",
      "integrity": "sha512-iO9ZQHkZxHn4mSakYV0vFHAVDyEOIJQrV2uZ06HxEPcx+mt8swXoZHIbaaJ2crJYFfErySgktuTZ3BeLz+XmFA==",
      "license": "MIT"
    },
    "node_modules/acorn": {
      "version": "8.8.2",
      "resolved": "https://registry.npmjs.org/acorn/-/acorn-8.8.2.tgz",
      "integrity": "sha512-xjIYgE8HBrkpd/sJqOGNspf8uHG+NOHGOw6a/Urj8taM2EXfdNAH2oFcPeIFfsv3+kz/mJrS5VuMqbNLjCa2vw==",
      "license": "MIT",
      "bin": {
        "acorn": "bin/acorn"
      },
      "engines": {
        "node": ">=0.4.0"
      }
    },
    "node_modules/acorn-walk": {
      "version": "8.2.0",
      "resolved": "https://registry.npmjs.org/acorn-walk/-/acorn-walk-8.2.0.tgz",
      "integrity": "sha512-k+iyHEuPgSw6SbuDpGQM+06HQUa04DZ3o+F6CSzXMvvI5KMvnaEqXe+YVe555R9nn6GPt404fos4wcgpw12SDA==",
      "license": "MIT",
      "engines": {
        "node": ">=0.4.0"
      }
    },
    "node_modules/ansi-colors": {
      "version": "4.1.3",
      "resolved": "https://registry.npmjs.org/ansi-colors/-/ansi-colors-4.1.3.tgz",
      "integrity": "sha512-/6w/C21Pm1A7aZitlI5Ni/2J6FFQN8i1Cvz3kHABAAbw93v/NlvKdVOqz7CCWz/3iv/JplRSEEZ83XION15ovw==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/ansi-escapes": {
      "version": "4.3.2",
      "resolved": "https://registry.npmjs.org/ansi-escapes/-/ansi-escapes-4.3.2.tgz",
      "integrity": "sha512-gKXj5ALrKWQLsYG9jlTRmR/xKluxHV+Z9QEwNIgCfM1/uwPMCuzVVnh5mwTd+OuBZcwSIMbqssNWRm1lE51QaQ==",
      "license": "MIT",
      "dependencies": {
        "type-fest": "^0.21.3"
      },
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/ansi-regex": {
      "version": "5.0.1",
      "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-5.0.1.tgz",
      "integrity": "sha512-quJQXlTSUGL2LH9SUXo8VwsY4soanhgo6LNSm84E1LBcE8s3O0wpdiRzyR9z/ZZJMlMWv37qOOb9pdJlMUEKFQ==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/ansi-styles": {
      "version": "4.3.0",
      "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-4.3.0.tgz",
      "integrity": "sha512-zbB9rCJAT1rbjiVDb2hqKFHNYLxgtk8NURxZ3IZwD3F6NtxbXZQCnnSi1Lkx+IDohdPlFp222wVALIheZJQSEg==",
      "license": "MIT",
      "dependencies": {
        "color-convert": "^2.0.1"
      },
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-styles?sponsor=1"
      }
    },
    "node_modules/anymatch": {
      "version": "3.1.3",
      "resolved": "https://registry.npmjs.org/anymatch/-/anymatch-3.1.3.tgz",
      "integrity": "sha512-KMReFUr0B4t+D+OBkjR3KYqvocp2XaSzO55UcB6mgQMd3KbcE+mWTyvVV7D/zsdEbNnV6acZUutkiHQXvTr1Rw==",
      "license": "ISC",
      "dependencies": {
        "normalize-path": "^3.0.0",
        "picomatch": "^2.0.4"
      },
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/arg": {
      "version": "4.1.3",
      "resolved": "https://registry.npmjs.org/arg/-/arg-4.1.3.tgz",
      "integrity": "sha512-58S9QDqG0Xx27YwPSt9fJxivjYl432YCwfDMfZ+71RAqUrZef7LrKQZ3LHLOwCS4FLNBplP533Zx895SeOCHvA==",
      "license": "MIT"
    },
    "node_modules/argparse": {
      "version": "1.0.10",
      "resolved": "https://registry.npmjs.org/argparse/-/argparse-1.0.10.tgz",
      "integrity": "sha512-o5Roy6tNG4SL/FOkCAN6RzjiakZS25RLYFrcMttJqbdd8BWrnA+fGz57iN5Pb06pvBGvl5gQ0B48dJlslXvoTg==",
      "license": "MIT",
      "dependencies": {
        "sprintf-js": "~1.0.2"
      }
    },
    "node_modules/axios": {
      "version": "0.25.0",
      "resolved": "https://registry.npmjs.org/axios/-/axios-0.25.0.tgz",
      "integrity": "sha512-cD8FOb0tRH3uuEe6+evtAbgJtfxr7ly3fQjYcMcuPlgkwVS9xboaVIpcDV+cYQe+yGykgwZCs1pzjntcGa6l5g==",
      "license": "MIT",
      "dependencies": {
        "follow-redirects": "^1.14.7"
      }
    },
    "node_modules/babel-jest": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/babel-jest/-/babel-jest-29.4.1.tgz",
      "integrity": "sha512-xBZa/pLSsF/1sNpkgsiT3CmY7zV1kAsZ9OxxtrFqYucnOuRftXAfcJqcDVyOPeN4lttWTwhLdu0T9f8uvoPEUg==",
      "license": "MIT",
      "dependencies": {
        "@jest/transform": "^29.4.1",
        "@types/babel__core": "^7.1.14",
        "babel-plugin-istanbul": "^6.1.1",
        "babel-preset-jest": "^29.4.0",
        "chalk": "^4.0.0",
        "graceful-fs": "^4.2.9",
        "slash": "^3.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.8.0"
      }
    },
    "node_modules/babel-plugin-istanbul": {
      "version": "6.1.1",
      "resolved": "https://registry.npmjs.org/babel-plugin-istanbul/-/babel-plugin-istanbul-6.1.1.tgz",
      "integrity": "sha512-Y1IQok9821cC9onCx5otgFfRm7Lm+I+wwxOx738M/WLPZ9Q42m4IG5W0FNX8WLL2gYMZo3JkuXIH2DOpWM+qwA==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "@babel/helper-plugin-utils": "^7.0.0",
        "@istanbuljs/load-nyc-config": "^1.0.0",
        "@istanbuljs/schema": "^0.1.2",
        "istanbul-lib-instrument": "^5.0.4",
        "test-exclude": "^6.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/babel-plugin-jest-hoist": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/babel-plugin-jest-hoist/-/babel-plugin-jest-hoist-29.4.0.tgz",
      "integrity": "sha512-a/sZRLQJEmsmejQ2rPEUe35nO1+C9dc9O1gplH1SXmJxveQSRUYdBk8yGZG/VOUuZs1u2aHZJusEGoRMbhhwCg==",
      "license": "MIT",
      "dependencies": {
        "@babel/template": "^7.3.3",
        "@babel/types": "^7.3.3",
        "@types/babel__core": "^7.1.14",
        "@types/babel__traverse": "^7.0.6"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/babel-preset-current-node-syntax": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/babel-preset-current-node-syntax/-/babel-preset-current-node-syntax-1.0.1.tgz",
      "integrity": "sha512-M7LQ0bxarkxQoN+vz5aJPsLBn77n8QgTFmo8WK0/44auK2xlCXrYcUxHFxgU7qW5Yzw/CjmLRK2uJzaCd7LvqQ==",
      "license": "MIT",
      "dependencies": {
        "@babel/plugin-syntax-async-generators": "^7.8.4",
        "@babel/plugin-syntax-bigint": "^7.8.3",
        "@babel/plugin-syntax-class-properties": "^7.8.3",
        "@babel/plugin-syntax-import-meta": "^7.8.3",
        "@babel/plugin-syntax-json-strings": "^7.8.3",
        "@babel/plugin-syntax-logical-assignment-operators": "^7.8.3",
        "@babel/plugin-syntax-nullish-coalescing-operator": "^7.8.3",
        "@babel/plugin-syntax-numeric-separator": "^7.8.3",
        "@babel/plugin-syntax-object-rest-spread": "^7.8.3",
        "@babel/plugin-syntax-optional-catch-binding": "^7.8.3",
        "@babel/plugin-syntax-optional-chaining": "^7.8.3",
        "@babel/plugin-syntax-top-level-await": "^7.8.3"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0"
      }
    },
    "node_modules/babel-preset-jest": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/babel-preset-jest/-/babel-preset-jest-29.4.0.tgz",
      "integrity": "sha512-fUB9vZflUSM3dO/6M2TCAepTzvA4VkOvl67PjErcrQMGt9Eve7uazaeyCZ2th3UtI7ljpiBJES0F7A1vBRsLZA==",
      "license": "MIT",
      "dependencies": {
        "babel-plugin-jest-hoist": "^29.4.0",
        "babel-preset-current-node-syntax": "^1.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "peerDependencies": {
        "@babel/core": "^7.0.0"
      }
    },
    "node_modules/balanced-match": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/balanced-match/-/balanced-match-1.0.2.tgz",
      "integrity": "sha512-3oSeUO0TMV67hN1AmbXsK4yaqU7tjiHlbxRDZOpH0KW9+CeX4bRAaX0Anxt0tx2MrpRpWwQaPwIlISEJhYU5Pw==",
      "license": "MIT"
    },
    "node_modules/base64-js": {
      "version": "1.5.1",
      "resolved": "https://registry.npmjs.org/base64-js/-/base64-js-1.5.1.tgz",
      "integrity": "sha512-AKpaYlHn8t4SVbOHCy+b5+KKgvR4vrsD8vbvrbiQJps7fKDTkjkDry6ji0rUJjC0kzbNePLwzxq8iypo41qeWA==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "MIT"
    },
    "node_modules/base64url": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/base64url/-/base64url-3.0.1.tgz",
      "integrity": "sha512-ir1UPr3dkwexU7FdV8qBBbNDRUhMmIekYMFZfi+C/sLNnRESKPl23nB9b2pltqfOQNnGzsDdId90AEtG5tCx4A==",
      "license": "MIT",
      "engines": {
        "node": ">=6.0.0"
      }
    },
    "node_modules/bl": {
      "version": "5.1.0",
      "resolved": "https://registry.npmjs.org/bl/-/bl-5.1.0.tgz",
      "integrity": "sha512-tv1ZJHLfTDnXE6tMHv73YgSJaWR2AFuPwMntBe7XL/GBFHnT0CLnsHMogfk5+GzCDC5ZWarSCYaIGATZt9dNsQ==",
      "license": "MIT",
      "dependencies": {
        "buffer": "^6.0.3",
        "inherits": "^2.0.4",
        "readable-stream": "^3.4.0"
      }
    },
    "node_modules/blockstore-core": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/blockstore-core/-/blockstore-core-1.0.5.tgz",
      "integrity": "sha512-i/9CUMMvBALVbtSqUIuiWB3tk//a4Q2I2CEWiBuYNnhJvk/DWplXjLt8Sqc5VGkRVXVPSsEuH8fUtqJt5UFYcA==",
      "license": "(Apache-2.0 OR MIT)",
      "dependencies": {
        "err-code": "^3.0.1",
        "interface-blockstore": "^2.0.2",
        "interface-store": "^2.0.1",
        "it-all": "^1.0.4",
        "it-drain": "^1.0.4",
        "it-filter": "^1.0.2",
        "it-take": "^1.0.1",
        "multiformats": "^9.4.7"
      }
    },
    "node_modules/brace-expansion": {
      "version": "1.1.11",
      "resolved": "https://registry.npmjs.org/brace-expansion/-/brace-expansion-1.1.11.tgz",
      "integrity": "sha512-iCuPHDFgrHX7H2vEI/5xpz07zSHB00TpugqhmYtVmMO6518mCuRMoOYFldEBl0g187ufozdaHgWKcYFb61qGiA==",
      "license": "MIT",
      "dependencies": {
        "balanced-match": "^1.0.0",
        "concat-map": "0.0.1"
      }
    },
    "node_modules/braces": {
      "version": "3.0.2",
      "resolved": "https://registry.npmjs.org/braces/-/braces-3.0.2.tgz",
      "integrity": "sha512-b8um+L1RzM3WDSzvhm6gIz1yfTbBt6YTlcEKAvsmqCZZFw46z626lVj9j1yEPW33H5H+lBQpZMP1k8l+78Ha0A==",
      "license": "MIT",
      "dependencies": {
        "fill-range": "^7.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/browserslist": {
      "version": "4.21.5",
      "resolved": "https://registry.npmjs.org/browserslist/-/browserslist-4.21.5.tgz",
      "integrity": "sha512-tUkiguQGW7S3IhB7N+c2MV/HZPSCPAAiYBZXLsBhFB/PCy6ZKKsZrmBayHV9fdGV/ARIfJ14NkxKzRDjvp7L6w==",
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/browserslist"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/browserslist"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "caniuse-lite": "^1.0.30001449",
        "electron-to-chromium": "^1.4.284",
        "node-releases": "^2.0.8",
        "update-browserslist-db": "^1.0.10"
      },
      "bin": {
        "browserslist": "cli.js"
      },
      "engines": {
        "node": "^6 || ^7 || ^8 || ^9 || ^10 || ^11 || ^12 || >=13.7"
      }
    },
    "node_modules/bs-logger": {
      "version": "0.2.6",
      "resolved": "https://registry.npmjs.org/bs-logger/-/bs-logger-0.2.6.tgz",
      "integrity": "sha512-pd8DCoxmbgc7hyPKOvxtqNcjYoOsABPQdcCUjGp3d42VR2CX1ORhk2A87oqqu5R1kk+76nsxZupkmyd+MVtCog==",
      "license": "MIT",
      "dependencies": {
        "fast-json-stable-stringify": "2.x"
      },
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/bser": {
      "version": "2.1.1",
      "resolved": "https://registry.npmjs.org/bser/-/bser-2.1.1.tgz",
      "integrity": "sha512-gQxTNE/GAfIIrmHLUE3oJyp5FO6HRBfhjnw4/wMmA63ZGDJnWBmgY/lyQBpnDUkGmAhbSe39tx2d/iTOAfglwQ==",
      "license": "Apache-2.0",
      "dependencies": {
        "node-int64": "^0.4.0"
      }
    },
    "node_modules/buffer": {
      "version": "6.0.3",
      "resolved": "https://registry.npmjs.org/buffer/-/buffer-6.0.3.tgz",
      "integrity": "sha512-FTiCpNxtwiZZHEZbcbTIcZjERVICn9yq/pDFkTl95/AxzD1naBctN7YO68riM/gLSDY7sdrMby8hofADYuuqOA==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "base64-js": "^1.3.1",
        "ieee754": "^1.2.1"
      }
    },
    "node_modules/buffer-from": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/buffer-from/-/buffer-from-1.1.2.tgz",
      "integrity": "sha512-E+XQCRwSbaaiChtv6k6Dwgc+bx+Bs6vuKJHHl5kox/BaKbhiXzqQOwK4cO22yElGp2OCmjwVhT3HmxgyPGnJfQ==",
      "license": "MIT"
    },
    "node_modules/call-bind": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/call-bind/-/call-bind-1.0.2.tgz",
      "integrity": "sha512-7O+FbCihrB5WGbFYesctwmTKae6rOiIzmz1icreWJ+0aA7LJfuqhEso2T9ncpcFtzMQtzXf2QGGueWJGTYsqrA==",
      "license": "MIT",
      "dependencies": {
        "function-bind": "^1.1.1",
        "get-intrinsic": "^1.0.2"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/callsites": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/callsites/-/callsites-3.1.0.tgz",
      "integrity": "sha512-P8BjAsXvZS+VIDUI11hHCQEv74YT67YUi5JJFNWIqL235sBmjX4+qx9Muvls5ivyNENctx46xQLQ3aTuE7ssaQ==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/camel-case": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/camel-case/-/camel-case-4.1.2.tgz",
      "integrity": "sha512-gxGWBrTT1JuMx6R+o5PTXMmUnhnVzLQ9SNutD4YqKtI6ap897t3tKECYla6gCWEkplXnlNybEkZg9GEGxKFCgw==",
      "license": "MIT",
      "dependencies": {
        "pascal-case": "^3.1.2",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/camelcase": {
      "version": "6.3.0",
      "resolved": "https://registry.npmjs.org/camelcase/-/camelcase-6.3.0.tgz",
      "integrity": "sha512-Gmy6FhYlCY7uOElZUSbxo2UCDH8owEk996gkbrpsgGtrJLM3J7jGxl9Ic7Qwwj4ivOE5AWZWRMecDdF7hqGjFA==",
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/caniuse-lite": {
      "version": "1.0.30001450",
      "resolved": "https://registry.npmjs.org/caniuse-lite/-/caniuse-lite-1.0.30001450.tgz",
      "integrity": "sha512-qMBmvmQmFXaSxexkjjfMvD5rnDL0+m+dUMZKoDYsGG8iZN29RuYh9eRoMvKsT6uMAWlyUUGDEQGJJYjzCIO9ew==",
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/browserslist"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/caniuse-lite"
        }
      ],
      "license": "CC-BY-4.0"
    },
    "node_modules/capital-case": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/capital-case/-/capital-case-1.0.4.tgz",
      "integrity": "sha512-ds37W8CytHgwnhGGTi88pcPyR15qoNkOpYwmMMfnWqqWgESapLqvDx6huFjQ5vqWSn2Z06173XNA7LtMOeUh1A==",
      "license": "MIT",
      "dependencies": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3",
        "upper-case-first": "^2.0.2"
      }
    },
    "node_modules/chalk": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/chalk/-/chalk-4.1.2.tgz",
      "integrity": "sha512-oKnbhFyRIXpUuez8iBMmyEa4nbj4IOQyuhc/wy9kY7/WVPcwIO9VA668Pu8RkO7+0G76SLROeyw9CpQ061i4mA==",
      "license": "MIT",
      "dependencies": {
        "ansi-styles": "^4.1.0",
        "supports-color": "^7.1.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/chalk/chalk?sponsor=1"
      }
    },
    "node_modules/change-case": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/change-case/-/change-case-4.1.2.tgz",
      "integrity": "sha512-bSxY2ws9OtviILG1EiY5K7NNxkqg/JnRnFxLtKQ96JaviiIxi7djMrSd0ECT9AC+lttClmYwKw53BWpOMblo7A==",
      "license": "MIT",
      "dependencies": {
        "camel-case": "^4.1.2",
        "capital-case": "^1.0.4",
        "constant-case": "^3.0.4",
        "dot-case": "^3.0.4",
        "header-case": "^2.0.4",
        "no-case": "^3.0.4",
        "param-case": "^3.0.4",
        "pascal-case": "^3.1.2",
        "path-case": "^3.0.4",
        "sentence-case": "^3.0.4",
        "snake-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/char-regex": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/char-regex/-/char-regex-1.0.2.tgz",
      "integrity": "sha512-kWWXztvZ5SBQV+eRgKFeh8q5sLuZY2+8WUIzlxWVTg+oGwY14qylx1KbKzHd8P6ZYkAg0xyIDU9JMHhyJMZ1jw==",
      "license": "MIT",
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/ci-info": {
      "version": "3.7.1",
      "resolved": "https://registry.npmjs.org/ci-info/-/ci-info-3.7.1.tgz",
      "integrity": "sha512-4jYS4MOAaCIStSRwiuxc4B8MYhIe676yO1sYGzARnjXkWpmzZMMYxY6zu8WYWDhSuth5zhrQ1rhNSibyyvv4/w==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/sibiraj-s"
        }
      ],
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/cjs-module-lexer": {
      "version": "1.2.2",
      "resolved": "https://registry.npmjs.org/cjs-module-lexer/-/cjs-module-lexer-1.2.2.tgz",
      "integrity": "sha512-cOU9usZw8/dXIXKtwa8pM0OTJQuJkxMN6w30csNRUerHfeQ5R6U3kkU/FtJeIf3M202OHfY2U8ccInBG7/xogA==",
      "license": "MIT"
    },
    "node_modules/cli-cursor": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/cli-cursor/-/cli-cursor-4.0.0.tgz",
      "integrity": "sha512-VGtlMu3x/4DOtIUwEkRezxUZ2lBacNJCHash0N0WeZDBS+7Ux1dm3XWAgWYxLJFMMdOeXMHXorshEFhbMSGelg==",
      "license": "MIT",
      "dependencies": {
        "restore-cursor": "^4.0.0"
      },
      "engines": {
        "node": "^12.20.0 || ^14.13.1 || >=16.0.0"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/cli-spinners": {
      "version": "2.7.0",
      "resolved": "https://registry.npmjs.org/cli-spinners/-/cli-spinners-2.7.0.tgz",
      "integrity": "sha512-qu3pN8Y3qHNgE2AFweciB1IfMnmZ/fsNTEE+NOFjmGB2F/7rLhnhzppvpCnN4FovtP26k8lHyy9ptEbNwWFLzw==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/cliui": {
      "version": "8.0.1",
      "resolved": "https://registry.npmjs.org/cliui/-/cliui-8.0.1.tgz",
      "integrity": "sha512-BSeNnyus75C4//NQ9gQt1/csTXyo/8Sb+afLAkzAptFuMsod9HFokGNudZpi/oQV73hnVK+sR+5PVRMd+Dr7YQ==",
      "license": "ISC",
      "dependencies": {
        "string-width": "^4.2.0",
        "strip-ansi": "^6.0.1",
        "wrap-ansi": "^7.0.0"
      },
      "engines": {
        "node": ">=12"
      }
    },
    "node_modules/clone": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/clone/-/clone-1.0.4.tgz",
      "integrity": "sha512-JQHZ2QMW6l3aH/j6xCqQThY/9OH4D/9ls34cgkUBiEeocRTU04tHfKPBsUK1PqZCUQM7GiA0IIXJSuXHI64Kbg==",
      "license": "MIT",
      "engines": {
        "node": ">=0.8"
      }
    },
    "node_modules/co": {
      "version": "4.6.0",
      "resolved": "https://registry.npmjs.org/co/-/co-4.6.0.tgz",
      "integrity": "sha512-QVb0dM5HvG+uaxitm8wONl7jltx8dqhfU33DcqtOZcLSVIKSDDLDi7+0LbAKiyI8hD9u42m2YxXSkMGWThaecQ==",
      "license": "MIT",
      "engines": {
        "iojs": ">= 1.0.0",
        "node": ">= 0.12.0"
      }
    },
    "node_modules/collect-v8-coverage": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/collect-v8-coverage/-/collect-v8-coverage-1.0.1.tgz",
      "integrity": "sha512-iBPtljfCNcTKNAto0KEtDfZ3qzjJvqE3aTGZsbhjSBlorqpXJlaWWtPO35D+ZImoC3KWejX64o+yPGxhWSTzfg==",
      "license": "MIT"
    },
    "node_modules/color-convert": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/color-convert/-/color-convert-2.0.1.tgz",
      "integrity": "sha512-RRECPsj7iu/xb5oKYcsFHSppFNnsj/52OVTRKb4zP5onXwVF3zVmmToNcOfGC+CRDpfK/U584fMg38ZHCaElKQ==",
      "license": "MIT",
      "dependencies": {
        "color-name": "~1.1.4"
      },
      "engines": {
        "node": ">=7.0.0"
      }
    },
    "node_modules/color-name": {
      "version": "1.1.4",
      "resolved": "https://registry.npmjs.org/color-name/-/color-name-1.1.4.tgz",
      "integrity": "sha512-dOy+3AuW3a2wNbZHIuMZpTcgjGuLU/uBL/ubcZF9OXbDo8ff4O8yVp5Bf0efS8uEoYo5q4Fx7dY9OgQGXgAsQA==",
      "license": "MIT"
    },
    "node_modules/concat-map": {
      "version": "0.0.1",
      "resolved": "https://registry.npmjs.org/concat-map/-/concat-map-0.0.1.tgz",
      "integrity": "sha512-/Srv4dswyQNBfohGpz9o6Yb3Gz3SrUDqBH5rTuhGR7ahtlbYKnVxw2bCFMRljaA7EXHaXZ8wsHdodFvbkhKmqg==",
      "license": "MIT"
    },
    "node_modules/constant-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/constant-case/-/constant-case-3.0.4.tgz",
      "integrity": "sha512-I2hSBi7Vvs7BEuJDr5dDHfzb/Ruj3FyvFyh7KLilAjNQw3Be+xgqUBA2W6scVEcL0hL1dwPRtIqEPVUCKkSsyQ==",
      "license": "MIT",
      "dependencies": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3",
        "upper-case": "^2.0.2"
      }
    },
    "node_modules/convert-source-map": {
      "version": "1.9.0",
      "resolved": "https://registry.npmjs.org/convert-source-map/-/convert-source-map-1.9.0.tgz",
      "integrity": "sha512-ASFBup0Mz1uyiIjANan1jzLQami9z1PoYSZCiiYW2FczPbenXc45FZdBZLzOT+r6+iciuEModtmCti+hjaAk0A==",
      "license": "MIT"
    },
    "node_modules/create-require": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/create-require/-/create-require-1.1.1.tgz",
      "integrity": "sha512-dcKFX3jn0MpIaXjisoRvexIJVEKzaq7z2rZKxf+MSr9TkdmHmsU4m2lcLojrj/FHl8mk5VxMmYA+ftRkP/3oKQ==",
      "license": "MIT"
    },
    "node_modules/cross-spawn": {
      "version": "7.0.3",
      "resolved": "https://registry.npmjs.org/cross-spawn/-/cross-spawn-7.0.3.tgz",
      "integrity": "sha512-iRDPJKUPVEND7dHPO8rkbOnPpyDygcDFtWjpeWNCgy8WP2rXcxXL8TskReQl6OrB2G7+UJrags1q15Fudc7G6w==",
      "license": "MIT",
      "dependencies": {
        "path-key": "^3.1.0",
        "shebang-command": "^2.0.0",
        "which": "^2.0.1"
      },
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/dataloader": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/dataloader/-/dataloader-2.1.0.tgz",
      "integrity": "sha512-qTcEYLen3r7ojZNgVUaRggOI+KM7jrKxXeSHhogh/TWxYMeONEMqY+hmkobiYQozsGIyg9OYVzO4ZIfoB4I0pQ==",
      "license": "MIT"
    },
    "node_modules/debug": {
      "version": "4.3.4",
      "resolved": "https://registry.npmjs.org/debug/-/debug-4.3.4.tgz",
      "integrity": "sha512-PRWFHuSU3eDtQJPvnNY7Jcket1j0t5OuOsFzPPzsekD52Zl8qUfFIPEiswXqIvHWGVHOgX+7G/vCNNhehwxfkQ==",
      "license": "MIT",
      "dependencies": {
        "ms": "2.1.2"
      },
      "engines": {
        "node": ">=6.0"
      },
      "peerDependenciesMeta": {
        "supports-color": {
          "optional": true
        }
      }
    },
    "node_modules/dedent": {
      "version": "0.7.0",
      "resolved": "https://registry.npmjs.org/dedent/-/dedent-0.7.0.tgz",
      "integrity": "sha512-Q6fKUPqnAHAyhiUgFU7BUzLiv0kd8saH9al7tnu5Q/okj6dnupxyTgFIBjVzJATdfIAm9NAsvXNzjaKa+bxVyA==",
      "license": "MIT"
    },
    "node_modules/deepmerge": {
      "version": "4.3.0",
      "resolved": "https://registry.npmjs.org/deepmerge/-/deepmerge-4.3.0.tgz",
      "integrity": "sha512-z2wJZXrmeHdvYJp/Ux55wIjqo81G5Bp4c+oELTW+7ar6SogWHajt5a9gO3s3IDaGSAXjDk0vlQKN3rms8ab3og==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/defaults": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/defaults/-/defaults-1.0.4.tgz",
      "integrity": "sha512-eFuaLoy/Rxalv2kr+lqMlUnrDWV+3j4pljOIJgLIhI058IQfWJ7vXhyEIHu+HtC738klGALYxOKDO0bQP3tg8A==",
      "license": "MIT",
      "dependencies": {
        "clone": "^1.0.2"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/define-lazy-prop": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/define-lazy-prop/-/define-lazy-prop-2.0.0.tgz",
      "integrity": "sha512-Ds09qNh8yw3khSjiJjiUInaGX9xlqZDY7JVryGxdxV7NPeuqQfplOpQ66yJFZut3jLa5zOwkXw1g9EI2uKh4Og==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/detect-newline": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/detect-newline/-/detect-newline-3.1.0.tgz",
      "integrity": "sha512-TLz+x/vEXm/Y7P7wn1EJFNLxYpUD4TgMosxY6fAVJUnJMbupHBOncxyWUG9OpTaH9EBD7uFI5LfEgmMOc54DsA==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/diff": {
      "version": "4.0.2",
      "resolved": "https://registry.npmjs.org/diff/-/diff-4.0.2.tgz",
      "integrity": "sha512-58lmxKSA4BNyLz+HHMUzlOEpg09FV+ev6ZMe3vJihgdxzgcwZ8VoEEPmALCZG9LmqfVoNMMKpttIYTVG6uDY7A==",
      "license": "BSD-3-Clause",
      "engines": {
        "node": ">=0.3.1"
      }
    },
    "node_modules/diff-sequences": {
      "version": "29.3.1",
      "resolved": "https://registry.npmjs.org/diff-sequences/-/diff-sequences-29.3.1.tgz",
      "integrity": "sha512-hlM3QR272NXCi4pq+N4Kok4kOp6EsgOM3ZSpJI7Da3UAs+Ttsi8MRmB6trM/lhyzUxGfOgnpkHtgqm5Q/CTcfQ==",
      "license": "MIT",
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/dot-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/dot-case/-/dot-case-3.0.4.tgz",
      "integrity": "sha512-Kv5nKlh6yRrdrGvxeJ2e5y2eRUpkUosIW4A2AS38zwSz27zu7ufDwQPi5Jhs3XAlGNetl3bmnGhQsMtkKJnj3w==",
      "license": "MIT",
      "dependencies": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/electron-to-chromium": {
      "version": "1.4.284",
      "resolved": "https://registry.npmjs.org/electron-to-chromium/-/electron-to-chromium-1.4.284.tgz",
      "integrity": "sha512-M8WEXFuKXMYMVr45fo8mq0wUrrJHheiKZf6BArTKk9ZBYCKJEOU5H8cdWgDT+qCVZf7Na4lVUaZsA+h6uA9+PA==",
      "license": "ISC"
    },
    "node_modules/emittery": {
      "version": "0.13.1",
      "resolved": "https://registry.npmjs.org/emittery/-/emittery-0.13.1.tgz",
      "integrity": "sha512-DeWwawk6r5yR9jFgnDKYt4sLS0LmHJJi3ZOnb5/JdbYwj3nW+FxQnHIjhBKz8YLC7oRNPVM9NQ47I3CVx34eqQ==",
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/sindresorhus/emittery?sponsor=1"
      }
    },
    "node_modules/emoji-regex": {
      "version": "8.0.0",
      "resolved": "https://registry.npmjs.org/emoji-regex/-/emoji-regex-8.0.0.tgz",
      "integrity": "sha512-MSjYzcWNOA0ewAHpz0MxpYFvwg6yjy1NG3xteoqz644VCo/RPgnr1/GGt+ic3iJTzQ8Eu3TdM14SawnVUmGE6A==",
      "license": "MIT"
    },
    "node_modules/enquirer": {
      "version": "2.3.6",
      "resolved": "https://registry.npmjs.org/enquirer/-/enquirer-2.3.6.tgz",
      "integrity": "sha512-yjNnPr315/FjS4zIsUxYguYUPP2e1NK4d7E7ZOLiyYCcbFBiTMyID+2wvm2w6+pZ/odMA7cRkjhsPbltwBOrLg==",
      "license": "MIT",
      "dependencies": {
        "ansi-colors": "^4.1.1"
      },
      "engines": {
        "node": ">=8.6"
      }
    },
    "node_modules/err-code": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/err-code/-/err-code-3.0.1.tgz",
      "integrity": "sha512-GiaH0KJUewYok+eeY05IIgjtAe4Yltygk9Wqp1V5yVWLdhf0hYZchRjNIT9bb0mSwRcIusT3cx7PJUf3zEIfUA==",
      "license": "MIT"
    },
    "node_modules/error-ex": {
      "version": "1.3.2",
      "resolved": "https://registry.npmjs.org/error-ex/-/error-ex-1.3.2.tgz",
      "integrity": "sha512-7dFHNmqeFSEt2ZBsCriorKnn3Z2pj+fd9kmI6QoWw4//DL+icEBfc0U7qJCisqrTsKTjw4fNFy2pW9OqStD84g==",
      "license": "MIT",
      "dependencies": {
        "is-arrayish": "^0.2.1"
      }
    },
    "node_modules/escalade": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/escalade/-/escalade-3.1.1.tgz",
      "integrity": "sha512-k0er2gUkLf8O0zKJiAhmkTnJlTvINGv7ygDNPbeIsX/TJjGJZHuh9B2UxbsaEkmlEo9MfhrSzmhIlhRlI2GXnw==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/escape-string-regexp": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/escape-string-regexp/-/escape-string-regexp-2.0.0.tgz",
      "integrity": "sha512-UpzcLCXolUWcNu5HtVMHYdXJjArjsF9C0aNnquZYY4uW/Vu0miy5YoWvbV345HauVvcAUnpRuhMMcqTcGOY2+w==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/esprima": {
      "version": "4.0.1",
      "resolved": "https://registry.npmjs.org/esprima/-/esprima-4.0.1.tgz",
      "integrity": "sha512-eGuFFw7Upda+g4p+QHvnW0RyTX/SVeJBDM/gCtMARO0cLuT2HcEKnTPvhjV6aGeqrCB/sbNop0Kszm0jsaWU4A==",
      "license": "BSD-2-Clause",
      "bin": {
        "esparse": "bin/esparse.js",
        "esvalidate": "bin/esvalidate.js"
      },
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/execa": {
      "version": "5.1.1",
      "resolved": "https://registry.npmjs.org/execa/-/execa-5.1.1.tgz",
      "integrity": "sha512-8uSpZZocAZRBAPIEINJj3Lo9HyGitllczc27Eh5YYojjMFMn8yHMDMaUHE2Jqfq05D/wucwI4JGURyXt1vchyg==",
      "license": "MIT",
      "dependencies": {
        "cross-spawn": "^7.0.3",
        "get-stream": "^6.0.0",
        "human-signals": "^2.1.0",
        "is-stream": "^2.0.0",
        "merge-stream": "^2.0.0",
        "npm-run-path": "^4.0.1",
        "onetime": "^5.1.2",
        "signal-exit": "^3.0.3",
        "strip-final-newline": "^2.0.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sindresorhus/execa?sponsor=1"
      }
    },
    "node_modules/exit": {
      "version": "0.1.2",
      "resolved": "https://registry.npmjs.org/exit/-/exit-0.1.2.tgz",
      "integrity": "sha512-Zk/eNKV2zbjpKzrsQ+n1G6poVbErQxJ0LBOJXaKZ1EViLzH+hrLu9cdXI4zw9dBQJslwBEpbQ2P1oS7nDxs6jQ==",
      "engines": {
        "node": ">= 0.8.0"
      }
    },
    "node_modules/expect": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/expect/-/expect-29.4.1.tgz",
      "integrity": "sha512-OKrGESHOaMxK3b6zxIq9SOW8kEXztKff/Dvg88j4xIJxur1hspEbedVkR3GpHe5LO+WB2Qw7OWN0RMTdp6as5A==",
      "license": "MIT",
      "dependencies": {
        "@jest/expect-utils": "^29.4.1",
        "jest-get-type": "^29.2.0",
        "jest-matcher-utils": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-util": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/fast-json-stable-stringify": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/fast-json-stable-stringify/-/fast-json-stable-stringify-2.1.0.tgz",
      "integrity": "sha512-lhd/wF+Lk98HZoTCtlVraHtfh5XYijIjalXck7saUtuanSDyLMxnHhSXEDJqHxD7msR8D0uCmqlkwjCV8xvwHw==",
      "license": "MIT"
    },
    "node_modules/fb-watchman": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/fb-watchman/-/fb-watchman-2.0.2.tgz",
      "integrity": "sha512-p5161BqbuCaSnB8jIbzQHOlpgsPmK5rJVDfDKO91Axs5NC1uu3HRQm6wt9cd9/+GtQQIO53JdGXXoyDpTAsgYA==",
      "license": "Apache-2.0",
      "dependencies": {
        "bser": "2.1.1"
      }
    },
    "node_modules/fill-range": {
      "version": "7.0.1",
      "resolved": "https://registry.npmjs.org/fill-range/-/fill-range-7.0.1.tgz",
      "integrity": "sha512-qOo9F+dMUmC2Lcb4BbVvnKJxTPjCm+RRpe4gDuGrzkL7mEVl/djYSu2OdQ2Pa302N4oqkSg9ir6jaLWJ2USVpQ==",
      "license": "MIT",
      "dependencies": {
        "to-regex-range": "^5.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/find-up": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/find-up/-/find-up-4.1.0.tgz",
      "integrity": "sha512-PpOwAdQ/YlXQ2vj8a3h8IipDuYRi3wceVQQGYWxNINccq40Anw7BlsEXCMbt1Zt+OLA6Fq9suIpIWD0OsnISlw==",
      "license": "MIT",
      "dependencies": {
        "locate-path": "^5.0.0",
        "path-exists": "^4.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/follow-redirects": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.15.2.tgz",
      "integrity": "sha512-VQLG33o04KaQ8uYi2tVNbdrWp1QWxNNea+nmIB4EVM28v0hmP17z7aG1+wAkNzVq4KeXTq3221ye5qTJP91JwA==",
      "funding": [
        {
          "type": "individual",
          "url": "https://github.com/sponsors/RubenVerborgh"
        }
      ],
      "license": "MIT",
      "engines": {
        "node": ">=4.0"
      },
      "peerDependenciesMeta": {
        "debug": {
          "optional": true
        }
      }
    },
    "node_modules/fp-ts": {
      "version": "2.13.1",
      "resolved": "https://registry.npmjs.org/fp-ts/-/fp-ts-2.13.1.tgz",
      "integrity": "sha512-0eu5ULPS2c/jsa1lGFneEFFEdTbembJv8e4QKXeVJ3lm/5hyve06dlKZrpxmMwJt6rYen7sxmHHK2CLaXvWuWQ==",
      "license": "MIT"
    },
    "node_modules/fs.realpath": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/fs.realpath/-/fs.realpath-1.0.0.tgz",
      "integrity": "sha512-OO0pH2lK6a0hZnAdau5ItzHPI6pUlvI7jMVnxUQRtw4owF2wk8lOSabtGDCTP4Ggrg2MbGnWO9X8K1t4+fGMDw==",
      "license": "ISC"
    },
    "node_modules/function-bind": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/function-bind/-/function-bind-1.1.1.tgz",
      "integrity": "sha512-yIovAzMX49sF8Yl58fSCWJ5svSLuaibPxXQJFLmBObTuCr0Mf1KiPopGM9NiFjiYBCbfaa2Fh6breQ6ANVTI0A==",
      "license": "MIT"
    },
    "node_modules/gensync": {
      "version": "1.0.0-beta.2",
      "resolved": "https://registry.npmjs.org/gensync/-/gensync-1.0.0-beta.2.tgz",
      "integrity": "sha512-3hN7NaskYvMDLQY55gnW3NQ+mesEAepTqlg+VEbj7zzqEMBVNhzcGYYeqFo/TlYz6eQiFcp1HcsCZO+nGgS8zg==",
      "license": "MIT",
      "engines": {
        "node": ">=6.9.0"
      }
    },
    "node_modules/get-caller-file": {
      "version": "2.0.5",
      "resolved": "https://registry.npmjs.org/get-caller-file/-/get-caller-file-2.0.5.tgz",
      "integrity": "sha512-DyFP3BM/3YHTQOCUL/w0OZHR0lpKeGrxotcHWcqNEdnltqFwXVfhEBQ94eIo34AfQpo0rGki4cyIiftY06h2Fg==",
      "license": "ISC",
      "engines": {
        "node": "6.* || 8.* || >= 10.*"
      }
    },
    "node_modules/get-intrinsic": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/get-intrinsic/-/get-intrinsic-1.2.0.tgz",
      "integrity": "sha512-L049y6nFOuom5wGyRc3/gdTLO94dySVKRACj1RmJZBQXlbTMhtNIgkWkUHq+jYmZvKf14EW1EoJnnjbmoHij0Q==",
      "license": "MIT",
      "dependencies": {
        "function-bind": "^1.1.1",
        "has": "^1.0.3",
        "has-symbols": "^1.0.3"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/get-package-type": {
      "version": "0.1.0",
      "resolved": "https://registry.npmjs.org/get-package-type/-/get-package-type-0.1.0.tgz",
      "integrity": "sha512-pjzuKtY64GYfWizNAJ0fr9VqttZkNiK2iS430LtIHzjBEr6bX8Am2zm4sW4Ro5wjWW5cAlRL1qAMTcXbjNAO2Q==",
      "license": "MIT",
      "engines": {
        "node": ">=8.0.0"
      }
    },
    "node_modules/get-stream": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/get-stream/-/get-stream-6.0.1.tgz",
      "integrity": "sha512-ts6Wi+2j3jQjqi70w5AlN8DFnkSwC+MqmxEzdEALB2qXZYV3X/b1CTfgPLGJNMeAWxdPfU8FO1ms3NUfaHCPYg==",
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/glob": {
      "version": "7.2.3",
      "resolved": "https://registry.npmjs.org/glob/-/glob-7.2.3.tgz",
      "integrity": "sha512-nFR0zLpU2YCaRxwoCJvL6UvCH2JFyFVIvwTLsIf21AuHlMskA1hhTdk+LlYJtOlYt9v6dvszD2BGRqBL+iQK9Q==",
      "license": "ISC",
      "dependencies": {
        "fs.realpath": "^1.0.0",
        "inflight": "^1.0.4",
        "inherits": "2",
        "minimatch": "^3.1.1",
        "once": "^1.3.0",
        "path-is-absolute": "^1.0.0"
      },
      "engines": {
        "node": "*"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/globals": {
      "version": "11.12.0",
      "resolved": "https://registry.npmjs.org/globals/-/globals-11.12.0.tgz",
      "integrity": "sha512-WOBp/EEGUiIsJSp7wcv/y6MO+lV9UoncWqxuFfm8eBwzWNgyfBd6Gz+IeKQ9jCmyhoH99g15M3T+QaVHFjizVA==",
      "license": "MIT",
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/graceful-fs": {
      "version": "4.2.10",
      "resolved": "https://registry.npmjs.org/graceful-fs/-/graceful-fs-4.2.10.tgz",
      "integrity": "sha512-9ByhssR2fPVsNZj478qUUbKfmL0+t5BDVyjShtyZZLiK7ZDAArFFfopyOTj0M05wE2tJPisA4iTnnXl2YoPvOA==",
      "license": "ISC"
    },
    "node_modules/hamt-sharding": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/hamt-sharding/-/hamt-sharding-2.0.1.tgz",
      "integrity": "sha512-vnjrmdXG9dDs1m/H4iJ6z0JFI2NtgsW5keRkTcM85NGak69Mkf5PHUqBz+Xs0T4sg0ppvj9O5EGAJo40FTxmmA==",
      "license": "MIT",
      "dependencies": {
        "sparse-array": "^1.3.1",
        "uint8arrays": "^3.0.0"
      },
      "engines": {
        "node": ">=10.0.0",
        "npm": ">=6.0.0"
      }
    },
    "node_modules/has": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/has/-/has-1.0.3.tgz",
      "integrity": "sha512-f2dvO0VU6Oej7RkWJGrehjbzMAjFp5/VKPp5tTpWIV4JHHZK1/BxbFRtf/siA2SWTe09caDmVtYYzWEIbBS4zw==",
      "license": "MIT",
      "dependencies": {
        "function-bind": "^1.1.1"
      },
      "engines": {
        "node": ">= 0.4.0"
      }
    },
    "node_modules/has-flag": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/has-flag/-/has-flag-4.0.0.tgz",
      "integrity": "sha512-EykJT/Q1KjTWctppgIAgfSO0tKVuZUjhgMr17kqTumMl6Afv3EISleU7qZUzoXDFTAHTDC4NOoG/ZxU3EvlMPQ==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/has-symbols": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/has-symbols/-/has-symbols-1.0.3.tgz",
      "integrity": "sha512-l3LCuF6MgDNwTDKkdYGEihYjt5pRPbEg46rtlmnSPlUbgmB8LOIrKJbYYFBSbnPaJexMKtiPO8hmeRjRz2Td+A==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/header-case": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/header-case/-/header-case-2.0.4.tgz",
      "integrity": "sha512-H/vuk5TEEVZwrR0lp2zed9OCo1uAILMlx0JEMgC26rzyJJ3N1v6XkwHHXJQdR2doSjcGPM6OKPYoJgf0plJ11Q==",
      "license": "MIT",
      "dependencies": {
        "capital-case": "^1.0.4",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/html-escaper": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/html-escaper/-/html-escaper-2.0.2.tgz",
      "integrity": "sha512-H2iMtd0I4Mt5eYiapRdIDjp+XzelXQ0tFE4JS7YFwFevXXMmOp9myNrUvCg0D6ws8iqkRPBfKHgbwig1SmlLfg==",
      "license": "MIT"
    },
    "node_modules/human-signals": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/human-signals/-/human-signals-2.1.0.tgz",
      "integrity": "sha512-B4FFZ6q/T2jhhksgkbEW3HBvWIfDW85snkQgawt07S7J5QXTk6BkNV+0yAeZrM5QpMAdYlocGoljn0sJ/WQkFw==",
      "license": "Apache-2.0",
      "engines": {
        "node": ">=10.17.0"
      }
    },
    "node_modules/ieee754": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/ieee754/-/ieee754-1.2.1.tgz",
      "integrity": "sha512-dcyqhDvX1C46lXZcVqCpK+FtMRQVdIMN6/Df5js2zouUsqG7I6sFxitIC+7KYK29KdXOLHdu9zL4sFnoVQnqaA==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "BSD-3-Clause"
    },
    "node_modules/import-local": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/import-local/-/import-local-3.1.0.tgz",
      "integrity": "sha512-ASB07uLtnDs1o6EHjKpX34BKYDSqnFerfTOJL2HvMqF70LnxpjkzDB8J44oT9pu4AMPkQwf8jl6szgvNd2tRIg==",
      "license": "MIT",
      "dependencies": {
        "pkg-dir": "^4.2.0",
        "resolve-cwd": "^3.0.0"
      },
      "bin": {
        "import-local-fixture": "fixtures/cli.js"
      },
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/imurmurhash": {
      "version": "0.1.4",
      "resolved": "https://registry.npmjs.org/imurmurhash/-/imurmurhash-0.1.4.tgz",
      "integrity": "sha512-JmXMZ6wuvDmLiHEml9ykzqO6lwFbof0GG4IkcGaENdCRDDmMVnny7s5HsIgHCbaq0w2MyPhDqkhTUgS2LU2PHA==",
      "license": "MIT",
      "engines": {
        "node": ">=0.8.19"
      }
    },
    "node_modules/inflight": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/inflight/-/inflight-1.0.6.tgz",
      "integrity": "sha512-k92I/b08q4wvFscXCLvqfsHCrjrF7yiXsQuIVvVE7N82W3+aqpzuUdBbfhWcy/FZR3/4IgflMgKLOsvPDrGCJA==",
      "license": "ISC",
      "dependencies": {
        "once": "^1.3.0",
        "wrappy": "1"
      }
    },
    "node_modules/inherits": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/inherits/-/inherits-2.0.4.tgz",
      "integrity": "sha512-k/vGaX4/Yla3WzyMCvTQOXYeIHvqOKtnqBduzTHpzpQZzAskKMhZ2K+EnBiSM9zGSoIFeMpXKxa4dYeZIQqewQ==",
      "license": "ISC"
    },
    "node_modules/interface-blockstore": {
      "version": "2.0.3",
      "resolved": "https://registry.npmjs.org/interface-blockstore/-/interface-blockstore-2.0.3.tgz",
      "integrity": "sha512-OwVUnlNcx7H5HloK0Myv6c/C1q9cNG11HX6afdeU6q6kbuNj8jKCwVnmJHhC94LZaJ+9hvVOk4IUstb3Esg81w==",
      "license": "(Apache-2.0 OR MIT)",
      "dependencies": {
        "interface-store": "^2.0.2",
        "multiformats": "^9.0.4"
      }
    },
    "node_modules/interface-store": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/interface-store/-/interface-store-2.0.2.tgz",
      "integrity": "sha512-rScRlhDcz6k199EkHqT8NpM87ebN89ICOzILoBHgaG36/WX50N32BnU/kpZgCGPLhARRAWUUX5/cyaIjt7Kipg==",
      "license": "(Apache-2.0 OR MIT)"
    },
    "node_modules/io-ts": {
      "version": "2.2.20",
      "resolved": "https://registry.npmjs.org/io-ts/-/io-ts-2.2.20.tgz",
      "integrity": "sha512-Rq2BsYmtwS5vVttie4rqrOCIfHCS9TgpRLFpKQCM1wZBBRY9nWVGmEvm2FnDbSE2un1UE39DvFpTR5UL47YDcA==",
      "license": "MIT",
      "peerDependencies": {
        "fp-ts": "^2.5.0"
      }
    },
    "node_modules/io-ts-reporters": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/io-ts-reporters/-/io-ts-reporters-2.0.1.tgz",
      "integrity": "sha512-RVpLstYBsmTGgCW9wJ5KVyN/eRnRUDp87Flt4D1O3aJ7oAnd8csq8aXuu7ZeNK8qEDKmjUl9oUuzfwikaNAMKQ==",
      "license": "MIT",
      "dependencies": {
        "@scarf/scarf": "^1.1.1"
      },
      "peerDependencies": {
        "fp-ts": "^2.10.5",
        "io-ts": "^2.2.16"
      }
    },
    "node_modules/ipfs-unixfs": {
      "version": "6.0.9",
      "resolved": "https://registry.npmjs.org/ipfs-unixfs/-/ipfs-unixfs-6.0.9.tgz",
      "integrity": "sha512-0DQ7p0/9dRB6XCb0mVCTli33GzIzSVx5udpJuVM47tGcD+W+Bl4LsnoLswd3ggNnNEakMv1FdoFITiEnchXDqQ==",
      "license": "Apache-2.0 OR MIT",
      "dependencies": {
        "err-code": "^3.0.1",
        "protobufjs": "^6.10.2"
      },
      "engines": {
        "node": ">=16.0.0",
        "npm": ">=7.0.0"
      }
    },
    "node_modules/ipfs-unixfs-importer": {
      "version": "9.0.10",
      "resolved": "https://registry.npmjs.org/ipfs-unixfs-importer/-/ipfs-unixfs-importer-9.0.10.tgz",
      "integrity": "sha512-W+tQTVcSmXtFh7FWYWwPBGXJ1xDgREbIyI1E5JzDcimZLIyT5gGMfxR3oKPxxWj+GKMpP5ilvMQrbsPzWcm3Fw==",
      "license": "Apache-2.0 OR MIT",
      "dependencies": {
        "@ipld/dag-pb": "^2.0.2",
        "@multiformats/murmur3": "^1.0.3",
        "bl": "^5.0.0",
        "err-code": "^3.0.1",
        "hamt-sharding": "^2.0.0",
        "interface-blockstore": "^2.0.3",
        "ipfs-unixfs": "^6.0.0",
        "it-all": "^1.0.5",
        "it-batch": "^1.0.8",
        "it-first": "^1.0.6",
        "it-parallel-batch": "^1.0.9",
        "merge-options": "^3.0.4",
        "multiformats": "^9.4.2",
        "rabin-wasm": "^0.1.4",
        "uint8arrays": "^3.0.0"
      },
      "engines": {
        "node": ">=16.0.0",
        "npm": ">=7.0.0"
      }
    },
    "node_modules/is-arrayish": {
      "version": "0.2.1",
      "resolved": "https://registry.npmjs.org/is-arrayish/-/is-arrayish-0.2.1.tgz",
      "integrity": "sha512-zz06S8t0ozoDXMG+ube26zeCTNXcKIPJZJi8hBrF4idCLms4CG9QtK7qBl1boi5ODzFpjswb5JPmHCbMpjaYzg==",
      "license": "MIT"
    },
    "node_modules/is-core-module": {
      "version": "2.11.0",
      "resolved": "https://registry.npmjs.org/is-core-module/-/is-core-module-2.11.0.tgz",
      "integrity": "sha512-RRjxlvLDkD1YJwDbroBHMb+cukurkDWNyHx7D3oNB5x9rb5ogcksMC5wHCadcXoo67gVr/+3GFySh3134zi6rw==",
      "license": "MIT",
      "dependencies": {
        "has": "^1.0.3"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/is-docker": {
      "version": "2.2.1",
      "resolved": "https://registry.npmjs.org/is-docker/-/is-docker-2.2.1.tgz",
      "integrity": "sha512-F+i2BKsFrH66iaUFc0woD8sLy8getkwTwtOBjvs56Cx4CgJDeKQeqfz8wAYiSb8JOprWhHH5p77PbmYCvvUuXQ==",
      "license": "MIT",
      "bin": {
        "is-docker": "cli.js"
      },
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/is-fullwidth-code-point": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/is-fullwidth-code-point/-/is-fullwidth-code-point-3.0.0.tgz",
      "integrity": "sha512-zymm5+u+sCsSWyD9qNaejV3DFvhCKclKdizYaJUuHA83RLjb7nSuGnddCHGv0hk+KY7BMAlsWeK4Ueg6EV6XQg==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/is-generator-fn": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/is-generator-fn/-/is-generator-fn-2.1.0.tgz",
      "integrity": "sha512-cTIB4yPYL/Grw0EaSzASzg6bBy9gqCofvWN8okThAYIxKJZC+udlRAmGbM0XLeniEJSs8uEgHPGuHSe1XsOLSQ==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/is-interactive": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/is-interactive/-/is-interactive-2.0.0.tgz",
      "integrity": "sha512-qP1vozQRI+BMOPcjFzrjXuQvdak2pHNUMZoeG2eRbiSqyvbEf/wQtEOTOX1guk6E3t36RkaqiSt8A/6YElNxLQ==",
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/is-number": {
      "version": "7.0.0",
      "resolved": "https://registry.npmjs.org/is-number/-/is-number-7.0.0.tgz",
      "integrity": "sha512-41Cifkg6e8TylSpdtTpeLVMqvSBEVzTttHvERD741+pnZ8ANv0004MRL43QKPDlK9cGvNp6NZWZUBlbGXYxxng==",
      "license": "MIT",
      "engines": {
        "node": ">=0.12.0"
      }
    },
    "node_modules/is-plain-obj": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/is-plain-obj/-/is-plain-obj-2.1.0.tgz",
      "integrity": "sha512-YWnfyRwxL/+SsrWYfOpUtz5b3YD+nyfkHvjbcanzk8zgyO4ASD67uVMRt8k5bM4lLMDnXfriRhOpemw+NfT1eA==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/is-stream": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/is-stream/-/is-stream-2.0.1.tgz",
      "integrity": "sha512-hFoiJiTl63nn+kstHGBtewWSKnQLpyb155KHheA1l39uvtO9nWIop1p3udqPcUd/xbF1VLMO4n7OI6p7RbngDg==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/is-unicode-supported": {
      "version": "1.3.0",
      "resolved": "https://registry.npmjs.org/is-unicode-supported/-/is-unicode-supported-1.3.0.tgz",
      "integrity": "sha512-43r2mRvz+8JRIKnWJ+3j8JtjRKZ6GmjzfaE/qiBJnikNnYv/6bagRJ1kUhNk8R5EX/GkobD+r+sfxCPJsiKBLQ==",
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/is-wsl": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/is-wsl/-/is-wsl-2.2.0.tgz",
      "integrity": "sha512-fKzAra0rGJUUBwGBgNkHZuToZcn+TtXHpeCgmkMJMMYx1sQDYaCSyjJBSCa2nH1DGm7s3n1oBnohoVTBaN7Lww==",
      "license": "MIT",
      "dependencies": {
        "is-docker": "^2.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/isexe": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/isexe/-/isexe-2.0.0.tgz",
      "integrity": "sha512-RHxMLp9lnKHGHRng9QFhRCMbYAcVpn69smSGcq3f36xjgVVWThj4qqLbTLlq7Ssj8B+fIQ1EuCEGI2lKsyQeIw==",
      "license": "ISC"
    },
    "node_modules/isomorphic-fetch": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/isomorphic-fetch/-/isomorphic-fetch-3.0.0.tgz",
      "integrity": "sha512-qvUtwJ3j6qwsF3jLxkZ72qCgjMysPzDfeV240JHiGZsANBYd+EEuu35v7dfrJ9Up0Ak07D7GGSkGhCHTqg/5wA==",
      "dependencies": {
        "node-fetch": "^2.6.1",
        "whatwg-fetch": "^3.4.1"
      }
    },
    "node_modules/istanbul-lib-coverage": {
      "version": "3.2.0",
      "resolved": "https://registry.npmjs.org/istanbul-lib-coverage/-/istanbul-lib-coverage-3.2.0.tgz",
      "integrity": "sha512-eOeJ5BHCmHYvQK7xt9GkdHuzuCGS1Y6g9Gvnx3Ym33fz/HpLRYxiS0wHNr+m/MBC8B647Xt608vCDEvhl9c6Mw==",
      "license": "BSD-3-Clause",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/istanbul-lib-instrument": {
      "version": "5.2.1",
      "resolved": "https://registry.npmjs.org/istanbul-lib-instrument/-/istanbul-lib-instrument-5.2.1.tgz",
      "integrity": "sha512-pzqtp31nLv/XFOzXGuvhCb8qhjmTVo5vjVk19XE4CRlSWz0KoeJ3bw9XsA7nOp9YBf4qHjwBxkDzKcME/J29Yg==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "@babel/core": "^7.12.3",
        "@babel/parser": "^7.14.7",
        "@istanbuljs/schema": "^0.1.2",
        "istanbul-lib-coverage": "^3.2.0",
        "semver": "^6.3.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/istanbul-lib-report": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/istanbul-lib-report/-/istanbul-lib-report-3.0.0.tgz",
      "integrity": "sha512-wcdi+uAKzfiGT2abPpKZ0hSU1rGQjUQnLvtY5MpQ7QCTahD3VODhcu4wcfY1YtkGaDD5yuydOLINXsfbus9ROw==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "istanbul-lib-coverage": "^3.0.0",
        "make-dir": "^3.0.0",
        "supports-color": "^7.1.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/istanbul-lib-source-maps": {
      "version": "4.0.1",
      "resolved": "https://registry.npmjs.org/istanbul-lib-source-maps/-/istanbul-lib-source-maps-4.0.1.tgz",
      "integrity": "sha512-n3s8EwkdFIJCG3BPKBYvskgXGoy88ARzvegkitk60NxRdwltLOTaH7CUiMRXvwYorl0Q712iEjcWB+fK/MrWVw==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "debug": "^4.1.1",
        "istanbul-lib-coverage": "^3.0.0",
        "source-map": "^0.6.1"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/istanbul-reports": {
      "version": "3.1.5",
      "resolved": "https://registry.npmjs.org/istanbul-reports/-/istanbul-reports-3.1.5.tgz",
      "integrity": "sha512-nUsEMa9pBt/NOHqbcbeJEgqIlY/K7rVWUX6Lql2orY5e9roQOthbR3vtY4zzf2orPELg80fnxxk9zUyPlgwD1w==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "html-escaper": "^2.0.0",
        "istanbul-lib-report": "^3.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/it-all": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/it-all/-/it-all-1.0.6.tgz",
      "integrity": "sha512-3cmCc6Heqe3uWi3CVM/k51fa/XbMFpQVzFoDsV0IZNHSQDyAXl3c4MjHkFX5kF3922OGj7Myv1nSEUgRtcuM1A==",
      "license": "ISC"
    },
    "node_modules/it-batch": {
      "version": "1.0.9",
      "resolved": "https://registry.npmjs.org/it-batch/-/it-batch-1.0.9.tgz",
      "integrity": "sha512-7Q7HXewMhNFltTsAMdSz6luNhyhkhEtGGbYek/8Xb/GiqYMtwUmopE1ocPSiJKKp3rM4Dt045sNFoUu+KZGNyA==",
      "license": "ISC"
    },
    "node_modules/it-drain": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/it-drain/-/it-drain-1.0.5.tgz",
      "integrity": "sha512-r/GjkiW1bZswC04TNmUnLxa6uovme7KKwPhc+cb1hHU65E3AByypHH6Pm91WHuvqfFsm+9ws0kPtDBV3/8vmIg==",
      "license": "ISC"
    },
    "node_modules/it-filter": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/it-filter/-/it-filter-1.0.3.tgz",
      "integrity": "sha512-EI3HpzUrKjTH01miLHWmhNWy3Xpbx4OXMXltgrNprL5lDpF3giVpHIouFpr5l+evXw6aOfxhnt01BIB+4VQA+w==",
      "license": "ISC"
    },
    "node_modules/it-first": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/it-first/-/it-first-1.0.7.tgz",
      "integrity": "sha512-nvJKZoBpZD/6Rtde6FXqwDqDZGF1sCADmr2Zoc0hZsIvnE449gRFnGctxDf09Bzc/FWnHXAdaHVIetY6lrE0/g==",
      "license": "ISC"
    },
    "node_modules/it-parallel-batch": {
      "version": "1.0.11",
      "resolved": "https://registry.npmjs.org/it-parallel-batch/-/it-parallel-batch-1.0.11.tgz",
      "integrity": "sha512-UWsWHv/kqBpMRmyZJzlmZeoAMA0F3SZr08FBdbhtbe+MtoEBgr/ZUAKrnenhXCBrsopy76QjRH2K/V8kNdupbQ==",
      "license": "ISC",
      "dependencies": {
        "it-batch": "^1.0.9"
      }
    },
    "node_modules/it-take": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/it-take/-/it-take-1.0.2.tgz",
      "integrity": "sha512-u7I6qhhxH7pSevcYNaMECtkvZW365ARqAIt9K+xjdK1B2WUDEjQSfETkOCT8bxFq/59LqrN3cMLUtTgmDBaygw==",
      "license": "ISC"
    },
    "node_modules/jest": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest/-/jest-29.4.1.tgz",
      "integrity": "sha512-cknimw7gAXPDOmj0QqztlxVtBVCw2lYY9CeIE5N6kD+kET1H4H79HSNISJmijb1HF+qk+G+ploJgiDi5k/fRlg==",
      "license": "MIT",
      "dependencies": {
        "@jest/core": "^29.4.1",
        "@jest/types": "^29.4.1",
        "import-local": "^3.0.2",
        "jest-cli": "^29.4.1"
      },
      "bin": {
        "jest": "bin/jest.js"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "peerDependencies": {
        "node-notifier": "^8.0.1 || ^9.0.0 || ^10.0.0"
      },
      "peerDependenciesMeta": {
        "node-notifier": {
          "optional": true
        }
      }
    },
    "node_modules/jest-changed-files": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/jest-changed-files/-/jest-changed-files-29.4.0.tgz",
      "integrity": "sha512-rnI1oPxgFghoz32Y8eZsGJMjW54UlqT17ycQeCEktcxxwqqKdlj9afl8LNeO0Pbu+h2JQHThQP0BzS67eTRx4w==",
      "license": "MIT",
      "dependencies": {
        "execa": "^5.0.0",
        "p-limit": "^3.1.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-circus": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-circus/-/jest-circus-29.4.1.tgz",
      "integrity": "sha512-v02NuL5crMNY4CGPHBEflLzl4v91NFb85a+dH9a1pUNx6Xjggrd8l9pPy4LZ1VYNRXlb+f65+7O/MSIbLir6pA==",
      "license": "MIT",
      "dependencies": {
        "@jest/environment": "^29.4.1",
        "@jest/expect": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "co": "^4.6.0",
        "dedent": "^0.7.0",
        "is-generator-fn": "^2.0.0",
        "jest-each": "^29.4.1",
        "jest-matcher-utils": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-runtime": "^29.4.1",
        "jest-snapshot": "^29.4.1",
        "jest-util": "^29.4.1",
        "p-limit": "^3.1.0",
        "pretty-format": "^29.4.1",
        "slash": "^3.0.0",
        "stack-utils": "^2.0.3"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-cli": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-cli/-/jest-cli-29.4.1.tgz",
      "integrity": "sha512-jz7GDIhtxQ37M+9dlbv5K+/FVcIo1O/b1sX3cJgzlQUf/3VG25nvuWzlDC4F1FLLzUThJeWLu8I7JF9eWpuURQ==",
      "license": "MIT",
      "dependencies": {
        "@jest/core": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/types": "^29.4.1",
        "chalk": "^4.0.0",
        "exit": "^0.1.2",
        "graceful-fs": "^4.2.9",
        "import-local": "^3.0.2",
        "jest-config": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-validate": "^29.4.1",
        "prompts": "^2.0.1",
        "yargs": "^17.3.1"
      },
      "bin": {
        "jest": "bin/jest.js"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "peerDependencies": {
        "node-notifier": "^8.0.1 || ^9.0.0 || ^10.0.0"
      },
      "peerDependenciesMeta": {
        "node-notifier": {
          "optional": true
        }
      }
    },
    "node_modules/jest-config": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-config/-/jest-config-29.4.1.tgz",
      "integrity": "sha512-g7p3q4NuXiM4hrS4XFATTkd+2z0Ml2RhFmFPM8c3WyKwVDNszbl4E7cV7WIx1YZeqqCtqbtTtZhGZWJlJqngzg==",
      "license": "MIT",
      "dependencies": {
        "@babel/core": "^7.11.6",
        "@jest/test-sequencer": "^29.4.1",
        "@jest/types": "^29.4.1",
        "babel-jest": "^29.4.1",
        "chalk": "^4.0.0",
        "ci-info": "^3.2.0",
        "deepmerge": "^4.2.2",
        "glob": "^7.1.3",
        "graceful-fs": "^4.2.9",
        "jest-circus": "^29.4.1",
        "jest-environment-node": "^29.4.1",
        "jest-get-type": "^29.2.0",
        "jest-regex-util": "^29.2.0",
        "jest-resolve": "^29.4.1",
        "jest-runner": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-validate": "^29.4.1",
        "micromatch": "^4.0.4",
        "parse-json": "^5.2.0",
        "pretty-format": "^29.4.1",
        "slash": "^3.0.0",
        "strip-json-comments": "^3.1.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "peerDependencies": {
        "@types/node": "*",
        "ts-node": ">=9.0.0"
      },
      "peerDependenciesMeta": {
        "@types/node": {
          "optional": true
        },
        "ts-node": {
          "optional": true
        }
      }
    },
    "node_modules/jest-diff": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-diff/-/jest-diff-29.4.1.tgz",
      "integrity": "sha512-uazdl2g331iY56CEyfbNA0Ut7Mn2ulAG5vUaEHXycf1L6IPyuImIxSz4F0VYBKi7LYIuxOwTZzK3wh5jHzASMw==",
      "license": "MIT",
      "dependencies": {
        "chalk": "^4.0.0",
        "diff-sequences": "^29.3.1",
        "jest-get-type": "^29.2.0",
        "pretty-format": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-docblock": {
      "version": "29.2.0",
      "resolved": "https://registry.npmjs.org/jest-docblock/-/jest-docblock-29.2.0.tgz",
      "integrity": "sha512-bkxUsxTgWQGbXV5IENmfiIuqZhJcyvF7tU4zJ/7ioTutdz4ToB5Yx6JOFBpgI+TphRY4lhOyCWGNH/QFQh5T6A==",
      "license": "MIT",
      "dependencies": {
        "detect-newline": "^3.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-each": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-each/-/jest-each-29.4.1.tgz",
      "integrity": "sha512-QlYFiX3llJMWUV0BtWht/esGEz9w+0i7BHwODKCze7YzZzizgExB9MOfiivF/vVT0GSQ8wXLhvHXh3x2fVD4QQ==",
      "license": "MIT",
      "dependencies": {
        "@jest/types": "^29.4.1",
        "chalk": "^4.0.0",
        "jest-get-type": "^29.2.0",
        "jest-util": "^29.4.1",
        "pretty-format": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-environment-node": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-environment-node/-/jest-environment-node-29.4.1.tgz",
      "integrity": "sha512-x/H2kdVgxSkxWAIlIh9MfMuBa0hZySmfsC5lCsWmWr6tZySP44ediRKDUiNggX/eHLH7Cd5ZN10Rw+XF5tXsqg==",
      "license": "MIT",
      "dependencies": {
        "@jest/environment": "^29.4.1",
        "@jest/fake-timers": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "jest-mock": "^29.4.1",
        "jest-util": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-get-type": {
      "version": "29.2.0",
      "resolved": "https://registry.npmjs.org/jest-get-type/-/jest-get-type-29.2.0.tgz",
      "integrity": "sha512-uXNJlg8hKFEnDgFsrCjznB+sTxdkuqiCL6zMgA75qEbAJjJYTs9XPrvDctrEig2GDow22T/LvHgO57iJhXB/UA==",
      "license": "MIT",
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-haste-map": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-haste-map/-/jest-haste-map-29.4.1.tgz",
      "integrity": "sha512-imTjcgfVVTvg02khXL11NNLTx9ZaofbAWhilrMg/G8dIkp+HYCswhxf0xxJwBkfhWb3e8dwbjuWburvxmcr58w==",
      "license": "MIT",
      "dependencies": {
        "@jest/types": "^29.4.1",
        "@types/graceful-fs": "^4.1.3",
        "@types/node": "*",
        "anymatch": "^3.0.3",
        "fb-watchman": "^2.0.0",
        "graceful-fs": "^4.2.9",
        "jest-regex-util": "^29.2.0",
        "jest-util": "^29.4.1",
        "jest-worker": "^29.4.1",
        "micromatch": "^4.0.4",
        "walker": "^1.0.8"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "optionalDependencies": {
        "fsevents": "^2.3.2"
      }
    },
    "node_modules/jest-leak-detector": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-leak-detector/-/jest-leak-detector-29.4.1.tgz",
      "integrity": "sha512-akpZv7TPyGMnH2RimOCgy+hPmWZf55EyFUvymQ4LMsQP8xSPlZumCPtXGoDhFNhUE2039RApZkTQDKU79p/FiQ==",
      "license": "MIT",
      "dependencies": {
        "jest-get-type": "^29.2.0",
        "pretty-format": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-matcher-utils": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-matcher-utils/-/jest-matcher-utils-29.4.1.tgz",
      "integrity": "sha512-k5h0u8V4nAEy6lSACepxL/rw78FLDkBnXhZVgFneVpnJONhb2DhZj/Gv4eNe+1XqQ5IhgUcqj745UwH0HJmMnA==",
      "license": "MIT",
      "dependencies": {
        "chalk": "^4.0.0",
        "jest-diff": "^29.4.1",
        "jest-get-type": "^29.2.0",
        "pretty-format": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-message-util": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-message-util/-/jest-message-util-29.4.1.tgz",
      "integrity": "sha512-H4/I0cXUaLeCw6FM+i4AwCnOwHRgitdaUFOdm49022YD5nfyr8C/DrbXOBEyJaj+w/y0gGJ57klssOaUiLLQGQ==",
      "license": "MIT",
      "dependencies": {
        "@babel/code-frame": "^7.12.13",
        "@jest/types": "^29.4.1",
        "@types/stack-utils": "^2.0.0",
        "chalk": "^4.0.0",
        "graceful-fs": "^4.2.9",
        "micromatch": "^4.0.4",
        "pretty-format": "^29.4.1",
        "slash": "^3.0.0",
        "stack-utils": "^2.0.3"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-mock": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-mock/-/jest-mock-29.4.1.tgz",
      "integrity": "sha512-MwA4hQ7zBOcgVCVnsM8TzaFLVUD/pFWTfbkY953Y81L5ret3GFRZtmPmRFAjKQSdCKoJvvqOu6Bvfpqlwwb0dQ==",
      "license": "MIT",
      "dependencies": {
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "jest-util": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-pnp-resolver": {
      "version": "1.2.3",
      "resolved": "https://registry.npmjs.org/jest-pnp-resolver/-/jest-pnp-resolver-1.2.3.tgz",
      "integrity": "sha512-+3NpwQEnRoIBtx4fyhblQDPgJI0H1IEIkX7ShLUjPGA7TtUTvI1oiKi3SR4oBR0hQhQR80l4WAe5RrXBwWMA8w==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      },
      "peerDependencies": {
        "jest-resolve": "*"
      },
      "peerDependenciesMeta": {
        "jest-resolve": {
          "optional": true
        }
      }
    },
    "node_modules/jest-regex-util": {
      "version": "29.2.0",
      "resolved": "https://registry.npmjs.org/jest-regex-util/-/jest-regex-util-29.2.0.tgz",
      "integrity": "sha512-6yXn0kg2JXzH30cr2NlThF+70iuO/3irbaB4mh5WyqNIvLLP+B6sFdluO1/1RJmslyh/f9osnefECflHvTbwVA==",
      "license": "MIT",
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-resolve": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-resolve/-/jest-resolve-29.4.1.tgz",
      "integrity": "sha512-j/ZFNV2lm9IJ2wmlq1uYK0Y/1PiyDq9g4HEGsNTNr3viRbJdV+8Lf1SXIiLZXFvyiisu0qUyIXGBnw+OKWkJwQ==",
      "license": "MIT",
      "dependencies": {
        "chalk": "^4.0.0",
        "graceful-fs": "^4.2.9",
        "jest-haste-map": "^29.4.1",
        "jest-pnp-resolver": "^1.2.2",
        "jest-util": "^29.4.1",
        "jest-validate": "^29.4.1",
        "resolve": "^1.20.0",
        "resolve.exports": "^2.0.0",
        "slash": "^3.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-resolve-dependencies": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-resolve-dependencies/-/jest-resolve-dependencies-29.4.1.tgz",
      "integrity": "sha512-Y3QG3M1ncAMxfjbYgtqNXC5B595zmB6e//p/qpA/58JkQXu/IpLDoLeOa8YoYfsSglBKQQzNUqtfGJJT/qLmJg==",
      "license": "MIT",
      "dependencies": {
        "jest-regex-util": "^29.2.0",
        "jest-snapshot": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-runner": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-runner/-/jest-runner-29.4.1.tgz",
      "integrity": "sha512-8d6XXXi7GtHmsHrnaqBKWxjKb166Eyj/ksSaUYdcBK09VbjPwIgWov1VwSmtupCIz8q1Xv4Qkzt/BTo3ZqiCeg==",
      "license": "MIT",
      "dependencies": {
        "@jest/console": "^29.4.1",
        "@jest/environment": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "emittery": "^0.13.1",
        "graceful-fs": "^4.2.9",
        "jest-docblock": "^29.2.0",
        "jest-environment-node": "^29.4.1",
        "jest-haste-map": "^29.4.1",
        "jest-leak-detector": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-resolve": "^29.4.1",
        "jest-runtime": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-watcher": "^29.4.1",
        "jest-worker": "^29.4.1",
        "p-limit": "^3.1.0",
        "source-map-support": "0.5.13"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-runtime": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-runtime/-/jest-runtime-29.4.1.tgz",
      "integrity": "sha512-UXTMU9uKu2GjYwTtoAw5rn4STxWw/nadOfW7v1sx6LaJYa3V/iymdCLQM6xy3+7C6mY8GfX22vKpgxY171UIoA==",
      "license": "MIT",
      "dependencies": {
        "@jest/environment": "^29.4.1",
        "@jest/fake-timers": "^29.4.1",
        "@jest/globals": "^29.4.1",
        "@jest/source-map": "^29.2.0",
        "@jest/test-result": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "cjs-module-lexer": "^1.0.0",
        "collect-v8-coverage": "^1.0.0",
        "glob": "^7.1.3",
        "graceful-fs": "^4.2.9",
        "jest-haste-map": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-mock": "^29.4.1",
        "jest-regex-util": "^29.2.0",
        "jest-resolve": "^29.4.1",
        "jest-snapshot": "^29.4.1",
        "jest-util": "^29.4.1",
        "semver": "^7.3.5",
        "slash": "^3.0.0",
        "strip-bom": "^4.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-runtime/node_modules/semver": {
      "version": "7.3.8",
      "resolved": "https://registry.npmjs.org/semver/-/semver-7.3.8.tgz",
      "integrity": "sha512-NB1ctGL5rlHrPJtFDVIVzTyQylMLu9N9VICA6HSFJo8MCGVTMW6gfpicwKmmK/dAjTOrqu5l63JJOpDSrAis3A==",
      "license": "ISC",
      "dependencies": {
        "lru-cache": "^6.0.0"
      },
      "bin": {
        "semver": "bin/semver.js"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/jest-snapshot": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-snapshot/-/jest-snapshot-29.4.1.tgz",
      "integrity": "sha512-l4iV8EjGgQWVz3ee/LR9sULDk2pCkqb71bjvlqn+qp90lFwpnulHj4ZBT8nm1hA1C5wowXLc7MGnw321u0tsYA==",
      "license": "MIT",
      "dependencies": {
        "@babel/core": "^7.11.6",
        "@babel/generator": "^7.7.2",
        "@babel/plugin-syntax-jsx": "^7.7.2",
        "@babel/plugin-syntax-typescript": "^7.7.2",
        "@babel/traverse": "^7.7.2",
        "@babel/types": "^7.3.3",
        "@jest/expect-utils": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/babel__traverse": "^7.0.6",
        "@types/prettier": "^2.1.5",
        "babel-preset-current-node-syntax": "^1.0.0",
        "chalk": "^4.0.0",
        "expect": "^29.4.1",
        "graceful-fs": "^4.2.9",
        "jest-diff": "^29.4.1",
        "jest-get-type": "^29.2.0",
        "jest-haste-map": "^29.4.1",
        "jest-matcher-utils": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-util": "^29.4.1",
        "natural-compare": "^1.4.0",
        "pretty-format": "^29.4.1",
        "semver": "^7.3.5"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-snapshot/node_modules/semver": {
      "version": "7.3.8",
      "resolved": "https://registry.npmjs.org/semver/-/semver-7.3.8.tgz",
      "integrity": "sha512-NB1ctGL5rlHrPJtFDVIVzTyQylMLu9N9VICA6HSFJo8MCGVTMW6gfpicwKmmK/dAjTOrqu5l63JJOpDSrAis3A==",
      "license": "ISC",
      "dependencies": {
        "lru-cache": "^6.0.0"
      },
      "bin": {
        "semver": "bin/semver.js"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/jest-util": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-util/-/jest-util-29.4.1.tgz",
      "integrity": "sha512-bQy9FPGxVutgpN4VRc0hk6w7Hx/m6L53QxpDreTZgJd9gfx/AV2MjyPde9tGyZRINAUrSv57p2inGBu2dRLmkQ==",
      "license": "MIT",
      "dependencies": {
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "ci-info": "^3.2.0",
        "graceful-fs": "^4.2.9",
        "picomatch": "^2.2.3"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-validate": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-validate/-/jest-validate-29.4.1.tgz",
      "integrity": "sha512-qNZXcZQdIQx4SfUB/atWnI4/I2HUvhz8ajOSYUu40CSmf9U5emil8EDHgE7M+3j9/pavtk3knlZBDsgFvv/SWw==",
      "license": "MIT",
      "dependencies": {
        "@jest/types": "^29.4.1",
        "camelcase": "^6.2.0",
        "chalk": "^4.0.0",
        "jest-get-type": "^29.2.0",
        "leven": "^3.1.0",
        "pretty-format": "^29.4.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-watcher": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-watcher/-/jest-watcher-29.4.1.tgz",
      "integrity": "sha512-vFOzflGFs27nU6h8dpnVRER3O2rFtL+VMEwnG0H3KLHcllLsU8y9DchSh0AL/Rg5nN1/wSiQ+P4ByMGpuybaVw==",
      "license": "MIT",
      "dependencies": {
        "@jest/test-result": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "ansi-escapes": "^4.2.1",
        "chalk": "^4.0.0",
        "emittery": "^0.13.1",
        "jest-util": "^29.4.1",
        "string-length": "^4.0.1"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-worker": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-worker/-/jest-worker-29.4.1.tgz",
      "integrity": "sha512-O9doU/S1EBe+yp/mstQ0VpPwpv0Clgn68TkNwGxL6/usX/KUW9Arnn4ag8C3jc6qHcXznhsT5Na1liYzAsuAbQ==",
      "license": "MIT",
      "dependencies": {
        "@types/node": "*",
        "jest-util": "^29.4.1",
        "merge-stream": "^2.0.0",
        "supports-color": "^8.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/jest-worker/node_modules/supports-color": {
      "version": "8.1.1",
      "resolved": "https://registry.npmjs.org/supports-color/-/supports-color-8.1.1.tgz",
      "integrity": "sha512-MpUEN2OodtUzxvKQl72cUF7RQ5EiHsGvSsVG0ia9c5RbWGL2CI4C7EpPS8UTBIplnlzZiNuV56w+FuNxy3ty2Q==",
      "license": "MIT",
      "dependencies": {
        "has-flag": "^4.0.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/chalk/supports-color?sponsor=1"
      }
    },
    "node_modules/js-tokens": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/js-tokens/-/js-tokens-4.0.0.tgz",
      "integrity": "sha512-RdJUflcE3cUzKiMqQgsCu06FPu9UdIJO0beYbPhHN4k6apgJtifcoCtT9bcxOpYBtpD2kCM6Sbzg4CausW/PKQ==",
      "license": "MIT"
    },
    "node_modules/js-yaml": {
      "version": "3.14.1",
      "resolved": "https://registry.npmjs.org/js-yaml/-/js-yaml-3.14.1.tgz",
      "integrity": "sha512-okMH7OXXJ7YrN9Ok3/SXrnu4iX9yOk+25nqX4imS2npuvTYDmo/QEZoqwZkYaIDk3jVvBOTOIEgEhaLOynBS9g==",
      "license": "MIT",
      "dependencies": {
        "argparse": "^1.0.7",
        "esprima": "^4.0.0"
      },
      "bin": {
        "js-yaml": "bin/js-yaml.js"
      }
    },
    "node_modules/jsesc": {
      "version": "2.5.2",
      "resolved": "https://registry.npmjs.org/jsesc/-/jsesc-2.5.2.tgz",
      "integrity": "sha512-OYu7XEzjkCQ3C5Ps3QIZsQfNpqoJyZZA99wd9aWd05NCtC5pWOkShK2mkL6HXQR6/Cy2lbNdPlZBpuQHXE63gA==",
      "license": "MIT",
      "bin": {
        "jsesc": "bin/jsesc"
      },
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/json-parse-even-better-errors": {
      "version": "2.3.1",
      "resolved": "https://registry.npmjs.org/json-parse-even-better-errors/-/json-parse-even-better-errors-2.3.1.tgz",
      "integrity": "sha512-xyFwyhro/JEof6Ghe2iz2NcXoj2sloNsWr/XsERDK/oiPCfaNhl5ONfp+jQdAZRQQ0IJWNzH9zIZF7li91kh2w==",
      "license": "MIT"
    },
    "node_modules/json5": {
      "version": "2.2.3",
      "resolved": "https://registry.npmjs.org/json5/-/json5-2.2.3.tgz",
      "integrity": "sha512-XmOWe7eyHYH14cLdVPoyg+GOH3rYX++KpzrylJwSW98t3Nk+U8XOl8FWKOgwtzdb8lXGf6zYwDUzeHMWfxasyg==",
      "license": "MIT",
      "bin": {
        "json5": "lib/cli.js"
      },
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/jssha": {
      "version": "3.2.0",
      "resolved": "https://registry.npmjs.org/jssha/-/jssha-3.2.0.tgz",
      "integrity": "sha512-QuruyBENDWdN4tZwJbQq7/eAK85FqrI4oDbXjy5IBhYD+2pTJyBUWZe8ctWaCkrV0gy6AaelgOZZBMeswEa/6Q==",
      "license": "BSD-3-Clause",
      "engines": {
        "node": "*"
      }
    },
    "node_modules/kleur": {
      "version": "3.0.3",
      "resolved": "https://registry.npmjs.org/kleur/-/kleur-3.0.3.tgz",
      "integrity": "sha512-eTIzlVOSUR+JxdDFepEYcBMtZ9Qqdef+rnzWdRZuMbOywu5tO2w2N7rqjoANZ5k9vywhL6Br1VRjUIgTQx4E8w==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/leven": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/leven/-/leven-3.1.0.tgz",
      "integrity": "sha512-qsda+H8jTaUaN/x5vzW2rzc+8Rw4TAQ/4KjB46IwK5VH+IlVeeeje/EoZRpiXvIqjFgK84QffqPztGI3VBLG1A==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/lines-and-columns": {
      "version": "1.2.4",
      "resolved": "https://registry.npmjs.org/lines-and-columns/-/lines-and-columns-1.2.4.tgz",
      "integrity": "sha512-7ylylesZQ/PV29jhEDl3Ufjo6ZX7gCqJr5F7PKrqc93v7fzSymt1BpwEU8nAUXs8qzzvqhbjhK5QZg6Mt/HkBg==",
      "license": "MIT"
    },
    "node_modules/locate-path": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/locate-path/-/locate-path-5.0.0.tgz",
      "integrity": "sha512-t7hw9pI+WvuwNJXwk5zVHpyhIqzg2qTlklJOf0mVxGSbe3Fp2VieZcduNYjaLDoy6p9uGpQEGWG87WpMKlNq8g==",
      "license": "MIT",
      "dependencies": {
        "p-locate": "^4.1.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/lodash.memoize": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/lodash.memoize/-/lodash.memoize-4.1.2.tgz",
      "integrity": "sha512-t7j+NzmgnQzTAYXcsHYLgimltOV1MXHtlOWf6GjL9Kj8GK5FInw5JotxvbOs+IvV1/Dzo04/fCGfLVs7aXb4Ag==",
      "license": "MIT"
    },
    "node_modules/log-symbols": {
      "version": "5.1.0",
      "resolved": "https://registry.npmjs.org/log-symbols/-/log-symbols-5.1.0.tgz",
      "integrity": "sha512-l0x2DvrW294C9uDCoQe1VSU4gf529FkSZ6leBl4TiqZH/e+0R7hSfHQBNut2mNygDgHwvYHfFLn6Oxb3VWj2rA==",
      "license": "MIT",
      "dependencies": {
        "chalk": "^5.0.0",
        "is-unicode-supported": "^1.1.0"
      },
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/log-symbols/node_modules/chalk": {
      "version": "5.2.0",
      "resolved": "https://registry.npmjs.org/chalk/-/chalk-5.2.0.tgz",
      "integrity": "sha512-ree3Gqw/nazQAPuJJEy+avdl7QfZMcUvmHIKgEZkGL+xOBzRvup5Hxo6LHuMceSxOabuJLJm5Yp/92R9eMmMvA==",
      "license": "MIT",
      "engines": {
        "node": "^12.17.0 || ^14.13 || >=16.0.0"
      },
      "funding": {
        "url": "https://github.com/chalk/chalk?sponsor=1"
      }
    },
    "node_modules/long": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/long/-/long-4.0.0.tgz",
      "integrity": "sha512-XsP+KhQif4bjX1kbuSiySJFNAehNxgLb6hPRGJ9QsUr8ajHkuXGdrHmFUTUUXhDwVX2R5bY4JNZEwbUiMhV+MA==",
      "license": "Apache-2.0"
    },
    "node_modules/lower-case": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/lower-case/-/lower-case-2.0.2.tgz",
      "integrity": "sha512-7fm3l3NAF9WfN6W3JOmf5drwpVqX78JtoGJ3A6W0a6ZnldM41w2fV5D490psKFTpMds8TJse/eHLFFsNHHjHgg==",
      "license": "MIT",
      "dependencies": {
        "tslib": "^2.0.3"
      }
    },
    "node_modules/lru-cache": {
      "version": "6.0.0",
      "resolved": "https://registry.npmjs.org/lru-cache/-/lru-cache-6.0.0.tgz",
      "integrity": "sha512-Jo6dJ04CmSjuznwJSS3pUeWmd/H0ffTlkXXgwZi+eq1UCmqQwCh+eLsYOYCwY991i2Fah4h1BEMCx4qThGbsiA==",
      "license": "ISC",
      "dependencies": {
        "yallist": "^4.0.0"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/make-dir": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/make-dir/-/make-dir-3.1.0.tgz",
      "integrity": "sha512-g3FeP20LNwhALb/6Cz6Dd4F2ngze0jz7tbzrD2wAV+o9FeNHe4rL+yK2md0J/fiSf1sa1ADhXqi5+oVwOM/eGw==",
      "license": "MIT",
      "dependencies": {
        "semver": "^6.0.0"
      },
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/make-error": {
      "version": "1.3.6",
      "resolved": "https://registry.npmjs.org/make-error/-/make-error-1.3.6.tgz",
      "integrity": "sha512-s8UhlNe7vPKomQhC1qFelMokr/Sc3AgNbso3n74mVPA5LTZwkB9NlXf4XPamLxJE8h0gh73rM94xvwRT2CVInw==",
      "license": "ISC"
    },
    "node_modules/makeerror": {
      "version": "1.0.12",
      "resolved": "https://registry.npmjs.org/makeerror/-/makeerror-1.0.12.tgz",
      "integrity": "sha512-JmqCvUhmt43madlpFzG4BQzG2Z3m6tvQDNKdClZnO3VbIudJYmxsT0FNJMeiB2+JTSlTQTSbU8QdesVmwJcmLg==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "tmpl": "1.0.5"
      }
    },
    "node_modules/merge-options": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/merge-options/-/merge-options-3.0.4.tgz",
      "integrity": "sha512-2Sug1+knBjkaMsMgf1ctR1Ujx+Ayku4EdJN4Z+C2+JzoeF7A3OZ9KM2GY0CpQS51NR61LTurMJrRKPhSs3ZRTQ==",
      "license": "MIT",
      "dependencies": {
        "is-plain-obj": "^2.1.0"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/merge-stream": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/merge-stream/-/merge-stream-2.0.0.tgz",
      "integrity": "sha512-abv/qOcuPfk3URPfDzmZU1LKmuw8kT+0nIHvKrKgFrwifol/doWcdA4ZqsWQ8ENrFKkd67Mfpo/LovbIUsbt3w==",
      "license": "MIT"
    },
    "node_modules/micromatch": {
      "version": "4.0.5",
      "resolved": "https://registry.npmjs.org/micromatch/-/micromatch-4.0.5.tgz",
      "integrity": "sha512-DMy+ERcEW2q8Z2Po+WNXuw3c5YaUSFjAO5GsJqfEl7UjvtIuFKO6ZrKvcItdy98dwFI2N1tg3zNIdKaQT+aNdA==",
      "license": "MIT",
      "dependencies": {
        "braces": "^3.0.2",
        "picomatch": "^2.3.1"
      },
      "engines": {
        "node": ">=8.6"
      }
    },
    "node_modules/mimic-fn": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/mimic-fn/-/mimic-fn-2.1.0.tgz",
      "integrity": "sha512-OqbOk5oEQeAZ8WXWydlu9HJjz9WVdEIvamMCcXmuqUYjTknH/sqsWvhQ3vgwKFRR1HpjvNBKQ37nbJgYzGqGcg==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/minimatch": {
      "version": "3.1.2",
      "resolved": "https://registry.npmjs.org/minimatch/-/minimatch-3.1.2.tgz",
      "integrity": "sha512-J7p63hRiAjw1NDEww1W7i37+ByIrOWO5XQQAzZ3VOcL0PNybwpfmV/N05zFAzwQ9USyEcX6t3UO+K5aqBQOIHw==",
      "license": "ISC",
      "dependencies": {
        "brace-expansion": "^1.1.7"
      },
      "engines": {
        "node": "*"
      }
    },
    "node_modules/minimist": {
      "version": "1.2.7",
      "resolved": "https://registry.npmjs.org/minimist/-/minimist-1.2.7.tgz",
      "integrity": "sha512-bzfL1YUZsP41gmu/qjrEk0Q6i2ix/cVeAhbCbqH9u3zYutS1cLg00qhrD0M2MVdCcx4Sc0UpP2eBWo9rotpq6g==",
      "license": "MIT",
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/ms": {
      "version": "2.1.2",
      "resolved": "https://registry.npmjs.org/ms/-/ms-2.1.2.tgz",
      "integrity": "sha512-sGkPx+VjMtmA6MX27oA4FBFELFCZZ4S4XqeGOXCv68tT+jb3vk/RyaKWP0PTKyWtmLSM0b+adUTEvbs1PEaH2w==",
      "license": "MIT"
    },
    "node_modules/multiformats": {
      "version": "9.9.0",
      "resolved": "https://registry.npmjs.org/multiformats/-/multiformats-9.9.0.tgz",
      "integrity": "sha512-HoMUjhH9T8DDBNT+6xzkrd9ga/XiBI4xLr58LJACwK6G3HTOPeMz4nB4KJs33L2BelrIJa7P0VuNaVF3hMYfjg==",
      "license": "(Apache-2.0 AND MIT)"
    },
    "node_modules/murmurhash3js-revisited": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/murmurhash3js-revisited/-/murmurhash3js-revisited-3.0.0.tgz",
      "integrity": "sha512-/sF3ee6zvScXMb1XFJ8gDsSnY+X8PbOyjIuBhtgis10W2Jx4ZjIhikUCIF9c4gpJxVnQIsPAFrSwTCuAjicP6g==",
      "license": "MIT",
      "engines": {
        "node": ">=8.0.0"
      }
    },
    "node_modules/natural-compare": {
      "version": "1.4.0",
      "resolved": "https://registry.npmjs.org/natural-compare/-/natural-compare-1.4.0.tgz",
      "integrity": "sha512-OWND8ei3VtNC9h7V60qff3SVobHr996CTwgxubgyQYEpg290h9J0buyECNNJexkFm5sOajh5G116RYA1c8ZMSw==",
      "license": "MIT"
    },
    "node_modules/no-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/no-case/-/no-case-3.0.4.tgz",
      "integrity": "sha512-fgAN3jGAh+RoxUGZHTSOLJIqUc2wmoBwGR4tbpNAKmmovFoWq0OdRkb0VkldReO2a2iBT/OEulG9XSUc10r3zg==",
      "license": "MIT",
      "dependencies": {
        "lower-case": "^2.0.2",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/node-fetch": {
      "version": "2.6.9",
      "resolved": "https://registry.npmjs.org/node-fetch/-/node-fetch-2.6.9.tgz",
      "integrity": "sha512-DJm/CJkZkRjKKj4Zi4BsKVZh3ValV5IR5s7LVZnW+6YMh0W1BfNA8XSs6DLMGYlId5F3KnA70uu2qepcR08Qqg==",
      "license": "MIT",
      "dependencies": {
        "whatwg-url": "^5.0.0"
      },
      "engines": {
        "node": "4.x || >=6.0.0"
      },
      "peerDependencies": {
        "encoding": "^0.1.0"
      },
      "peerDependenciesMeta": {
        "encoding": {
          "optional": true
        }
      }
    },
    "node_modules/node-int64": {
      "version": "0.4.0",
      "resolved": "https://registry.npmjs.org/node-int64/-/node-int64-0.4.0.tgz",
      "integrity": "sha512-O5lz91xSOeoXP6DulyHfllpq+Eg00MWitZIbtPfoSEvqIHdl5gfcY6hYzDWnj0qD5tz52PI08u9qUvSVeUBeHw==",
      "license": "MIT"
    },
    "node_modules/node-releases": {
      "version": "2.0.9",
      "resolved": "https://registry.npmjs.org/node-releases/-/node-releases-2.0.9.tgz",
      "integrity": "sha512-2xfmOrRkGogbTK9R6Leda0DGiXeY3p2NJpy4+gNCffdUvV6mdEJnaDEic1i3Ec2djAo8jWYoJMR5PB0MSMpxUA==",
      "license": "MIT"
    },
    "node_modules/normalize-path": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/normalize-path/-/normalize-path-3.0.0.tgz",
      "integrity": "sha512-6eZs5Ls3WtCisHWp9S2GUy8dqkpGi4BVSz3GaqiE6ezub0512ESztXUwUB6C6IKbQkY2Pnb/mD4WYojCRwcwLA==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/npm-run-path": {
      "version": "4.0.1",
      "resolved": "https://registry.npmjs.org/npm-run-path/-/npm-run-path-4.0.1.tgz",
      "integrity": "sha512-S48WzZW777zhNIrn7gxOlISNAqi9ZC/uQFnRdbeIHhZhCA6UqpkOT8T1G7BvfdgP4Er8gF4sUbaS0i7QvIfCWw==",
      "license": "MIT",
      "dependencies": {
        "path-key": "^3.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/object-inspect": {
      "version": "1.12.3",
      "resolved": "https://registry.npmjs.org/object-inspect/-/object-inspect-1.12.3.tgz",
      "integrity": "sha512-geUvdk7c+eizMNUDkRpW1wJwgfOiOeHbxBR/hLXK1aT6zmVSO0jsQcs7fj6MGw89jC/cjGfLcNOrtMYtGqm81g==",
      "license": "MIT",
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/ohm-js": {
      "version": "16.6.0",
      "resolved": "https://registry.npmjs.org/ohm-js/-/ohm-js-16.6.0.tgz",
      "integrity": "sha512-X9P4koSGa7swgVQ0gt71UCYtkAQGOjciJPJAz74kDxWt8nXbH5HrDOQG6qBDH7SR40ktNv4x61BwpTDE9q4lRA==",
      "license": "MIT",
      "engines": {
        "node": ">=0.12.1"
      }
    },
    "node_modules/once": {
      "version": "1.4.0",
      "resolved": "https://registry.npmjs.org/once/-/once-1.4.0.tgz",
      "integrity": "sha512-lNaJgI+2Q5URQBkccEKHTQOPaXdUxnZZElQTZY0MFUAuaEqe1E+Nyvgdz/aIyNi6Z9MzO5dv1H8n58/GELp3+w==",
      "license": "ISC",
      "dependencies": {
        "wrappy": "1"
      }
    },
    "node_modules/onetime": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/onetime/-/onetime-5.1.2.tgz",
      "integrity": "sha512-kbpaSSGJTWdAY5KPVeMOKXSrPtr8C8C7wodJbcsd51jRnmD+GZu8Y0VoU6Dm5Z4vWr0Ig/1NKuWRKf7j5aaYSg==",
      "license": "MIT",
      "dependencies": {
        "mimic-fn": "^2.1.0"
      },
      "engines": {
        "node": ">=6"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/open": {
      "version": "8.4.0",
      "resolved": "https://registry.npmjs.org/open/-/open-8.4.0.tgz",
      "integrity": "sha512-XgFPPM+B28FtCCgSb9I+s9szOC1vZRSwgWsRUA5ylIxRTgKozqjOCrVOqGsYABPYK5qnfqClxZTFBa8PKt2v6Q==",
      "license": "MIT",
      "dependencies": {
        "define-lazy-prop": "^2.0.0",
        "is-docker": "^2.1.1",
        "is-wsl": "^2.2.0"
      },
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/ora": {
      "version": "6.1.2",
      "resolved": "https://registry.npmjs.org/ora/-/ora-6.1.2.tgz",
      "integrity": "sha512-EJQ3NiP5Xo94wJXIzAyOtSb0QEIAUu7m8t6UZ9krbz0vAJqr92JpcK/lEXg91q6B9pEGqrykkd2EQplnifDSBw==",
      "license": "MIT",
      "dependencies": {
        "bl": "^5.0.0",
        "chalk": "^5.0.0",
        "cli-cursor": "^4.0.0",
        "cli-spinners": "^2.6.1",
        "is-interactive": "^2.0.0",
        "is-unicode-supported": "^1.1.0",
        "log-symbols": "^5.1.0",
        "strip-ansi": "^7.0.1",
        "wcwidth": "^1.0.1"
      },
      "engines": {
        "node": "^12.20.0 || ^14.13.1 || >=16.0.0"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/ora/node_modules/ansi-regex": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-6.0.1.tgz",
      "integrity": "sha512-n5M855fKb2SsfMIiFFoVrABHJC8QtHwVx+mHWP3QcEqBHYienj5dHSgjbxtC0WEZXYt4wcD6zrQElDPhFuZgfA==",
      "license": "MIT",
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-regex?sponsor=1"
      }
    },
    "node_modules/ora/node_modules/chalk": {
      "version": "5.2.0",
      "resolved": "https://registry.npmjs.org/chalk/-/chalk-5.2.0.tgz",
      "integrity": "sha512-ree3Gqw/nazQAPuJJEy+avdl7QfZMcUvmHIKgEZkGL+xOBzRvup5Hxo6LHuMceSxOabuJLJm5Yp/92R9eMmMvA==",
      "license": "MIT",
      "engines": {
        "node": "^12.17.0 || ^14.13 || >=16.0.0"
      },
      "funding": {
        "url": "https://github.com/chalk/chalk?sponsor=1"
      }
    },
    "node_modules/ora/node_modules/strip-ansi": {
      "version": "7.0.1",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-7.0.1.tgz",
      "integrity": "sha512-cXNxvT8dFNRVfhVME3JAe98mkXDYN2O1l7jmcwMnOslDeESg1rF/OZMtK0nRAhiari1unG5cD4jG3rapUAkLbw==",
      "license": "MIT",
      "dependencies": {
        "ansi-regex": "^6.0.1"
      },
      "engines": {
        "node": ">=12"
      },
      "funding": {
        "url": "https://github.com/chalk/strip-ansi?sponsor=1"
      }
    },
    "node_modules/p-limit": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/p-limit/-/p-limit-3.1.0.tgz",
      "integrity": "sha512-TYOanM3wGwNGsZN2cVTYPArw454xnXj5qmWF1bEoAc4+cU/ol7GVh7odevjp1FNHduHc3KZMcFduxU5Xc6uJRQ==",
      "license": "MIT",
      "dependencies": {
        "yocto-queue": "^0.1.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/p-locate": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/p-locate/-/p-locate-4.1.0.tgz",
      "integrity": "sha512-R79ZZ/0wAxKGu3oYMlz8jy/kbhsNrS7SKZ7PxEHBgJ5+F2mtFW2fK2cOtBh1cHYkQsbzFV7I+EoRKe6Yt0oK7A==",
      "license": "MIT",
      "dependencies": {
        "p-limit": "^2.2.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/p-locate/node_modules/p-limit": {
      "version": "2.3.0",
      "resolved": "https://registry.npmjs.org/p-limit/-/p-limit-2.3.0.tgz",
      "integrity": "sha512-//88mFWSJx8lxCzwdAABTJL2MyWB12+eIY7MDL2SqLmAkeKU9qxRvWuSyTjm3FUmpBEMuFfckAIqEaVGUDxb6w==",
      "license": "MIT",
      "dependencies": {
        "p-try": "^2.0.0"
      },
      "engines": {
        "node": ">=6"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/p-try": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/p-try/-/p-try-2.2.0.tgz",
      "integrity": "sha512-R4nPAVTAU0B9D35/Gk3uJf/7XYbQcyohSKdvAxIRSNghFl4e71hVoGnBNQz9cWaXxO2I10KTC+3jMdvvoKw6dQ==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/param-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/param-case/-/param-case-3.0.4.tgz",
      "integrity": "sha512-RXlj7zCYokReqWpOPH9oYivUzLYZ5vAPIfEmCTNViosC78F8F0H9y7T7gG2M39ymgutxF5gcFEsyZQSph9Bp3A==",
      "license": "MIT",
      "dependencies": {
        "dot-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/parse-json": {
      "version": "5.2.0",
      "resolved": "https://registry.npmjs.org/parse-json/-/parse-json-5.2.0.tgz",
      "integrity": "sha512-ayCKvm/phCGxOkYRSCM82iDwct8/EonSEgCSxWxD7ve6jHggsFl4fZVQBPRNgQoKiuV/odhFrGzQXZwbifC8Rg==",
      "license": "MIT",
      "dependencies": {
        "@babel/code-frame": "^7.0.0",
        "error-ex": "^1.3.1",
        "json-parse-even-better-errors": "^2.3.0",
        "lines-and-columns": "^1.1.6"
      },
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/pascal-case": {
      "version": "3.1.2",
      "resolved": "https://registry.npmjs.org/pascal-case/-/pascal-case-3.1.2.tgz",
      "integrity": "sha512-uWlGT3YSnK9x3BQJaOdcZwrnV6hPpd8jFH1/ucpiLRPh/2zCVJKS19E4GvYHvaCcACn3foXZ0cLB9Wrx1KGe5g==",
      "license": "MIT",
      "dependencies": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/path-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/path-case/-/path-case-3.0.4.tgz",
      "integrity": "sha512-qO4qCFjXqVTrcbPt/hQfhTQ+VhFsqNKOPtytgNKkKxSoEp3XPUQ8ObFuePylOIok5gjn69ry8XiULxCwot3Wfg==",
      "license": "MIT",
      "dependencies": {
        "dot-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/path-exists": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/path-exists/-/path-exists-4.0.0.tgz",
      "integrity": "sha512-ak9Qy5Q7jYb2Wwcey5Fpvg2KoAc/ZIhLSLOSBmRmygPsGwkVVt0fZa0qrtMz+m6tJTAHfZQ8FnmB4MG4LWy7/w==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/path-is-absolute": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/path-is-absolute/-/path-is-absolute-1.0.1.tgz",
      "integrity": "sha512-AVbw3UJ2e9bq64vSaS9Am0fje1Pa8pbGqTTsmXfaIiMpnr5DlDhfJOuLj9Sf95ZPVDAUerDfEk88MPmPe7UCQg==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/path-key": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/path-key/-/path-key-3.1.1.tgz",
      "integrity": "sha512-ojmeN0qd+y0jszEtoY48r0Peq5dwMEkIlCOu6Q5f41lfkswXuKtYrhgoTpLnyIcHm24Uhqx+5Tqm2InSwLhE6Q==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/path-parse": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/path-parse/-/path-parse-1.0.7.tgz",
      "integrity": "sha512-LDJzPVEEEPR+y48z93A0Ed0yXb8pAByGWo/k5YYdYgpY2/2EsOsksJrq7lOHxryrVOn1ejG6oAp8ahvOIQD8sw==",
      "license": "MIT"
    },
    "node_modules/picocolors": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/picocolors/-/picocolors-1.0.0.tgz",
      "integrity": "sha512-1fygroTLlHu66zi26VoTDv8yRgm0Fccecssto+MhsZ0D/DGW2sm8E8AjW7NU5VVTRt5GxbeZ5qBuJr+HyLYkjQ==",
      "license": "ISC"
    },
    "node_modules/picomatch": {
      "version": "2.3.1",
      "resolved": "https://registry.npmjs.org/picomatch/-/picomatch-2.3.1.tgz",
      "integrity": "sha512-JU3teHTNjmE2VCGFzuY8EXzCDVwEqB2a8fsIvwaStHhAWJEeVd1o1QD80CU6+ZdEXXSLbSsuLwJjkCBWqRQUVA==",
      "license": "MIT",
      "engines": {
        "node": ">=8.6"
      },
      "funding": {
        "url": "https://github.com/sponsors/jonschlinkert"
      }
    },
    "node_modules/pirates": {
      "version": "4.0.5",
      "resolved": "https://registry.npmjs.org/pirates/-/pirates-4.0.5.tgz",
      "integrity": "sha512-8V9+HQPupnaXMA23c5hvl69zXvTwTzyAYasnkb0Tts4XvO4CliqONMOnvlq26rkhLC3nWDFBJf73LU1e1VZLaQ==",
      "license": "MIT",
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/pkg-dir": {
      "version": "4.2.0",
      "resolved": "https://registry.npmjs.org/pkg-dir/-/pkg-dir-4.2.0.tgz",
      "integrity": "sha512-HRDzbaKjC+AOWVXxAU/x54COGeIv9eb+6CkDSQoNTt4XyWoIJvuPsXizxu/Fr23EiekbtZwmh1IcIG/l/a10GQ==",
      "license": "MIT",
      "dependencies": {
        "find-up": "^4.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/prando": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/prando/-/prando-6.0.1.tgz",
      "integrity": "sha512-ghUWxQ1T9IJmPu6eshc3VU0OwveUtXQ33ZLXYUcz1Oc5ppKLDXKp0TBDj6b0epwhEctzcQSNGR2iHyvQSn4W5A==",
      "license": "MIT"
    },
    "node_modules/prettier": {
      "version": "2.8.3",
      "resolved": "https://registry.npmjs.org/prettier/-/prettier-2.8.3.tgz",
      "integrity": "sha512-tJ/oJ4amDihPoufT5sM0Z1SKEuKay8LfVAMlbbhnnkvt6BUserZylqo2PN+p9KeljLr0OHa2rXHU1T8reeoTrw==",
      "license": "MIT",
      "bin": {
        "prettier": "bin-prettier.js"
      },
      "engines": {
        "node": ">=10.13.0"
      },
      "funding": {
        "url": "https://github.com/prettier/prettier?sponsor=1"
      }
    },
    "node_modules/pretty-format": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/pretty-format/-/pretty-format-29.4.1.tgz",
      "integrity": "sha512-dt/Z761JUVsrIKaY215o1xQJBGlSmTx/h4cSqXqjHLnU1+Kt+mavVE7UgqJJO5ukx5HjSswHfmXz4LjS2oIJfg==",
      "license": "MIT",
      "dependencies": {
        "@jest/schemas": "^29.4.0",
        "ansi-styles": "^5.0.0",
        "react-is": "^18.0.0"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      }
    },
    "node_modules/pretty-format/node_modules/ansi-styles": {
      "version": "5.2.0",
      "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-5.2.0.tgz",
      "integrity": "sha512-Cxwpt2SfTzTtXcfOlzGEee8O+c+MmUgGrNiBcXnuWxuFJHe6a5Hz7qwhwe5OgaSYI0IJvkLqWX1ASG+cJOkEiA==",
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/chalk/ansi-styles?sponsor=1"
      }
    },
    "node_modules/prompts": {
      "version": "2.4.2",
      "resolved": "https://registry.npmjs.org/prompts/-/prompts-2.4.2.tgz",
      "integrity": "sha512-NxNv/kLguCA7p3jE8oL2aEBsrJWgAakBpgmgK6lpPWV+WuOmY6r2/zbAVnP+T8bQlA0nzHXSJSJW0Hq7ylaD2Q==",
      "license": "MIT",
      "dependencies": {
        "kleur": "^3.0.3",
        "sisteransi": "^1.0.5"
      },
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/protobufjs": {
      "version": "6.11.3",
      "resolved": "https://registry.npmjs.org/protobufjs/-/protobufjs-6.11.3.tgz",
      "integrity": "sha512-xL96WDdCZYdU7Slin569tFX712BxsxslWwAfAhCYjQKGTq7dAU91Lomy6nLLhh/dyGhk/YH4TwTSRxTzhuHyZg==",
      "hasInstallScript": true,
      "license": "BSD-3-Clause",
      "dependencies": {
        "@protobufjs/aspromise": "^1.1.2",
        "@protobufjs/base64": "^1.1.2",
        "@protobufjs/codegen": "^2.0.4",
        "@protobufjs/eventemitter": "^1.1.0",
        "@protobufjs/fetch": "^1.1.0",
        "@protobufjs/float": "^1.0.2",
        "@protobufjs/inquire": "^1.1.0",
        "@protobufjs/path": "^1.1.2",
        "@protobufjs/pool": "^1.1.0",
        "@protobufjs/utf8": "^1.1.0",
        "@types/long": "^4.0.1",
        "@types/node": ">=13.7.0",
        "long": "^4.0.0"
      },
      "bin": {
        "pbjs": "bin/pbjs",
        "pbts": "bin/pbts"
      }
    },
    "node_modules/qs": {
      "version": "6.11.0",
      "resolved": "https://registry.npmjs.org/qs/-/qs-6.11.0.tgz",
      "integrity": "sha512-MvjoMCJwEarSbUYk5O+nmoSzSutSsTwF85zcHPQ9OrlFoZOYIjaqBAJIqIXjptyD5vThxGq52Xu/MaJzRkIk4Q==",
      "license": "BSD-3-Clause",
      "dependencies": {
        "side-channel": "^1.0.4"
      },
      "engines": {
        "node": ">=0.6"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/rabin-wasm": {
      "version": "0.1.5",
      "resolved": "https://registry.npmjs.org/rabin-wasm/-/rabin-wasm-0.1.5.tgz",
      "integrity": "sha512-uWgQTo7pim1Rnj5TuWcCewRDTf0PEFTSlaUjWP4eY9EbLV9em08v89oCz/WO+wRxpYuO36XEHp4wgYQnAgOHzA==",
      "license": "MIT",
      "dependencies": {
        "@assemblyscript/loader": "^0.9.4",
        "bl": "^5.0.0",
        "debug": "^4.3.1",
        "minimist": "^1.2.5",
        "node-fetch": "^2.6.1",
        "readable-stream": "^3.6.0"
      },
      "bin": {
        "rabin-wasm": "cli/bin.js"
      }
    },
    "node_modules/react-is": {
      "version": "18.2.0",
      "resolved": "https://registry.npmjs.org/react-is/-/react-is-18.2.0.tgz",
      "integrity": "sha512-xWGDIW6x921xtzPkhiULtthJHoJvBbF3q26fzloPCK0hsvxtPVelvftw3zjbHWSkR2km9Z+4uxbDDK/6Zw9B8w==",
      "license": "MIT"
    },
    "node_modules/readable-stream": {
      "version": "3.6.0",
      "resolved": "https://registry.npmjs.org/readable-stream/-/readable-stream-3.6.0.tgz",
      "integrity": "sha512-BViHy7LKeTz4oNnkcLJ+lVSL6vpiFeX6/d3oSH8zCW7UxP2onchk+vTGB143xuFjHS3deTgkKoXXymXqymiIdA==",
      "license": "MIT",
      "dependencies": {
        "inherits": "^2.0.3",
        "string_decoder": "^1.1.1",
        "util-deprecate": "^1.0.1"
      },
      "engines": {
        "node": ">= 6"
      }
    },
    "node_modules/require-directory": {
      "version": "2.1.1",
      "resolved": "https://registry.npmjs.org/require-directory/-/require-directory-2.1.1.tgz",
      "integrity": "sha512-fGxEI7+wsG9xrvdjsrlmL22OMTTiHRwAMroiEeMgq8gzoLC/PQr7RsRDSTLUg/bZAZtF+TVIkHc6/4RIKrui+Q==",
      "license": "MIT",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/resolve": {
      "version": "1.22.1",
      "resolved": "https://registry.npmjs.org/resolve/-/resolve-1.22.1.tgz",
      "integrity": "sha512-nBpuuYuY5jFsli/JIs1oldw6fOQCBioohqWZg/2hiaOybXOft4lonv85uDOKXdf8rhyK159cxU5cDcK/NKk8zw==",
      "license": "MIT",
      "dependencies": {
        "is-core-module": "^2.9.0",
        "path-parse": "^1.0.7",
        "supports-preserve-symlinks-flag": "^1.0.0"
      },
      "bin": {
        "resolve": "bin/resolve"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/resolve-cwd": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/resolve-cwd/-/resolve-cwd-3.0.0.tgz",
      "integrity": "sha512-OrZaX2Mb+rJCpH/6CpSqt9xFVpN++x01XnN2ie9g6P5/3xelLAkXWVADpdz1IHD/KFfEXyE6V0U01OQ3UO2rEg==",
      "license": "MIT",
      "dependencies": {
        "resolve-from": "^5.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/resolve-from": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/resolve-from/-/resolve-from-5.0.0.tgz",
      "integrity": "sha512-qYg9KP24dD5qka9J47d0aVky0N+b4fTU89LN9iDnjB5waksiC49rvMB0PrUJQGoTmH50XPiqOvAjDfaijGxYZw==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/resolve.exports": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/resolve.exports/-/resolve.exports-2.0.0.tgz",
      "integrity": "sha512-6K/gDlqgQscOlg9fSRpWstA8sYe8rbELsSTNpx+3kTrsVCzvSl0zIvRErM7fdl9ERWDsKnrLnwB+Ne89918XOg==",
      "license": "MIT",
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/restore-cursor": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/restore-cursor/-/restore-cursor-4.0.0.tgz",
      "integrity": "sha512-I9fPXU9geO9bHOt9pHHOhOkYerIMsmVaWB0rA2AI9ERh/+x/i7MV5HKBNrg+ljO5eoPVgCcnFuRjJ9uH6I/3eg==",
      "license": "MIT",
      "dependencies": {
        "onetime": "^5.1.0",
        "signal-exit": "^3.0.2"
      },
      "engines": {
        "node": "^12.20.0 || ^14.13.1 || >=16.0.0"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/rimraf": {
      "version": "3.0.2",
      "resolved": "https://registry.npmjs.org/rimraf/-/rimraf-3.0.2.tgz",
      "integrity": "sha512-JZkJMZkAGFFPP2YqXZXPbMlMBgsxzE8ILs4lMIX/2o0L9UBw9O/Y3o6wFw/i9YLapcUJWwqbi3kdxIPdC62TIA==",
      "license": "ISC",
      "dependencies": {
        "glob": "^7.1.3"
      },
      "bin": {
        "rimraf": "bin.js"
      },
      "funding": {
        "url": "https://github.com/sponsors/isaacs"
      }
    },
    "node_modules/safe-buffer": {
      "version": "5.2.1",
      "resolved": "https://registry.npmjs.org/safe-buffer/-/safe-buffer-5.2.1.tgz",
      "integrity": "sha512-rp3So07KcdmmKbGvgaNxQSJr7bGVSVk5S9Eq1F+ppbRo70+YeaDxkw5Dd8NPN+GD6bjnYm2VuPuCXmpuYvmCXQ==",
      "funding": [
        {
          "type": "github",
          "url": "https://github.com/sponsors/feross"
        },
        {
          "type": "patreon",
          "url": "https://www.patreon.com/feross"
        },
        {
          "type": "consulting",
          "url": "https://feross.org/support"
        }
      ],
      "license": "MIT"
    },
    "node_modules/semver": {
      "version": "6.3.0",
      "resolved": "https://registry.npmjs.org/semver/-/semver-6.3.0.tgz",
      "integrity": "sha512-b39TBaTSfV6yBrapU89p5fKekE2m/NwnDocOVruQFS1/veMgdzuPcnOM34M6CwxW8jH/lxEa5rBoDeUwu5HHTw==",
      "license": "ISC",
      "bin": {
        "semver": "bin/semver.js"
      }
    },
    "node_modules/sentence-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/sentence-case/-/sentence-case-3.0.4.tgz",
      "integrity": "sha512-8LS0JInaQMCRoQ7YUytAo/xUu5W2XnQxV2HI/6uM6U7CITS1RqPElr30V6uIqyMKM9lJGRVFy5/4CuzcixNYSg==",
      "license": "MIT",
      "dependencies": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3",
        "upper-case-first": "^2.0.2"
      }
    },
    "node_modules/shebang-command": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/shebang-command/-/shebang-command-2.0.0.tgz",
      "integrity": "sha512-kHxr2zZpYtdmrN1qDjrrX/Z1rR1kG8Dx+gkpK1G4eXmvXswmcE1hTWBWYUzlraYw1/yZp6YuDY77YtvbN0dmDA==",
      "license": "MIT",
      "dependencies": {
        "shebang-regex": "^3.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/shebang-regex": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/shebang-regex/-/shebang-regex-3.0.0.tgz",
      "integrity": "sha512-7++dFhtcx3353uBaq8DDR4NuxBetBzC7ZQOhmTQInHEd6bSrXdiEyzCvG07Z44UYdLShWUyXt5M/yhz8ekcb1A==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/side-channel": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/side-channel/-/side-channel-1.0.4.tgz",
      "integrity": "sha512-q5XPytqFEIKHkGdiMIrY10mvLRvnQh42/+GoBlFW3b2LXLE2xxJpZFdm94we0BaoV3RwJyGqg5wS7epxTv0Zvw==",
      "license": "MIT",
      "dependencies": {
        "call-bind": "^1.0.0",
        "get-intrinsic": "^1.0.2",
        "object-inspect": "^1.9.0"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/signal-exit": {
      "version": "3.0.7",
      "resolved": "https://registry.npmjs.org/signal-exit/-/signal-exit-3.0.7.tgz",
      "integrity": "sha512-wnD2ZE+l+SPC/uoS0vXeE9L1+0wuaMqKlfz9AMUo38JsyLSBWSFcHR1Rri62LZc12vLr1gb3jl7iwQhgwpAbGQ==",
      "license": "ISC"
    },
    "node_modules/sisteransi": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/sisteransi/-/sisteransi-1.0.5.tgz",
      "integrity": "sha512-bLGGlR1QxBcynn2d5YmDX4MGjlZvy2MRBDRNHLJ8VI6l6+9FUiyTFNJ0IveOSP0bcXgVDPRcfGqA0pjaqUpfVg==",
      "license": "MIT"
    },
    "node_modules/slash": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/slash/-/slash-3.0.0.tgz",
      "integrity": "sha512-g9Q1haeby36OSStwb4ntCGGGaKsaVSjQ68fBxoQcutl5fS1vuY18H3wSt3jFyFtrkx+Kz0V1G85A4MyAdDMi2Q==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/snake-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/snake-case/-/snake-case-3.0.4.tgz",
      "integrity": "sha512-LAOh4z89bGQvl9pFfNF8V146i7o7/CqFPbqzYgP+yYzDIDeS9HaNFtXABamRW+AQzEVODcvE79ljJ+8a9YSdMg==",
      "license": "MIT",
      "dependencies": {
        "dot-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "node_modules/source-map": {
      "version": "0.6.1",
      "resolved": "https://registry.npmjs.org/source-map/-/source-map-0.6.1.tgz",
      "integrity": "sha512-UjgapumWlbMhkBgzT7Ykc5YXUT46F0iKu8SGXq0bcwP5dz/h0Plj6enJqjz1Zbq2l5WaqYnrVbwWOWMyF3F47g==",
      "license": "BSD-3-Clause",
      "engines": {
        "node": ">=0.10.0"
      }
    },
    "node_modules/source-map-support": {
      "version": "0.5.13",
      "resolved": "https://registry.npmjs.org/source-map-support/-/source-map-support-0.5.13.tgz",
      "integrity": "sha512-SHSKFHadjVA5oR4PPqhtAVdcBWwRYVd6g6cAXnIbRiIwc2EhPrTuKUBdSLvlEKyIP3GCf89fltvcZiP9MMFA1w==",
      "license": "MIT",
      "dependencies": {
        "buffer-from": "^1.0.0",
        "source-map": "^0.6.0"
      }
    },
    "node_modules/sparse-array": {
      "version": "1.3.2",
      "resolved": "https://registry.npmjs.org/sparse-array/-/sparse-array-1.3.2.tgz",
      "integrity": "sha512-ZT711fePGn3+kQyLuv1fpd3rNSkNF8vd5Kv2D+qnOANeyKs3fx6bUMGWRPvgTTcYV64QMqZKZwcuaQSP3AZ0tg==",
      "license": "ISC"
    },
    "node_modules/sprintf-js": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/sprintf-js/-/sprintf-js-1.0.3.tgz",
      "integrity": "sha512-D9cPgkvLlV3t3IzL0D0YLvGA9Ahk4PcvVwUbN0dSGr1aP0Nrt4AEnTUbuGvquEC0mA64Gqt1fzirlRs5ibXx8g==",
      "license": "BSD-3-Clause"
    },
    "node_modules/stack-utils": {
      "version": "2.0.6",
      "resolved": "https://registry.npmjs.org/stack-utils/-/stack-utils-2.0.6.tgz",
      "integrity": "sha512-XlkWvfIm6RmsWtNJx+uqtKLS8eqFbxUg0ZzLXqY0caEy9l7hruX8IpiDnjsLavoBgqCCR71TqWO8MaXYheJ3RQ==",
      "license": "MIT",
      "dependencies": {
        "escape-string-regexp": "^2.0.0"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/string_decoder": {
      "version": "1.3.0",
      "resolved": "https://registry.npmjs.org/string_decoder/-/string_decoder-1.3.0.tgz",
      "integrity": "sha512-hkRX8U1WjJFd8LsDJ2yQ/wWWxaopEsABU1XfkM8A+j0+85JAGppt16cr1Whg6KIbb4okU6Mql6BOj+uup/wKeA==",
      "license": "MIT",
      "dependencies": {
        "safe-buffer": "~5.2.0"
      }
    },
    "node_modules/string-length": {
      "version": "4.0.2",
      "resolved": "https://registry.npmjs.org/string-length/-/string-length-4.0.2.tgz",
      "integrity": "sha512-+l6rNN5fYHNhZZy41RXsYptCjA2Igmq4EG7kZAYFQI1E1VTXarr6ZPXBg6eq7Y6eK4FEhY6AJlyuFIb/v/S0VQ==",
      "license": "MIT",
      "dependencies": {
        "char-regex": "^1.0.2",
        "strip-ansi": "^6.0.0"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/string-width": {
      "version": "4.2.3",
      "resolved": "https://registry.npmjs.org/string-width/-/string-width-4.2.3.tgz",
      "integrity": "sha512-wKyQRQpjJ0sIp62ErSZdGsjMJWsap5oRNihHhu6G7JVO/9jIB6UyevL+tXuOqrng8j/cxKTWyWUwvSTriiZz/g==",
      "license": "MIT",
      "dependencies": {
        "emoji-regex": "^8.0.0",
        "is-fullwidth-code-point": "^3.0.0",
        "strip-ansi": "^6.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/strip-ansi": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-6.0.1.tgz",
      "integrity": "sha512-Y38VPSHcqkFrCpFnQ9vuSXmquuv5oXOKpGeT6aGrr3o3Gc9AlVa6JBfUSOCnbxGGZF+/0ooI7KrPuUSztUdU5A==",
      "license": "MIT",
      "dependencies": {
        "ansi-regex": "^5.0.1"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/strip-bom": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/strip-bom/-/strip-bom-4.0.0.tgz",
      "integrity": "sha512-3xurFv5tEgii33Zi8Jtp55wEIILR9eh34FAW00PZf+JnSsTmV/ioewSgQl97JHvgjoRGwPShsWm+IdrxB35d0w==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/strip-final-newline": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/strip-final-newline/-/strip-final-newline-2.0.0.tgz",
      "integrity": "sha512-BrpvfNAE3dcvq7ll3xVumzjKjZQ5tI1sEUIKr3Uoks0XUl45St3FlatVqef9prk4jRDzhW6WZg+3bk93y6pLjA==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/strip-json-comments": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/strip-json-comments/-/strip-json-comments-3.1.1.tgz",
      "integrity": "sha512-6fPc+R4ihwqP6N/aIv2f1gMH8lOVtWQHoqC4yK6oSDVVocumAsfCqjkXnqiYMhmMwS/mEHLp7Vehlt3ql6lEig==",
      "license": "MIT",
      "engines": {
        "node": ">=8"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/supports-color": {
      "version": "7.2.0",
      "resolved": "https://registry.npmjs.org/supports-color/-/supports-color-7.2.0.tgz",
      "integrity": "sha512-qpCAvRl9stuOHveKsn7HncJRvv501qIacKzQlO/+Lwxc9+0q2wLyv4Dfvt80/DPn2pqOBsJdDiogXGR9+OvwRw==",
      "license": "MIT",
      "dependencies": {
        "has-flag": "^4.0.0"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/supports-preserve-symlinks-flag": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/supports-preserve-symlinks-flag/-/supports-preserve-symlinks-flag-1.0.0.tgz",
      "integrity": "sha512-ot0WnXS9fgdkgIcePe6RHNk1WA8+muPa6cSjeR3V8K27q9BB1rTE3R1p7Hv0z1ZyAc8s6Vvv8DIyWf681MAt0w==",
      "license": "MIT",
      "engines": {
        "node": ">= 0.4"
      },
      "funding": {
        "url": "https://github.com/sponsors/ljharb"
      }
    },
    "node_modules/symbol.inspect": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/symbol.inspect/-/symbol.inspect-1.0.1.tgz",
      "integrity": "sha512-YQSL4duoHmLhsTD1Pw8RW6TZ5MaTX5rXJnqacJottr2P2LZBF/Yvrc3ku4NUpMOm8aM0KOCqM+UAkMA5HWQCzQ==",
      "license": "ISC"
    },
    "node_modules/teslabot": {
      "version": "1.5.0",
      "resolved": "https://registry.npmjs.org/teslabot/-/teslabot-1.5.0.tgz",
      "integrity": "sha512-e2MmELhCgrgZEGo7PQu/6bmYG36IDH+YrBI1iGm6jovXkeDIGa3pZ2WSqRjzkuw2vt1EqfkZoV5GpXgqL8QJVg==",
      "license": "MIT"
    },
    "node_modules/test-exclude": {
      "version": "6.0.0",
      "resolved": "https://registry.npmjs.org/test-exclude/-/test-exclude-6.0.0.tgz",
      "integrity": "sha512-cAGWPIyOHU6zlmg88jwm7VRyXnMN7iV68OGAbYDk/Mh/xC/pzVPlQtY6ngoIH/5/tciuhGfvESU8GrHrcxD56w==",
      "license": "ISC",
      "dependencies": {
        "@istanbuljs/schema": "^0.1.2",
        "glob": "^7.1.4",
        "minimatch": "^3.0.4"
      },
      "engines": {
        "node": ">=8"
      }
    },
    "node_modules/tmp": {
      "version": "0.2.1",
      "resolved": "https://registry.npmjs.org/tmp/-/tmp-0.2.1.tgz",
      "integrity": "sha512-76SUhtfqR2Ijn+xllcI5P1oyannHNHByD80W1q447gU3mp9G9PSpGdWmjUOHRDPiHYacIk66W7ubDTuPF3BEtQ==",
      "license": "MIT",
      "dependencies": {
        "rimraf": "^3.0.0"
      },
      "engines": {
        "node": ">=8.17.0"
      }
    },
    "node_modules/tmpl": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/tmpl/-/tmpl-1.0.5.tgz",
      "integrity": "sha512-3f0uOEAQwIqGuWW2MVzYg8fV/QNnc/IpuJNG837rLuczAaLVHslWHZQj4IGiEl5Hs3kkbhwL9Ab7Hrsmuj+Smw==",
      "license": "BSD-3-Clause"
    },
    "node_modules/to-fast-properties": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/to-fast-properties/-/to-fast-properties-2.0.0.tgz",
      "integrity": "sha512-/OaKK0xYrs3DmxRYqL/yDc+FxFUVYhDlXMhRmv3z915w2HF1tnN1omB354j8VUGO/hbRzyD6Y3sA7v7GS/ceog==",
      "license": "MIT",
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/to-regex-range": {
      "version": "5.0.1",
      "resolved": "https://registry.npmjs.org/to-regex-range/-/to-regex-range-5.0.1.tgz",
      "integrity": "sha512-65P7iz6X5yEr1cwcgvQxbbIw7Uk3gOy5dIdtZ4rDveLqhrdJP+Li/Hx6tyK0NEb+2GCyneCMJiGqrADCSNk8sQ==",
      "license": "MIT",
      "dependencies": {
        "is-number": "^7.0.0"
      },
      "engines": {
        "node": ">=8.0"
      }
    },
    "node_modules/ton": {
      "version": "13.3.0",
      "resolved": "https://registry.npmjs.org/ton/-/ton-13.3.0.tgz",
      "integrity": "sha512-ygNZ3a8xgDcftudgmq2lNzFNrQtNhUdmBneLJI8C2iBuD9RAfpnjae4eIpjPLfCsLKH8Nmvh2JOESfM7lvsCSw==",
      "dependencies": {
        "axios": "^0.25.0",
        "dataloader": "^2.0.0",
        "fp-ts": "^2.11.1",
        "io-ts": "^2.2.16",
        "io-ts-reporters": "^2.0.0",
        "symbol.inspect": "1.0.1",
        "teslabot": "^1.3.0"
      },
      "peerDependencies": {
        "ton-core": ">=0.32.0",
        "ton-crypto": ">=3.2.0"
      }
    },
    "node_modules/ton-core": {
      "version": "0.47.1",
      "resolved": "https://registry.npmjs.org/ton-core/-/ton-core-0.47.1.tgz",
      "integrity": "sha512-XxcgLYH+Ngo3uh7O7jkzA0/O8nfG3WC3fgUmdvY9/IkGKpkO3Y/KHtrZgAOHYAkxJCmaXpi4aPf4JEnZEiPrWQ==",
      "dependencies": {
        "symbol.inspect": "1.0.1"
      },
      "peerDependencies": {
        "ton-crypto": ">=3.2.0"
      }
    },
    "node_modules/ton-crypto": {
      "version": "3.2.0",
      "resolved": "https://registry.npmjs.org/ton-crypto/-/ton-crypto-3.2.0.tgz",
      "integrity": "sha512-fltdBNQ45gARMuGMEOjPZWPJ5eSql8p3CA0Dj7tPv5lhU5ziT8SxXLAzDraR9HJ8YpjBHLVvYyhMLRiEwxgtMQ==",
      "license": "MIT",
      "dependencies": {
        "jssha": "3.2.0",
        "ton-crypto-primitives": "2.0.0",
        "tweetnacl": "1.0.3"
      }
    },
    "node_modules/ton-crypto-primitives": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/ton-crypto-primitives/-/ton-crypto-primitives-2.0.0.tgz",
      "integrity": "sha512-K+qKjpS0h9sPW6oExcpxnzuQ7nEgHEiDKwIqE/jWD25o8iFGe3FWj1gKxFNbKE9wwYKc5IV8FwrU+raF0KO5nQ==",
      "license": "MIT",
      "dependencies": {
        "jssha": "3.2.0"
      }
    },
    "node_modules/ton-emulator": {
      "version": "1.6.1",
      "resolved": "https://registry.npmjs.org/ton-emulator/-/ton-emulator-1.6.1.tgz",
      "integrity": "sha512-th4K5llFixKFmC72eDDSNsLbczJaUaAu/c+FOunMgdPFyS/FUr3MOLNTjhlGk97PaKDfMgLnMAwmpd2V4R6OZg==",
      "license": "MIT",
      "dependencies": {
        "prando": "^6.0.1",
        "teslabot": "^1.5.0",
        "zod": "^3.20.2"
      },
      "peerDependencies": {
        "ton-core": ">=0.36.0",
        "ton-crypto": "^3.2.0"
      }
    },
    "node_modules/ton-tact": {
      "version": "0.9.0",
      "resolved": "https://registry.npmjs.org/ton-tact/-/ton-tact-0.9.0.tgz",
      "integrity": "sha512-TK9idKg4sPQi1VZ+naBZ1kzm64qlXQSqiroDHZD0ffhsnIdOW2n6BbQDk5NqjvA5Db49ZsgjMSAlwJ0dGFdm1Q==",
      "license": "MIT",
      "dependencies": {
        "@ipld/dag-pb": "2.1.18",
        "@types/tmp": "^0.2.3",
        "arg": "^5.0.2",
        "blockstore-core": "1.0.5",
        "change-case": "^4.1.2",
        "ipfs-unixfs-importer": "9.0.10",
        "multiformats": "9.9.0",
        "ohm-js": "^16.4.0",
        "ora": "^6.1.2",
        "prando": "^6.0.1",
        "qs": "^6.11.0",
        "tmp": "^0.2.1",
        "ton-core": ">=0.44.0",
        "ton-crypto": "^3.2.0",
        "tvm-disassembler": "^2.0.0",
        "zod": "^3.20.2"
      },
      "bin": {
        "tact": "bin/tact",
        "tact-bindings": "bin/tact-bindings"
      }
    },
    "node_modules/ton-tact/node_modules/arg": {
      "version": "5.0.2",
      "resolved": "https://registry.npmjs.org/arg/-/arg-5.0.2.tgz",
      "integrity": "sha512-PYjyFOLKQ9y57JvQ6QLo8dAgNqswh8M1RMJYdQduT6xbWSgK36P/Z/v+p888pM69jMMfS8Xd8F6I1kQ/I9HUGg==",
      "license": "MIT"
    },
    "node_modules/tr46": {
      "version": "0.0.3",
      "resolved": "https://registry.npmjs.org/tr46/-/tr46-0.0.3.tgz",
      "integrity": "sha512-N3WMsuqV66lT30CrXNbEjx4GEwlow3v6rr4mCcv6prnfwhS01rkgyFdjPNBYd9br7LpXV1+Emh01fHnq2Gdgrw==",
      "license": "MIT"
    },
    "node_modules/ts-jest": {
      "version": "29.0.5",
      "resolved": "https://registry.npmjs.org/ts-jest/-/ts-jest-29.0.5.tgz",
      "integrity": "sha512-PL3UciSgIpQ7f6XjVOmbi96vmDHUqAyqDr8YxzopDqX3kfgYtX1cuNeBjP+L9sFXi6nzsGGA6R3fP3DDDJyrxA==",
      "license": "MIT",
      "dependencies": {
        "bs-logger": "0.x",
        "fast-json-stable-stringify": "2.x",
        "jest-util": "^29.0.0",
        "json5": "^2.2.3",
        "lodash.memoize": "4.x",
        "make-error": "1.x",
        "semver": "7.x",
        "yargs-parser": "^21.0.1"
      },
      "bin": {
        "ts-jest": "cli.js"
      },
      "engines": {
        "node": "^14.15.0 || ^16.10.0 || >=18.0.0"
      },
      "peerDependencies": {
        "@babel/core": ">=7.0.0-beta.0 <8",
        "@jest/types": "^29.0.0",
        "babel-jest": "^29.0.0",
        "jest": "^29.0.0",
        "typescript": ">=4.3"
      },
      "peerDependenciesMeta": {
        "@babel/core": {
          "optional": true
        },
        "@jest/types": {
          "optional": true
        },
        "babel-jest": {
          "optional": true
        },
        "esbuild": {
          "optional": true
        }
      }
    },
    "node_modules/ts-jest/node_modules/semver": {
      "version": "7.3.8",
      "resolved": "https://registry.npmjs.org/semver/-/semver-7.3.8.tgz",
      "integrity": "sha512-NB1ctGL5rlHrPJtFDVIVzTyQylMLu9N9VICA6HSFJo8MCGVTMW6gfpicwKmmK/dAjTOrqu5l63JJOpDSrAis3A==",
      "license": "ISC",
      "dependencies": {
        "lru-cache": "^6.0.0"
      },
      "bin": {
        "semver": "bin/semver.js"
      },
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/ts-node": {
      "version": "10.9.1",
      "resolved": "https://registry.npmjs.org/ts-node/-/ts-node-10.9.1.tgz",
      "integrity": "sha512-NtVysVPkxxrwFGUUxGYhfux8k78pQB3JqYBXlLRZgdGUqTO5wU/UyHop5p70iEbGhB7q5KmiZiU0Y3KlJrScEw==",
      "dependencies": {
        "@cspotcode/source-map-support": "^0.8.0",
        "@tsconfig/node10": "^1.0.7",
        "@tsconfig/node12": "^1.0.7",
        "@tsconfig/node14": "^1.0.0",
        "@tsconfig/node16": "^1.0.2",
        "acorn": "^8.4.1",
        "acorn-walk": "^8.1.1",
        "arg": "^4.1.0",
        "create-require": "^1.1.0",
        "diff": "^4.0.1",
        "make-error": "^1.1.1",
        "v8-compile-cache-lib": "^3.0.1",
        "yn": "3.1.1"
      },
      "bin": {
        "ts-node": "dist/bin.js",
        "ts-node-cwd": "dist/bin-cwd.js",
        "ts-node-esm": "dist/bin-esm.js",
        "ts-node-script": "dist/bin-script.js",
        "ts-node-transpile-only": "dist/bin-transpile.js",
        "ts-script": "dist/bin-script-deprecated.js"
      },
      "peerDependencies": {
        "@swc/core": ">=1.2.50",
        "@swc/wasm": ">=1.2.50",
        "@types/node": "*",
        "typescript": ">=2.7"
      },
      "peerDependenciesMeta": {
        "@swc/core": {
          "optional": true
        },
        "@swc/wasm": {
          "optional": true
        }
      }
    },
    "node_modules/tslib": {
      "version": "2.5.0",
      "resolved": "https://registry.npmjs.org/tslib/-/tslib-2.5.0.tgz",
      "integrity": "sha512-336iVw3rtn2BUK7ORdIAHTyxHGRIHVReokCR3XjbckJMK7ms8FysBfhLR8IXnAgy7T0PTPNBWKiH514FOW/WSg==",
      "license": "0BSD"
    },
    "node_modules/tvm-disassembler": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/tvm-disassembler/-/tvm-disassembler-2.0.0.tgz",
      "integrity": "sha512-59WejM7BhGl0Z6H6ZFaUwrc0WixAzX9O9VX6qhUBoD+O2RcYA7zs1cYFTSDW5eOs40Fv4LuG4P6sdlF9YR11zw==",
      "license": "MIT",
      "peerDependencies": {
        "ton-core": ">=0.27.0"
      }
    },
    "node_modules/tweetnacl": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/tweetnacl/-/tweetnacl-1.0.3.tgz",
      "integrity": "sha512-6rt+RN7aOi1nGMyC4Xa5DdYiukl2UWCbcJft7YhxReBGQD7OAM8Pbxw6YMo4r2diNEA8FEmu32YOn9rhaiE5yw==",
      "license": "Unlicense"
    },
    "node_modules/type-detect": {
      "version": "4.0.8",
      "resolved": "https://registry.npmjs.org/type-detect/-/type-detect-4.0.8.tgz",
      "integrity": "sha512-0fr/mIH1dlO+x7TlcMy+bIDqKPsw/70tVyeHW787goQjhmqaZe10uwLujubK9q9Lg6Fiho1KUKDYz0Z7k7g5/g==",
      "license": "MIT",
      "engines": {
        "node": ">=4"
      }
    },
    "node_modules/type-fest": {
      "version": "0.21.3",
      "resolved": "https://registry.npmjs.org/type-fest/-/type-fest-0.21.3.tgz",
      "integrity": "sha512-t0rzBq87m3fVcduHDUFhKmyyX+9eo6WQjZvf51Ea/M0Q7+T374Jp1aUiyUl0GKxp8M/OETVHSDvmkyPgvX+X2w==",
      "license": "(MIT OR CC0-1.0)",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/typescript": {
      "version": "4.9.5",
      "resolved": "https://registry.npmjs.org/typescript/-/typescript-4.9.5.tgz",
      "integrity": "sha512-1FXk9E2Hm+QzZQ7z+McJiHL4NW1F2EzMu9Nq9i3zAaGqibafqYwCVU6WyWAuyQRRzOlxou8xZSyXLEN8oKj24g==",
      "license": "Apache-2.0",
      "bin": {
        "tsc": "bin/tsc",
        "tsserver": "bin/tsserver"
      },
      "engines": {
        "node": ">=4.2.0"
      }
    },
    "node_modules/uint8arrays": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/uint8arrays/-/uint8arrays-3.1.1.tgz",
      "integrity": "sha512-+QJa8QRnbdXVpHYjLoTpJIdCTiw9Ir62nocClWuXIq2JIh4Uta0cQsTSpFL678p2CN8B+XSApwcU+pQEqVpKWg==",
      "license": "MIT",
      "dependencies": {
        "multiformats": "^9.4.2"
      }
    },
    "node_modules/update-browserslist-db": {
      "version": "1.0.10",
      "resolved": "https://registry.npmjs.org/update-browserslist-db/-/update-browserslist-db-1.0.10.tgz",
      "integrity": "sha512-OztqDenkfFkbSG+tRxBeAnCVPckDBcvibKd35yDONx6OU8N7sqgwc7rCbkJ/WcYtVRZ4ba68d6byhC21GFh7sQ==",
      "funding": [
        {
          "type": "opencollective",
          "url": "https://opencollective.com/browserslist"
        },
        {
          "type": "tidelift",
          "url": "https://tidelift.com/funding/github/npm/browserslist"
        }
      ],
      "license": "MIT",
      "dependencies": {
        "escalade": "^3.1.1",
        "picocolors": "^1.0.0"
      },
      "bin": {
        "browserslist-lint": "cli.js"
      },
      "peerDependencies": {
        "browserslist": ">= 4.21.0"
      }
    },
    "node_modules/upper-case": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/upper-case/-/upper-case-2.0.2.tgz",
      "integrity": "sha512-KgdgDGJt2TpuwBUIjgG6lzw2GWFRCW9Qkfkiv0DxqHHLYJHmtmdUIKcZd8rHgFSjopVTlw6ggzCm1b8MFQwikg==",
      "license": "MIT",
      "dependencies": {
        "tslib": "^2.0.3"
      }
    },
    "node_modules/upper-case-first": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/upper-case-first/-/upper-case-first-2.0.2.tgz",
      "integrity": "sha512-514ppYHBaKwfJRK/pNC6c/OxfGa0obSnAl106u97Ed0I625Nin96KAjttZF6ZL3e1XLtphxnqrOi9iWgm+u+bg==",
      "license": "MIT",
      "dependencies": {
        "tslib": "^2.0.3"
      }
    },
    "node_modules/util-deprecate": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/util-deprecate/-/util-deprecate-1.0.2.tgz",
      "integrity": "sha512-EPD5q1uXyFxJpCrLnCc1nHnq3gOa6DZBocAIiI2TaSCA7VCJ1UJDMagCzIkXNsUYfD1daK//LTEQ8xiIbrHtcw==",
      "license": "MIT"
    },
    "node_modules/v8-compile-cache-lib": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/v8-compile-cache-lib/-/v8-compile-cache-lib-3.0.1.tgz",
      "integrity": "sha512-wa7YjyUGfNZngI/vtK0UHAN+lgDCxBPCylVXGp0zu59Fz5aiGtNXaq3DhIov063MorB+VfufLh3JlF2KdTK3xg==",
      "license": "MIT"
    },
    "node_modules/v8-to-istanbul": {
      "version": "9.0.1",
      "resolved": "https://registry.npmjs.org/v8-to-istanbul/-/v8-to-istanbul-9.0.1.tgz",
      "integrity": "sha512-74Y4LqY74kLE6IFyIjPtkSTWzUZmj8tdHT9Ii/26dvQ6K9Dl2NbEfj0XgU2sHCtKgt5VupqhlO/5aWuqS+IY1w==",
      "license": "ISC",
      "dependencies": {
        "@jridgewell/trace-mapping": "^0.3.12",
        "@types/istanbul-lib-coverage": "^2.0.1",
        "convert-source-map": "^1.6.0"
      },
      "engines": {
        "node": ">=10.12.0"
      }
    },
    "node_modules/walker": {
      "version": "1.0.8",
      "resolved": "https://registry.npmjs.org/walker/-/walker-1.0.8.tgz",
      "integrity": "sha512-ts/8E8l5b7kY0vlWLewOkDXMmPdLcVV4GmOQLyxuSswIJsweeFZtAsMF7k1Nszz+TYBQrlYRmzOnr398y1JemQ==",
      "license": "Apache-2.0",
      "dependencies": {
        "makeerror": "1.0.12"
      }
    },
    "node_modules/wcwidth": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/wcwidth/-/wcwidth-1.0.1.tgz",
      "integrity": "sha512-XHPEwS0q6TaxcvG85+8EYkbiCux2XtWG2mkc47Ng2A77BQu9+DqIOJldST4HgPkuea7dvKSj5VgX3P1d4rW8Tg==",
      "license": "MIT",
      "dependencies": {
        "defaults": "^1.0.3"
      }
    },
    "node_modules/webidl-conversions": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/webidl-conversions/-/webidl-conversions-3.0.1.tgz",
      "integrity": "sha512-2JAn3z8AR6rjK8Sm8orRC0h/bcl/DqL7tRPdGZ4I1CjdF+EaMLmYxBHyXuKL849eucPFhvBoxMsflfOb8kxaeQ==",
      "license": "BSD-2-Clause"
    },
    "node_modules/whatwg-fetch": {
      "version": "3.6.2",
      "resolved": "https://registry.npmjs.org/whatwg-fetch/-/whatwg-fetch-3.6.2.tgz",
      "integrity": "sha512-bJlen0FcuU/0EMLrdbJ7zOnW6ITZLrZMIarMUVmdKtsGvZna8vxKYaexICWPfZ8qwf9fzNq+UEIZrnSaApt6RA=="
    },
    "node_modules/whatwg-url": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/whatwg-url/-/whatwg-url-5.0.0.tgz",
      "integrity": "sha512-saE57nupxk6v3HY35+jzBwYa0rKSy0XR8JSxZPwgLr7ys0IBzhGviA1/TUGJLmSVqs8pb9AnvICXEuOHLprYTw==",
      "license": "MIT",
      "dependencies": {
        "tr46": "~0.0.3",
        "webidl-conversions": "^3.0.0"
      }
    },
    "node_modules/which": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/which/-/which-2.0.2.tgz",
      "integrity": "sha512-BLI3Tl1TW3Pvl70l3yq3Y64i+awpwXqsGBYWkkqMtnbXgrMD+yj7rhW0kuEDxzJaYXGjEW5ogapKNMEKNMjibA==",
      "license": "ISC",
      "dependencies": {
        "isexe": "^2.0.0"
      },
      "bin": {
        "node-which": "bin/node-which"
      },
      "engines": {
        "node": ">= 8"
      }
    },
    "node_modules/wrap-ansi": {
      "version": "7.0.0",
      "resolved": "https://registry.npmjs.org/wrap-ansi/-/wrap-ansi-7.0.0.tgz",
      "integrity": "sha512-YVGIj2kamLSTxw6NsZjoBxfSwsn0ycdesmc4p+Q21c5zPuZ1pl+NfxVdxPtdHvmNVOQ6XSYG4AUtyt/Fi7D16Q==",
      "license": "MIT",
      "dependencies": {
        "ansi-styles": "^4.0.0",
        "string-width": "^4.1.0",
        "strip-ansi": "^6.0.0"
      },
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/chalk/wrap-ansi?sponsor=1"
      }
    },
    "node_modules/wrappy": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/wrappy/-/wrappy-1.0.2.tgz",
      "integrity": "sha512-l4Sp/DRseor9wL6EvV2+TuQn63dMkPjZ/sp9XkghTEbV9KlPS1xUsZ3u7/IQO4wxtcFB4bgpQPRcR3QCvezPcQ==",
      "license": "ISC"
    },
    "node_modules/write-file-atomic": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/write-file-atomic/-/write-file-atomic-5.0.0.tgz",
      "integrity": "sha512-R7NYMnHSlV42K54lwY9lvW6MnSm1HSJqZL3xiSgi9E7//FYaI74r2G0rd+/X6VAMkHEdzxQaU5HUOXWUz5kA/w==",
      "license": "ISC",
      "dependencies": {
        "imurmurhash": "^0.1.4",
        "signal-exit": "^3.0.7"
      },
      "engines": {
        "node": "^14.17.0 || ^16.13.0 || >=18.0.0"
      }
    },
    "node_modules/y18n": {
      "version": "5.0.8",
      "resolved": "https://registry.npmjs.org/y18n/-/y18n-5.0.8.tgz",
      "integrity": "sha512-0pfFzegeDWJHJIAmTLRP2DwHjdF5s7jo9tuztdQxAhINCdvS+3nGINqPd00AphqJR/0LhANUS6/+7SCb98YOfA==",
      "license": "ISC",
      "engines": {
        "node": ">=10"
      }
    },
    "node_modules/yallist": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/yallist/-/yallist-4.0.0.tgz",
      "integrity": "sha512-3wdGidZyq5PB084XLES5TpOSRA3wjXAlIWMhum2kRcv/41Sn2emQ0dycQW4uZXLejwKvg6EsvbdlVL+FYEct7A==",
      "license": "ISC"
    },
    "node_modules/yargs": {
      "version": "17.6.2",
      "resolved": "https://registry.npmjs.org/yargs/-/yargs-17.6.2.tgz",
      "integrity": "sha512-1/9UrdHjDZc0eOU0HxOHoS78C69UD3JRMvzlJ7S79S2nTaWRA/whGCTV8o9e/N/1Va9YIV7Q4sOxD8VV4pCWOw==",
      "license": "MIT",
      "dependencies": {
        "cliui": "^8.0.1",
        "escalade": "^3.1.1",
        "get-caller-file": "^2.0.5",
        "require-directory": "^2.1.1",
        "string-width": "^4.2.3",
        "y18n": "^5.0.5",
        "yargs-parser": "^21.1.1"
      },
      "engines": {
        "node": ">=12"
      }
    },
    "node_modules/yargs-parser": {
      "version": "21.1.1",
      "resolved": "https://registry.npmjs.org/yargs-parser/-/yargs-parser-21.1.1.tgz",
      "integrity": "sha512-tVpsJW7DdjecAiFpbIB1e3qxIQsE6NoPc5/eTdrbbIC4h0LVsWhnoa3g+m2HclBIujHzsxZ4VJVA+GUuc2/LBw==",
      "license": "ISC",
      "engines": {
        "node": ">=12"
      }
    },
    "node_modules/yn": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/yn/-/yn-3.1.1.tgz",
      "integrity": "sha512-Ux4ygGWsu2c7isFWe8Yu1YluJmqVhxqK2cLXNQA5AcC3QfbGNpM7fu0Y8b/z16pXLnFxZYvWhd3fhBY9DLmC6Q==",
      "license": "MIT",
      "engines": {
        "node": ">=6"
      }
    },
    "node_modules/yocto-queue": {
      "version": "0.1.0",
      "resolved": "https://registry.npmjs.org/yocto-queue/-/yocto-queue-0.1.0.tgz",
      "integrity": "sha512-rVksvsnNCdJ/ohGc6xgPwyN8eheCxsiLM8mxuE/t/mOVqJewPuO1miLpTHQiRgTKCLexL4MeAFVagts7HmNZ2Q==",
      "license": "MIT",
      "engines": {
        "node": ">=10"
      },
      "funding": {
        "url": "https://github.com/sponsors/sindresorhus"
      }
    },
    "node_modules/zod": {
      "version": "3.20.2",
      "resolved": "https://registry.npmjs.org/zod/-/zod-3.20.2.tgz",
      "integrity": "sha512-1MzNQdAvO+54H+EaK5YpyEy0T+Ejo/7YLHS93G3RnYWh5gaotGHwGeN/ZO687qEDU2y4CdStQYXVHIgrUl5UVQ==",
      "license": "MIT",
      "funding": {
        "url": "https://github.com/sponsors/colinhacks"
      }
    }
  },
  "dependencies": {
    "@ampproject/remapping": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/@ampproject/remapping/-/remapping-2.2.0.tgz",
      "integrity": "sha512-qRmjj8nj9qmLTQXXmaR1cck3UXSRMPrbsLJAasZpF+t3riI71BXed5ebIOYwQntykeZuhjsdweEc9BxH5Jc26w==",
      "requires": {
        "@jridgewell/gen-mapping": "^0.1.0",
        "@jridgewell/trace-mapping": "^0.3.9"
      },
      "dependencies": {
        "@jridgewell/gen-mapping": {
          "version": "0.1.1",
          "resolved": "https://registry.npmjs.org/@jridgewell/gen-mapping/-/gen-mapping-0.1.1.tgz",
          "integrity": "sha512-sQXCasFk+U8lWYEe66WxRDOE9PjVz4vSM51fTu3Hw+ClTpUSQb718772vH3pyS5pShp6lvQM7SxgIDXXXmOX7w==",
          "requires": {
            "@jridgewell/set-array": "^1.0.0",
            "@jridgewell/sourcemap-codec": "^1.4.10"
          }
        }
      }
    },
    "@assemblyscript/loader": {
      "version": "0.9.4",
      "resolved": "https://registry.npmjs.org/@assemblyscript/loader/-/loader-0.9.4.tgz",
      "integrity": "sha512-HazVq9zwTVwGmqdwYzu7WyQ6FQVZ7SwET0KKQuKm55jD0IfUpZgN0OPIiZG3zV1iSrVYcN0bdwLRXI/VNCYsUA=="
    },
    "@babel/code-frame": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/code-frame/-/code-frame-7.18.6.tgz",
      "integrity": "sha512-TDCmlK5eOvH+eH7cdAFlNXeVJqWIQ7gW9tY1GJIpUtFb6CmjVyq2VM3u71bOyR8CRihcCgMUYoDNyLXao3+70Q==",
      "requires": {
        "@babel/highlight": "^7.18.6"
      }
    },
    "@babel/compat-data": {
      "version": "7.20.14",
      "resolved": "https://registry.npmjs.org/@babel/compat-data/-/compat-data-7.20.14.tgz",
      "integrity": "sha512-0YpKHD6ImkWMEINCyDAD0HLLUH/lPCefG8ld9it8DJB2wnApraKuhgYTvTY1z7UFIfBTGy5LwncZ+5HWWGbhFw=="
    },
    "@babel/core": {
      "version": "7.20.12",
      "resolved": "https://registry.npmjs.org/@babel/core/-/core-7.20.12.tgz",
      "integrity": "sha512-XsMfHovsUYHFMdrIHkZphTN/2Hzzi78R08NuHfDBehym2VsPDL6Zn/JAD/JQdnRvbSsbQc4mVaU1m6JgtTEElg==",
      "requires": {
        "@ampproject/remapping": "^2.1.0",
        "@babel/code-frame": "^7.18.6",
        "@babel/generator": "^7.20.7",
        "@babel/helper-compilation-targets": "^7.20.7",
        "@babel/helper-module-transforms": "^7.20.11",
        "@babel/helpers": "^7.20.7",
        "@babel/parser": "^7.20.7",
        "@babel/template": "^7.20.7",
        "@babel/traverse": "^7.20.12",
        "@babel/types": "^7.20.7",
        "convert-source-map": "^1.7.0",
        "debug": "^4.1.0",
        "gensync": "^1.0.0-beta.2",
        "json5": "^2.2.2",
        "semver": "^6.3.0"
      }
    },
    "@babel/generator": {
      "version": "7.20.14",
      "resolved": "https://registry.npmjs.org/@babel/generator/-/generator-7.20.14.tgz",
      "integrity": "sha512-AEmuXHdcD3A52HHXxaTmYlb8q/xMEhoRP67B3T4Oq7lbmSoqroMZzjnGj3+i1io3pdnF8iBYVu4Ilj+c4hBxYg==",
      "requires": {
        "@babel/types": "^7.20.7",
        "@jridgewell/gen-mapping": "^0.3.2",
        "jsesc": "^2.5.1"
      }
    },
    "@babel/helper-compilation-targets": {
      "version": "7.20.7",
      "resolved": "https://registry.npmjs.org/@babel/helper-compilation-targets/-/helper-compilation-targets-7.20.7.tgz",
      "integrity": "sha512-4tGORmfQcrc+bvrjb5y3dG9Mx1IOZjsHqQVUz7XCNHO+iTmqxWnVg3KRygjGmpRLJGdQSKuvFinbIb0CnZwHAQ==",
      "requires": {
        "@babel/compat-data": "^7.20.5",
        "@babel/helper-validator-option": "^7.18.6",
        "browserslist": "^4.21.3",
        "lru-cache": "^5.1.1",
        "semver": "^6.3.0"
      },
      "dependencies": {
        "lru-cache": {
          "version": "5.1.1",
          "resolved": "https://registry.npmjs.org/lru-cache/-/lru-cache-5.1.1.tgz",
          "integrity": "sha512-KpNARQA3Iwv+jTA0utUVVbrh+Jlrr1Fv0e56GGzAFOXN7dk/FviaDW8LHmK52DlcH4WP2n6gI8vN1aesBFgo9w==",
          "requires": {
            "yallist": "^3.0.2"
          }
        },
        "yallist": {
          "version": "3.1.1",
          "resolved": "https://registry.npmjs.org/yallist/-/yallist-3.1.1.tgz",
          "integrity": "sha512-a4UGQaWPH59mOXUYnAG2ewncQS4i4F43Tv3JoAM+s2VDAmS9NsK8GpDMLrCHPksFT7h3K6TOoUNn2pb7RoXx4g=="
        }
      }
    },
    "@babel/helper-environment-visitor": {
      "version": "7.18.9",
      "resolved": "https://registry.npmjs.org/@babel/helper-environment-visitor/-/helper-environment-visitor-7.18.9.tgz",
      "integrity": "sha512-3r/aACDJ3fhQ/EVgFy0hpj8oHyHpQc+LPtJoY9SzTThAsStm4Ptegq92vqKoE3vD706ZVFWITnMnxucw+S9Ipg=="
    },
    "@babel/helper-function-name": {
      "version": "7.19.0",
      "resolved": "https://registry.npmjs.org/@babel/helper-function-name/-/helper-function-name-7.19.0.tgz",
      "integrity": "sha512-WAwHBINyrpqywkUH0nTnNgI5ina5TFn85HKS0pbPDfxFfhyR/aNQEn4hGi1P1JyT//I0t4OgXUlofzWILRvS5w==",
      "requires": {
        "@babel/template": "^7.18.10",
        "@babel/types": "^7.19.0"
      }
    },
    "@babel/helper-hoist-variables": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/helper-hoist-variables/-/helper-hoist-variables-7.18.6.tgz",
      "integrity": "sha512-UlJQPkFqFULIcyW5sbzgbkxn2FKRgwWiRexcuaR8RNJRy8+LLveqPjwZV/bwrLZCN0eUHD/x8D0heK1ozuoo6Q==",
      "requires": {
        "@babel/types": "^7.18.6"
      }
    },
    "@babel/helper-module-imports": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/helper-module-imports/-/helper-module-imports-7.18.6.tgz",
      "integrity": "sha512-0NFvs3VkuSYbFi1x2Vd6tKrywq+z/cLeYC/RJNFrIX/30Bf5aiGYbtvGXolEktzJH8o5E5KJ3tT+nkxuuZFVlA==",
      "requires": {
        "@babel/types": "^7.18.6"
      }
    },
    "@babel/helper-module-transforms": {
      "version": "7.20.11",
      "resolved": "https://registry.npmjs.org/@babel/helper-module-transforms/-/helper-module-transforms-7.20.11.tgz",
      "integrity": "sha512-uRy78kN4psmji1s2QtbtcCSaj/LILFDp0f/ymhpQH5QY3nljUZCaNWz9X1dEj/8MBdBEFECs7yRhKn8i7NjZgg==",
      "requires": {
        "@babel/helper-environment-visitor": "^7.18.9",
        "@babel/helper-module-imports": "^7.18.6",
        "@babel/helper-simple-access": "^7.20.2",
        "@babel/helper-split-export-declaration": "^7.18.6",
        "@babel/helper-validator-identifier": "^7.19.1",
        "@babel/template": "^7.20.7",
        "@babel/traverse": "^7.20.10",
        "@babel/types": "^7.20.7"
      }
    },
    "@babel/helper-plugin-utils": {
      "version": "7.20.2",
      "resolved": "https://registry.npmjs.org/@babel/helper-plugin-utils/-/helper-plugin-utils-7.20.2.tgz",
      "integrity": "sha512-8RvlJG2mj4huQ4pZ+rU9lqKi9ZKiRmuvGuM2HlWmkmgOhbs6zEAw6IEiJ5cQqGbDzGZOhwuOQNtZMi/ENLjZoQ=="
    },
    "@babel/helper-simple-access": {
      "version": "7.20.2",
      "resolved": "https://registry.npmjs.org/@babel/helper-simple-access/-/helper-simple-access-7.20.2.tgz",
      "integrity": "sha512-+0woI/WPq59IrqDYbVGfshjT5Dmk/nnbdpcF8SnMhhXObpTq2KNBdLFRFrkVdbDOyUmHBCxzm5FHV1rACIkIbA==",
      "requires": {
        "@babel/types": "^7.20.2"
      }
    },
    "@babel/helper-split-export-declaration": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/helper-split-export-declaration/-/helper-split-export-declaration-7.18.6.tgz",
      "integrity": "sha512-bde1etTx6ZyTmobl9LLMMQsaizFVZrquTEHOqKeQESMKo4PlObf+8+JA25ZsIpZhT/WEd39+vOdLXAFG/nELpA==",
      "requires": {
        "@babel/types": "^7.18.6"
      }
    },
    "@babel/helper-string-parser": {
      "version": "7.19.4",
      "resolved": "https://registry.npmjs.org/@babel/helper-string-parser/-/helper-string-parser-7.19.4.tgz",
      "integrity": "sha512-nHtDoQcuqFmwYNYPz3Rah5ph2p8PFeFCsZk9A/48dPc/rGocJ5J3hAAZ7pb76VWX3fZKu+uEr/FhH5jLx7umrw=="
    },
    "@babel/helper-validator-identifier": {
      "version": "7.19.1",
      "resolved": "https://registry.npmjs.org/@babel/helper-validator-identifier/-/helper-validator-identifier-7.19.1.tgz",
      "integrity": "sha512-awrNfaMtnHUr653GgGEs++LlAvW6w+DcPrOliSMXWCKo597CwL5Acf/wWdNkf/tfEQE3mjkeD1YOVZOUV/od1w=="
    },
    "@babel/helper-validator-option": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/helper-validator-option/-/helper-validator-option-7.18.6.tgz",
      "integrity": "sha512-XO7gESt5ouv/LRJdrVjkShckw6STTaB7l9BrpBaAHDeF5YZT+01PCwmR0SJHnkW6i8OwW/EVWRShfi4j2x+KQw=="
    },
    "@babel/helpers": {
      "version": "7.20.13",
      "resolved": "https://registry.npmjs.org/@babel/helpers/-/helpers-7.20.13.tgz",
      "integrity": "sha512-nzJ0DWCL3gB5RCXbUO3KIMMsBY2Eqbx8mBpKGE/02PgyRQFcPQLbkQ1vyy596mZLaP+dAfD+R4ckASzNVmW3jg==",
      "requires": {
        "@babel/template": "^7.20.7",
        "@babel/traverse": "^7.20.13",
        "@babel/types": "^7.20.7"
      }
    },
    "@babel/highlight": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/highlight/-/highlight-7.18.6.tgz",
      "integrity": "sha512-u7stbOuYjaPezCuLj29hNW1v64M2Md2qupEKP1fHc7WdOA3DgLh37suiSrZYY7haUB7iBeQZ9P1uiRF359do3g==",
      "requires": {
        "@babel/helper-validator-identifier": "^7.18.6",
        "chalk": "^2.0.0",
        "js-tokens": "^4.0.0"
      },
      "dependencies": {
        "ansi-styles": {
          "version": "3.2.1",
          "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-3.2.1.tgz",
          "integrity": "sha512-VT0ZI6kZRdTh8YyJw3SMbYm/u+NqfsAxEpWO0Pf9sq8/e94WxxOpPKx9FR1FlyCtOVDNOQ+8ntlqFxiRc+r5qA==",
          "requires": {
            "color-convert": "^1.9.0"
          }
        },
        "chalk": {
          "version": "2.4.2",
          "resolved": "https://registry.npmjs.org/chalk/-/chalk-2.4.2.tgz",
          "integrity": "sha512-Mti+f9lpJNcwF4tWV8/OrTTtF1gZi+f8FqlyAdouralcFWFQWF2+NgCHShjkCb+IFBLq9buZwE1xckQU4peSuQ==",
          "requires": {
            "ansi-styles": "^3.2.1",
            "escape-string-regexp": "^1.0.5",
            "supports-color": "^5.3.0"
          }
        },
        "color-convert": {
          "version": "1.9.3",
          "resolved": "https://registry.npmjs.org/color-convert/-/color-convert-1.9.3.tgz",
          "integrity": "sha512-QfAUtd+vFdAtFQcC8CCyYt1fYWxSqAiK2cSD6zDB8N3cpsEBAvRxp9zOGg6G/SHHJYAT88/az/IuDGALsNVbGg==",
          "requires": {
            "color-name": "1.1.3"
          }
        },
        "color-name": {
          "version": "1.1.3",
          "resolved": "https://registry.npmjs.org/color-name/-/color-name-1.1.3.tgz",
          "integrity": "sha512-72fSenhMw2HZMTVHeCA9KCmpEIbzWiQsjN+BHcBbS9vr1mtt+vJjPdksIBNUmKAW8TFUDPJK5SUU3QhE9NEXDw=="
        },
        "escape-string-regexp": {
          "version": "1.0.5",
          "resolved": "https://registry.npmjs.org/escape-string-regexp/-/escape-string-regexp-1.0.5.tgz",
          "integrity": "sha512-vbRorB5FUQWvla16U8R/qgaFIya2qGzwDrNmCZuYKrbdSUMG6I1ZCGQRefkRVhuOkIGVne7BQ35DSfo1qvJqFg=="
        },
        "has-flag": {
          "version": "3.0.0",
          "resolved": "https://registry.npmjs.org/has-flag/-/has-flag-3.0.0.tgz",
          "integrity": "sha512-sKJf1+ceQBr4SMkvQnBDNDtf4TXpVhVGateu0t918bl30FnbE2m4vNLX+VWe/dpjlb+HugGYzW7uQXH98HPEYw=="
        },
        "supports-color": {
          "version": "5.5.0",
          "resolved": "https://registry.npmjs.org/supports-color/-/supports-color-5.5.0.tgz",
          "integrity": "sha512-QjVjwdXIt408MIiAqCX4oUKsgU2EqAGzs2Ppkm4aQYbjm+ZEWEcW4SfFNTr4uMNZma0ey4f5lgLrkB0aX0QMow==",
          "requires": {
            "has-flag": "^3.0.0"
          }
        }
      }
    },
    "@babel/parser": {
      "version": "7.20.13",
      "resolved": "https://registry.npmjs.org/@babel/parser/-/parser-7.20.13.tgz",
      "integrity": "sha512-gFDLKMfpiXCsjt4za2JA9oTMn70CeseCehb11kRZgvd7+F67Hih3OHOK24cRrWECJ/ljfPGac6ygXAs/C8kIvw=="
    },
    "@babel/plugin-syntax-async-generators": {
      "version": "7.8.4",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-async-generators/-/plugin-syntax-async-generators-7.8.4.tgz",
      "integrity": "sha512-tycmZxkGfZaxhMRbXlPXuVFpdWlXpir2W4AMhSJgRKzk/eDlIXOhb2LHWoLpDF7TEHylV5zNhykX6KAgHJmTNw==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.8.0"
      }
    },
    "@babel/plugin-syntax-bigint": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-bigint/-/plugin-syntax-bigint-7.8.3.tgz",
      "integrity": "sha512-wnTnFlG+YxQm3vDxpGE57Pj0srRU4sHE/mDkt1qv2YJJSeUAec2ma4WLUnUPeKjyrfntVwe/N6dCXpU+zL3Npg==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.8.0"
      }
    },
    "@babel/plugin-syntax-class-properties": {
      "version": "7.12.13",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-class-properties/-/plugin-syntax-class-properties-7.12.13.tgz",
      "integrity": "sha512-fm4idjKla0YahUNgFNLCB0qySdsoPiZP3iQE3rky0mBUtMZ23yDJ9SJdg6dXTSDnulOVqiF3Hgr9nbXvXTQZYA==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.12.13"
      }
    },
    "@babel/plugin-syntax-import-meta": {
      "version": "7.10.4",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-import-meta/-/plugin-syntax-import-meta-7.10.4.tgz",
      "integrity": "sha512-Yqfm+XDx0+Prh3VSeEQCPU81yC+JWZ2pDPFSS4ZdpfZhp4MkFMaDC1UqseovEKwSUpnIL7+vK+Clp7bfh0iD7g==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.10.4"
      }
    },
    "@babel/plugin-syntax-json-strings": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-json-strings/-/plugin-syntax-json-strings-7.8.3.tgz",
      "integrity": "sha512-lY6kdGpWHvjoe2vk4WrAapEuBR69EMxZl+RoGRhrFGNYVK8mOPAW8VfbT/ZgrFbXlDNiiaxQnAtgVCZ6jv30EA==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.8.0"
      }
    },
    "@babel/plugin-syntax-jsx": {
      "version": "7.18.6",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-jsx/-/plugin-syntax-jsx-7.18.6.tgz",
      "integrity": "sha512-6mmljtAedFGTWu2p/8WIORGwy+61PLgOMPOdazc7YoJ9ZCWUyFy3A6CpPkRKLKD1ToAesxX8KGEViAiLo9N+7Q==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.18.6"
      }
    },
    "@babel/plugin-syntax-logical-assignment-operators": {
      "version": "7.10.4",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-logical-assignment-operators/-/plugin-syntax-logical-assignment-operators-7.10.4.tgz",
      "integrity": "sha512-d8waShlpFDinQ5MtvGU9xDAOzKH47+FFoney2baFIoMr952hKOLp1HR7VszoZvOsV/4+RRszNY7D17ba0te0ig==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.10.4"
      }
    },
    "@babel/plugin-syntax-nullish-coalescing-operator": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-nullish-coalescing-operator/-/plugin-syntax-nullish-coalescing-operator-7.8.3.tgz",
      "integrity": "sha512-aSff4zPII1u2QD7y+F8oDsz19ew4IGEJg9SVW+bqwpwtfFleiQDMdzA/R+UlWDzfnHFCxxleFT0PMIrR36XLNQ==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.8.0"
      }
    },
    "@babel/plugin-syntax-numeric-separator": {
      "version": "7.10.4",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-numeric-separator/-/plugin-syntax-numeric-separator-7.10.4.tgz",
      "integrity": "sha512-9H6YdfkcK/uOnY/K7/aA2xpzaAgkQn37yzWUMRK7OaPOqOpGS1+n0H5hxT9AUw9EsSjPW8SVyMJwYRtWs3X3ug==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.10.4"
      }
    },
    "@babel/plugin-syntax-object-rest-spread": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-object-rest-spread/-/plugin-syntax-object-rest-spread-7.8.3.tgz",
      "integrity": "sha512-XoqMijGZb9y3y2XskN+P1wUGiVwWZ5JmoDRwx5+3GmEplNyVM2s2Dg8ILFQm8rWM48orGy5YpI5Bl8U1y7ydlA==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.8.0"
      }
    },
    "@babel/plugin-syntax-optional-catch-binding": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-optional-catch-binding/-/plugin-syntax-optional-catch-binding-7.8.3.tgz",
      "integrity": "sha512-6VPD0Pc1lpTqw0aKoeRTMiB+kWhAoT24PA+ksWSBrFtl5SIRVpZlwN3NNPQjehA2E/91FV3RjLWoVTglWcSV3Q==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.8.0"
      }
    },
    "@babel/plugin-syntax-optional-chaining": {
      "version": "7.8.3",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-optional-chaining/-/plugin-syntax-optional-chaining-7.8.3.tgz",
      "integrity": "sha512-KoK9ErH1MBlCPxV0VANkXW2/dw4vlbGDrFgz8bmUsBGYkFRcbRwMh6cIJubdPrkxRwuGdtCk0v/wPTKbQgBjkg==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.8.0"
      }
    },
    "@babel/plugin-syntax-top-level-await": {
      "version": "7.14.5",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-top-level-await/-/plugin-syntax-top-level-await-7.14.5.tgz",
      "integrity": "sha512-hx++upLv5U1rgYfwe1xBQUhRmU41NEvpUvrp8jkrSCdvGSnM5/qdRMtylJ6PG5OFkBaHkbTAKTnd3/YyESRHFw==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.14.5"
      }
    },
    "@babel/plugin-syntax-typescript": {
      "version": "7.20.0",
      "resolved": "https://registry.npmjs.org/@babel/plugin-syntax-typescript/-/plugin-syntax-typescript-7.20.0.tgz",
      "integrity": "sha512-rd9TkG+u1CExzS4SM1BlMEhMXwFLKVjOAFFCDx9PbX5ycJWDoWMcwdJH9RhkPu1dOgn5TrxLot/Gx6lWFuAUNQ==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.19.0"
      }
    },
    "@babel/template": {
      "version": "7.20.7",
      "resolved": "https://registry.npmjs.org/@babel/template/-/template-7.20.7.tgz",
      "integrity": "sha512-8SegXApWe6VoNw0r9JHpSteLKTpTiLZ4rMlGIm9JQ18KiCtyQiAMEazujAHrUS5flrcqYZa75ukev3P6QmUwUw==",
      "requires": {
        "@babel/code-frame": "^7.18.6",
        "@babel/parser": "^7.20.7",
        "@babel/types": "^7.20.7"
      }
    },
    "@babel/traverse": {
      "version": "7.20.13",
      "resolved": "https://registry.npmjs.org/@babel/traverse/-/traverse-7.20.13.tgz",
      "integrity": "sha512-kMJXfF0T6DIS9E8cgdLCSAL+cuCK+YEZHWiLK0SXpTo8YRj5lpJu3CDNKiIBCne4m9hhTIqUg6SYTAI39tAiVQ==",
      "requires": {
        "@babel/code-frame": "^7.18.6",
        "@babel/generator": "^7.20.7",
        "@babel/helper-environment-visitor": "^7.18.9",
        "@babel/helper-function-name": "^7.19.0",
        "@babel/helper-hoist-variables": "^7.18.6",
        "@babel/helper-split-export-declaration": "^7.18.6",
        "@babel/parser": "^7.20.13",
        "@babel/types": "^7.20.7",
        "debug": "^4.1.0",
        "globals": "^11.1.0"
      }
    },
    "@babel/types": {
      "version": "7.20.7",
      "resolved": "https://registry.npmjs.org/@babel/types/-/types-7.20.7.tgz",
      "integrity": "sha512-69OnhBxSSgK0OzTJai4kyPDiKTIe3j+ctaHdIGVbRahTLAT7L3R9oeXHC2aVSuGYt3cVnoAMDmOCgJ2yaiLMvg==",
      "requires": {
        "@babel/helper-string-parser": "^7.19.4",
        "@babel/helper-validator-identifier": "^7.19.1",
        "to-fast-properties": "^2.0.0"
      }
    },
    "@bcoe/v8-coverage": {
      "version": "0.2.3",
      "resolved": "https://registry.npmjs.org/@bcoe/v8-coverage/-/v8-coverage-0.2.3.tgz",
      "integrity": "sha512-0hYQ8SB4Db5zvZB4axdMHGwEaQjkZzFjQiN9LVYvIFB2nSUHW9tYpxWriPrWDASIxiaXax83REcLxuSdnGPZtw=="
    },
    "@cspotcode/source-map-support": {
      "version": "0.8.1",
      "resolved": "https://registry.npmjs.org/@cspotcode/source-map-support/-/source-map-support-0.8.1.tgz",
      "integrity": "sha512-IchNf6dN4tHoMFIn/7OE8LWZ19Y6q/67Bmf6vnGREv8RSbBVb9LPJxEcnwrcwX6ixSvaiGoomAUvu4YSxXrVgw==",
      "requires": {
        "@jridgewell/trace-mapping": "0.3.9"
      },
      "dependencies": {
        "@jridgewell/trace-mapping": {
          "version": "0.3.9",
          "resolved": "https://registry.npmjs.org/@jridgewell/trace-mapping/-/trace-mapping-0.3.9.tgz",
          "integrity": "sha512-3Belt6tdc8bPgAtbcmdtNJlirVoTmEb5e2gC94PnkwEW9jI6CAHUeoG85tjWP5WquqfavoMtMwiG4P926ZKKuQ==",
          "requires": {
            "@jridgewell/resolve-uri": "^3.0.3",
            "@jridgewell/sourcemap-codec": "^1.4.10"
          }
        }
      }
    },
    "@ipld/dag-pb": {
      "version": "2.1.18",
      "resolved": "https://registry.npmjs.org/@ipld/dag-pb/-/dag-pb-2.1.18.tgz",
      "integrity": "sha512-ZBnf2fuX9y3KccADURG5vb9FaOeMjFkCrNysB0PtftME/4iCTjxfaLoNq/IAh5fTqUOMXvryN6Jyka4ZGuMLIg==",
      "requires": {
        "multiformats": "^9.5.4"
      }
    },
    "@istanbuljs/load-nyc-config": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@istanbuljs/load-nyc-config/-/load-nyc-config-1.1.0.tgz",
      "integrity": "sha512-VjeHSlIzpv/NyD3N0YuHfXOPDIixcA1q2ZV98wsMqcYlPmv2n3Yb2lYP9XMElnaFVXg5A7YLTeLu6V84uQDjmQ==",
      "requires": {
        "camelcase": "^5.3.1",
        "find-up": "^4.1.0",
        "get-package-type": "^0.1.0",
        "js-yaml": "^3.13.1",
        "resolve-from": "^5.0.0"
      },
      "dependencies": {
        "camelcase": {
          "version": "5.3.1",
          "resolved": "https://registry.npmjs.org/camelcase/-/camelcase-5.3.1.tgz",
          "integrity": "sha512-L28STB170nwWS63UjtlEOE3dldQApaJXZkOI1uMFfzf3rRuPegHaHesyee+YxQ+W6SvRDQV6UrdOdRiR153wJg=="
        }
      }
    },
    "@istanbuljs/schema": {
      "version": "0.1.3",
      "resolved": "https://registry.npmjs.org/@istanbuljs/schema/-/schema-0.1.3.tgz",
      "integrity": "sha512-ZXRY4jNvVgSVQ8DL3LTcakaAtXwTVUxE81hslsyD2AtoXW/wVob10HkOJ1X/pAlcI7D+2YoZKg5do8G/w6RYgA=="
    },
    "@jest/console": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/console/-/console-29.4.1.tgz",
      "integrity": "sha512-m+XpwKSi3PPM9znm5NGS8bBReeAJJpSkL1OuFCqaMaJL2YX9YXLkkI+MBchMPwu+ZuM2rynL51sgfkQteQ1CKQ==",
      "requires": {
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "jest-message-util": "^29.4.1",
        "jest-util": "^29.4.1",
        "slash": "^3.0.0"
      }
    },
    "@jest/core": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/core/-/core-29.4.1.tgz",
      "integrity": "sha512-RXFTohpBqpaTebNdg5l3I5yadnKo9zLBajMT0I38D0tDhreVBYv3fA8kywthI00sWxPztWLD3yjiUkewwu/wKA==",
      "requires": {
        "@jest/console": "^29.4.1",
        "@jest/reporters": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "ansi-escapes": "^4.2.1",
        "chalk": "^4.0.0",
        "ci-info": "^3.2.0",
        "exit": "^0.1.2",
        "graceful-fs": "^4.2.9",
        "jest-changed-files": "^29.4.0",
        "jest-config": "^29.4.1",
        "jest-haste-map": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-regex-util": "^29.2.0",
        "jest-resolve": "^29.4.1",
        "jest-resolve-dependencies": "^29.4.1",
        "jest-runner": "^29.4.1",
        "jest-runtime": "^29.4.1",
        "jest-snapshot": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-validate": "^29.4.1",
        "jest-watcher": "^29.4.1",
        "micromatch": "^4.0.4",
        "pretty-format": "^29.4.1",
        "slash": "^3.0.0",
        "strip-ansi": "^6.0.0"
      }
    },
    "@jest/environment": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/environment/-/environment-29.4.1.tgz",
      "integrity": "sha512-pJ14dHGSQke7Q3mkL/UZR9ZtTOxqskZaC91NzamEH4dlKRt42W+maRBXiw/LWkdJe+P0f/zDR37+SPMplMRlPg==",
      "requires": {
        "@jest/fake-timers": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "jest-mock": "^29.4.1"
      }
    },
    "@jest/expect": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/expect/-/expect-29.4.1.tgz",
      "integrity": "sha512-ZxKJP5DTUNF2XkpJeZIzvnzF1KkfrhEF6Rz0HGG69fHl6Bgx5/GoU3XyaeFYEjuuKSOOsbqD/k72wFvFxc3iTw==",
      "requires": {
        "expect": "^29.4.1",
        "jest-snapshot": "^29.4.1"
      }
    },
    "@jest/expect-utils": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/expect-utils/-/expect-utils-29.4.1.tgz",
      "integrity": "sha512-w6YJMn5DlzmxjO00i9wu2YSozUYRBhIoJ6nQwpMYcBMtiqMGJm1QBzOf6DDgRao8dbtpDoaqLg6iiQTvv0UHhQ==",
      "requires": {
        "jest-get-type": "^29.2.0"
      }
    },
    "@jest/fake-timers": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/fake-timers/-/fake-timers-29.4.1.tgz",
      "integrity": "sha512-/1joI6rfHFmmm39JxNfmNAO3Nwm6Y0VoL5fJDy7H1AtWrD1CgRtqJbN9Ld6rhAkGO76qqp4cwhhxJ9o9kYjQMw==",
      "requires": {
        "@jest/types": "^29.4.1",
        "@sinonjs/fake-timers": "^10.0.2",
        "@types/node": "*",
        "jest-message-util": "^29.4.1",
        "jest-mock": "^29.4.1",
        "jest-util": "^29.4.1"
      }
    },
    "@jest/globals": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/globals/-/globals-29.4.1.tgz",
      "integrity": "sha512-znoK2EuFytbHH0ZSf2mQK2K1xtIgmaw4Da21R2C/NE/+NnItm5mPEFQmn8gmF3f0rfOlmZ3Y3bIf7bFj7DHxAA==",
      "requires": {
        "@jest/environment": "^29.4.1",
        "@jest/expect": "^29.4.1",
        "@jest/types": "^29.4.1",
        "jest-mock": "^29.4.1"
      }
    },
    "@jest/reporters": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/reporters/-/reporters-29.4.1.tgz",
      "integrity": "sha512-AISY5xpt2Xpxj9R6y0RF1+O6GRy9JsGa8+vK23Lmzdy1AYcpQn5ItX79wJSsTmfzPKSAcsY1LNt/8Y5Xe5LOSg==",
      "requires": {
        "@bcoe/v8-coverage": "^0.2.3",
        "@jest/console": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@jridgewell/trace-mapping": "^0.3.15",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "collect-v8-coverage": "^1.0.0",
        "exit": "^0.1.2",
        "glob": "^7.1.3",
        "graceful-fs": "^4.2.9",
        "istanbul-lib-coverage": "^3.0.0",
        "istanbul-lib-instrument": "^5.1.0",
        "istanbul-lib-report": "^3.0.0",
        "istanbul-lib-source-maps": "^4.0.0",
        "istanbul-reports": "^3.1.3",
        "jest-message-util": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-worker": "^29.4.1",
        "slash": "^3.0.0",
        "string-length": "^4.0.1",
        "strip-ansi": "^6.0.0",
        "v8-to-istanbul": "^9.0.1"
      }
    },
    "@jest/schemas": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/@jest/schemas/-/schemas-29.4.0.tgz",
      "integrity": "sha512-0E01f/gOZeNTG76i5eWWSupvSHaIINrTie7vCyjiYFKgzNdyEGd12BUv4oNBFHOqlHDbtoJi3HrQ38KCC90NsQ==",
      "requires": {
        "@sinclair/typebox": "^0.25.16"
      }
    },
    "@jest/source-map": {
      "version": "29.2.0",
      "resolved": "https://registry.npmjs.org/@jest/source-map/-/source-map-29.2.0.tgz",
      "integrity": "sha512-1NX9/7zzI0nqa6+kgpSdKPK+WU1p+SJk3TloWZf5MzPbxri9UEeXX5bWZAPCzbQcyuAzubcdUHA7hcNznmRqWQ==",
      "requires": {
        "@jridgewell/trace-mapping": "^0.3.15",
        "callsites": "^3.0.0",
        "graceful-fs": "^4.2.9"
      }
    },
    "@jest/test-result": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/test-result/-/test-result-29.4.1.tgz",
      "integrity": "sha512-WRt29Lwt+hEgfN8QDrXqXGgCTidq1rLyFqmZ4lmJOpVArC8daXrZWkWjiaijQvgd3aOUj2fM8INclKHsQW9YyQ==",
      "requires": {
        "@jest/console": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/istanbul-lib-coverage": "^2.0.0",
        "collect-v8-coverage": "^1.0.0"
      }
    },
    "@jest/test-sequencer": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/test-sequencer/-/test-sequencer-29.4.1.tgz",
      "integrity": "sha512-v5qLBNSsM0eHzWLXsQ5fiB65xi49A3ILPSFQKPXzGL4Vyux0DPZAIN7NAFJa9b4BiTDP9MBF/Zqc/QA1vuiJ0w==",
      "requires": {
        "@jest/test-result": "^29.4.1",
        "graceful-fs": "^4.2.9",
        "jest-haste-map": "^29.4.1",
        "slash": "^3.0.0"
      }
    },
    "@jest/transform": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/transform/-/transform-29.4.1.tgz",
      "integrity": "sha512-5w6YJrVAtiAgr0phzKjYd83UPbCXsBRTeYI4BXokv9Er9CcrH9hfXL/crCvP2d2nGOcovPUnlYiLPFLZrkG5Hg==",
      "requires": {
        "@babel/core": "^7.11.6",
        "@jest/types": "^29.4.1",
        "@jridgewell/trace-mapping": "^0.3.15",
        "babel-plugin-istanbul": "^6.1.1",
        "chalk": "^4.0.0",
        "convert-source-map": "^2.0.0",
        "fast-json-stable-stringify": "^2.1.0",
        "graceful-fs": "^4.2.9",
        "jest-haste-map": "^29.4.1",
        "jest-regex-util": "^29.2.0",
        "jest-util": "^29.4.1",
        "micromatch": "^4.0.4",
        "pirates": "^4.0.4",
        "slash": "^3.0.0",
        "write-file-atomic": "^5.0.0"
      },
      "dependencies": {
        "convert-source-map": {
          "version": "2.0.0",
          "resolved": "https://registry.npmjs.org/convert-source-map/-/convert-source-map-2.0.0.tgz",
          "integrity": "sha512-Kvp459HrV2FEJ1CAsi1Ku+MY3kasH19TFykTz2xWmMeq6bk2NU3XXvfJ+Q61m0xktWwt+1HSYf3JZsTms3aRJg=="
        }
      }
    },
    "@jest/types": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/@jest/types/-/types-29.4.1.tgz",
      "integrity": "sha512-zbrAXDUOnpJ+FMST2rV7QZOgec8rskg2zv8g2ajeqitp4tvZiyqTCYXANrKsM+ryj5o+LI+ZN2EgU9drrkiwSA==",
      "requires": {
        "@jest/schemas": "^29.4.0",
        "@types/istanbul-lib-coverage": "^2.0.0",
        "@types/istanbul-reports": "^3.0.0",
        "@types/node": "*",
        "@types/yargs": "^17.0.8",
        "chalk": "^4.0.0"
      }
    },
    "@jridgewell/gen-mapping": {
      "version": "0.3.2",
      "resolved": "https://registry.npmjs.org/@jridgewell/gen-mapping/-/gen-mapping-0.3.2.tgz",
      "integrity": "sha512-mh65xKQAzI6iBcFzwv28KVWSmCkdRBWoOh+bYQGW3+6OZvbbN3TqMGo5hqYxQniRcH9F2VZIoJCm4pa3BPDK/A==",
      "requires": {
        "@jridgewell/set-array": "^1.0.1",
        "@jridgewell/sourcemap-codec": "^1.4.10",
        "@jridgewell/trace-mapping": "^0.3.9"
      }
    },
    "@jridgewell/resolve-uri": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/@jridgewell/resolve-uri/-/resolve-uri-3.1.0.tgz",
      "integrity": "sha512-F2msla3tad+Mfht5cJq7LSXcdudKTWCVYUgw6pLFOOHSTtZlj6SWNYAp+AhuqLmWdBO2X5hPrLcu8cVP8fy28w=="
    },
    "@jridgewell/set-array": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/@jridgewell/set-array/-/set-array-1.1.2.tgz",
      "integrity": "sha512-xnkseuNADM0gt2bs+BvhO0p78Mk762YnZdsuzFV018NoG1Sj1SCQvpSqa7XUaTam5vAGasABV9qXASMKnFMwMw=="
    },
    "@jridgewell/sourcemap-codec": {
      "version": "1.4.14",
      "resolved": "https://registry.npmjs.org/@jridgewell/sourcemap-codec/-/sourcemap-codec-1.4.14.tgz",
      "integrity": "sha512-XPSJHWmi394fuUuzDnGz1wiKqWfo1yXecHQMRf2l6hztTO+nPru658AyDngaBe7isIxEkRsPR3FZh+s7iVa4Uw=="
    },
    "@jridgewell/trace-mapping": {
      "version": "0.3.17",
      "resolved": "https://registry.npmjs.org/@jridgewell/trace-mapping/-/trace-mapping-0.3.17.tgz",
      "integrity": "sha512-MCNzAp77qzKca9+W/+I0+sEpaUnZoeasnghNeVc41VZCEKaCH73Vq3BZZ/SzWIgrqE4H4ceI+p+b6C0mHf9T4g==",
      "requires": {
        "@jridgewell/resolve-uri": "3.1.0",
        "@jridgewell/sourcemap-codec": "1.4.14"
      }
    },
    "@multiformats/murmur3": {
      "version": "1.1.3",
      "resolved": "https://registry.npmjs.org/@multiformats/murmur3/-/murmur3-1.1.3.tgz",
      "integrity": "sha512-wAPLUErGR8g6Lt+bAZn6218k9YQPym+sjszsXL6o4zfxbA22P+gxWZuuD9wDbwL55xrKO5idpcuQUX7/E3oHcw==",
      "requires": {
        "multiformats": "^9.5.4",
        "murmurhash3js-revisited": "^3.0.0"
      }
    },
    "@orbs-network/ton-access": {
      "version": "2.2.2",
      "resolved": "https://registry.npmjs.org/@orbs-network/ton-access/-/ton-access-2.2.2.tgz",
      "integrity": "sha512-ygcbNxqZez2CpDMFhMTgbNAm7MGoDCbF1Zbp/liUAWqrKjytUDAoAAVXIWulhl0exWaacn7YWI75GNt8ouxjwA==",
      "requires": {
        "isomorphic-fetch": "^3.0.0"
      }
    },
    "@protobufjs/aspromise": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/@protobufjs/aspromise/-/aspromise-1.1.2.tgz",
      "integrity": "sha512-j+gKExEuLmKwvz3OgROXtrJ2UG2x8Ch2YZUxahh+s1F2HZ+wAceUNLkvy6zKCPVRkU++ZWQrdxsUeQXmcg4uoQ=="
    },
    "@protobufjs/base64": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/@protobufjs/base64/-/base64-1.1.2.tgz",
      "integrity": "sha512-AZkcAA5vnN/v4PDqKyMR5lx7hZttPDgClv83E//FMNhR2TMcLUhfRUBHCmSl0oi9zMgDDqRUJkSxO3wm85+XLg=="
    },
    "@protobufjs/codegen": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/@protobufjs/codegen/-/codegen-2.0.4.tgz",
      "integrity": "sha512-YyFaikqM5sH0ziFZCN3xDC7zeGaB/d0IUb9CATugHWbd1FRFwWwt4ld4OYMPWu5a3Xe01mGAULCdqhMlPl29Jg=="
    },
    "@protobufjs/eventemitter": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/eventemitter/-/eventemitter-1.1.0.tgz",
      "integrity": "sha512-j9ednRT81vYJ9OfVuXG6ERSTdEL1xVsNgqpkxMsbIabzSo3goCjDIveeGv5d03om39ML71RdmrGNjG5SReBP/Q=="
    },
    "@protobufjs/fetch": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/fetch/-/fetch-1.1.0.tgz",
      "integrity": "sha512-lljVXpqXebpsijW71PZaCYeIcE5on1w5DlQy5WH6GLbFryLUrBD4932W/E2BSpfRJWseIL4v/KPgBFxDOIdKpQ==",
      "requires": {
        "@protobufjs/aspromise": "^1.1.1",
        "@protobufjs/inquire": "^1.1.0"
      }
    },
    "@protobufjs/float": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/@protobufjs/float/-/float-1.0.2.tgz",
      "integrity": "sha512-Ddb+kVXlXst9d+R9PfTIxh1EdNkgoRe5tOX6t01f1lYWOvJnSPDBlG241QLzcyPdoNTsblLUdujGSE4RzrTZGQ=="
    },
    "@protobufjs/inquire": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/inquire/-/inquire-1.1.0.tgz",
      "integrity": "sha512-kdSefcPdruJiFMVSbn801t4vFK7KB/5gd2fYvrxhuJYg8ILrmn9SKSX2tZdV6V+ksulWqS7aXjBcRXl3wHoD9Q=="
    },
    "@protobufjs/path": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/@protobufjs/path/-/path-1.1.2.tgz",
      "integrity": "sha512-6JOcJ5Tm08dOHAbdR3GrvP+yUUfkjG5ePsHYczMFLq3ZmMkAD98cDgcT2iA1lJ9NVwFd4tH/iSSoe44YWkltEA=="
    },
    "@protobufjs/pool": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/pool/-/pool-1.1.0.tgz",
      "integrity": "sha512-0kELaGSIDBKvcgS4zkjz1PeddatrjYcmMWOlAuAPwAeccUrPHdUqo/J6LiymHHEiJT5NrF1UVwxY14f+fy4WQw=="
    },
    "@protobufjs/utf8": {
      "version": "1.1.0",
      "resolved": "https://registry.npmjs.org/@protobufjs/utf8/-/utf8-1.1.0.tgz",
      "integrity": "sha512-Vvn3zZrhQZkkBE8LSuW3em98c0FwgO4nxzv6OdSxPKJIEKY2bGbHn+mhGIPerzI4twdxaP8/0+06HBpwf345Lw=="
    },
    "@scarf/scarf": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/@scarf/scarf/-/scarf-1.1.1.tgz",
      "integrity": "sha512-VGbKDbk1RFIaSmdVb0cNjjWJoRWRI/Weo23AjRCC2nryO0iAS8pzsToJfPVPtVs74WHw4L1UTADNdIYRLkirZQ=="
    },
    "@sinclair/typebox": {
      "version": "0.25.21",
      "resolved": "https://registry.npmjs.org/@sinclair/typebox/-/typebox-0.25.21.tgz",
      "integrity": "sha512-gFukHN4t8K4+wVC+ECqeqwzBDeFeTzBXroBTqE6vcWrQGbEUpHO7LYdG0f4xnvYq4VOEwITSlHlp0JBAIFMS/g=="
    },
    "@sinonjs/commons": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/@sinonjs/commons/-/commons-2.0.0.tgz",
      "integrity": "sha512-uLa0j859mMrg2slwQYdO/AkrOfmH+X6LTVmNTS9CqexuE2IvVORIkSpJLqePAbEnKJ77aMmCwr1NUZ57120Xcg==",
      "requires": {
        "type-detect": "4.0.8"
      }
    },
    "@sinonjs/fake-timers": {
      "version": "10.0.2",
      "resolved": "https://registry.npmjs.org/@sinonjs/fake-timers/-/fake-timers-10.0.2.tgz",
      "integrity": "sha512-SwUDyjWnah1AaNl7kxsa7cfLhlTYoiyhDAIgyh+El30YvXs/o7OLXpYH88Zdhyx9JExKrmHDJ+10bwIcY80Jmw==",
      "requires": {
        "@sinonjs/commons": "^2.0.0"
      }
    },
    "@tsconfig/node10": {
      "version": "1.0.9",
      "resolved": "https://registry.npmjs.org/@tsconfig/node10/-/node10-1.0.9.tgz",
      "integrity": "sha512-jNsYVVxU8v5g43Erja32laIDHXeoNvFEpX33OK4d6hljo3jDhCBDhx5dhCCTMWUojscpAagGiRkBKxpdl9fxqA=="
    },
    "@tsconfig/node12": {
      "version": "1.0.11",
      "resolved": "https://registry.npmjs.org/@tsconfig/node12/-/node12-1.0.11.tgz",
      "integrity": "sha512-cqefuRsh12pWyGsIoBKJA9luFu3mRxCA+ORZvA4ktLSzIuCUtWVxGIuXigEwO5/ywWFMZ2QEGKWvkZG1zDMTag=="
    },
    "@tsconfig/node14": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/@tsconfig/node14/-/node14-1.0.3.tgz",
      "integrity": "sha512-ysT8mhdixWK6Hw3i1V2AeRqZ5WfXg1G43mqoYlM2nc6388Fq5jcXyr5mRsqViLx/GJYdoL0bfXD8nmF+Zn/Iow=="
    },
    "@tsconfig/node16": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/@tsconfig/node16/-/node16-1.0.3.tgz",
      "integrity": "sha512-yOlFc+7UtL/89t2ZhjPvvB/DeAr3r+Dq58IgzsFkOAvVC6NMJXmCGjbptdXdR9qsX7pKcTL+s87FtYREi2dEEQ=="
    },
    "@types/babel__core": {
      "version": "7.20.0",
      "resolved": "https://registry.npmjs.org/@types/babel__core/-/babel__core-7.20.0.tgz",
      "integrity": "sha512-+n8dL/9GWblDO0iU6eZAwEIJVr5DWigtle+Q6HLOrh/pdbXOhOtqzq8VPPE2zvNJzSKY4vH/z3iT3tn0A3ypiQ==",
      "requires": {
        "@babel/parser": "^7.20.7",
        "@babel/types": "^7.20.7",
        "@types/babel__generator": "*",
        "@types/babel__template": "*",
        "@types/babel__traverse": "*"
      }
    },
    "@types/babel__generator": {
      "version": "7.6.4",
      "resolved": "https://registry.npmjs.org/@types/babel__generator/-/babel__generator-7.6.4.tgz",
      "integrity": "sha512-tFkciB9j2K755yrTALxD44McOrk+gfpIpvC3sxHjRawj6PfnQxrse4Clq5y/Rq+G3mrBurMax/lG8Qn2t9mSsg==",
      "requires": {
        "@babel/types": "^7.0.0"
      }
    },
    "@types/babel__template": {
      "version": "7.4.1",
      "resolved": "https://registry.npmjs.org/@types/babel__template/-/babel__template-7.4.1.tgz",
      "integrity": "sha512-azBFKemX6kMg5Io+/rdGT0dkGreboUVR0Cdm3fz9QJWpaQGJRQXl7C+6hOTCZcMll7KFyEQpgbYI2lHdsS4U7g==",
      "requires": {
        "@babel/parser": "^7.1.0",
        "@babel/types": "^7.0.0"
      }
    },
    "@types/babel__traverse": {
      "version": "7.18.3",
      "resolved": "https://registry.npmjs.org/@types/babel__traverse/-/babel__traverse-7.18.3.tgz",
      "integrity": "sha512-1kbcJ40lLB7MHsj39U4Sh1uTd2E7rLEa79kmDpI6cy+XiXsteB3POdQomoq4FxszMrO3ZYchkhYJw7A2862b3w==",
      "requires": {
        "@babel/types": "^7.3.0"
      }
    },
    "@types/graceful-fs": {
      "version": "4.1.6",
      "resolved": "https://registry.npmjs.org/@types/graceful-fs/-/graceful-fs-4.1.6.tgz",
      "integrity": "sha512-Sig0SNORX9fdW+bQuTEovKj3uHcUL6LQKbCrrqb1X7J6/ReAbhCXRAhc+SMejhLELFj2QcyuxmUooZ4bt5ReSw==",
      "requires": {
        "@types/node": "*"
      }
    },
    "@types/istanbul-lib-coverage": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/@types/istanbul-lib-coverage/-/istanbul-lib-coverage-2.0.4.tgz",
      "integrity": "sha512-z/QT1XN4K4KYuslS23k62yDIDLwLFkzxOuMplDtObz0+y7VqJCaO2o+SPwHCvLFZh7xazvvoor2tA/hPz9ee7g=="
    },
    "@types/istanbul-lib-report": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/@types/istanbul-lib-report/-/istanbul-lib-report-3.0.0.tgz",
      "integrity": "sha512-plGgXAPfVKFoYfa9NpYDAkseG+g6Jr294RqeqcqDixSbU34MZVJRi/P+7Y8GDpzkEwLaGZZOpKIEmeVZNtKsrg==",
      "requires": {
        "@types/istanbul-lib-coverage": "*"
      }
    },
    "@types/istanbul-reports": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/@types/istanbul-reports/-/istanbul-reports-3.0.1.tgz",
      "integrity": "sha512-c3mAZEuK0lvBp8tmuL74XRKn1+y2dcwOUpH7x4WrF6gk1GIgiluDRgMYQtw2OFcBvAJWlt6ASU3tSqxp0Uu0Aw==",
      "requires": {
        "@types/istanbul-lib-report": "*"
      }
    },
    "@types/jest": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/@types/jest/-/jest-29.4.0.tgz",
      "integrity": "sha512-VaywcGQ9tPorCX/Jkkni7RWGFfI11whqzs8dvxF41P17Z+z872thvEvlIbznjPJ02kl1HMX3LmLOonsj2n7HeQ==",
      "requires": {
        "expect": "^29.0.0",
        "pretty-format": "^29.0.0"
      }
    },
    "@types/long": {
      "version": "4.0.2",
      "resolved": "https://registry.npmjs.org/@types/long/-/long-4.0.2.tgz",
      "integrity": "sha512-MqTGEo5bj5t157U6fA/BiDynNkn0YknVdh48CMPkTSpFTVmvao5UQmm7uEF6xBEo7qIMAlY/JSleYaE6VOdpaA=="
    },
    "@types/node": {
      "version": "18.11.18",
      "resolved": "https://registry.npmjs.org/@types/node/-/node-18.11.18.tgz",
      "integrity": "sha512-DHQpWGjyQKSHj3ebjFI/wRKcqQcdR+MoFBygntYOZytCqNfkd2ZC4ARDJ2DQqhjH5p85Nnd3jhUJIXrszFX/JA=="
    },
    "@types/prettier": {
      "version": "2.7.2",
      "resolved": "https://registry.npmjs.org/@types/prettier/-/prettier-2.7.2.tgz",
      "integrity": "sha512-KufADq8uQqo1pYKVIYzfKbJfBAc0sOeXqGbFaSpv8MRmC/zXgowNZmFcbngndGk922QDmOASEXUZCaY48gs4cg=="
    },
    "@types/qs": {
      "version": "6.9.7",
      "resolved": "https://registry.npmjs.org/@types/qs/-/qs-6.9.7.tgz",
      "integrity": "sha512-FGa1F62FT09qcrueBA6qYTrJPVDzah9a+493+o2PCXsesWHIn27G98TsSMs3WPNbZIEj4+VJf6saSFpvD+3Zsw=="
    },
    "@types/stack-utils": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/@types/stack-utils/-/stack-utils-2.0.1.tgz",
      "integrity": "sha512-Hl219/BT5fLAaz6NDkSuhzasy49dwQS/DSdu4MdggFB8zcXv7vflBI3xp7FEmkmdDkBUI2bPUNeMttp2knYdxw=="
    },
    "@types/tmp": {
      "version": "0.2.3",
      "resolved": "https://registry.npmjs.org/@types/tmp/-/tmp-0.2.3.tgz",
      "integrity": "sha512-dDZH/tXzwjutnuk4UacGgFRwV+JSLaXL1ikvidfJprkb7L9Nx1njcRHHmi3Dsvt7pgqqTEeucQuOrWHPFgzVHA=="
    },
    "@types/yargs": {
      "version": "17.0.22",
      "resolved": "https://registry.npmjs.org/@types/yargs/-/yargs-17.0.22.tgz",
      "integrity": "sha512-pet5WJ9U8yPVRhkwuEIp5ktAeAqRZOq4UdAyWLWzxbtpyXnzbtLdKiXAjJzi/KLmPGS9wk86lUFWZFN6sISo4g==",
      "requires": {
        "@types/yargs-parser": "*"
      }
    },
    "@types/yargs-parser": {
      "version": "21.0.0",
      "resolved": "https://registry.npmjs.org/@types/yargs-parser/-/yargs-parser-21.0.0.tgz",
      "integrity": "sha512-iO9ZQHkZxHn4mSakYV0vFHAVDyEOIJQrV2uZ06HxEPcx+mt8swXoZHIbaaJ2crJYFfErySgktuTZ3BeLz+XmFA=="
    },
    "acorn": {
      "version": "8.8.2",
      "resolved": "https://registry.npmjs.org/acorn/-/acorn-8.8.2.tgz",
      "integrity": "sha512-xjIYgE8HBrkpd/sJqOGNspf8uHG+NOHGOw6a/Urj8taM2EXfdNAH2oFcPeIFfsv3+kz/mJrS5VuMqbNLjCa2vw=="
    },
    "acorn-walk": {
      "version": "8.2.0",
      "resolved": "https://registry.npmjs.org/acorn-walk/-/acorn-walk-8.2.0.tgz",
      "integrity": "sha512-k+iyHEuPgSw6SbuDpGQM+06HQUa04DZ3o+F6CSzXMvvI5KMvnaEqXe+YVe555R9nn6GPt404fos4wcgpw12SDA=="
    },
    "ansi-colors": {
      "version": "4.1.3",
      "resolved": "https://registry.npmjs.org/ansi-colors/-/ansi-colors-4.1.3.tgz",
      "integrity": "sha512-/6w/C21Pm1A7aZitlI5Ni/2J6FFQN8i1Cvz3kHABAAbw93v/NlvKdVOqz7CCWz/3iv/JplRSEEZ83XION15ovw=="
    },
    "ansi-escapes": {
      "version": "4.3.2",
      "resolved": "https://registry.npmjs.org/ansi-escapes/-/ansi-escapes-4.3.2.tgz",
      "integrity": "sha512-gKXj5ALrKWQLsYG9jlTRmR/xKluxHV+Z9QEwNIgCfM1/uwPMCuzVVnh5mwTd+OuBZcwSIMbqssNWRm1lE51QaQ==",
      "requires": {
        "type-fest": "^0.21.3"
      }
    },
    "ansi-regex": {
      "version": "5.0.1",
      "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-5.0.1.tgz",
      "integrity": "sha512-quJQXlTSUGL2LH9SUXo8VwsY4soanhgo6LNSm84E1LBcE8s3O0wpdiRzyR9z/ZZJMlMWv37qOOb9pdJlMUEKFQ=="
    },
    "ansi-styles": {
      "version": "4.3.0",
      "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-4.3.0.tgz",
      "integrity": "sha512-zbB9rCJAT1rbjiVDb2hqKFHNYLxgtk8NURxZ3IZwD3F6NtxbXZQCnnSi1Lkx+IDohdPlFp222wVALIheZJQSEg==",
      "requires": {
        "color-convert": "^2.0.1"
      }
    },
    "anymatch": {
      "version": "3.1.3",
      "resolved": "https://registry.npmjs.org/anymatch/-/anymatch-3.1.3.tgz",
      "integrity": "sha512-KMReFUr0B4t+D+OBkjR3KYqvocp2XaSzO55UcB6mgQMd3KbcE+mWTyvVV7D/zsdEbNnV6acZUutkiHQXvTr1Rw==",
      "requires": {
        "normalize-path": "^3.0.0",
        "picomatch": "^2.0.4"
      }
    },
    "arg": {
      "version": "4.1.3",
      "resolved": "https://registry.npmjs.org/arg/-/arg-4.1.3.tgz",
      "integrity": "sha512-58S9QDqG0Xx27YwPSt9fJxivjYl432YCwfDMfZ+71RAqUrZef7LrKQZ3LHLOwCS4FLNBplP533Zx895SeOCHvA=="
    },
    "argparse": {
      "version": "1.0.10",
      "resolved": "https://registry.npmjs.org/argparse/-/argparse-1.0.10.tgz",
      "integrity": "sha512-o5Roy6tNG4SL/FOkCAN6RzjiakZS25RLYFrcMttJqbdd8BWrnA+fGz57iN5Pb06pvBGvl5gQ0B48dJlslXvoTg==",
      "requires": {
        "sprintf-js": "~1.0.2"
      }
    },
    "axios": {
      "version": "0.25.0",
      "resolved": "https://registry.npmjs.org/axios/-/axios-0.25.0.tgz",
      "integrity": "sha512-cD8FOb0tRH3uuEe6+evtAbgJtfxr7ly3fQjYcMcuPlgkwVS9xboaVIpcDV+cYQe+yGykgwZCs1pzjntcGa6l5g==",
      "requires": {
        "follow-redirects": "^1.14.7"
      }
    },
    "babel-jest": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/babel-jest/-/babel-jest-29.4.1.tgz",
      "integrity": "sha512-xBZa/pLSsF/1sNpkgsiT3CmY7zV1kAsZ9OxxtrFqYucnOuRftXAfcJqcDVyOPeN4lttWTwhLdu0T9f8uvoPEUg==",
      "requires": {
        "@jest/transform": "^29.4.1",
        "@types/babel__core": "^7.1.14",
        "babel-plugin-istanbul": "^6.1.1",
        "babel-preset-jest": "^29.4.0",
        "chalk": "^4.0.0",
        "graceful-fs": "^4.2.9",
        "slash": "^3.0.0"
      }
    },
    "babel-plugin-istanbul": {
      "version": "6.1.1",
      "resolved": "https://registry.npmjs.org/babel-plugin-istanbul/-/babel-plugin-istanbul-6.1.1.tgz",
      "integrity": "sha512-Y1IQok9821cC9onCx5otgFfRm7Lm+I+wwxOx738M/WLPZ9Q42m4IG5W0FNX8WLL2gYMZo3JkuXIH2DOpWM+qwA==",
      "requires": {
        "@babel/helper-plugin-utils": "^7.0.0",
        "@istanbuljs/load-nyc-config": "^1.0.0",
        "@istanbuljs/schema": "^0.1.2",
        "istanbul-lib-instrument": "^5.0.4",
        "test-exclude": "^6.0.0"
      }
    },
    "babel-plugin-jest-hoist": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/babel-plugin-jest-hoist/-/babel-plugin-jest-hoist-29.4.0.tgz",
      "integrity": "sha512-a/sZRLQJEmsmejQ2rPEUe35nO1+C9dc9O1gplH1SXmJxveQSRUYdBk8yGZG/VOUuZs1u2aHZJusEGoRMbhhwCg==",
      "requires": {
        "@babel/template": "^7.3.3",
        "@babel/types": "^7.3.3",
        "@types/babel__core": "^7.1.14",
        "@types/babel__traverse": "^7.0.6"
      }
    },
    "babel-preset-current-node-syntax": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/babel-preset-current-node-syntax/-/babel-preset-current-node-syntax-1.0.1.tgz",
      "integrity": "sha512-M7LQ0bxarkxQoN+vz5aJPsLBn77n8QgTFmo8WK0/44auK2xlCXrYcUxHFxgU7qW5Yzw/CjmLRK2uJzaCd7LvqQ==",
      "requires": {
        "@babel/plugin-syntax-async-generators": "^7.8.4",
        "@babel/plugin-syntax-bigint": "^7.8.3",
        "@babel/plugin-syntax-class-properties": "^7.8.3",
        "@babel/plugin-syntax-import-meta": "^7.8.3",
        "@babel/plugin-syntax-json-strings": "^7.8.3",
        "@babel/plugin-syntax-logical-assignment-operators": "^7.8.3",
        "@babel/plugin-syntax-nullish-coalescing-operator": "^7.8.3",
        "@babel/plugin-syntax-numeric-separator": "^7.8.3",
        "@babel/plugin-syntax-object-rest-spread": "^7.8.3",
        "@babel/plugin-syntax-optional-catch-binding": "^7.8.3",
        "@babel/plugin-syntax-optional-chaining": "^7.8.3",
        "@babel/plugin-syntax-top-level-await": "^7.8.3"
      }
    },
    "babel-preset-jest": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/babel-preset-jest/-/babel-preset-jest-29.4.0.tgz",
      "integrity": "sha512-fUB9vZflUSM3dO/6M2TCAepTzvA4VkOvl67PjErcrQMGt9Eve7uazaeyCZ2th3UtI7ljpiBJES0F7A1vBRsLZA==",
      "requires": {
        "babel-plugin-jest-hoist": "^29.4.0",
        "babel-preset-current-node-syntax": "^1.0.0"
      }
    },
    "balanced-match": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/balanced-match/-/balanced-match-1.0.2.tgz",
      "integrity": "sha512-3oSeUO0TMV67hN1AmbXsK4yaqU7tjiHlbxRDZOpH0KW9+CeX4bRAaX0Anxt0tx2MrpRpWwQaPwIlISEJhYU5Pw=="
    },
    "base64-js": {
      "version": "1.5.1",
      "resolved": "https://registry.npmjs.org/base64-js/-/base64-js-1.5.1.tgz",
      "integrity": "sha512-AKpaYlHn8t4SVbOHCy+b5+KKgvR4vrsD8vbvrbiQJps7fKDTkjkDry6ji0rUJjC0kzbNePLwzxq8iypo41qeWA=="
    },
    "base64url": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/base64url/-/base64url-3.0.1.tgz",
      "integrity": "sha512-ir1UPr3dkwexU7FdV8qBBbNDRUhMmIekYMFZfi+C/sLNnRESKPl23nB9b2pltqfOQNnGzsDdId90AEtG5tCx4A=="
    },
    "bl": {
      "version": "5.1.0",
      "resolved": "https://registry.npmjs.org/bl/-/bl-5.1.0.tgz",
      "integrity": "sha512-tv1ZJHLfTDnXE6tMHv73YgSJaWR2AFuPwMntBe7XL/GBFHnT0CLnsHMogfk5+GzCDC5ZWarSCYaIGATZt9dNsQ==",
      "requires": {
        "buffer": "^6.0.3",
        "inherits": "^2.0.4",
        "readable-stream": "^3.4.0"
      }
    },
    "blockstore-core": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/blockstore-core/-/blockstore-core-1.0.5.tgz",
      "integrity": "sha512-i/9CUMMvBALVbtSqUIuiWB3tk//a4Q2I2CEWiBuYNnhJvk/DWplXjLt8Sqc5VGkRVXVPSsEuH8fUtqJt5UFYcA==",
      "requires": {
        "err-code": "^3.0.1",
        "interface-blockstore": "^2.0.2",
        "interface-store": "^2.0.1",
        "it-all": "^1.0.4",
        "it-drain": "^1.0.4",
        "it-filter": "^1.0.2",
        "it-take": "^1.0.1",
        "multiformats": "^9.4.7"
      }
    },
    "brace-expansion": {
      "version": "1.1.11",
      "resolved": "https://registry.npmjs.org/brace-expansion/-/brace-expansion-1.1.11.tgz",
      "integrity": "sha512-iCuPHDFgrHX7H2vEI/5xpz07zSHB00TpugqhmYtVmMO6518mCuRMoOYFldEBl0g187ufozdaHgWKcYFb61qGiA==",
      "requires": {
        "balanced-match": "^1.0.0",
        "concat-map": "0.0.1"
      }
    },
    "braces": {
      "version": "3.0.2",
      "resolved": "https://registry.npmjs.org/braces/-/braces-3.0.2.tgz",
      "integrity": "sha512-b8um+L1RzM3WDSzvhm6gIz1yfTbBt6YTlcEKAvsmqCZZFw46z626lVj9j1yEPW33H5H+lBQpZMP1k8l+78Ha0A==",
      "requires": {
        "fill-range": "^7.0.1"
      }
    },
    "browserslist": {
      "version": "4.21.5",
      "resolved": "https://registry.npmjs.org/browserslist/-/browserslist-4.21.5.tgz",
      "integrity": "sha512-tUkiguQGW7S3IhB7N+c2MV/HZPSCPAAiYBZXLsBhFB/PCy6ZKKsZrmBayHV9fdGV/ARIfJ14NkxKzRDjvp7L6w==",
      "requires": {
        "caniuse-lite": "^1.0.30001449",
        "electron-to-chromium": "^1.4.284",
        "node-releases": "^2.0.8",
        "update-browserslist-db": "^1.0.10"
      }
    },
    "bs-logger": {
      "version": "0.2.6",
      "resolved": "https://registry.npmjs.org/bs-logger/-/bs-logger-0.2.6.tgz",
      "integrity": "sha512-pd8DCoxmbgc7hyPKOvxtqNcjYoOsABPQdcCUjGp3d42VR2CX1ORhk2A87oqqu5R1kk+76nsxZupkmyd+MVtCog==",
      "requires": {
        "fast-json-stable-stringify": "2.x"
      }
    },
    "bser": {
      "version": "2.1.1",
      "resolved": "https://registry.npmjs.org/bser/-/bser-2.1.1.tgz",
      "integrity": "sha512-gQxTNE/GAfIIrmHLUE3oJyp5FO6HRBfhjnw4/wMmA63ZGDJnWBmgY/lyQBpnDUkGmAhbSe39tx2d/iTOAfglwQ==",
      "requires": {
        "node-int64": "^0.4.0"
      }
    },
    "buffer": {
      "version": "6.0.3",
      "resolved": "https://registry.npmjs.org/buffer/-/buffer-6.0.3.tgz",
      "integrity": "sha512-FTiCpNxtwiZZHEZbcbTIcZjERVICn9yq/pDFkTl95/AxzD1naBctN7YO68riM/gLSDY7sdrMby8hofADYuuqOA==",
      "requires": {
        "base64-js": "^1.3.1",
        "ieee754": "^1.2.1"
      }
    },
    "buffer-from": {
      "version": "1.1.2",
      "resolved": "https://registry.npmjs.org/buffer-from/-/buffer-from-1.1.2.tgz",
      "integrity": "sha512-E+XQCRwSbaaiChtv6k6Dwgc+bx+Bs6vuKJHHl5kox/BaKbhiXzqQOwK4cO22yElGp2OCmjwVhT3HmxgyPGnJfQ=="
    },
    "call-bind": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/call-bind/-/call-bind-1.0.2.tgz",
      "integrity": "sha512-7O+FbCihrB5WGbFYesctwmTKae6rOiIzmz1icreWJ+0aA7LJfuqhEso2T9ncpcFtzMQtzXf2QGGueWJGTYsqrA==",
      "requires": {
        "function-bind": "^1.1.1",
        "get-intrinsic": "^1.0.2"
      }
    },
    "callsites": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/callsites/-/callsites-3.1.0.tgz",
      "integrity": "sha512-P8BjAsXvZS+VIDUI11hHCQEv74YT67YUi5JJFNWIqL235sBmjX4+qx9Muvls5ivyNENctx46xQLQ3aTuE7ssaQ=="
    },
    "camel-case": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/camel-case/-/camel-case-4.1.2.tgz",
      "integrity": "sha512-gxGWBrTT1JuMx6R+o5PTXMmUnhnVzLQ9SNutD4YqKtI6ap897t3tKECYla6gCWEkplXnlNybEkZg9GEGxKFCgw==",
      "requires": {
        "pascal-case": "^3.1.2",
        "tslib": "^2.0.3"
      }
    },
    "camelcase": {
      "version": "6.3.0",
      "resolved": "https://registry.npmjs.org/camelcase/-/camelcase-6.3.0.tgz",
      "integrity": "sha512-Gmy6FhYlCY7uOElZUSbxo2UCDH8owEk996gkbrpsgGtrJLM3J7jGxl9Ic7Qwwj4ivOE5AWZWRMecDdF7hqGjFA=="
    },
    "caniuse-lite": {
      "version": "1.0.30001450",
      "resolved": "https://registry.npmjs.org/caniuse-lite/-/caniuse-lite-1.0.30001450.tgz",
      "integrity": "sha512-qMBmvmQmFXaSxexkjjfMvD5rnDL0+m+dUMZKoDYsGG8iZN29RuYh9eRoMvKsT6uMAWlyUUGDEQGJJYjzCIO9ew=="
    },
    "capital-case": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/capital-case/-/capital-case-1.0.4.tgz",
      "integrity": "sha512-ds37W8CytHgwnhGGTi88pcPyR15qoNkOpYwmMMfnWqqWgESapLqvDx6huFjQ5vqWSn2Z06173XNA7LtMOeUh1A==",
      "requires": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3",
        "upper-case-first": "^2.0.2"
      }
    },
    "chalk": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/chalk/-/chalk-4.1.2.tgz",
      "integrity": "sha512-oKnbhFyRIXpUuez8iBMmyEa4nbj4IOQyuhc/wy9kY7/WVPcwIO9VA668Pu8RkO7+0G76SLROeyw9CpQ061i4mA==",
      "requires": {
        "ansi-styles": "^4.1.0",
        "supports-color": "^7.1.0"
      }
    },
    "change-case": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/change-case/-/change-case-4.1.2.tgz",
      "integrity": "sha512-bSxY2ws9OtviILG1EiY5K7NNxkqg/JnRnFxLtKQ96JaviiIxi7djMrSd0ECT9AC+lttClmYwKw53BWpOMblo7A==",
      "requires": {
        "camel-case": "^4.1.2",
        "capital-case": "^1.0.4",
        "constant-case": "^3.0.4",
        "dot-case": "^3.0.4",
        "header-case": "^2.0.4",
        "no-case": "^3.0.4",
        "param-case": "^3.0.4",
        "pascal-case": "^3.1.2",
        "path-case": "^3.0.4",
        "sentence-case": "^3.0.4",
        "snake-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "char-regex": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/char-regex/-/char-regex-1.0.2.tgz",
      "integrity": "sha512-kWWXztvZ5SBQV+eRgKFeh8q5sLuZY2+8WUIzlxWVTg+oGwY14qylx1KbKzHd8P6ZYkAg0xyIDU9JMHhyJMZ1jw=="
    },
    "ci-info": {
      "version": "3.7.1",
      "resolved": "https://registry.npmjs.org/ci-info/-/ci-info-3.7.1.tgz",
      "integrity": "sha512-4jYS4MOAaCIStSRwiuxc4B8MYhIe676yO1sYGzARnjXkWpmzZMMYxY6zu8WYWDhSuth5zhrQ1rhNSibyyvv4/w=="
    },
    "cjs-module-lexer": {
      "version": "1.2.2",
      "resolved": "https://registry.npmjs.org/cjs-module-lexer/-/cjs-module-lexer-1.2.2.tgz",
      "integrity": "sha512-cOU9usZw8/dXIXKtwa8pM0OTJQuJkxMN6w30csNRUerHfeQ5R6U3kkU/FtJeIf3M202OHfY2U8ccInBG7/xogA=="
    },
    "cli-cursor": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/cli-cursor/-/cli-cursor-4.0.0.tgz",
      "integrity": "sha512-VGtlMu3x/4DOtIUwEkRezxUZ2lBacNJCHash0N0WeZDBS+7Ux1dm3XWAgWYxLJFMMdOeXMHXorshEFhbMSGelg==",
      "requires": {
        "restore-cursor": "^4.0.0"
      }
    },
    "cli-spinners": {
      "version": "2.7.0",
      "resolved": "https://registry.npmjs.org/cli-spinners/-/cli-spinners-2.7.0.tgz",
      "integrity": "sha512-qu3pN8Y3qHNgE2AFweciB1IfMnmZ/fsNTEE+NOFjmGB2F/7rLhnhzppvpCnN4FovtP26k8lHyy9ptEbNwWFLzw=="
    },
    "cliui": {
      "version": "8.0.1",
      "resolved": "https://registry.npmjs.org/cliui/-/cliui-8.0.1.tgz",
      "integrity": "sha512-BSeNnyus75C4//NQ9gQt1/csTXyo/8Sb+afLAkzAptFuMsod9HFokGNudZpi/oQV73hnVK+sR+5PVRMd+Dr7YQ==",
      "requires": {
        "string-width": "^4.2.0",
        "strip-ansi": "^6.0.1",
        "wrap-ansi": "^7.0.0"
      }
    },
    "clone": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/clone/-/clone-1.0.4.tgz",
      "integrity": "sha512-JQHZ2QMW6l3aH/j6xCqQThY/9OH4D/9ls34cgkUBiEeocRTU04tHfKPBsUK1PqZCUQM7GiA0IIXJSuXHI64Kbg=="
    },
    "co": {
      "version": "4.6.0",
      "resolved": "https://registry.npmjs.org/co/-/co-4.6.0.tgz",
      "integrity": "sha512-QVb0dM5HvG+uaxitm8wONl7jltx8dqhfU33DcqtOZcLSVIKSDDLDi7+0LbAKiyI8hD9u42m2YxXSkMGWThaecQ=="
    },
    "collect-v8-coverage": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/collect-v8-coverage/-/collect-v8-coverage-1.0.1.tgz",
      "integrity": "sha512-iBPtljfCNcTKNAto0KEtDfZ3qzjJvqE3aTGZsbhjSBlorqpXJlaWWtPO35D+ZImoC3KWejX64o+yPGxhWSTzfg=="
    },
    "color-convert": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/color-convert/-/color-convert-2.0.1.tgz",
      "integrity": "sha512-RRECPsj7iu/xb5oKYcsFHSppFNnsj/52OVTRKb4zP5onXwVF3zVmmToNcOfGC+CRDpfK/U584fMg38ZHCaElKQ==",
      "requires": {
        "color-name": "~1.1.4"
      }
    },
    "color-name": {
      "version": "1.1.4",
      "resolved": "https://registry.npmjs.org/color-name/-/color-name-1.1.4.tgz",
      "integrity": "sha512-dOy+3AuW3a2wNbZHIuMZpTcgjGuLU/uBL/ubcZF9OXbDo8ff4O8yVp5Bf0efS8uEoYo5q4Fx7dY9OgQGXgAsQA=="
    },
    "concat-map": {
      "version": "0.0.1",
      "resolved": "https://registry.npmjs.org/concat-map/-/concat-map-0.0.1.tgz",
      "integrity": "sha512-/Srv4dswyQNBfohGpz9o6Yb3Gz3SrUDqBH5rTuhGR7ahtlbYKnVxw2bCFMRljaA7EXHaXZ8wsHdodFvbkhKmqg=="
    },
    "constant-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/constant-case/-/constant-case-3.0.4.tgz",
      "integrity": "sha512-I2hSBi7Vvs7BEuJDr5dDHfzb/Ruj3FyvFyh7KLilAjNQw3Be+xgqUBA2W6scVEcL0hL1dwPRtIqEPVUCKkSsyQ==",
      "requires": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3",
        "upper-case": "^2.0.2"
      }
    },
    "convert-source-map": {
      "version": "1.9.0",
      "resolved": "https://registry.npmjs.org/convert-source-map/-/convert-source-map-1.9.0.tgz",
      "integrity": "sha512-ASFBup0Mz1uyiIjANan1jzLQami9z1PoYSZCiiYW2FczPbenXc45FZdBZLzOT+r6+iciuEModtmCti+hjaAk0A=="
    },
    "create-require": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/create-require/-/create-require-1.1.1.tgz",
      "integrity": "sha512-dcKFX3jn0MpIaXjisoRvexIJVEKzaq7z2rZKxf+MSr9TkdmHmsU4m2lcLojrj/FHl8mk5VxMmYA+ftRkP/3oKQ=="
    },
    "cross-spawn": {
      "version": "7.0.3",
      "resolved": "https://registry.npmjs.org/cross-spawn/-/cross-spawn-7.0.3.tgz",
      "integrity": "sha512-iRDPJKUPVEND7dHPO8rkbOnPpyDygcDFtWjpeWNCgy8WP2rXcxXL8TskReQl6OrB2G7+UJrags1q15Fudc7G6w==",
      "requires": {
        "path-key": "^3.1.0",
        "shebang-command": "^2.0.0",
        "which": "^2.0.1"
      }
    },
    "dataloader": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/dataloader/-/dataloader-2.1.0.tgz",
      "integrity": "sha512-qTcEYLen3r7ojZNgVUaRggOI+KM7jrKxXeSHhogh/TWxYMeONEMqY+hmkobiYQozsGIyg9OYVzO4ZIfoB4I0pQ=="
    },
    "debug": {
      "version": "4.3.4",
      "resolved": "https://registry.npmjs.org/debug/-/debug-4.3.4.tgz",
      "integrity": "sha512-PRWFHuSU3eDtQJPvnNY7Jcket1j0t5OuOsFzPPzsekD52Zl8qUfFIPEiswXqIvHWGVHOgX+7G/vCNNhehwxfkQ==",
      "requires": {
        "ms": "2.1.2"
      }
    },
    "dedent": {
      "version": "0.7.0",
      "resolved": "https://registry.npmjs.org/dedent/-/dedent-0.7.0.tgz",
      "integrity": "sha512-Q6fKUPqnAHAyhiUgFU7BUzLiv0kd8saH9al7tnu5Q/okj6dnupxyTgFIBjVzJATdfIAm9NAsvXNzjaKa+bxVyA=="
    },
    "deepmerge": {
      "version": "4.3.0",
      "resolved": "https://registry.npmjs.org/deepmerge/-/deepmerge-4.3.0.tgz",
      "integrity": "sha512-z2wJZXrmeHdvYJp/Ux55wIjqo81G5Bp4c+oELTW+7ar6SogWHajt5a9gO3s3IDaGSAXjDk0vlQKN3rms8ab3og=="
    },
    "defaults": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/defaults/-/defaults-1.0.4.tgz",
      "integrity": "sha512-eFuaLoy/Rxalv2kr+lqMlUnrDWV+3j4pljOIJgLIhI058IQfWJ7vXhyEIHu+HtC738klGALYxOKDO0bQP3tg8A==",
      "requires": {
        "clone": "^1.0.2"
      }
    },
    "define-lazy-prop": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/define-lazy-prop/-/define-lazy-prop-2.0.0.tgz",
      "integrity": "sha512-Ds09qNh8yw3khSjiJjiUInaGX9xlqZDY7JVryGxdxV7NPeuqQfplOpQ66yJFZut3jLa5zOwkXw1g9EI2uKh4Og=="
    },
    "detect-newline": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/detect-newline/-/detect-newline-3.1.0.tgz",
      "integrity": "sha512-TLz+x/vEXm/Y7P7wn1EJFNLxYpUD4TgMosxY6fAVJUnJMbupHBOncxyWUG9OpTaH9EBD7uFI5LfEgmMOc54DsA=="
    },
    "diff": {
      "version": "4.0.2",
      "resolved": "https://registry.npmjs.org/diff/-/diff-4.0.2.tgz",
      "integrity": "sha512-58lmxKSA4BNyLz+HHMUzlOEpg09FV+ev6ZMe3vJihgdxzgcwZ8VoEEPmALCZG9LmqfVoNMMKpttIYTVG6uDY7A=="
    },
    "diff-sequences": {
      "version": "29.3.1",
      "resolved": "https://registry.npmjs.org/diff-sequences/-/diff-sequences-29.3.1.tgz",
      "integrity": "sha512-hlM3QR272NXCi4pq+N4Kok4kOp6EsgOM3ZSpJI7Da3UAs+Ttsi8MRmB6trM/lhyzUxGfOgnpkHtgqm5Q/CTcfQ=="
    },
    "dot-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/dot-case/-/dot-case-3.0.4.tgz",
      "integrity": "sha512-Kv5nKlh6yRrdrGvxeJ2e5y2eRUpkUosIW4A2AS38zwSz27zu7ufDwQPi5Jhs3XAlGNetl3bmnGhQsMtkKJnj3w==",
      "requires": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "electron-to-chromium": {
      "version": "1.4.284",
      "resolved": "https://registry.npmjs.org/electron-to-chromium/-/electron-to-chromium-1.4.284.tgz",
      "integrity": "sha512-M8WEXFuKXMYMVr45fo8mq0wUrrJHheiKZf6BArTKk9ZBYCKJEOU5H8cdWgDT+qCVZf7Na4lVUaZsA+h6uA9+PA=="
    },
    "emittery": {
      "version": "0.13.1",
      "resolved": "https://registry.npmjs.org/emittery/-/emittery-0.13.1.tgz",
      "integrity": "sha512-DeWwawk6r5yR9jFgnDKYt4sLS0LmHJJi3ZOnb5/JdbYwj3nW+FxQnHIjhBKz8YLC7oRNPVM9NQ47I3CVx34eqQ=="
    },
    "emoji-regex": {
      "version": "8.0.0",
      "resolved": "https://registry.npmjs.org/emoji-regex/-/emoji-regex-8.0.0.tgz",
      "integrity": "sha512-MSjYzcWNOA0ewAHpz0MxpYFvwg6yjy1NG3xteoqz644VCo/RPgnr1/GGt+ic3iJTzQ8Eu3TdM14SawnVUmGE6A=="
    },
    "enquirer": {
      "version": "2.3.6",
      "resolved": "https://registry.npmjs.org/enquirer/-/enquirer-2.3.6.tgz",
      "integrity": "sha512-yjNnPr315/FjS4zIsUxYguYUPP2e1NK4d7E7ZOLiyYCcbFBiTMyID+2wvm2w6+pZ/odMA7cRkjhsPbltwBOrLg==",
      "requires": {
        "ansi-colors": "^4.1.1"
      }
    },
    "err-code": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/err-code/-/err-code-3.0.1.tgz",
      "integrity": "sha512-GiaH0KJUewYok+eeY05IIgjtAe4Yltygk9Wqp1V5yVWLdhf0hYZchRjNIT9bb0mSwRcIusT3cx7PJUf3zEIfUA=="
    },
    "error-ex": {
      "version": "1.3.2",
      "resolved": "https://registry.npmjs.org/error-ex/-/error-ex-1.3.2.tgz",
      "integrity": "sha512-7dFHNmqeFSEt2ZBsCriorKnn3Z2pj+fd9kmI6QoWw4//DL+icEBfc0U7qJCisqrTsKTjw4fNFy2pW9OqStD84g==",
      "requires": {
        "is-arrayish": "^0.2.1"
      }
    },
    "escalade": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/escalade/-/escalade-3.1.1.tgz",
      "integrity": "sha512-k0er2gUkLf8O0zKJiAhmkTnJlTvINGv7ygDNPbeIsX/TJjGJZHuh9B2UxbsaEkmlEo9MfhrSzmhIlhRlI2GXnw=="
    },
    "escape-string-regexp": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/escape-string-regexp/-/escape-string-regexp-2.0.0.tgz",
      "integrity": "sha512-UpzcLCXolUWcNu5HtVMHYdXJjArjsF9C0aNnquZYY4uW/Vu0miy5YoWvbV345HauVvcAUnpRuhMMcqTcGOY2+w=="
    },
    "esprima": {
      "version": "4.0.1",
      "resolved": "https://registry.npmjs.org/esprima/-/esprima-4.0.1.tgz",
      "integrity": "sha512-eGuFFw7Upda+g4p+QHvnW0RyTX/SVeJBDM/gCtMARO0cLuT2HcEKnTPvhjV6aGeqrCB/sbNop0Kszm0jsaWU4A=="
    },
    "execa": {
      "version": "5.1.1",
      "resolved": "https://registry.npmjs.org/execa/-/execa-5.1.1.tgz",
      "integrity": "sha512-8uSpZZocAZRBAPIEINJj3Lo9HyGitllczc27Eh5YYojjMFMn8yHMDMaUHE2Jqfq05D/wucwI4JGURyXt1vchyg==",
      "requires": {
        "cross-spawn": "^7.0.3",
        "get-stream": "^6.0.0",
        "human-signals": "^2.1.0",
        "is-stream": "^2.0.0",
        "merge-stream": "^2.0.0",
        "npm-run-path": "^4.0.1",
        "onetime": "^5.1.2",
        "signal-exit": "^3.0.3",
        "strip-final-newline": "^2.0.0"
      }
    },
    "exit": {
      "version": "0.1.2",
      "resolved": "https://registry.npmjs.org/exit/-/exit-0.1.2.tgz",
      "integrity": "sha512-Zk/eNKV2zbjpKzrsQ+n1G6poVbErQxJ0LBOJXaKZ1EViLzH+hrLu9cdXI4zw9dBQJslwBEpbQ2P1oS7nDxs6jQ=="
    },
    "expect": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/expect/-/expect-29.4.1.tgz",
      "integrity": "sha512-OKrGESHOaMxK3b6zxIq9SOW8kEXztKff/Dvg88j4xIJxur1hspEbedVkR3GpHe5LO+WB2Qw7OWN0RMTdp6as5A==",
      "requires": {
        "@jest/expect-utils": "^29.4.1",
        "jest-get-type": "^29.2.0",
        "jest-matcher-utils": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-util": "^29.4.1"
      }
    },
    "fast-json-stable-stringify": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/fast-json-stable-stringify/-/fast-json-stable-stringify-2.1.0.tgz",
      "integrity": "sha512-lhd/wF+Lk98HZoTCtlVraHtfh5XYijIjalXck7saUtuanSDyLMxnHhSXEDJqHxD7msR8D0uCmqlkwjCV8xvwHw=="
    },
    "fb-watchman": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/fb-watchman/-/fb-watchman-2.0.2.tgz",
      "integrity": "sha512-p5161BqbuCaSnB8jIbzQHOlpgsPmK5rJVDfDKO91Axs5NC1uu3HRQm6wt9cd9/+GtQQIO53JdGXXoyDpTAsgYA==",
      "requires": {
        "bser": "2.1.1"
      }
    },
    "fill-range": {
      "version": "7.0.1",
      "resolved": "https://registry.npmjs.org/fill-range/-/fill-range-7.0.1.tgz",
      "integrity": "sha512-qOo9F+dMUmC2Lcb4BbVvnKJxTPjCm+RRpe4gDuGrzkL7mEVl/djYSu2OdQ2Pa302N4oqkSg9ir6jaLWJ2USVpQ==",
      "requires": {
        "to-regex-range": "^5.0.1"
      }
    },
    "find-up": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/find-up/-/find-up-4.1.0.tgz",
      "integrity": "sha512-PpOwAdQ/YlXQ2vj8a3h8IipDuYRi3wceVQQGYWxNINccq40Anw7BlsEXCMbt1Zt+OLA6Fq9suIpIWD0OsnISlw==",
      "requires": {
        "locate-path": "^5.0.0",
        "path-exists": "^4.0.0"
      }
    },
    "follow-redirects": {
      "version": "1.15.2",
      "resolved": "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.15.2.tgz",
      "integrity": "sha512-VQLG33o04KaQ8uYi2tVNbdrWp1QWxNNea+nmIB4EVM28v0hmP17z7aG1+wAkNzVq4KeXTq3221ye5qTJP91JwA=="
    },
    "fp-ts": {
      "version": "2.13.1",
      "resolved": "https://registry.npmjs.org/fp-ts/-/fp-ts-2.13.1.tgz",
      "integrity": "sha512-0eu5ULPS2c/jsa1lGFneEFFEdTbembJv8e4QKXeVJ3lm/5hyve06dlKZrpxmMwJt6rYen7sxmHHK2CLaXvWuWQ=="
    },
    "fs.realpath": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/fs.realpath/-/fs.realpath-1.0.0.tgz",
      "integrity": "sha512-OO0pH2lK6a0hZnAdau5ItzHPI6pUlvI7jMVnxUQRtw4owF2wk8lOSabtGDCTP4Ggrg2MbGnWO9X8K1t4+fGMDw=="
    },
    "function-bind": {
      "version": "1.1.1",
      "resolved": "https://registry.npmjs.org/function-bind/-/function-bind-1.1.1.tgz",
      "integrity": "sha512-yIovAzMX49sF8Yl58fSCWJ5svSLuaibPxXQJFLmBObTuCr0Mf1KiPopGM9NiFjiYBCbfaa2Fh6breQ6ANVTI0A=="
    },
    "gensync": {
      "version": "1.0.0-beta.2",
      "resolved": "https://registry.npmjs.org/gensync/-/gensync-1.0.0-beta.2.tgz",
      "integrity": "sha512-3hN7NaskYvMDLQY55gnW3NQ+mesEAepTqlg+VEbj7zzqEMBVNhzcGYYeqFo/TlYz6eQiFcp1HcsCZO+nGgS8zg=="
    },
    "get-caller-file": {
      "version": "2.0.5",
      "resolved": "https://registry.npmjs.org/get-caller-file/-/get-caller-file-2.0.5.tgz",
      "integrity": "sha512-DyFP3BM/3YHTQOCUL/w0OZHR0lpKeGrxotcHWcqNEdnltqFwXVfhEBQ94eIo34AfQpo0rGki4cyIiftY06h2Fg=="
    },
    "get-intrinsic": {
      "version": "1.2.0",
      "resolved": "https://registry.npmjs.org/get-intrinsic/-/get-intrinsic-1.2.0.tgz",
      "integrity": "sha512-L049y6nFOuom5wGyRc3/gdTLO94dySVKRACj1RmJZBQXlbTMhtNIgkWkUHq+jYmZvKf14EW1EoJnnjbmoHij0Q==",
      "requires": {
        "function-bind": "^1.1.1",
        "has": "^1.0.3",
        "has-symbols": "^1.0.3"
      }
    },
    "get-package-type": {
      "version": "0.1.0",
      "resolved": "https://registry.npmjs.org/get-package-type/-/get-package-type-0.1.0.tgz",
      "integrity": "sha512-pjzuKtY64GYfWizNAJ0fr9VqttZkNiK2iS430LtIHzjBEr6bX8Am2zm4sW4Ro5wjWW5cAlRL1qAMTcXbjNAO2Q=="
    },
    "get-stream": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/get-stream/-/get-stream-6.0.1.tgz",
      "integrity": "sha512-ts6Wi+2j3jQjqi70w5AlN8DFnkSwC+MqmxEzdEALB2qXZYV3X/b1CTfgPLGJNMeAWxdPfU8FO1ms3NUfaHCPYg=="
    },
    "glob": {
      "version": "7.2.3",
      "resolved": "https://registry.npmjs.org/glob/-/glob-7.2.3.tgz",
      "integrity": "sha512-nFR0zLpU2YCaRxwoCJvL6UvCH2JFyFVIvwTLsIf21AuHlMskA1hhTdk+LlYJtOlYt9v6dvszD2BGRqBL+iQK9Q==",
      "requires": {
        "fs.realpath": "^1.0.0",
        "inflight": "^1.0.4",
        "inherits": "2",
        "minimatch": "^3.1.1",
        "once": "^1.3.0",
        "path-is-absolute": "^1.0.0"
      }
    },
    "globals": {
      "version": "11.12.0",
      "resolved": "https://registry.npmjs.org/globals/-/globals-11.12.0.tgz",
      "integrity": "sha512-WOBp/EEGUiIsJSp7wcv/y6MO+lV9UoncWqxuFfm8eBwzWNgyfBd6Gz+IeKQ9jCmyhoH99g15M3T+QaVHFjizVA=="
    },
    "graceful-fs": {
      "version": "4.2.10",
      "resolved": "https://registry.npmjs.org/graceful-fs/-/graceful-fs-4.2.10.tgz",
      "integrity": "sha512-9ByhssR2fPVsNZj478qUUbKfmL0+t5BDVyjShtyZZLiK7ZDAArFFfopyOTj0M05wE2tJPisA4iTnnXl2YoPvOA=="
    },
    "hamt-sharding": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/hamt-sharding/-/hamt-sharding-2.0.1.tgz",
      "integrity": "sha512-vnjrmdXG9dDs1m/H4iJ6z0JFI2NtgsW5keRkTcM85NGak69Mkf5PHUqBz+Xs0T4sg0ppvj9O5EGAJo40FTxmmA==",
      "requires": {
        "sparse-array": "^1.3.1",
        "uint8arrays": "^3.0.0"
      }
    },
    "has": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/has/-/has-1.0.3.tgz",
      "integrity": "sha512-f2dvO0VU6Oej7RkWJGrehjbzMAjFp5/VKPp5tTpWIV4JHHZK1/BxbFRtf/siA2SWTe09caDmVtYYzWEIbBS4zw==",
      "requires": {
        "function-bind": "^1.1.1"
      }
    },
    "has-flag": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/has-flag/-/has-flag-4.0.0.tgz",
      "integrity": "sha512-EykJT/Q1KjTWctppgIAgfSO0tKVuZUjhgMr17kqTumMl6Afv3EISleU7qZUzoXDFTAHTDC4NOoG/ZxU3EvlMPQ=="
    },
    "has-symbols": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/has-symbols/-/has-symbols-1.0.3.tgz",
      "integrity": "sha512-l3LCuF6MgDNwTDKkdYGEihYjt5pRPbEg46rtlmnSPlUbgmB8LOIrKJbYYFBSbnPaJexMKtiPO8hmeRjRz2Td+A=="
    },
    "header-case": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/header-case/-/header-case-2.0.4.tgz",
      "integrity": "sha512-H/vuk5TEEVZwrR0lp2zed9OCo1uAILMlx0JEMgC26rzyJJ3N1v6XkwHHXJQdR2doSjcGPM6OKPYoJgf0plJ11Q==",
      "requires": {
        "capital-case": "^1.0.4",
        "tslib": "^2.0.3"
      }
    },
    "html-escaper": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/html-escaper/-/html-escaper-2.0.2.tgz",
      "integrity": "sha512-H2iMtd0I4Mt5eYiapRdIDjp+XzelXQ0tFE4JS7YFwFevXXMmOp9myNrUvCg0D6ws8iqkRPBfKHgbwig1SmlLfg=="
    },
    "human-signals": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/human-signals/-/human-signals-2.1.0.tgz",
      "integrity": "sha512-B4FFZ6q/T2jhhksgkbEW3HBvWIfDW85snkQgawt07S7J5QXTk6BkNV+0yAeZrM5QpMAdYlocGoljn0sJ/WQkFw=="
    },
    "ieee754": {
      "version": "1.2.1",
      "resolved": "https://registry.npmjs.org/ieee754/-/ieee754-1.2.1.tgz",
      "integrity": "sha512-dcyqhDvX1C46lXZcVqCpK+FtMRQVdIMN6/Df5js2zouUsqG7I6sFxitIC+7KYK29KdXOLHdu9zL4sFnoVQnqaA=="
    },
    "import-local": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/import-local/-/import-local-3.1.0.tgz",
      "integrity": "sha512-ASB07uLtnDs1o6EHjKpX34BKYDSqnFerfTOJL2HvMqF70LnxpjkzDB8J44oT9pu4AMPkQwf8jl6szgvNd2tRIg==",
      "requires": {
        "pkg-dir": "^4.2.0",
        "resolve-cwd": "^3.0.0"
      }
    },
    "imurmurhash": {
      "version": "0.1.4",
      "resolved": "https://registry.npmjs.org/imurmurhash/-/imurmurhash-0.1.4.tgz",
      "integrity": "sha512-JmXMZ6wuvDmLiHEml9ykzqO6lwFbof0GG4IkcGaENdCRDDmMVnny7s5HsIgHCbaq0w2MyPhDqkhTUgS2LU2PHA=="
    },
    "inflight": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/inflight/-/inflight-1.0.6.tgz",
      "integrity": "sha512-k92I/b08q4wvFscXCLvqfsHCrjrF7yiXsQuIVvVE7N82W3+aqpzuUdBbfhWcy/FZR3/4IgflMgKLOsvPDrGCJA==",
      "requires": {
        "once": "^1.3.0",
        "wrappy": "1"
      }
    },
    "inherits": {
      "version": "2.0.4",
      "resolved": "https://registry.npmjs.org/inherits/-/inherits-2.0.4.tgz",
      "integrity": "sha512-k/vGaX4/Yla3WzyMCvTQOXYeIHvqOKtnqBduzTHpzpQZzAskKMhZ2K+EnBiSM9zGSoIFeMpXKxa4dYeZIQqewQ=="
    },
    "interface-blockstore": {
      "version": "2.0.3",
      "resolved": "https://registry.npmjs.org/interface-blockstore/-/interface-blockstore-2.0.3.tgz",
      "integrity": "sha512-OwVUnlNcx7H5HloK0Myv6c/C1q9cNG11HX6afdeU6q6kbuNj8jKCwVnmJHhC94LZaJ+9hvVOk4IUstb3Esg81w==",
      "requires": {
        "interface-store": "^2.0.2",
        "multiformats": "^9.0.4"
      }
    },
    "interface-store": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/interface-store/-/interface-store-2.0.2.tgz",
      "integrity": "sha512-rScRlhDcz6k199EkHqT8NpM87ebN89ICOzILoBHgaG36/WX50N32BnU/kpZgCGPLhARRAWUUX5/cyaIjt7Kipg=="
    },
    "io-ts": {
      "version": "2.2.20",
      "resolved": "https://registry.npmjs.org/io-ts/-/io-ts-2.2.20.tgz",
      "integrity": "sha512-Rq2BsYmtwS5vVttie4rqrOCIfHCS9TgpRLFpKQCM1wZBBRY9nWVGmEvm2FnDbSE2un1UE39DvFpTR5UL47YDcA==",
      "requires": {}
    },
    "io-ts-reporters": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/io-ts-reporters/-/io-ts-reporters-2.0.1.tgz",
      "integrity": "sha512-RVpLstYBsmTGgCW9wJ5KVyN/eRnRUDp87Flt4D1O3aJ7oAnd8csq8aXuu7ZeNK8qEDKmjUl9oUuzfwikaNAMKQ==",
      "requires": {
        "@scarf/scarf": "^1.1.1"
      }
    },
    "ipfs-unixfs": {
      "version": "6.0.9",
      "resolved": "https://registry.npmjs.org/ipfs-unixfs/-/ipfs-unixfs-6.0.9.tgz",
      "integrity": "sha512-0DQ7p0/9dRB6XCb0mVCTli33GzIzSVx5udpJuVM47tGcD+W+Bl4LsnoLswd3ggNnNEakMv1FdoFITiEnchXDqQ==",
      "requires": {
        "err-code": "^3.0.1",
        "protobufjs": "^6.10.2"
      }
    },
    "ipfs-unixfs-importer": {
      "version": "9.0.10",
      "resolved": "https://registry.npmjs.org/ipfs-unixfs-importer/-/ipfs-unixfs-importer-9.0.10.tgz",
      "integrity": "sha512-W+tQTVcSmXtFh7FWYWwPBGXJ1xDgREbIyI1E5JzDcimZLIyT5gGMfxR3oKPxxWj+GKMpP5ilvMQrbsPzWcm3Fw==",
      "requires": {
        "@ipld/dag-pb": "^2.0.2",
        "@multiformats/murmur3": "^1.0.3",
        "bl": "^5.0.0",
        "err-code": "^3.0.1",
        "hamt-sharding": "^2.0.0",
        "interface-blockstore": "^2.0.3",
        "ipfs-unixfs": "^6.0.0",
        "it-all": "^1.0.5",
        "it-batch": "^1.0.8",
        "it-first": "^1.0.6",
        "it-parallel-batch": "^1.0.9",
        "merge-options": "^3.0.4",
        "multiformats": "^9.4.2",
        "rabin-wasm": "^0.1.4",
        "uint8arrays": "^3.0.0"
      }
    },
    "is-arrayish": {
      "version": "0.2.1",
      "resolved": "https://registry.npmjs.org/is-arrayish/-/is-arrayish-0.2.1.tgz",
      "integrity": "sha512-zz06S8t0ozoDXMG+ube26zeCTNXcKIPJZJi8hBrF4idCLms4CG9QtK7qBl1boi5ODzFpjswb5JPmHCbMpjaYzg=="
    },
    "is-core-module": {
      "version": "2.11.0",
      "resolved": "https://registry.npmjs.org/is-core-module/-/is-core-module-2.11.0.tgz",
      "integrity": "sha512-RRjxlvLDkD1YJwDbroBHMb+cukurkDWNyHx7D3oNB5x9rb5ogcksMC5wHCadcXoo67gVr/+3GFySh3134zi6rw==",
      "requires": {
        "has": "^1.0.3"
      }
    },
    "is-docker": {
      "version": "2.2.1",
      "resolved": "https://registry.npmjs.org/is-docker/-/is-docker-2.2.1.tgz",
      "integrity": "sha512-F+i2BKsFrH66iaUFc0woD8sLy8getkwTwtOBjvs56Cx4CgJDeKQeqfz8wAYiSb8JOprWhHH5p77PbmYCvvUuXQ=="
    },
    "is-fullwidth-code-point": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/is-fullwidth-code-point/-/is-fullwidth-code-point-3.0.0.tgz",
      "integrity": "sha512-zymm5+u+sCsSWyD9qNaejV3DFvhCKclKdizYaJUuHA83RLjb7nSuGnddCHGv0hk+KY7BMAlsWeK4Ueg6EV6XQg=="
    },
    "is-generator-fn": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/is-generator-fn/-/is-generator-fn-2.1.0.tgz",
      "integrity": "sha512-cTIB4yPYL/Grw0EaSzASzg6bBy9gqCofvWN8okThAYIxKJZC+udlRAmGbM0XLeniEJSs8uEgHPGuHSe1XsOLSQ=="
    },
    "is-interactive": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/is-interactive/-/is-interactive-2.0.0.tgz",
      "integrity": "sha512-qP1vozQRI+BMOPcjFzrjXuQvdak2pHNUMZoeG2eRbiSqyvbEf/wQtEOTOX1guk6E3t36RkaqiSt8A/6YElNxLQ=="
    },
    "is-number": {
      "version": "7.0.0",
      "resolved": "https://registry.npmjs.org/is-number/-/is-number-7.0.0.tgz",
      "integrity": "sha512-41Cifkg6e8TylSpdtTpeLVMqvSBEVzTttHvERD741+pnZ8ANv0004MRL43QKPDlK9cGvNp6NZWZUBlbGXYxxng=="
    },
    "is-plain-obj": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/is-plain-obj/-/is-plain-obj-2.1.0.tgz",
      "integrity": "sha512-YWnfyRwxL/+SsrWYfOpUtz5b3YD+nyfkHvjbcanzk8zgyO4ASD67uVMRt8k5bM4lLMDnXfriRhOpemw+NfT1eA=="
    },
    "is-stream": {
      "version": "2.0.1",
      "resolved": "https://registry.npmjs.org/is-stream/-/is-stream-2.0.1.tgz",
      "integrity": "sha512-hFoiJiTl63nn+kstHGBtewWSKnQLpyb155KHheA1l39uvtO9nWIop1p3udqPcUd/xbF1VLMO4n7OI6p7RbngDg=="
    },
    "is-unicode-supported": {
      "version": "1.3.0",
      "resolved": "https://registry.npmjs.org/is-unicode-supported/-/is-unicode-supported-1.3.0.tgz",
      "integrity": "sha512-43r2mRvz+8JRIKnWJ+3j8JtjRKZ6GmjzfaE/qiBJnikNnYv/6bagRJ1kUhNk8R5EX/GkobD+r+sfxCPJsiKBLQ=="
    },
    "is-wsl": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/is-wsl/-/is-wsl-2.2.0.tgz",
      "integrity": "sha512-fKzAra0rGJUUBwGBgNkHZuToZcn+TtXHpeCgmkMJMMYx1sQDYaCSyjJBSCa2nH1DGm7s3n1oBnohoVTBaN7Lww==",
      "requires": {
        "is-docker": "^2.0.0"
      }
    },
    "isexe": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/isexe/-/isexe-2.0.0.tgz",
      "integrity": "sha512-RHxMLp9lnKHGHRng9QFhRCMbYAcVpn69smSGcq3f36xjgVVWThj4qqLbTLlq7Ssj8B+fIQ1EuCEGI2lKsyQeIw=="
    },
    "isomorphic-fetch": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/isomorphic-fetch/-/isomorphic-fetch-3.0.0.tgz",
      "integrity": "sha512-qvUtwJ3j6qwsF3jLxkZ72qCgjMysPzDfeV240JHiGZsANBYd+EEuu35v7dfrJ9Up0Ak07D7GGSkGhCHTqg/5wA==",
      "requires": {
        "node-fetch": "^2.6.1",
        "whatwg-fetch": "^3.4.1"
      }
    },
    "istanbul-lib-coverage": {
      "version": "3.2.0",
      "resolved": "https://registry.npmjs.org/istanbul-lib-coverage/-/istanbul-lib-coverage-3.2.0.tgz",
      "integrity": "sha512-eOeJ5BHCmHYvQK7xt9GkdHuzuCGS1Y6g9Gvnx3Ym33fz/HpLRYxiS0wHNr+m/MBC8B647Xt608vCDEvhl9c6Mw=="
    },
    "istanbul-lib-instrument": {
      "version": "5.2.1",
      "resolved": "https://registry.npmjs.org/istanbul-lib-instrument/-/istanbul-lib-instrument-5.2.1.tgz",
      "integrity": "sha512-pzqtp31nLv/XFOzXGuvhCb8qhjmTVo5vjVk19XE4CRlSWz0KoeJ3bw9XsA7nOp9YBf4qHjwBxkDzKcME/J29Yg==",
      "requires": {
        "@babel/core": "^7.12.3",
        "@babel/parser": "^7.14.7",
        "@istanbuljs/schema": "^0.1.2",
        "istanbul-lib-coverage": "^3.2.0",
        "semver": "^6.3.0"
      }
    },
    "istanbul-lib-report": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/istanbul-lib-report/-/istanbul-lib-report-3.0.0.tgz",
      "integrity": "sha512-wcdi+uAKzfiGT2abPpKZ0hSU1rGQjUQnLvtY5MpQ7QCTahD3VODhcu4wcfY1YtkGaDD5yuydOLINXsfbus9ROw==",
      "requires": {
        "istanbul-lib-coverage": "^3.0.0",
        "make-dir": "^3.0.0",
        "supports-color": "^7.1.0"
      }
    },
    "istanbul-lib-source-maps": {
      "version": "4.0.1",
      "resolved": "https://registry.npmjs.org/istanbul-lib-source-maps/-/istanbul-lib-source-maps-4.0.1.tgz",
      "integrity": "sha512-n3s8EwkdFIJCG3BPKBYvskgXGoy88ARzvegkitk60NxRdwltLOTaH7CUiMRXvwYorl0Q712iEjcWB+fK/MrWVw==",
      "requires": {
        "debug": "^4.1.1",
        "istanbul-lib-coverage": "^3.0.0",
        "source-map": "^0.6.1"
      }
    },
    "istanbul-reports": {
      "version": "3.1.5",
      "resolved": "https://registry.npmjs.org/istanbul-reports/-/istanbul-reports-3.1.5.tgz",
      "integrity": "sha512-nUsEMa9pBt/NOHqbcbeJEgqIlY/K7rVWUX6Lql2orY5e9roQOthbR3vtY4zzf2orPELg80fnxxk9zUyPlgwD1w==",
      "requires": {
        "html-escaper": "^2.0.0",
        "istanbul-lib-report": "^3.0.0"
      }
    },
    "it-all": {
      "version": "1.0.6",
      "resolved": "https://registry.npmjs.org/it-all/-/it-all-1.0.6.tgz",
      "integrity": "sha512-3cmCc6Heqe3uWi3CVM/k51fa/XbMFpQVzFoDsV0IZNHSQDyAXl3c4MjHkFX5kF3922OGj7Myv1nSEUgRtcuM1A=="
    },
    "it-batch": {
      "version": "1.0.9",
      "resolved": "https://registry.npmjs.org/it-batch/-/it-batch-1.0.9.tgz",
      "integrity": "sha512-7Q7HXewMhNFltTsAMdSz6luNhyhkhEtGGbYek/8Xb/GiqYMtwUmopE1ocPSiJKKp3rM4Dt045sNFoUu+KZGNyA=="
    },
    "it-drain": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/it-drain/-/it-drain-1.0.5.tgz",
      "integrity": "sha512-r/GjkiW1bZswC04TNmUnLxa6uovme7KKwPhc+cb1hHU65E3AByypHH6Pm91WHuvqfFsm+9ws0kPtDBV3/8vmIg=="
    },
    "it-filter": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/it-filter/-/it-filter-1.0.3.tgz",
      "integrity": "sha512-EI3HpzUrKjTH01miLHWmhNWy3Xpbx4OXMXltgrNprL5lDpF3giVpHIouFpr5l+evXw6aOfxhnt01BIB+4VQA+w=="
    },
    "it-first": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/it-first/-/it-first-1.0.7.tgz",
      "integrity": "sha512-nvJKZoBpZD/6Rtde6FXqwDqDZGF1sCADmr2Zoc0hZsIvnE449gRFnGctxDf09Bzc/FWnHXAdaHVIetY6lrE0/g=="
    },
    "it-parallel-batch": {
      "version": "1.0.11",
      "resolved": "https://registry.npmjs.org/it-parallel-batch/-/it-parallel-batch-1.0.11.tgz",
      "integrity": "sha512-UWsWHv/kqBpMRmyZJzlmZeoAMA0F3SZr08FBdbhtbe+MtoEBgr/ZUAKrnenhXCBrsopy76QjRH2K/V8kNdupbQ==",
      "requires": {
        "it-batch": "^1.0.9"
      }
    },
    "it-take": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/it-take/-/it-take-1.0.2.tgz",
      "integrity": "sha512-u7I6qhhxH7pSevcYNaMECtkvZW365ARqAIt9K+xjdK1B2WUDEjQSfETkOCT8bxFq/59LqrN3cMLUtTgmDBaygw=="
    },
    "jest": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest/-/jest-29.4.1.tgz",
      "integrity": "sha512-cknimw7gAXPDOmj0QqztlxVtBVCw2lYY9CeIE5N6kD+kET1H4H79HSNISJmijb1HF+qk+G+ploJgiDi5k/fRlg==",
      "requires": {
        "@jest/core": "^29.4.1",
        "@jest/types": "^29.4.1",
        "import-local": "^3.0.2",
        "jest-cli": "^29.4.1"
      }
    },
    "jest-changed-files": {
      "version": "29.4.0",
      "resolved": "https://registry.npmjs.org/jest-changed-files/-/jest-changed-files-29.4.0.tgz",
      "integrity": "sha512-rnI1oPxgFghoz32Y8eZsGJMjW54UlqT17ycQeCEktcxxwqqKdlj9afl8LNeO0Pbu+h2JQHThQP0BzS67eTRx4w==",
      "requires": {
        "execa": "^5.0.0",
        "p-limit": "^3.1.0"
      }
    },
    "jest-circus": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-circus/-/jest-circus-29.4.1.tgz",
      "integrity": "sha512-v02NuL5crMNY4CGPHBEflLzl4v91NFb85a+dH9a1pUNx6Xjggrd8l9pPy4LZ1VYNRXlb+f65+7O/MSIbLir6pA==",
      "requires": {
        "@jest/environment": "^29.4.1",
        "@jest/expect": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "co": "^4.6.0",
        "dedent": "^0.7.0",
        "is-generator-fn": "^2.0.0",
        "jest-each": "^29.4.1",
        "jest-matcher-utils": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-runtime": "^29.4.1",
        "jest-snapshot": "^29.4.1",
        "jest-util": "^29.4.1",
        "p-limit": "^3.1.0",
        "pretty-format": "^29.4.1",
        "slash": "^3.0.0",
        "stack-utils": "^2.0.3"
      }
    },
    "jest-cli": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-cli/-/jest-cli-29.4.1.tgz",
      "integrity": "sha512-jz7GDIhtxQ37M+9dlbv5K+/FVcIo1O/b1sX3cJgzlQUf/3VG25nvuWzlDC4F1FLLzUThJeWLu8I7JF9eWpuURQ==",
      "requires": {
        "@jest/core": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/types": "^29.4.1",
        "chalk": "^4.0.0",
        "exit": "^0.1.2",
        "graceful-fs": "^4.2.9",
        "import-local": "^3.0.2",
        "jest-config": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-validate": "^29.4.1",
        "prompts": "^2.0.1",
        "yargs": "^17.3.1"
      }
    },
    "jest-config": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-config/-/jest-config-29.4.1.tgz",
      "integrity": "sha512-g7p3q4NuXiM4hrS4XFATTkd+2z0Ml2RhFmFPM8c3WyKwVDNszbl4E7cV7WIx1YZeqqCtqbtTtZhGZWJlJqngzg==",
      "requires": {
        "@babel/core": "^7.11.6",
        "@jest/test-sequencer": "^29.4.1",
        "@jest/types": "^29.4.1",
        "babel-jest": "^29.4.1",
        "chalk": "^4.0.0",
        "ci-info": "^3.2.0",
        "deepmerge": "^4.2.2",
        "glob": "^7.1.3",
        "graceful-fs": "^4.2.9",
        "jest-circus": "^29.4.1",
        "jest-environment-node": "^29.4.1",
        "jest-get-type": "^29.2.0",
        "jest-regex-util": "^29.2.0",
        "jest-resolve": "^29.4.1",
        "jest-runner": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-validate": "^29.4.1",
        "micromatch": "^4.0.4",
        "parse-json": "^5.2.0",
        "pretty-format": "^29.4.1",
        "slash": "^3.0.0",
        "strip-json-comments": "^3.1.1"
      }
    },
    "jest-diff": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-diff/-/jest-diff-29.4.1.tgz",
      "integrity": "sha512-uazdl2g331iY56CEyfbNA0Ut7Mn2ulAG5vUaEHXycf1L6IPyuImIxSz4F0VYBKi7LYIuxOwTZzK3wh5jHzASMw==",
      "requires": {
        "chalk": "^4.0.0",
        "diff-sequences": "^29.3.1",
        "jest-get-type": "^29.2.0",
        "pretty-format": "^29.4.1"
      }
    },
    "jest-docblock": {
      "version": "29.2.0",
      "resolved": "https://registry.npmjs.org/jest-docblock/-/jest-docblock-29.2.0.tgz",
      "integrity": "sha512-bkxUsxTgWQGbXV5IENmfiIuqZhJcyvF7tU4zJ/7ioTutdz4ToB5Yx6JOFBpgI+TphRY4lhOyCWGNH/QFQh5T6A==",
      "requires": {
        "detect-newline": "^3.0.0"
      }
    },
    "jest-each": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-each/-/jest-each-29.4.1.tgz",
      "integrity": "sha512-QlYFiX3llJMWUV0BtWht/esGEz9w+0i7BHwODKCze7YzZzizgExB9MOfiivF/vVT0GSQ8wXLhvHXh3x2fVD4QQ==",
      "requires": {
        "@jest/types": "^29.4.1",
        "chalk": "^4.0.0",
        "jest-get-type": "^29.2.0",
        "jest-util": "^29.4.1",
        "pretty-format": "^29.4.1"
      }
    },
    "jest-environment-node": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-environment-node/-/jest-environment-node-29.4.1.tgz",
      "integrity": "sha512-x/H2kdVgxSkxWAIlIh9MfMuBa0hZySmfsC5lCsWmWr6tZySP44ediRKDUiNggX/eHLH7Cd5ZN10Rw+XF5tXsqg==",
      "requires": {
        "@jest/environment": "^29.4.1",
        "@jest/fake-timers": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "jest-mock": "^29.4.1",
        "jest-util": "^29.4.1"
      }
    },
    "jest-get-type": {
      "version": "29.2.0",
      "resolved": "https://registry.npmjs.org/jest-get-type/-/jest-get-type-29.2.0.tgz",
      "integrity": "sha512-uXNJlg8hKFEnDgFsrCjznB+sTxdkuqiCL6zMgA75qEbAJjJYTs9XPrvDctrEig2GDow22T/LvHgO57iJhXB/UA=="
    },
    "jest-haste-map": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-haste-map/-/jest-haste-map-29.4.1.tgz",
      "integrity": "sha512-imTjcgfVVTvg02khXL11NNLTx9ZaofbAWhilrMg/G8dIkp+HYCswhxf0xxJwBkfhWb3e8dwbjuWburvxmcr58w==",
      "requires": {
        "@jest/types": "^29.4.1",
        "@types/graceful-fs": "^4.1.3",
        "@types/node": "*",
        "anymatch": "^3.0.3",
        "fb-watchman": "^2.0.0",
        "fsevents": "^2.3.2",
        "graceful-fs": "^4.2.9",
        "jest-regex-util": "^29.2.0",
        "jest-util": "^29.4.1",
        "jest-worker": "^29.4.1",
        "micromatch": "^4.0.4",
        "walker": "^1.0.8"
      }
    },
    "jest-leak-detector": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-leak-detector/-/jest-leak-detector-29.4.1.tgz",
      "integrity": "sha512-akpZv7TPyGMnH2RimOCgy+hPmWZf55EyFUvymQ4LMsQP8xSPlZumCPtXGoDhFNhUE2039RApZkTQDKU79p/FiQ==",
      "requires": {
        "jest-get-type": "^29.2.0",
        "pretty-format": "^29.4.1"
      }
    },
    "jest-matcher-utils": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-matcher-utils/-/jest-matcher-utils-29.4.1.tgz",
      "integrity": "sha512-k5h0u8V4nAEy6lSACepxL/rw78FLDkBnXhZVgFneVpnJONhb2DhZj/Gv4eNe+1XqQ5IhgUcqj745UwH0HJmMnA==",
      "requires": {
        "chalk": "^4.0.0",
        "jest-diff": "^29.4.1",
        "jest-get-type": "^29.2.0",
        "pretty-format": "^29.4.1"
      }
    },
    "jest-message-util": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-message-util/-/jest-message-util-29.4.1.tgz",
      "integrity": "sha512-H4/I0cXUaLeCw6FM+i4AwCnOwHRgitdaUFOdm49022YD5nfyr8C/DrbXOBEyJaj+w/y0gGJ57klssOaUiLLQGQ==",
      "requires": {
        "@babel/code-frame": "^7.12.13",
        "@jest/types": "^29.4.1",
        "@types/stack-utils": "^2.0.0",
        "chalk": "^4.0.0",
        "graceful-fs": "^4.2.9",
        "micromatch": "^4.0.4",
        "pretty-format": "^29.4.1",
        "slash": "^3.0.0",
        "stack-utils": "^2.0.3"
      }
    },
    "jest-mock": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-mock/-/jest-mock-29.4.1.tgz",
      "integrity": "sha512-MwA4hQ7zBOcgVCVnsM8TzaFLVUD/pFWTfbkY953Y81L5ret3GFRZtmPmRFAjKQSdCKoJvvqOu6Bvfpqlwwb0dQ==",
      "requires": {
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "jest-util": "^29.4.1"
      }
    },
    "jest-pnp-resolver": {
      "version": "1.2.3",
      "resolved": "https://registry.npmjs.org/jest-pnp-resolver/-/jest-pnp-resolver-1.2.3.tgz",
      "integrity": "sha512-+3NpwQEnRoIBtx4fyhblQDPgJI0H1IEIkX7ShLUjPGA7TtUTvI1oiKi3SR4oBR0hQhQR80l4WAe5RrXBwWMA8w==",
      "requires": {}
    },
    "jest-regex-util": {
      "version": "29.2.0",
      "resolved": "https://registry.npmjs.org/jest-regex-util/-/jest-regex-util-29.2.0.tgz",
      "integrity": "sha512-6yXn0kg2JXzH30cr2NlThF+70iuO/3irbaB4mh5WyqNIvLLP+B6sFdluO1/1RJmslyh/f9osnefECflHvTbwVA=="
    },
    "jest-resolve": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-resolve/-/jest-resolve-29.4.1.tgz",
      "integrity": "sha512-j/ZFNV2lm9IJ2wmlq1uYK0Y/1PiyDq9g4HEGsNTNr3viRbJdV+8Lf1SXIiLZXFvyiisu0qUyIXGBnw+OKWkJwQ==",
      "requires": {
        "chalk": "^4.0.0",
        "graceful-fs": "^4.2.9",
        "jest-haste-map": "^29.4.1",
        "jest-pnp-resolver": "^1.2.2",
        "jest-util": "^29.4.1",
        "jest-validate": "^29.4.1",
        "resolve": "^1.20.0",
        "resolve.exports": "^2.0.0",
        "slash": "^3.0.0"
      }
    },
    "jest-resolve-dependencies": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-resolve-dependencies/-/jest-resolve-dependencies-29.4.1.tgz",
      "integrity": "sha512-Y3QG3M1ncAMxfjbYgtqNXC5B595zmB6e//p/qpA/58JkQXu/IpLDoLeOa8YoYfsSglBKQQzNUqtfGJJT/qLmJg==",
      "requires": {
        "jest-regex-util": "^29.2.0",
        "jest-snapshot": "^29.4.1"
      }
    },
    "jest-runner": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-runner/-/jest-runner-29.4.1.tgz",
      "integrity": "sha512-8d6XXXi7GtHmsHrnaqBKWxjKb166Eyj/ksSaUYdcBK09VbjPwIgWov1VwSmtupCIz8q1Xv4Qkzt/BTo3ZqiCeg==",
      "requires": {
        "@jest/console": "^29.4.1",
        "@jest/environment": "^29.4.1",
        "@jest/test-result": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "emittery": "^0.13.1",
        "graceful-fs": "^4.2.9",
        "jest-docblock": "^29.2.0",
        "jest-environment-node": "^29.4.1",
        "jest-haste-map": "^29.4.1",
        "jest-leak-detector": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-resolve": "^29.4.1",
        "jest-runtime": "^29.4.1",
        "jest-util": "^29.4.1",
        "jest-watcher": "^29.4.1",
        "jest-worker": "^29.4.1",
        "p-limit": "^3.1.0",
        "source-map-support": "0.5.13"
      }
    },
    "jest-runtime": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-runtime/-/jest-runtime-29.4.1.tgz",
      "integrity": "sha512-UXTMU9uKu2GjYwTtoAw5rn4STxWw/nadOfW7v1sx6LaJYa3V/iymdCLQM6xy3+7C6mY8GfX22vKpgxY171UIoA==",
      "requires": {
        "@jest/environment": "^29.4.1",
        "@jest/fake-timers": "^29.4.1",
        "@jest/globals": "^29.4.1",
        "@jest/source-map": "^29.2.0",
        "@jest/test-result": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "cjs-module-lexer": "^1.0.0",
        "collect-v8-coverage": "^1.0.0",
        "glob": "^7.1.3",
        "graceful-fs": "^4.2.9",
        "jest-haste-map": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-mock": "^29.4.1",
        "jest-regex-util": "^29.2.0",
        "jest-resolve": "^29.4.1",
        "jest-snapshot": "^29.4.1",
        "jest-util": "^29.4.1",
        "semver": "^7.3.5",
        "slash": "^3.0.0",
        "strip-bom": "^4.0.0"
      },
      "dependencies": {
        "semver": {
          "version": "7.3.8",
          "resolved": "https://registry.npmjs.org/semver/-/semver-7.3.8.tgz",
          "integrity": "sha512-NB1ctGL5rlHrPJtFDVIVzTyQylMLu9N9VICA6HSFJo8MCGVTMW6gfpicwKmmK/dAjTOrqu5l63JJOpDSrAis3A==",
          "requires": {
            "lru-cache": "^6.0.0"
          }
        }
      }
    },
    "jest-snapshot": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-snapshot/-/jest-snapshot-29.4.1.tgz",
      "integrity": "sha512-l4iV8EjGgQWVz3ee/LR9sULDk2pCkqb71bjvlqn+qp90lFwpnulHj4ZBT8nm1hA1C5wowXLc7MGnw321u0tsYA==",
      "requires": {
        "@babel/core": "^7.11.6",
        "@babel/generator": "^7.7.2",
        "@babel/plugin-syntax-jsx": "^7.7.2",
        "@babel/plugin-syntax-typescript": "^7.7.2",
        "@babel/traverse": "^7.7.2",
        "@babel/types": "^7.3.3",
        "@jest/expect-utils": "^29.4.1",
        "@jest/transform": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/babel__traverse": "^7.0.6",
        "@types/prettier": "^2.1.5",
        "babel-preset-current-node-syntax": "^1.0.0",
        "chalk": "^4.0.0",
        "expect": "^29.4.1",
        "graceful-fs": "^4.2.9",
        "jest-diff": "^29.4.1",
        "jest-get-type": "^29.2.0",
        "jest-haste-map": "^29.4.1",
        "jest-matcher-utils": "^29.4.1",
        "jest-message-util": "^29.4.1",
        "jest-util": "^29.4.1",
        "natural-compare": "^1.4.0",
        "pretty-format": "^29.4.1",
        "semver": "^7.3.5"
      },
      "dependencies": {
        "semver": {
          "version": "7.3.8",
          "resolved": "https://registry.npmjs.org/semver/-/semver-7.3.8.tgz",
          "integrity": "sha512-NB1ctGL5rlHrPJtFDVIVzTyQylMLu9N9VICA6HSFJo8MCGVTMW6gfpicwKmmK/dAjTOrqu5l63JJOpDSrAis3A==",
          "requires": {
            "lru-cache": "^6.0.0"
          }
        }
      }
    },
    "jest-util": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-util/-/jest-util-29.4.1.tgz",
      "integrity": "sha512-bQy9FPGxVutgpN4VRc0hk6w7Hx/m6L53QxpDreTZgJd9gfx/AV2MjyPde9tGyZRINAUrSv57p2inGBu2dRLmkQ==",
      "requires": {
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "chalk": "^4.0.0",
        "ci-info": "^3.2.0",
        "graceful-fs": "^4.2.9",
        "picomatch": "^2.2.3"
      }
    },
    "jest-validate": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-validate/-/jest-validate-29.4.1.tgz",
      "integrity": "sha512-qNZXcZQdIQx4SfUB/atWnI4/I2HUvhz8ajOSYUu40CSmf9U5emil8EDHgE7M+3j9/pavtk3knlZBDsgFvv/SWw==",
      "requires": {
        "@jest/types": "^29.4.1",
        "camelcase": "^6.2.0",
        "chalk": "^4.0.0",
        "jest-get-type": "^29.2.0",
        "leven": "^3.1.0",
        "pretty-format": "^29.4.1"
      }
    },
    "jest-watcher": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-watcher/-/jest-watcher-29.4.1.tgz",
      "integrity": "sha512-vFOzflGFs27nU6h8dpnVRER3O2rFtL+VMEwnG0H3KLHcllLsU8y9DchSh0AL/Rg5nN1/wSiQ+P4ByMGpuybaVw==",
      "requires": {
        "@jest/test-result": "^29.4.1",
        "@jest/types": "^29.4.1",
        "@types/node": "*",
        "ansi-escapes": "^4.2.1",
        "chalk": "^4.0.0",
        "emittery": "^0.13.1",
        "jest-util": "^29.4.1",
        "string-length": "^4.0.1"
      }
    },
    "jest-worker": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/jest-worker/-/jest-worker-29.4.1.tgz",
      "integrity": "sha512-O9doU/S1EBe+yp/mstQ0VpPwpv0Clgn68TkNwGxL6/usX/KUW9Arnn4ag8C3jc6qHcXznhsT5Na1liYzAsuAbQ==",
      "requires": {
        "@types/node": "*",
        "jest-util": "^29.4.1",
        "merge-stream": "^2.0.0",
        "supports-color": "^8.0.0"
      },
      "dependencies": {
        "supports-color": {
          "version": "8.1.1",
          "resolved": "https://registry.npmjs.org/supports-color/-/supports-color-8.1.1.tgz",
          "integrity": "sha512-MpUEN2OodtUzxvKQl72cUF7RQ5EiHsGvSsVG0ia9c5RbWGL2CI4C7EpPS8UTBIplnlzZiNuV56w+FuNxy3ty2Q==",
          "requires": {
            "has-flag": "^4.0.0"
          }
        }
      }
    },
    "js-tokens": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/js-tokens/-/js-tokens-4.0.0.tgz",
      "integrity": "sha512-RdJUflcE3cUzKiMqQgsCu06FPu9UdIJO0beYbPhHN4k6apgJtifcoCtT9bcxOpYBtpD2kCM6Sbzg4CausW/PKQ=="
    },
    "js-yaml": {
      "version": "3.14.1",
      "resolved": "https://registry.npmjs.org/js-yaml/-/js-yaml-3.14.1.tgz",
      "integrity": "sha512-okMH7OXXJ7YrN9Ok3/SXrnu4iX9yOk+25nqX4imS2npuvTYDmo/QEZoqwZkYaIDk3jVvBOTOIEgEhaLOynBS9g==",
      "requires": {
        "argparse": "^1.0.7",
        "esprima": "^4.0.0"
      }
    },
    "jsesc": {
      "version": "2.5.2",
      "resolved": "https://registry.npmjs.org/jsesc/-/jsesc-2.5.2.tgz",
      "integrity": "sha512-OYu7XEzjkCQ3C5Ps3QIZsQfNpqoJyZZA99wd9aWd05NCtC5pWOkShK2mkL6HXQR6/Cy2lbNdPlZBpuQHXE63gA=="
    },
    "json-parse-even-better-errors": {
      "version": "2.3.1",
      "resolved": "https://registry.npmjs.org/json-parse-even-better-errors/-/json-parse-even-better-errors-2.3.1.tgz",
      "integrity": "sha512-xyFwyhro/JEof6Ghe2iz2NcXoj2sloNsWr/XsERDK/oiPCfaNhl5ONfp+jQdAZRQQ0IJWNzH9zIZF7li91kh2w=="
    },
    "json5": {
      "version": "2.2.3",
      "resolved": "https://registry.npmjs.org/json5/-/json5-2.2.3.tgz",
      "integrity": "sha512-XmOWe7eyHYH14cLdVPoyg+GOH3rYX++KpzrylJwSW98t3Nk+U8XOl8FWKOgwtzdb8lXGf6zYwDUzeHMWfxasyg=="
    },
    "jssha": {
      "version": "3.2.0",
      "resolved": "https://registry.npmjs.org/jssha/-/jssha-3.2.0.tgz",
      "integrity": "sha512-QuruyBENDWdN4tZwJbQq7/eAK85FqrI4oDbXjy5IBhYD+2pTJyBUWZe8ctWaCkrV0gy6AaelgOZZBMeswEa/6Q=="
    },
    "kleur": {
      "version": "3.0.3",
      "resolved": "https://registry.npmjs.org/kleur/-/kleur-3.0.3.tgz",
      "integrity": "sha512-eTIzlVOSUR+JxdDFepEYcBMtZ9Qqdef+rnzWdRZuMbOywu5tO2w2N7rqjoANZ5k9vywhL6Br1VRjUIgTQx4E8w=="
    },
    "leven": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/leven/-/leven-3.1.0.tgz",
      "integrity": "sha512-qsda+H8jTaUaN/x5vzW2rzc+8Rw4TAQ/4KjB46IwK5VH+IlVeeeje/EoZRpiXvIqjFgK84QffqPztGI3VBLG1A=="
    },
    "lines-and-columns": {
      "version": "1.2.4",
      "resolved": "https://registry.npmjs.org/lines-and-columns/-/lines-and-columns-1.2.4.tgz",
      "integrity": "sha512-7ylylesZQ/PV29jhEDl3Ufjo6ZX7gCqJr5F7PKrqc93v7fzSymt1BpwEU8nAUXs8qzzvqhbjhK5QZg6Mt/HkBg=="
    },
    "locate-path": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/locate-path/-/locate-path-5.0.0.tgz",
      "integrity": "sha512-t7hw9pI+WvuwNJXwk5zVHpyhIqzg2qTlklJOf0mVxGSbe3Fp2VieZcduNYjaLDoy6p9uGpQEGWG87WpMKlNq8g==",
      "requires": {
        "p-locate": "^4.1.0"
      }
    },
    "lodash.memoize": {
      "version": "4.1.2",
      "resolved": "https://registry.npmjs.org/lodash.memoize/-/lodash.memoize-4.1.2.tgz",
      "integrity": "sha512-t7j+NzmgnQzTAYXcsHYLgimltOV1MXHtlOWf6GjL9Kj8GK5FInw5JotxvbOs+IvV1/Dzo04/fCGfLVs7aXb4Ag=="
    },
    "log-symbols": {
      "version": "5.1.0",
      "resolved": "https://registry.npmjs.org/log-symbols/-/log-symbols-5.1.0.tgz",
      "integrity": "sha512-l0x2DvrW294C9uDCoQe1VSU4gf529FkSZ6leBl4TiqZH/e+0R7hSfHQBNut2mNygDgHwvYHfFLn6Oxb3VWj2rA==",
      "requires": {
        "chalk": "^5.0.0",
        "is-unicode-supported": "^1.1.0"
      },
      "dependencies": {
        "chalk": {
          "version": "5.2.0",
          "resolved": "https://registry.npmjs.org/chalk/-/chalk-5.2.0.tgz",
          "integrity": "sha512-ree3Gqw/nazQAPuJJEy+avdl7QfZMcUvmHIKgEZkGL+xOBzRvup5Hxo6LHuMceSxOabuJLJm5Yp/92R9eMmMvA=="
        }
      }
    },
    "long": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/long/-/long-4.0.0.tgz",
      "integrity": "sha512-XsP+KhQif4bjX1kbuSiySJFNAehNxgLb6hPRGJ9QsUr8ajHkuXGdrHmFUTUUXhDwVX2R5bY4JNZEwbUiMhV+MA=="
    },
    "lower-case": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/lower-case/-/lower-case-2.0.2.tgz",
      "integrity": "sha512-7fm3l3NAF9WfN6W3JOmf5drwpVqX78JtoGJ3A6W0a6ZnldM41w2fV5D490psKFTpMds8TJse/eHLFFsNHHjHgg==",
      "requires": {
        "tslib": "^2.0.3"
      }
    },
    "lru-cache": {
      "version": "6.0.0",
      "resolved": "https://registry.npmjs.org/lru-cache/-/lru-cache-6.0.0.tgz",
      "integrity": "sha512-Jo6dJ04CmSjuznwJSS3pUeWmd/H0ffTlkXXgwZi+eq1UCmqQwCh+eLsYOYCwY991i2Fah4h1BEMCx4qThGbsiA==",
      "requires": {
        "yallist": "^4.0.0"
      }
    },
    "make-dir": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/make-dir/-/make-dir-3.1.0.tgz",
      "integrity": "sha512-g3FeP20LNwhALb/6Cz6Dd4F2ngze0jz7tbzrD2wAV+o9FeNHe4rL+yK2md0J/fiSf1sa1ADhXqi5+oVwOM/eGw==",
      "requires": {
        "semver": "^6.0.0"
      }
    },
    "make-error": {
      "version": "1.3.6",
      "resolved": "https://registry.npmjs.org/make-error/-/make-error-1.3.6.tgz",
      "integrity": "sha512-s8UhlNe7vPKomQhC1qFelMokr/Sc3AgNbso3n74mVPA5LTZwkB9NlXf4XPamLxJE8h0gh73rM94xvwRT2CVInw=="
    },
    "makeerror": {
      "version": "1.0.12",
      "resolved": "https://registry.npmjs.org/makeerror/-/makeerror-1.0.12.tgz",
      "integrity": "sha512-JmqCvUhmt43madlpFzG4BQzG2Z3m6tvQDNKdClZnO3VbIudJYmxsT0FNJMeiB2+JTSlTQTSbU8QdesVmwJcmLg==",
      "requires": {
        "tmpl": "1.0.5"
      }
    },
    "merge-options": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/merge-options/-/merge-options-3.0.4.tgz",
      "integrity": "sha512-2Sug1+knBjkaMsMgf1ctR1Ujx+Ayku4EdJN4Z+C2+JzoeF7A3OZ9KM2GY0CpQS51NR61LTurMJrRKPhSs3ZRTQ==",
      "requires": {
        "is-plain-obj": "^2.1.0"
      }
    },
    "merge-stream": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/merge-stream/-/merge-stream-2.0.0.tgz",
      "integrity": "sha512-abv/qOcuPfk3URPfDzmZU1LKmuw8kT+0nIHvKrKgFrwifol/doWcdA4ZqsWQ8ENrFKkd67Mfpo/LovbIUsbt3w=="
    },
    "micromatch": {
      "version": "4.0.5",
      "resolved": "https://registry.npmjs.org/micromatch/-/micromatch-4.0.5.tgz",
      "integrity": "sha512-DMy+ERcEW2q8Z2Po+WNXuw3c5YaUSFjAO5GsJqfEl7UjvtIuFKO6ZrKvcItdy98dwFI2N1tg3zNIdKaQT+aNdA==",
      "requires": {
        "braces": "^3.0.2",
        "picomatch": "^2.3.1"
      }
    },
    "mimic-fn": {
      "version": "2.1.0",
      "resolved": "https://registry.npmjs.org/mimic-fn/-/mimic-fn-2.1.0.tgz",
      "integrity": "sha512-OqbOk5oEQeAZ8WXWydlu9HJjz9WVdEIvamMCcXmuqUYjTknH/sqsWvhQ3vgwKFRR1HpjvNBKQ37nbJgYzGqGcg=="
    },
    "minimatch": {
      "version": "3.1.2",
      "resolved": "https://registry.npmjs.org/minimatch/-/minimatch-3.1.2.tgz",
      "integrity": "sha512-J7p63hRiAjw1NDEww1W7i37+ByIrOWO5XQQAzZ3VOcL0PNybwpfmV/N05zFAzwQ9USyEcX6t3UO+K5aqBQOIHw==",
      "requires": {
        "brace-expansion": "^1.1.7"
      }
    },
    "minimist": {
      "version": "1.2.7",
      "resolved": "https://registry.npmjs.org/minimist/-/minimist-1.2.7.tgz",
      "integrity": "sha512-bzfL1YUZsP41gmu/qjrEk0Q6i2ix/cVeAhbCbqH9u3zYutS1cLg00qhrD0M2MVdCcx4Sc0UpP2eBWo9rotpq6g=="
    },
    "ms": {
      "version": "2.1.2",
      "resolved": "https://registry.npmjs.org/ms/-/ms-2.1.2.tgz",
      "integrity": "sha512-sGkPx+VjMtmA6MX27oA4FBFELFCZZ4S4XqeGOXCv68tT+jb3vk/RyaKWP0PTKyWtmLSM0b+adUTEvbs1PEaH2w=="
    },
    "multiformats": {
      "version": "9.9.0",
      "resolved": "https://registry.npmjs.org/multiformats/-/multiformats-9.9.0.tgz",
      "integrity": "sha512-HoMUjhH9T8DDBNT+6xzkrd9ga/XiBI4xLr58LJACwK6G3HTOPeMz4nB4KJs33L2BelrIJa7P0VuNaVF3hMYfjg=="
    },
    "murmurhash3js-revisited": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/murmurhash3js-revisited/-/murmurhash3js-revisited-3.0.0.tgz",
      "integrity": "sha512-/sF3ee6zvScXMb1XFJ8gDsSnY+X8PbOyjIuBhtgis10W2Jx4ZjIhikUCIF9c4gpJxVnQIsPAFrSwTCuAjicP6g=="
    },
    "natural-compare": {
      "version": "1.4.0",
      "resolved": "https://registry.npmjs.org/natural-compare/-/natural-compare-1.4.0.tgz",
      "integrity": "sha512-OWND8ei3VtNC9h7V60qff3SVobHr996CTwgxubgyQYEpg290h9J0buyECNNJexkFm5sOajh5G116RYA1c8ZMSw=="
    },
    "no-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/no-case/-/no-case-3.0.4.tgz",
      "integrity": "sha512-fgAN3jGAh+RoxUGZHTSOLJIqUc2wmoBwGR4tbpNAKmmovFoWq0OdRkb0VkldReO2a2iBT/OEulG9XSUc10r3zg==",
      "requires": {
        "lower-case": "^2.0.2",
        "tslib": "^2.0.3"
      }
    },
    "node-fetch": {
      "version": "2.6.9",
      "resolved": "https://registry.npmjs.org/node-fetch/-/node-fetch-2.6.9.tgz",
      "integrity": "sha512-DJm/CJkZkRjKKj4Zi4BsKVZh3ValV5IR5s7LVZnW+6YMh0W1BfNA8XSs6DLMGYlId5F3KnA70uu2qepcR08Qqg==",
      "requires": {
        "whatwg-url": "^5.0.0"
      }
    },
    "node-int64": {
      "version": "0.4.0",
      "resolved": "https://registry.npmjs.org/node-int64/-/node-int64-0.4.0.tgz",
      "integrity": "sha512-O5lz91xSOeoXP6DulyHfllpq+Eg00MWitZIbtPfoSEvqIHdl5gfcY6hYzDWnj0qD5tz52PI08u9qUvSVeUBeHw=="
    },
    "node-releases": {
      "version": "2.0.9",
      "resolved": "https://registry.npmjs.org/node-releases/-/node-releases-2.0.9.tgz",
      "integrity": "sha512-2xfmOrRkGogbTK9R6Leda0DGiXeY3p2NJpy4+gNCffdUvV6mdEJnaDEic1i3Ec2djAo8jWYoJMR5PB0MSMpxUA=="
    },
    "normalize-path": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/normalize-path/-/normalize-path-3.0.0.tgz",
      "integrity": "sha512-6eZs5Ls3WtCisHWp9S2GUy8dqkpGi4BVSz3GaqiE6ezub0512ESztXUwUB6C6IKbQkY2Pnb/mD4WYojCRwcwLA=="
    },
    "npm-run-path": {
      "version": "4.0.1",
      "resolved": "https://registry.npmjs.org/npm-run-path/-/npm-run-path-4.0.1.tgz",
      "integrity": "sha512-S48WzZW777zhNIrn7gxOlISNAqi9ZC/uQFnRdbeIHhZhCA6UqpkOT8T1G7BvfdgP4Er8gF4sUbaS0i7QvIfCWw==",
      "requires": {
        "path-key": "^3.0.0"
      }
    },
    "object-inspect": {
      "version": "1.12.3",
      "resolved": "https://registry.npmjs.org/object-inspect/-/object-inspect-1.12.3.tgz",
      "integrity": "sha512-geUvdk7c+eizMNUDkRpW1wJwgfOiOeHbxBR/hLXK1aT6zmVSO0jsQcs7fj6MGw89jC/cjGfLcNOrtMYtGqm81g=="
    },
    "ohm-js": {
      "version": "16.6.0",
      "resolved": "https://registry.npmjs.org/ohm-js/-/ohm-js-16.6.0.tgz",
      "integrity": "sha512-X9P4koSGa7swgVQ0gt71UCYtkAQGOjciJPJAz74kDxWt8nXbH5HrDOQG6qBDH7SR40ktNv4x61BwpTDE9q4lRA=="
    },
    "once": {
      "version": "1.4.0",
      "resolved": "https://registry.npmjs.org/once/-/once-1.4.0.tgz",
      "integrity": "sha512-lNaJgI+2Q5URQBkccEKHTQOPaXdUxnZZElQTZY0MFUAuaEqe1E+Nyvgdz/aIyNi6Z9MzO5dv1H8n58/GELp3+w==",
      "requires": {
        "wrappy": "1"
      }
    },
    "onetime": {
      "version": "5.1.2",
      "resolved": "https://registry.npmjs.org/onetime/-/onetime-5.1.2.tgz",
      "integrity": "sha512-kbpaSSGJTWdAY5KPVeMOKXSrPtr8C8C7wodJbcsd51jRnmD+GZu8Y0VoU6Dm5Z4vWr0Ig/1NKuWRKf7j5aaYSg==",
      "requires": {
        "mimic-fn": "^2.1.0"
      }
    },
    "open": {
      "version": "8.4.0",
      "resolved": "https://registry.npmjs.org/open/-/open-8.4.0.tgz",
      "integrity": "sha512-XgFPPM+B28FtCCgSb9I+s9szOC1vZRSwgWsRUA5ylIxRTgKozqjOCrVOqGsYABPYK5qnfqClxZTFBa8PKt2v6Q==",
      "requires": {
        "define-lazy-prop": "^2.0.0",
        "is-docker": "^2.1.1",
        "is-wsl": "^2.2.0"
      }
    },
    "ora": {
      "version": "6.1.2",
      "resolved": "https://registry.npmjs.org/ora/-/ora-6.1.2.tgz",
      "integrity": "sha512-EJQ3NiP5Xo94wJXIzAyOtSb0QEIAUu7m8t6UZ9krbz0vAJqr92JpcK/lEXg91q6B9pEGqrykkd2EQplnifDSBw==",
      "requires": {
        "bl": "^5.0.0",
        "chalk": "^5.0.0",
        "cli-cursor": "^4.0.0",
        "cli-spinners": "^2.6.1",
        "is-interactive": "^2.0.0",
        "is-unicode-supported": "^1.1.0",
        "log-symbols": "^5.1.0",
        "strip-ansi": "^7.0.1",
        "wcwidth": "^1.0.1"
      },
      "dependencies": {
        "ansi-regex": {
          "version": "6.0.1",
          "resolved": "https://registry.npmjs.org/ansi-regex/-/ansi-regex-6.0.1.tgz",
          "integrity": "sha512-n5M855fKb2SsfMIiFFoVrABHJC8QtHwVx+mHWP3QcEqBHYienj5dHSgjbxtC0WEZXYt4wcD6zrQElDPhFuZgfA=="
        },
        "chalk": {
          "version": "5.2.0",
          "resolved": "https://registry.npmjs.org/chalk/-/chalk-5.2.0.tgz",
          "integrity": "sha512-ree3Gqw/nazQAPuJJEy+avdl7QfZMcUvmHIKgEZkGL+xOBzRvup5Hxo6LHuMceSxOabuJLJm5Yp/92R9eMmMvA=="
        },
        "strip-ansi": {
          "version": "7.0.1",
          "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-7.0.1.tgz",
          "integrity": "sha512-cXNxvT8dFNRVfhVME3JAe98mkXDYN2O1l7jmcwMnOslDeESg1rF/OZMtK0nRAhiari1unG5cD4jG3rapUAkLbw==",
          "requires": {
            "ansi-regex": "^6.0.1"
          }
        }
      }
    },
    "p-limit": {
      "version": "3.1.0",
      "resolved": "https://registry.npmjs.org/p-limit/-/p-limit-3.1.0.tgz",
      "integrity": "sha512-TYOanM3wGwNGsZN2cVTYPArw454xnXj5qmWF1bEoAc4+cU/ol7GVh7odevjp1FNHduHc3KZMcFduxU5Xc6uJRQ==",
      "requires": {
        "yocto-queue": "^0.1.0"
      }
    },
    "p-locate": {
      "version": "4.1.0",
      "resolved": "https://registry.npmjs.org/p-locate/-/p-locate-4.1.0.tgz",
      "integrity": "sha512-R79ZZ/0wAxKGu3oYMlz8jy/kbhsNrS7SKZ7PxEHBgJ5+F2mtFW2fK2cOtBh1cHYkQsbzFV7I+EoRKe6Yt0oK7A==",
      "requires": {
        "p-limit": "^2.2.0"
      },
      "dependencies": {
        "p-limit": {
          "version": "2.3.0",
          "resolved": "https://registry.npmjs.org/p-limit/-/p-limit-2.3.0.tgz",
          "integrity": "sha512-//88mFWSJx8lxCzwdAABTJL2MyWB12+eIY7MDL2SqLmAkeKU9qxRvWuSyTjm3FUmpBEMuFfckAIqEaVGUDxb6w==",
          "requires": {
            "p-try": "^2.0.0"
          }
        }
      }
    },
    "p-try": {
      "version": "2.2.0",
      "resolved": "https://registry.npmjs.org/p-try/-/p-try-2.2.0.tgz",
      "integrity": "sha512-R4nPAVTAU0B9D35/Gk3uJf/7XYbQcyohSKdvAxIRSNghFl4e71hVoGnBNQz9cWaXxO2I10KTC+3jMdvvoKw6dQ=="
    },
    "param-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/param-case/-/param-case-3.0.4.tgz",
      "integrity": "sha512-RXlj7zCYokReqWpOPH9oYivUzLYZ5vAPIfEmCTNViosC78F8F0H9y7T7gG2M39ymgutxF5gcFEsyZQSph9Bp3A==",
      "requires": {
        "dot-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "parse-json": {
      "version": "5.2.0",
      "resolved": "https://registry.npmjs.org/parse-json/-/parse-json-5.2.0.tgz",
      "integrity": "sha512-ayCKvm/phCGxOkYRSCM82iDwct8/EonSEgCSxWxD7ve6jHggsFl4fZVQBPRNgQoKiuV/odhFrGzQXZwbifC8Rg==",
      "requires": {
        "@babel/code-frame": "^7.0.0",
        "error-ex": "^1.3.1",
        "json-parse-even-better-errors": "^2.3.0",
        "lines-and-columns": "^1.1.6"
      }
    },
    "pascal-case": {
      "version": "3.1.2",
      "resolved": "https://registry.npmjs.org/pascal-case/-/pascal-case-3.1.2.tgz",
      "integrity": "sha512-uWlGT3YSnK9x3BQJaOdcZwrnV6hPpd8jFH1/ucpiLRPh/2zCVJKS19E4GvYHvaCcACn3foXZ0cLB9Wrx1KGe5g==",
      "requires": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "path-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/path-case/-/path-case-3.0.4.tgz",
      "integrity": "sha512-qO4qCFjXqVTrcbPt/hQfhTQ+VhFsqNKOPtytgNKkKxSoEp3XPUQ8ObFuePylOIok5gjn69ry8XiULxCwot3Wfg==",
      "requires": {
        "dot-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "path-exists": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/path-exists/-/path-exists-4.0.0.tgz",
      "integrity": "sha512-ak9Qy5Q7jYb2Wwcey5Fpvg2KoAc/ZIhLSLOSBmRmygPsGwkVVt0fZa0qrtMz+m6tJTAHfZQ8FnmB4MG4LWy7/w=="
    },
    "path-is-absolute": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/path-is-absolute/-/path-is-absolute-1.0.1.tgz",
      "integrity": "sha512-AVbw3UJ2e9bq64vSaS9Am0fje1Pa8pbGqTTsmXfaIiMpnr5DlDhfJOuLj9Sf95ZPVDAUerDfEk88MPmPe7UCQg=="
    },
    "path-key": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/path-key/-/path-key-3.1.1.tgz",
      "integrity": "sha512-ojmeN0qd+y0jszEtoY48r0Peq5dwMEkIlCOu6Q5f41lfkswXuKtYrhgoTpLnyIcHm24Uhqx+5Tqm2InSwLhE6Q=="
    },
    "path-parse": {
      "version": "1.0.7",
      "resolved": "https://registry.npmjs.org/path-parse/-/path-parse-1.0.7.tgz",
      "integrity": "sha512-LDJzPVEEEPR+y48z93A0Ed0yXb8pAByGWo/k5YYdYgpY2/2EsOsksJrq7lOHxryrVOn1ejG6oAp8ahvOIQD8sw=="
    },
    "picocolors": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/picocolors/-/picocolors-1.0.0.tgz",
      "integrity": "sha512-1fygroTLlHu66zi26VoTDv8yRgm0Fccecssto+MhsZ0D/DGW2sm8E8AjW7NU5VVTRt5GxbeZ5qBuJr+HyLYkjQ=="
    },
    "picomatch": {
      "version": "2.3.1",
      "resolved": "https://registry.npmjs.org/picomatch/-/picomatch-2.3.1.tgz",
      "integrity": "sha512-JU3teHTNjmE2VCGFzuY8EXzCDVwEqB2a8fsIvwaStHhAWJEeVd1o1QD80CU6+ZdEXXSLbSsuLwJjkCBWqRQUVA=="
    },
    "pirates": {
      "version": "4.0.5",
      "resolved": "https://registry.npmjs.org/pirates/-/pirates-4.0.5.tgz",
      "integrity": "sha512-8V9+HQPupnaXMA23c5hvl69zXvTwTzyAYasnkb0Tts4XvO4CliqONMOnvlq26rkhLC3nWDFBJf73LU1e1VZLaQ=="
    },
    "pkg-dir": {
      "version": "4.2.0",
      "resolved": "https://registry.npmjs.org/pkg-dir/-/pkg-dir-4.2.0.tgz",
      "integrity": "sha512-HRDzbaKjC+AOWVXxAU/x54COGeIv9eb+6CkDSQoNTt4XyWoIJvuPsXizxu/Fr23EiekbtZwmh1IcIG/l/a10GQ==",
      "requires": {
        "find-up": "^4.0.0"
      }
    },
    "prando": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/prando/-/prando-6.0.1.tgz",
      "integrity": "sha512-ghUWxQ1T9IJmPu6eshc3VU0OwveUtXQ33ZLXYUcz1Oc5ppKLDXKp0TBDj6b0epwhEctzcQSNGR2iHyvQSn4W5A=="
    },
    "prettier": {
      "version": "2.8.3",
      "resolved": "https://registry.npmjs.org/prettier/-/prettier-2.8.3.tgz",
      "integrity": "sha512-tJ/oJ4amDihPoufT5sM0Z1SKEuKay8LfVAMlbbhnnkvt6BUserZylqo2PN+p9KeljLr0OHa2rXHU1T8reeoTrw=="
    },
    "pretty-format": {
      "version": "29.4.1",
      "resolved": "https://registry.npmjs.org/pretty-format/-/pretty-format-29.4.1.tgz",
      "integrity": "sha512-dt/Z761JUVsrIKaY215o1xQJBGlSmTx/h4cSqXqjHLnU1+Kt+mavVE7UgqJJO5ukx5HjSswHfmXz4LjS2oIJfg==",
      "requires": {
        "@jest/schemas": "^29.4.0",
        "ansi-styles": "^5.0.0",
        "react-is": "^18.0.0"
      },
      "dependencies": {
        "ansi-styles": {
          "version": "5.2.0",
          "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-5.2.0.tgz",
          "integrity": "sha512-Cxwpt2SfTzTtXcfOlzGEee8O+c+MmUgGrNiBcXnuWxuFJHe6a5Hz7qwhwe5OgaSYI0IJvkLqWX1ASG+cJOkEiA=="
        }
      }
    },
    "prompts": {
      "version": "2.4.2",
      "resolved": "https://registry.npmjs.org/prompts/-/prompts-2.4.2.tgz",
      "integrity": "sha512-NxNv/kLguCA7p3jE8oL2aEBsrJWgAakBpgmgK6lpPWV+WuOmY6r2/zbAVnP+T8bQlA0nzHXSJSJW0Hq7ylaD2Q==",
      "requires": {
        "kleur": "^3.0.3",
        "sisteransi": "^1.0.5"
      }
    },
    "protobufjs": {
      "version": "6.11.3",
      "resolved": "https://registry.npmjs.org/protobufjs/-/protobufjs-6.11.3.tgz",
      "integrity": "sha512-xL96WDdCZYdU7Slin569tFX712BxsxslWwAfAhCYjQKGTq7dAU91Lomy6nLLhh/dyGhk/YH4TwTSRxTzhuHyZg==",
      "requires": {
        "@protobufjs/aspromise": "^1.1.2",
        "@protobufjs/base64": "^1.1.2",
        "@protobufjs/codegen": "^2.0.4",
        "@protobufjs/eventemitter": "^1.1.0",
        "@protobufjs/fetch": "^1.1.0",
        "@protobufjs/float": "^1.0.2",
        "@protobufjs/inquire": "^1.1.0",
        "@protobufjs/path": "^1.1.2",
        "@protobufjs/pool": "^1.1.0",
        "@protobufjs/utf8": "^1.1.0",
        "@types/long": "^4.0.1",
        "@types/node": ">=13.7.0",
        "long": "^4.0.0"
      }
    },
    "qs": {
      "version": "6.11.0",
      "resolved": "https://registry.npmjs.org/qs/-/qs-6.11.0.tgz",
      "integrity": "sha512-MvjoMCJwEarSbUYk5O+nmoSzSutSsTwF85zcHPQ9OrlFoZOYIjaqBAJIqIXjptyD5vThxGq52Xu/MaJzRkIk4Q==",
      "requires": {
        "side-channel": "^1.0.4"
      }
    },
    "rabin-wasm": {
      "version": "0.1.5",
      "resolved": "https://registry.npmjs.org/rabin-wasm/-/rabin-wasm-0.1.5.tgz",
      "integrity": "sha512-uWgQTo7pim1Rnj5TuWcCewRDTf0PEFTSlaUjWP4eY9EbLV9em08v89oCz/WO+wRxpYuO36XEHp4wgYQnAgOHzA==",
      "requires": {
        "@assemblyscript/loader": "^0.9.4",
        "bl": "^5.0.0",
        "debug": "^4.3.1",
        "minimist": "^1.2.5",
        "node-fetch": "^2.6.1",
        "readable-stream": "^3.6.0"
      }
    },
    "react-is": {
      "version": "18.2.0",
      "resolved": "https://registry.npmjs.org/react-is/-/react-is-18.2.0.tgz",
      "integrity": "sha512-xWGDIW6x921xtzPkhiULtthJHoJvBbF3q26fzloPCK0hsvxtPVelvftw3zjbHWSkR2km9Z+4uxbDDK/6Zw9B8w=="
    },
    "readable-stream": {
      "version": "3.6.0",
      "resolved": "https://registry.npmjs.org/readable-stream/-/readable-stream-3.6.0.tgz",
      "integrity": "sha512-BViHy7LKeTz4oNnkcLJ+lVSL6vpiFeX6/d3oSH8zCW7UxP2onchk+vTGB143xuFjHS3deTgkKoXXymXqymiIdA==",
      "requires": {
        "inherits": "^2.0.3",
        "string_decoder": "^1.1.1",
        "util-deprecate": "^1.0.1"
      }
    },
    "require-directory": {
      "version": "2.1.1",
      "resolved": "https://registry.npmjs.org/require-directory/-/require-directory-2.1.1.tgz",
      "integrity": "sha512-fGxEI7+wsG9xrvdjsrlmL22OMTTiHRwAMroiEeMgq8gzoLC/PQr7RsRDSTLUg/bZAZtF+TVIkHc6/4RIKrui+Q=="
    },
    "resolve": {
      "version": "1.22.1",
      "resolved": "https://registry.npmjs.org/resolve/-/resolve-1.22.1.tgz",
      "integrity": "sha512-nBpuuYuY5jFsli/JIs1oldw6fOQCBioohqWZg/2hiaOybXOft4lonv85uDOKXdf8rhyK159cxU5cDcK/NKk8zw==",
      "requires": {
        "is-core-module": "^2.9.0",
        "path-parse": "^1.0.7",
        "supports-preserve-symlinks-flag": "^1.0.0"
      }
    },
    "resolve-cwd": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/resolve-cwd/-/resolve-cwd-3.0.0.tgz",
      "integrity": "sha512-OrZaX2Mb+rJCpH/6CpSqt9xFVpN++x01XnN2ie9g6P5/3xelLAkXWVADpdz1IHD/KFfEXyE6V0U01OQ3UO2rEg==",
      "requires": {
        "resolve-from": "^5.0.0"
      }
    },
    "resolve-from": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/resolve-from/-/resolve-from-5.0.0.tgz",
      "integrity": "sha512-qYg9KP24dD5qka9J47d0aVky0N+b4fTU89LN9iDnjB5waksiC49rvMB0PrUJQGoTmH50XPiqOvAjDfaijGxYZw=="
    },
    "resolve.exports": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/resolve.exports/-/resolve.exports-2.0.0.tgz",
      "integrity": "sha512-6K/gDlqgQscOlg9fSRpWstA8sYe8rbELsSTNpx+3kTrsVCzvSl0zIvRErM7fdl9ERWDsKnrLnwB+Ne89918XOg=="
    },
    "restore-cursor": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/restore-cursor/-/restore-cursor-4.0.0.tgz",
      "integrity": "sha512-I9fPXU9geO9bHOt9pHHOhOkYerIMsmVaWB0rA2AI9ERh/+x/i7MV5HKBNrg+ljO5eoPVgCcnFuRjJ9uH6I/3eg==",
      "requires": {
        "onetime": "^5.1.0",
        "signal-exit": "^3.0.2"
      }
    },
    "rimraf": {
      "version": "3.0.2",
      "resolved": "https://registry.npmjs.org/rimraf/-/rimraf-3.0.2.tgz",
      "integrity": "sha512-JZkJMZkAGFFPP2YqXZXPbMlMBgsxzE8ILs4lMIX/2o0L9UBw9O/Y3o6wFw/i9YLapcUJWwqbi3kdxIPdC62TIA==",
      "requires": {
        "glob": "^7.1.3"
      }
    },
    "safe-buffer": {
      "version": "5.2.1",
      "resolved": "https://registry.npmjs.org/safe-buffer/-/safe-buffer-5.2.1.tgz",
      "integrity": "sha512-rp3So07KcdmmKbGvgaNxQSJr7bGVSVk5S9Eq1F+ppbRo70+YeaDxkw5Dd8NPN+GD6bjnYm2VuPuCXmpuYvmCXQ=="
    },
    "semver": {
      "version": "6.3.0",
      "resolved": "https://registry.npmjs.org/semver/-/semver-6.3.0.tgz",
      "integrity": "sha512-b39TBaTSfV6yBrapU89p5fKekE2m/NwnDocOVruQFS1/veMgdzuPcnOM34M6CwxW8jH/lxEa5rBoDeUwu5HHTw=="
    },
    "sentence-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/sentence-case/-/sentence-case-3.0.4.tgz",
      "integrity": "sha512-8LS0JInaQMCRoQ7YUytAo/xUu5W2XnQxV2HI/6uM6U7CITS1RqPElr30V6uIqyMKM9lJGRVFy5/4CuzcixNYSg==",
      "requires": {
        "no-case": "^3.0.4",
        "tslib": "^2.0.3",
        "upper-case-first": "^2.0.2"
      }
    },
    "shebang-command": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/shebang-command/-/shebang-command-2.0.0.tgz",
      "integrity": "sha512-kHxr2zZpYtdmrN1qDjrrX/Z1rR1kG8Dx+gkpK1G4eXmvXswmcE1hTWBWYUzlraYw1/yZp6YuDY77YtvbN0dmDA==",
      "requires": {
        "shebang-regex": "^3.0.0"
      }
    },
    "shebang-regex": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/shebang-regex/-/shebang-regex-3.0.0.tgz",
      "integrity": "sha512-7++dFhtcx3353uBaq8DDR4NuxBetBzC7ZQOhmTQInHEd6bSrXdiEyzCvG07Z44UYdLShWUyXt5M/yhz8ekcb1A=="
    },
    "side-channel": {
      "version": "1.0.4",
      "resolved": "https://registry.npmjs.org/side-channel/-/side-channel-1.0.4.tgz",
      "integrity": "sha512-q5XPytqFEIKHkGdiMIrY10mvLRvnQh42/+GoBlFW3b2LXLE2xxJpZFdm94we0BaoV3RwJyGqg5wS7epxTv0Zvw==",
      "requires": {
        "call-bind": "^1.0.0",
        "get-intrinsic": "^1.0.2",
        "object-inspect": "^1.9.0"
      }
    },
    "signal-exit": {
      "version": "3.0.7",
      "resolved": "https://registry.npmjs.org/signal-exit/-/signal-exit-3.0.7.tgz",
      "integrity": "sha512-wnD2ZE+l+SPC/uoS0vXeE9L1+0wuaMqKlfz9AMUo38JsyLSBWSFcHR1Rri62LZc12vLr1gb3jl7iwQhgwpAbGQ=="
    },
    "sisteransi": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/sisteransi/-/sisteransi-1.0.5.tgz",
      "integrity": "sha512-bLGGlR1QxBcynn2d5YmDX4MGjlZvy2MRBDRNHLJ8VI6l6+9FUiyTFNJ0IveOSP0bcXgVDPRcfGqA0pjaqUpfVg=="
    },
    "slash": {
      "version": "3.0.0",
      "resolved": "https://registry.npmjs.org/slash/-/slash-3.0.0.tgz",
      "integrity": "sha512-g9Q1haeby36OSStwb4ntCGGGaKsaVSjQ68fBxoQcutl5fS1vuY18H3wSt3jFyFtrkx+Kz0V1G85A4MyAdDMi2Q=="
    },
    "snake-case": {
      "version": "3.0.4",
      "resolved": "https://registry.npmjs.org/snake-case/-/snake-case-3.0.4.tgz",
      "integrity": "sha512-LAOh4z89bGQvl9pFfNF8V146i7o7/CqFPbqzYgP+yYzDIDeS9HaNFtXABamRW+AQzEVODcvE79ljJ+8a9YSdMg==",
      "requires": {
        "dot-case": "^3.0.4",
        "tslib": "^2.0.3"
      }
    },
    "source-map": {
      "version": "0.6.1",
      "resolved": "https://registry.npmjs.org/source-map/-/source-map-0.6.1.tgz",
      "integrity": "sha512-UjgapumWlbMhkBgzT7Ykc5YXUT46F0iKu8SGXq0bcwP5dz/h0Plj6enJqjz1Zbq2l5WaqYnrVbwWOWMyF3F47g=="
    },
    "source-map-support": {
      "version": "0.5.13",
      "resolved": "https://registry.npmjs.org/source-map-support/-/source-map-support-0.5.13.tgz",
      "integrity": "sha512-SHSKFHadjVA5oR4PPqhtAVdcBWwRYVd6g6cAXnIbRiIwc2EhPrTuKUBdSLvlEKyIP3GCf89fltvcZiP9MMFA1w==",
      "requires": {
        "buffer-from": "^1.0.0",
        "source-map": "^0.6.0"
      }
    },
    "sparse-array": {
      "version": "1.3.2",
      "resolved": "https://registry.npmjs.org/sparse-array/-/sparse-array-1.3.2.tgz",
      "integrity": "sha512-ZT711fePGn3+kQyLuv1fpd3rNSkNF8vd5Kv2D+qnOANeyKs3fx6bUMGWRPvgTTcYV64QMqZKZwcuaQSP3AZ0tg=="
    },
    "sprintf-js": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/sprintf-js/-/sprintf-js-1.0.3.tgz",
      "integrity": "sha512-D9cPgkvLlV3t3IzL0D0YLvGA9Ahk4PcvVwUbN0dSGr1aP0Nrt4AEnTUbuGvquEC0mA64Gqt1fzirlRs5ibXx8g=="
    },
    "stack-utils": {
      "version": "2.0.6",
      "resolved": "https://registry.npmjs.org/stack-utils/-/stack-utils-2.0.6.tgz",
      "integrity": "sha512-XlkWvfIm6RmsWtNJx+uqtKLS8eqFbxUg0ZzLXqY0caEy9l7hruX8IpiDnjsLavoBgqCCR71TqWO8MaXYheJ3RQ==",
      "requires": {
        "escape-string-regexp": "^2.0.0"
      }
    },
    "string_decoder": {
      "version": "1.3.0",
      "resolved": "https://registry.npmjs.org/string_decoder/-/string_decoder-1.3.0.tgz",
      "integrity": "sha512-hkRX8U1WjJFd8LsDJ2yQ/wWWxaopEsABU1XfkM8A+j0+85JAGppt16cr1Whg6KIbb4okU6Mql6BOj+uup/wKeA==",
      "requires": {
        "safe-buffer": "~5.2.0"
      }
    },
    "string-length": {
      "version": "4.0.2",
      "resolved": "https://registry.npmjs.org/string-length/-/string-length-4.0.2.tgz",
      "integrity": "sha512-+l6rNN5fYHNhZZy41RXsYptCjA2Igmq4EG7kZAYFQI1E1VTXarr6ZPXBg6eq7Y6eK4FEhY6AJlyuFIb/v/S0VQ==",
      "requires": {
        "char-regex": "^1.0.2",
        "strip-ansi": "^6.0.0"
      }
    },
    "string-width": {
      "version": "4.2.3",
      "resolved": "https://registry.npmjs.org/string-width/-/string-width-4.2.3.tgz",
      "integrity": "sha512-wKyQRQpjJ0sIp62ErSZdGsjMJWsap5oRNihHhu6G7JVO/9jIB6UyevL+tXuOqrng8j/cxKTWyWUwvSTriiZz/g==",
      "requires": {
        "emoji-regex": "^8.0.0",
        "is-fullwidth-code-point": "^3.0.0",
        "strip-ansi": "^6.0.1"
      }
    },
    "strip-ansi": {
      "version": "6.0.1",
      "resolved": "https://registry.npmjs.org/strip-ansi/-/strip-ansi-6.0.1.tgz",
      "integrity": "sha512-Y38VPSHcqkFrCpFnQ9vuSXmquuv5oXOKpGeT6aGrr3o3Gc9AlVa6JBfUSOCnbxGGZF+/0ooI7KrPuUSztUdU5A==",
      "requires": {
        "ansi-regex": "^5.0.1"
      }
    },
    "strip-bom": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/strip-bom/-/strip-bom-4.0.0.tgz",
      "integrity": "sha512-3xurFv5tEgii33Zi8Jtp55wEIILR9eh34FAW00PZf+JnSsTmV/ioewSgQl97JHvgjoRGwPShsWm+IdrxB35d0w=="
    },
    "strip-final-newline": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/strip-final-newline/-/strip-final-newline-2.0.0.tgz",
      "integrity": "sha512-BrpvfNAE3dcvq7ll3xVumzjKjZQ5tI1sEUIKr3Uoks0XUl45St3FlatVqef9prk4jRDzhW6WZg+3bk93y6pLjA=="
    },
    "strip-json-comments": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/strip-json-comments/-/strip-json-comments-3.1.1.tgz",
      "integrity": "sha512-6fPc+R4ihwqP6N/aIv2f1gMH8lOVtWQHoqC4yK6oSDVVocumAsfCqjkXnqiYMhmMwS/mEHLp7Vehlt3ql6lEig=="
    },
    "supports-color": {
      "version": "7.2.0",
      "resolved": "https://registry.npmjs.org/supports-color/-/supports-color-7.2.0.tgz",
      "integrity": "sha512-qpCAvRl9stuOHveKsn7HncJRvv501qIacKzQlO/+Lwxc9+0q2wLyv4Dfvt80/DPn2pqOBsJdDiogXGR9+OvwRw==",
      "requires": {
        "has-flag": "^4.0.0"
      }
    },
    "supports-preserve-symlinks-flag": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/supports-preserve-symlinks-flag/-/supports-preserve-symlinks-flag-1.0.0.tgz",
      "integrity": "sha512-ot0WnXS9fgdkgIcePe6RHNk1WA8+muPa6cSjeR3V8K27q9BB1rTE3R1p7Hv0z1ZyAc8s6Vvv8DIyWf681MAt0w=="
    },
    "symbol.inspect": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/symbol.inspect/-/symbol.inspect-1.0.1.tgz",
      "integrity": "sha512-YQSL4duoHmLhsTD1Pw8RW6TZ5MaTX5rXJnqacJottr2P2LZBF/Yvrc3ku4NUpMOm8aM0KOCqM+UAkMA5HWQCzQ=="
    },
    "teslabot": {
      "version": "1.5.0",
      "resolved": "https://registry.npmjs.org/teslabot/-/teslabot-1.5.0.tgz",
      "integrity": "sha512-e2MmELhCgrgZEGo7PQu/6bmYG36IDH+YrBI1iGm6jovXkeDIGa3pZ2WSqRjzkuw2vt1EqfkZoV5GpXgqL8QJVg=="
    },
    "test-exclude": {
      "version": "6.0.0",
      "resolved": "https://registry.npmjs.org/test-exclude/-/test-exclude-6.0.0.tgz",
      "integrity": "sha512-cAGWPIyOHU6zlmg88jwm7VRyXnMN7iV68OGAbYDk/Mh/xC/pzVPlQtY6ngoIH/5/tciuhGfvESU8GrHrcxD56w==",
      "requires": {
        "@istanbuljs/schema": "^0.1.2",
        "glob": "^7.1.4",
        "minimatch": "^3.0.4"
      }
    },
    "tmp": {
      "version": "0.2.1",
      "resolved": "https://registry.npmjs.org/tmp/-/tmp-0.2.1.tgz",
      "integrity": "sha512-76SUhtfqR2Ijn+xllcI5P1oyannHNHByD80W1q447gU3mp9G9PSpGdWmjUOHRDPiHYacIk66W7ubDTuPF3BEtQ==",
      "requires": {
        "rimraf": "^3.0.0"
      }
    },
    "tmpl": {
      "version": "1.0.5",
      "resolved": "https://registry.npmjs.org/tmpl/-/tmpl-1.0.5.tgz",
      "integrity": "sha512-3f0uOEAQwIqGuWW2MVzYg8fV/QNnc/IpuJNG837rLuczAaLVHslWHZQj4IGiEl5Hs3kkbhwL9Ab7Hrsmuj+Smw=="
    },
    "to-fast-properties": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/to-fast-properties/-/to-fast-properties-2.0.0.tgz",
      "integrity": "sha512-/OaKK0xYrs3DmxRYqL/yDc+FxFUVYhDlXMhRmv3z915w2HF1tnN1omB354j8VUGO/hbRzyD6Y3sA7v7GS/ceog=="
    },
    "to-regex-range": {
      "version": "5.0.1",
      "resolved": "https://registry.npmjs.org/to-regex-range/-/to-regex-range-5.0.1.tgz",
      "integrity": "sha512-65P7iz6X5yEr1cwcgvQxbbIw7Uk3gOy5dIdtZ4rDveLqhrdJP+Li/Hx6tyK0NEb+2GCyneCMJiGqrADCSNk8sQ==",
      "requires": {
        "is-number": "^7.0.0"
      }
    },
    "ton": {
      "version": "13.3.0",
      "resolved": "https://registry.npmjs.org/ton/-/ton-13.3.0.tgz",
      "integrity": "sha512-ygNZ3a8xgDcftudgmq2lNzFNrQtNhUdmBneLJI8C2iBuD9RAfpnjae4eIpjPLfCsLKH8Nmvh2JOESfM7lvsCSw==",
      "requires": {
        "axios": "^0.25.0",
        "dataloader": "^2.0.0",
        "fp-ts": "^2.11.1",
        "io-ts": "^2.2.16",
        "io-ts-reporters": "^2.0.0",
        "symbol.inspect": "1.0.1",
        "teslabot": "^1.3.0"
      }
    },
    "ton-core": {
      "version": "0.47.1",
      "resolved": "https://registry.npmjs.org/ton-core/-/ton-core-0.47.1.tgz",
      "integrity": "sha512-XxcgLYH+Ngo3uh7O7jkzA0/O8nfG3WC3fgUmdvY9/IkGKpkO3Y/KHtrZgAOHYAkxJCmaXpi4aPf4JEnZEiPrWQ==",
      "requires": {
        "symbol.inspect": "1.0.1"
      }
    },
    "ton-crypto": {
      "version": "3.2.0",
      "resolved": "https://registry.npmjs.org/ton-crypto/-/ton-crypto-3.2.0.tgz",
      "integrity": "sha512-fltdBNQ45gARMuGMEOjPZWPJ5eSql8p3CA0Dj7tPv5lhU5ziT8SxXLAzDraR9HJ8YpjBHLVvYyhMLRiEwxgtMQ==",
      "requires": {
        "jssha": "3.2.0",
        "ton-crypto-primitives": "2.0.0",
        "tweetnacl": "1.0.3"
      }
    },
    "ton-crypto-primitives": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/ton-crypto-primitives/-/ton-crypto-primitives-2.0.0.tgz",
      "integrity": "sha512-K+qKjpS0h9sPW6oExcpxnzuQ7nEgHEiDKwIqE/jWD25o8iFGe3FWj1gKxFNbKE9wwYKc5IV8FwrU+raF0KO5nQ==",
      "requires": {
        "jssha": "3.2.0"
      }
    },
    "ton-emulator": {
      "version": "1.6.1",
      "resolved": "https://registry.npmjs.org/ton-emulator/-/ton-emulator-1.6.1.tgz",
      "integrity": "sha512-th4K5llFixKFmC72eDDSNsLbczJaUaAu/c+FOunMgdPFyS/FUr3MOLNTjhlGk97PaKDfMgLnMAwmpd2V4R6OZg==",
      "requires": {
        "prando": "^6.0.1",
        "teslabot": "^1.5.0",
        "zod": "^3.20.2"
      }
    },
    "ton-tact": {
      "version": "0.9.0",
      "resolved": "https://registry.npmjs.org/ton-tact/-/ton-tact-0.9.0.tgz",
      "integrity": "sha512-TK9idKg4sPQi1VZ+naBZ1kzm64qlXQSqiroDHZD0ffhsnIdOW2n6BbQDk5NqjvA5Db49ZsgjMSAlwJ0dGFdm1Q==",
      "requires": {
        "@ipld/dag-pb": "2.1.18",
        "@types/tmp": "^0.2.3",
        "arg": "^5.0.2",
        "blockstore-core": "1.0.5",
        "change-case": "^4.1.2",
        "ipfs-unixfs-importer": "9.0.10",
        "multiformats": "9.9.0",
        "ohm-js": "^16.4.0",
        "ora": "^6.1.2",
        "prando": "^6.0.1",
        "qs": "^6.11.0",
        "tmp": "^0.2.1",
        "ton-core": ">=0.44.0",
        "ton-crypto": "^3.2.0",
        "tvm-disassembler": "^2.0.0",
        "zod": "^3.20.2"
      },
      "dependencies": {
        "arg": {
          "version": "5.0.2",
          "resolved": "https://registry.npmjs.org/arg/-/arg-5.0.2.tgz",
          "integrity": "sha512-PYjyFOLKQ9y57JvQ6QLo8dAgNqswh8M1RMJYdQduT6xbWSgK36P/Z/v+p888pM69jMMfS8Xd8F6I1kQ/I9HUGg=="
        }
      }
    },
    "tr46": {
      "version": "0.0.3",
      "resolved": "https://registry.npmjs.org/tr46/-/tr46-0.0.3.tgz",
      "integrity": "sha512-N3WMsuqV66lT30CrXNbEjx4GEwlow3v6rr4mCcv6prnfwhS01rkgyFdjPNBYd9br7LpXV1+Emh01fHnq2Gdgrw=="
    },
    "ts-jest": {
      "version": "29.0.5",
      "resolved": "https://registry.npmjs.org/ts-jest/-/ts-jest-29.0.5.tgz",
      "integrity": "sha512-PL3UciSgIpQ7f6XjVOmbi96vmDHUqAyqDr8YxzopDqX3kfgYtX1cuNeBjP+L9sFXi6nzsGGA6R3fP3DDDJyrxA==",
      "requires": {
        "bs-logger": "0.x",
        "fast-json-stable-stringify": "2.x",
        "jest-util": "^29.0.0",
        "json5": "^2.2.3",
        "lodash.memoize": "4.x",
        "make-error": "1.x",
        "semver": "7.x",
        "yargs-parser": "^21.0.1"
      },
      "dependencies": {
        "semver": {
          "version": "7.3.8",
          "resolved": "https://registry.npmjs.org/semver/-/semver-7.3.8.tgz",
          "integrity": "sha512-NB1ctGL5rlHrPJtFDVIVzTyQylMLu9N9VICA6HSFJo8MCGVTMW6gfpicwKmmK/dAjTOrqu5l63JJOpDSrAis3A==",
          "requires": {
            "lru-cache": "^6.0.0"
          }
        }
      }
    },
    "ts-node": {
      "version": "10.9.1",
      "resolved": "https://registry.npmjs.org/ts-node/-/ts-node-10.9.1.tgz",
      "integrity": "sha512-NtVysVPkxxrwFGUUxGYhfux8k78pQB3JqYBXlLRZgdGUqTO5wU/UyHop5p70iEbGhB7q5KmiZiU0Y3KlJrScEw==",
      "requires": {
        "@cspotcode/source-map-support": "^0.8.0",
        "@tsconfig/node10": "^1.0.7",
        "@tsconfig/node12": "^1.0.7",
        "@tsconfig/node14": "^1.0.0",
        "@tsconfig/node16": "^1.0.2",
        "acorn": "^8.4.1",
        "acorn-walk": "^8.1.1",
        "arg": "^4.1.0",
        "create-require": "^1.1.0",
        "diff": "^4.0.1",
        "make-error": "^1.1.1",
        "v8-compile-cache-lib": "^3.0.1",
        "yn": "3.1.1"
      }
    },
    "tslib": {
      "version": "2.5.0",
      "resolved": "https://registry.npmjs.org/tslib/-/tslib-2.5.0.tgz",
      "integrity": "sha512-336iVw3rtn2BUK7ORdIAHTyxHGRIHVReokCR3XjbckJMK7ms8FysBfhLR8IXnAgy7T0PTPNBWKiH514FOW/WSg=="
    },
    "tvm-disassembler": {
      "version": "2.0.0",
      "resolved": "https://registry.npmjs.org/tvm-disassembler/-/tvm-disassembler-2.0.0.tgz",
      "integrity": "sha512-59WejM7BhGl0Z6H6ZFaUwrc0WixAzX9O9VX6qhUBoD+O2RcYA7zs1cYFTSDW5eOs40Fv4LuG4P6sdlF9YR11zw==",
      "requires": {}
    },
    "tweetnacl": {
      "version": "1.0.3",
      "resolved": "https://registry.npmjs.org/tweetnacl/-/tweetnacl-1.0.3.tgz",
      "integrity": "sha512-6rt+RN7aOi1nGMyC4Xa5DdYiukl2UWCbcJft7YhxReBGQD7OAM8Pbxw6YMo4r2diNEA8FEmu32YOn9rhaiE5yw=="
    },
    "type-detect": {
      "version": "4.0.8",
      "resolved": "https://registry.npmjs.org/type-detect/-/type-detect-4.0.8.tgz",
      "integrity": "sha512-0fr/mIH1dlO+x7TlcMy+bIDqKPsw/70tVyeHW787goQjhmqaZe10uwLujubK9q9Lg6Fiho1KUKDYz0Z7k7g5/g=="
    },
    "type-fest": {
      "version": "0.21.3",
      "resolved": "https://registry.npmjs.org/type-fest/-/type-fest-0.21.3.tgz",
      "integrity": "sha512-t0rzBq87m3fVcduHDUFhKmyyX+9eo6WQjZvf51Ea/M0Q7+T374Jp1aUiyUl0GKxp8M/OETVHSDvmkyPgvX+X2w=="
    },
    "typescript": {
      "version": "4.9.5",
      "resolved": "https://registry.npmjs.org/typescript/-/typescript-4.9.5.tgz",
      "integrity": "sha512-1FXk9E2Hm+QzZQ7z+McJiHL4NW1F2EzMu9Nq9i3zAaGqibafqYwCVU6WyWAuyQRRzOlxou8xZSyXLEN8oKj24g=="
    },
    "uint8arrays": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/uint8arrays/-/uint8arrays-3.1.1.tgz",
      "integrity": "sha512-+QJa8QRnbdXVpHYjLoTpJIdCTiw9Ir62nocClWuXIq2JIh4Uta0cQsTSpFL678p2CN8B+XSApwcU+pQEqVpKWg==",
      "requires": {
        "multiformats": "^9.4.2"
      }
    },
    "update-browserslist-db": {
      "version": "1.0.10",
      "resolved": "https://registry.npmjs.org/update-browserslist-db/-/update-browserslist-db-1.0.10.tgz",
      "integrity": "sha512-OztqDenkfFkbSG+tRxBeAnCVPckDBcvibKd35yDONx6OU8N7sqgwc7rCbkJ/WcYtVRZ4ba68d6byhC21GFh7sQ==",
      "requires": {
        "escalade": "^3.1.1",
        "picocolors": "^1.0.0"
      }
    },
    "upper-case": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/upper-case/-/upper-case-2.0.2.tgz",
      "integrity": "sha512-KgdgDGJt2TpuwBUIjgG6lzw2GWFRCW9Qkfkiv0DxqHHLYJHmtmdUIKcZd8rHgFSjopVTlw6ggzCm1b8MFQwikg==",
      "requires": {
        "tslib": "^2.0.3"
      }
    },
    "upper-case-first": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/upper-case-first/-/upper-case-first-2.0.2.tgz",
      "integrity": "sha512-514ppYHBaKwfJRK/pNC6c/OxfGa0obSnAl106u97Ed0I625Nin96KAjttZF6ZL3e1XLtphxnqrOi9iWgm+u+bg==",
      "requires": {
        "tslib": "^2.0.3"
      }
    },
    "util-deprecate": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/util-deprecate/-/util-deprecate-1.0.2.tgz",
      "integrity": "sha512-EPD5q1uXyFxJpCrLnCc1nHnq3gOa6DZBocAIiI2TaSCA7VCJ1UJDMagCzIkXNsUYfD1daK//LTEQ8xiIbrHtcw=="
    },
    "v8-compile-cache-lib": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/v8-compile-cache-lib/-/v8-compile-cache-lib-3.0.1.tgz",
      "integrity": "sha512-wa7YjyUGfNZngI/vtK0UHAN+lgDCxBPCylVXGp0zu59Fz5aiGtNXaq3DhIov063MorB+VfufLh3JlF2KdTK3xg=="
    },
    "v8-to-istanbul": {
      "version": "9.0.1",
      "resolved": "https://registry.npmjs.org/v8-to-istanbul/-/v8-to-istanbul-9.0.1.tgz",
      "integrity": "sha512-74Y4LqY74kLE6IFyIjPtkSTWzUZmj8tdHT9Ii/26dvQ6K9Dl2NbEfj0XgU2sHCtKgt5VupqhlO/5aWuqS+IY1w==",
      "requires": {
        "@jridgewell/trace-mapping": "^0.3.12",
        "@types/istanbul-lib-coverage": "^2.0.1",
        "convert-source-map": "^1.6.0"
      }
    },
    "walker": {
      "version": "1.0.8",
      "resolved": "https://registry.npmjs.org/walker/-/walker-1.0.8.tgz",
      "integrity": "sha512-ts/8E8l5b7kY0vlWLewOkDXMmPdLcVV4GmOQLyxuSswIJsweeFZtAsMF7k1Nszz+TYBQrlYRmzOnr398y1JemQ==",
      "requires": {
        "makeerror": "1.0.12"
      }
    },
    "wcwidth": {
      "version": "1.0.1",
      "resolved": "https://registry.npmjs.org/wcwidth/-/wcwidth-1.0.1.tgz",
      "integrity": "sha512-XHPEwS0q6TaxcvG85+8EYkbiCux2XtWG2mkc47Ng2A77BQu9+DqIOJldST4HgPkuea7dvKSj5VgX3P1d4rW8Tg==",
      "requires": {
        "defaults": "^1.0.3"
      }
    },
    "webidl-conversions": {
      "version": "3.0.1",
      "resolved": "https://registry.npmjs.org/webidl-conversions/-/webidl-conversions-3.0.1.tgz",
      "integrity": "sha512-2JAn3z8AR6rjK8Sm8orRC0h/bcl/DqL7tRPdGZ4I1CjdF+EaMLmYxBHyXuKL849eucPFhvBoxMsflfOb8kxaeQ=="
    },
    "whatwg-fetch": {
      "version": "3.6.2",
      "resolved": "https://registry.npmjs.org/whatwg-fetch/-/whatwg-fetch-3.6.2.tgz",
      "integrity": "sha512-bJlen0FcuU/0EMLrdbJ7zOnW6ITZLrZMIarMUVmdKtsGvZna8vxKYaexICWPfZ8qwf9fzNq+UEIZrnSaApt6RA=="
    },
    "whatwg-url": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/whatwg-url/-/whatwg-url-5.0.0.tgz",
      "integrity": "sha512-saE57nupxk6v3HY35+jzBwYa0rKSy0XR8JSxZPwgLr7ys0IBzhGviA1/TUGJLmSVqs8pb9AnvICXEuOHLprYTw==",
      "requires": {
        "tr46": "~0.0.3",
        "webidl-conversions": "^3.0.0"
      }
    },
    "which": {
      "version": "2.0.2",
      "resolved": "https://registry.npmjs.org/which/-/which-2.0.2.tgz",
      "integrity": "sha512-BLI3Tl1TW3Pvl70l3yq3Y64i+awpwXqsGBYWkkqMtnbXgrMD+yj7rhW0kuEDxzJaYXGjEW5ogapKNMEKNMjibA==",
      "requires": {
        "isexe": "^2.0.0"
      }
    },
    "wrap-ansi": {
      "version": "7.0.0",
      "resolved": "https://registry.npmjs.org/wrap-ansi/-/wrap-ansi-7.0.0.tgz",
      "integrity": "sha512-YVGIj2kamLSTxw6NsZjoBxfSwsn0ycdesmc4p+Q21c5zPuZ1pl+NfxVdxPtdHvmNVOQ6XSYG4AUtyt/Fi7D16Q==",
      "requires": {
        "ansi-styles": "^4.0.0",
        "string-width": "^4.1.0",
        "strip-ansi": "^6.0.0"
      }
    },
    "wrappy": {
      "version": "1.0.2",
      "resolved": "https://registry.npmjs.org/wrappy/-/wrappy-1.0.2.tgz",
      "integrity": "sha512-l4Sp/DRseor9wL6EvV2+TuQn63dMkPjZ/sp9XkghTEbV9KlPS1xUsZ3u7/IQO4wxtcFB4bgpQPRcR3QCvezPcQ=="
    },
    "write-file-atomic": {
      "version": "5.0.0",
      "resolved": "https://registry.npmjs.org/write-file-atomic/-/write-file-atomic-5.0.0.tgz",
      "integrity": "sha512-R7NYMnHSlV42K54lwY9lvW6MnSm1HSJqZL3xiSgi9E7//FYaI74r2G0rd+/X6VAMkHEdzxQaU5HUOXWUz5kA/w==",
      "requires": {
        "imurmurhash": "^0.1.4",
        "signal-exit": "^3.0.7"
      }
    },
    "y18n": {
      "version": "5.0.8",
      "resolved": "https://registry.npmjs.org/y18n/-/y18n-5.0.8.tgz",
      "integrity": "sha512-0pfFzegeDWJHJIAmTLRP2DwHjdF5s7jo9tuztdQxAhINCdvS+3nGINqPd00AphqJR/0LhANUS6/+7SCb98YOfA=="
    },
    "yallist": {
      "version": "4.0.0",
      "resolved": "https://registry.npmjs.org/yallist/-/yallist-4.0.0.tgz",
      "integrity": "sha512-3wdGidZyq5PB084XLES5TpOSRA3wjXAlIWMhum2kRcv/41Sn2emQ0dycQW4uZXLejwKvg6EsvbdlVL+FYEct7A=="
    },
    "yargs": {
      "version": "17.6.2",
      "resolved": "https://registry.npmjs.org/yargs/-/yargs-17.6.2.tgz",
      "integrity": "sha512-1/9UrdHjDZc0eOU0HxOHoS78C69UD3JRMvzlJ7S79S2nTaWRA/whGCTV8o9e/N/1Va9YIV7Q4sOxD8VV4pCWOw==",
      "requires": {
        "cliui": "^8.0.1",
        "escalade": "^3.1.1",
        "get-caller-file": "^2.0.5",
        "require-directory": "^2.1.1",
        "string-width": "^4.2.3",
        "y18n": "^5.0.5",
        "yargs-parser": "^21.1.1"
      }
    },
    "yargs-parser": {
      "version": "21.1.1",
      "resolved": "https://registry.npmjs.org/yargs-parser/-/yargs-parser-21.1.1.tgz",
      "integrity": "sha512-tVpsJW7DdjecAiFpbIB1e3qxIQsE6NoPc5/eTdrbbIC4h0LVsWhnoa3g+m2HclBIujHzsxZ4VJVA+GUuc2/LBw=="
    },
    "yn": {
      "version": "3.1.1",
      "resolved": "https://registry.npmjs.org/yn/-/yn-3.1.1.tgz",
      "integrity": "sha512-Ux4ygGWsu2c7isFWe8Yu1YluJmqVhxqK2cLXNQA5AcC3QfbGNpM7fu0Y8b/z16pXLnFxZYvWhd3fhBY9DLmC6Q=="
    },
    "yocto-queue": {
      "version": "0.1.0",
      "resolved": "https://registry.npmjs.org/yocto-queue/-/yocto-queue-0.1.0.tgz",
      "integrity": "sha512-rVksvsnNCdJ/ohGc6xgPwyN8eheCxsiLM8mxuE/t/mOVqJewPuO1miLpTHQiRgTKCLexL4MeAFVagts7HmNZ2Q=="
    },
    "zod": {
      "version": "3.20.2",
      "resolved": "https://registry.npmjs.org/zod/-/zod-3.20.2.tgz",
      "integrity": "sha512-1MzNQdAvO+54H+EaK5YpyEy0T+Ejo/7YLHS93G3RnYWh5gaotGHwGeN/ZO687qEDU2y4CdStQYXVHIgrUl5UVQ=="
    }
  }
}


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/package.json
{
  "private": true,
  "scripts": {
    "build": "tact --config ./tact.config.json",
    "test": "jest",
    "deploy": "ts-node ./sources/contract.deploy.ts",
    "api_deploy": "ts-node ./sources/contract.deploy_api.ts",
    "read": "ts-node ./sources/contract.read.ts"
  },
  "dependencies": {
    "@orbs-network/ton-access": "^2.2.2",
    "@tact-lang/compiler": "~1.3.0",
    "@tact-lang/coverage": "^0.0.8",
    "@tact-lang/deployer": "^0.2.0",
    "@tact-lang/emulator": "^4.2.3",
    "@tact-lang/ton-abi": "^0.0.3",
    "@tact-lang/ton-jest": "^0.0.4",
    "@ton/core": "^0.55.0",
    "@ton/crypto": "^3.2.0",
    "@ton/sandbox": "^0.19.0",
    "@ton/test-utils": "^0.4.2",
    "@ton/ton": "^13.9.0",
    "@types/jest": "^29.2.4",
    "@types/node": "^18.11.14",
    "@types/qs": "^6.9.7",
    "base64url": "^3.0.1",
    "dotenv": "^16.0.3",
    "enquirer": "^2.3.6",
    "jest": "^29.3.1",
    "open": "^8.4.0",
    "prando": "^6.0.1",
    "prettier": "^2.5.1",
    "qs": "^6.11.0",
    "ts-jest": "^29.0.3",
    "ts-node": "^10.9.1",
    "typescript": "^4.9.4"
  }
}


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/tact.config.json
{
    "projects": [{
        "name": "sample",
        "path": "./sources/contract.tact",
        "output": "./sources/output",
        "options": {
            "external": true,  
            "debug": true   
        }
    }]
}

## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/tsconfig.json
{
  "compilerOptions": {
    /* Visit https://aka.ms/tsconfig.json to read more about this file */
    /* Basic Options */
    // "incremental": true,                         /* Enable incremental compilation */
    "target": "esnext", /* Specify ECMAScript target version: 'ES3' (default), 'ES5', 'ES2015', 'ES2016', 'ES2017', 'ES2018', 'ES2019', 'ES2020', 'ES2021', or 'ESNEXT'. */
    "module": "commonjs", /* Specify module code generation: 'none', 'commonjs', 'amd', 'system', 'umd', 'es2015', 'es2020', or 'ESNext'. */
    // "lib": [],                                   /* Specify library files to be included in the compilation. */
    // "allowJs": true,                             /* Allow javascript files to be compiled. */
    // "checkJs": true,                             /* Report errors in .js files. */
    // "jsx": "preserve",                           /* Specify JSX code generation: 'preserve', 'react-native', 'react', 'react-jsx' or 'react-jsxdev'. */
    "declaration": true, /* Generates corresponding '.d.ts' file. */
    // "declarationMap": true,                      /* Generates a sourcemap for each corresponding '.d.ts' file. */
    // "sourceMap": true,                           /* Generates corresponding '.map' file. */
    // "outFile": "./",                             /* Concatenate and emit output to single file. */
    "outDir": "./dist", /* Redirect output structure to the directory. */
    // "rootDir": "./",                             /* Specify the root directory of input files. Use to control the output directory structure with --outDir. */
    // "composite": true,                           /* Enable project compilation */
    // "tsBuildInfoFile": "./",                     /* Specify file to store incremental compilation information */
    // "removeComments": true,                      /* Do not emit comments to output. */
    // "noEmit": false,                              /* Do not emit outputs. */
    // "importHelpers": true,                       /* Import emit helpers from 'tslib'. */
    "downlevelIteration": true, /* Provide full support for iterables in 'for-of', spread, and destructuring when targeting 'ES5' or 'ES3'. */
    // "isolatedModules": true,                     /* Transpile each file as a separate module (similar to 'ts.transpileModule'). */
    /* Strict Type-Checking Options */
    "strict": true, /* Enable all strict type-checking options. */
    // "noImplicitAny": true,                       /* Raise error on expressions and declarations with an implied 'any' type. */
    // "strictNullChecks": true,                    /* Enable strict null checks. */
    // "strictFunctionTypes": true,                 /* Enable strict checking of function types. */
    // "strictBindCallApply": true,                 /* Enable strict 'bind', 'call', and 'apply' methods on functions. */
    // "strictPropertyInitialization": true,        /* Enable strict checking of property initialization in classes. */
    // "noImplicitThis": true,                      /* Raise error on 'this' expressions with an implied 'any' type. */
    // "alwaysStrict": true,                        /* Parse in strict mode and emit "use strict" for each source file. */
    /* Additional Checks */
    // "noUnusedLocals": true,                      /* Report errors on unused locals. */
    // "noUnusedParameters": true,                  /* Report errors on unused parameters. */
    // "noImplicitReturns": true,                   /* Report error when not all code paths in function return a value. */
    // "noFallthroughCasesInSwitch": true,          /* Report errors for fallthrough cases in switch statement. */
    // "noUncheckedIndexedAccess": true,            /* Include 'undefined' in index signature results */
    // "noImplicitOverride": true,                  /* Ensure overriding members in derived classes are marked with an 'override' modifier. */
    // "noPropertyAccessFromIndexSignature": true,  /* Require undeclared properties from index signatures to use element accesses. */
    /* Module Resolution Options */
    // "moduleResolution": "node",                  /* Specify module resolution strategy: 'node' (Node.js) or 'classic' (TypeScript pre-1.6). */
    // "baseUrl": "./",                             /* Base directory to resolve non-absolute module names. */
    // "paths": {},                                 /* A series of entries which re-map imports to lookup locations relative to the 'baseUrl'. */
    // "rootDirs": [],                              /* List of root folders whose combined content represents the structure of the project at runtime. */
    // "typeRoots": [],                             /* List of folders to include type definitions from. */
    // "types": [],                                 /* Type declaration files to be included in compilation. */
    "allowSyntheticDefaultImports": true, /* Allow default imports from modules with no default export. This does not affect code emit, just typechecking. */
    "esModuleInterop": true, /* Enables emit interoperability between CommonJS and ES Modules via creation of namespace objects for all imports. Implies 'allowSyntheticDefaultImports'. */
    // "preserveSymlinks": true,                    /* Do not resolve the real path of symlinks. */
    // "allowUmdGlobalAccess": true,                /* Allow accessing UMD globals from modules. */
    /* Source Map Options */
    // "sourceRoot": "",                            /* Specify the location where debugger should locate TypeScript files instead of source locations. */
    // "mapRoot": "",                               /* Specify the location where debugger should locate map files instead of generated locations. */
    // "inlineSourceMap": true,                     /* Emit a single file with source maps instead of having a separate file. */
    // "inlineSources": true,                       /* Emit the source alongside the sourcemaps within a single file; requires '--inlineSourceMap' or '--sourceMap' to be set. */
    /* Experimental Options */
    // "experimentalDecorators": true,              /* Enables experimental support for ES7 decorators. */
    // "emitDecoratorMetadata": true,               /* Enables experimental support for emitting type metadata for decorators. */
    /* Advanced Options */
    "skipLibCheck": true, /* Skip type checking of declaration files. */
    "forceConsistentCasingInFileNames": true /* Disallow inconsistently-cased references to the same file. */,
    "resolveJsonModule": true
  },
  "include": [
    "src/**/*"
  ]
}

## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/contract.deploy.ts
import { beginCell, contractAddress, toNano, Address } from "@ton/ton";
import { deploy } from "./utils/deploy";
import { printAddress, printDeploy, printHeader } from "./utils/print";
// ================================================================= //
import { NftCollection } from "./output/sample_NftCollection";
// ================================================================= //

(async () => {
    const OFFCHAIN_CONTENT_PREFIX = 0x01;
    const string_first = "https://s.getgems.io/nft-staging/c/628f6ab8077060a7a8d52d63/"; // Change to the content URL you prepared
    let newContent = beginCell().storeInt(OFFCHAIN_CONTENT_PREFIX, 8).storeStringRefTail(string_first).endCell();

    // ===== Parameters =====
    // Replace owner with your address
    let owner = Address.parse("YOUR ADDRESS"); // 🔴🔴🔴

    // Prepare the initial code and data for the contract
    let init = await NftCollection.init(owner, newContent, {
        $$type: "RoyaltyParams",
        numerator: 350n, // 350n = 35%
        denominator: 1000n,
        destination: owner,
    });

    let address = contractAddress(0, init);
    let deployAmount = toNano("0.15");
    let testnet = true;

    // The Transaction body we want to pass to the smart contract
    let body = beginCell().storeUint(0, 32).storeStringTail("Mint").endCell();

    // Do deploy
    await deploy(init, deployAmount, body, testnet);
    printHeader("sampleNFT_Contract");
    printAddress(address);
})();


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/contract.deploy_api.ts
import {
    Address,
    beginCell,
    contractAddress,
    toNano,
    TonClient4,
    internal,
    fromNano,
    WalletContractV4,
} from "@ton/ton";
import { deploy } from "./utils/deploy";
import { printAddress, printDeploy, printHeader, printSeparator } from "./utils/print";
import { mnemonicToPrivateKey } from "@ton/crypto";
import * as dotenv from "dotenv";
dotenv.config();
// ================================================================= //
import { NftCollection } from "./output/sample_NftCollection";
import { NftItem } from "./output/sample_NftItem";
// ================================================================= //

(async () => {
    // Create client for testnet sandboxv4 API - alternative endpoint
    const client4 = new TonClient4({
        endpoint: "https://sandbox-v4.tonhubapi.com", // Test-net
    });

    // Parameters for NFTs
    const OFFCHAIN_CONTENT_PREFIX = 0x01;
    const string_first = "https://s.getgems.io/nft-staging/c/628f6ab8077060a7a8d52d63/"; // Change to the content URL you prepared
    let newContent = beginCell().storeInt(OFFCHAIN_CONTENT_PREFIX, 8).storeStringRefTail(string_first).endCell();

    let mnemonics = (process.env.mnemonics_2 || "").toString(); // 🔴 Change to your own, by creating .env file!
    let keyPair = await mnemonicToPrivateKey(mnemonics.split(" "));
    let secretKey = keyPair.secretKey;
    let workchain = 0;
    let wallet = WalletContractV4.create({ workchain, publicKey: keyPair.publicKey });
    let wallet_contract = client4.open(wallet);
    console.log("Wallet address: ", wallet_contract.address);

    // Replace owner with your address
    let owner = wallet.address;

    // Prepare the initial code and data for the contract
    let init = await NftCollection.init(owner, newContent, {
        $$type: "RoyaltyParams",
        numerator: 350n, // 350n = 35%
        denominator: 1000n,
        destination: owner,
    });
    let deployContract = contractAddress(0, init);
    // ========================================
    let packed = beginCell().storeUint(0, 32).storeStringTail("Mint").endCell();
    // ========================================
    let deployAmount = toNano("0.3");
    let seqno: number = await wallet_contract.getSeqno();
    let balance: bigint = await wallet_contract.getBalance();
    // ========================================
    console.log("Current deployment wallet balance: ", fromNano(balance).toString(), "💎TON");
    printSeparator();
    console.log("Deploying contract to address: ", deployContract);
    await wallet_contract.sendTransfer({
        seqno,
        secretKey,
        messages: [
            internal({
                to: deployContract,
                value: deployAmount,
                init: { code: init.code, data: init.data },
                bounce: true,
                body: packed,
            }),
        ],
    });

    let collection_client = client4.open(NftCollection.fromAddress(deployContract));
    let latest_indexId = (await collection_client.getGetCollectionData()).next_item_index;
    console.log("Latest indexID:[", latest_indexId, "]");
    let item_address = await collection_client.getGetNftAddressByIndex(latest_indexId);
    console.log("Minting NFT Item: ", item_address);
})();


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/contract.read.ts
import { beginCell, contractAddress, toNano, Cell, Address, TonClient4 } from "ton";
import { deploy } from "./utils/deploy";
import { printAddress, printDeploy, printHeader } from "./utils/print";
// ================================================================= //
import { NftCollection } from "./output/sample_NftCollection";
// ================================================================= //

(async () => {
    const client = new TonClient4({
        // endpoint: "https://mainnet-v4.tonhubapi.com", // 🔴 Main-net API endpoint
        endpoint: "https://sandbox-v4.tonhubapi.com", // 🔴 Test-net API endpoint
    });

    // Parameters
    let collection_address = Address.parse("YOUR Collection ADDRESS");

    let contract_address = await NftCollection.fromAddress(collection_address);
    let client_open = client.open(contract_address);

    const nft_index = 0n;
    let address_by_index = await client_open.getGetNftAddressByIndex(nft_index);
    printHeader("sampleNFT_Contract");
    // printAddress(collection_address
    // printHeader("1234");
    console.log("NFT ID[" + nft_index + "]: " + address_by_index);
})();


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/contract.tact
import "./message.tact";
const minTonsForStorage: Int = ton("0.02");
const gasConsumption: Int = ton("0.02");

contract NftCollection {
    next_item_index: Int as uint32 = 0;
    owner_address: Address;
    royalty_params: RoyaltyParams?;                      
    collection_content: Cell;   

    init(owner_address: Address, collection_content: Cell, royalty_params: RoyaltyParams){
        self.owner_address = owner_address;
        self.collection_content = collection_content; 
        self.royalty_params = royalty_params;
    }

    receive("Mint"){
        let ctx: Context = context(); // get sender Info
        let msgValue: Int = ctx.value;
        let tonBalanceBeforeMsg: Int = myBalance() - msgValue;
        let storageFee: Int = minTonsForStorage - min(tonBalanceBeforeMsg, minTonsForStorage);
        msgValue = msgValue - (storageFee + gasConsumption);
        self.mint(ctx.sender, msgValue);

        emit(LogEventMintRecord{ minter: sender(), item_id: self.next_item_index, generate_number: nativeRandom() }.toCell());
    }

    // ===== Private Methods ===== //
    fun mint(sender: Address, msgValue: Int) {
        require(self.next_item_index >= 0, "non-sequential NFTs");
        let nft_init: StateInit = self.getNftItemInit(self.next_item_index);
        send(SendParameters{
                to: contractAddress(nft_init), 
                value: msgValue, 
                bounce: false,
                mode: SendIgnoreErrors,
                body: Transfer {
                    query_id: 0,
                    new_owner: sender,
                    response_destination: self.owner_address,
                    custom_payload: self.collection_content,
                    forward_amount: 0,
                    forward_payload: emptySlice()
                }.toCell(),
                code: nft_init.code,
                data: nft_init.data
            });
        // dump(self.next_item_index); // Reference at: https://tact-by-example.org/03-emit
        self.next_item_index = self.next_item_index + 1;
    }

    receive(msg: GetRoyaltyParams) {   
        let ctx: Context = context(); // get sender Info
        send(SendParameters{
            to: ctx.sender,
            value: 0,
            mode: 64, 
            bounce: false,
            body: ReportRoyaltyParams {
                query_id: msg.query_id,
                numerator:  (self.royalty_params!!).numerator,
                denominator: (self.royalty_params!!).denominator,
                destination: self.owner_address
            }.toCell()
        });        
    }

    // ------------------ Get Function  ------------------ //
    get fun get_collection_data(): CollectionData {     
        let b: StringBuilder = beginString();
        let collectionDataString: String = self.collection_content.asSlice().asString();
        b.append(collectionDataString);
        b.append("meta.json"); // You can changed this your self.
        return CollectionData{
            next_item_index: self.next_item_index, 
            collection_content: b.toCell(), 
            owner_address: self.owner_address
        };
    }

    get fun get_nft_address_by_index(item_index: Int): Address?{      
        let initCode: StateInit = self.getNftItemInit(item_index);
        return contractAddress(initCode);
    }

    get fun getNftItemInit(item_index: Int): StateInit {
        return initOf NftItem(myAddress(), item_index);
    }
    
    get fun get_nft_content(index: Int, individual_content: Cell): Cell { 
        let b: StringBuilder = beginString();
        let ic: String = individual_content.asSlice().asString();
        b.append(ic);
        return b.toCell();
    }

    get fun royalty_params(): RoyaltyParams {
        return self.royalty_params!!;
    }
}

contract NftItem {
    collection_address: Address;
    item_index: Int; 
    is_initialized: Bool;

    owner: Address?;
    individual_content: Cell?;

    init(collection_address: Address, item_index: Int){
        require(sender() == collection_address, "not from collection");
        self.collection_address = collection_address;
        self.item_index = item_index;
        self.is_initialized = false;
    }

    receive(msg: Transfer){
        let ctx: Context = context(); // Reference: https://docs.tact-lang.org/language/ref/common#context
        let msgValue: Int = self.msgValue(ctx.value);
        
        if (self.is_initialized == false) {  // Initial Transfer, aka the "Minting" of the NFT
            require(ctx.sender == self.collection_address, "initialized tx need from collection");
            self.is_initialized = true;
            self.owner = msg.new_owner;
            self.individual_content = msg.custom_payload;
            send(SendParameters{
                to: msg.response_destination!!,
                value: msgValue,
                mode: SendPayGasSeparately,
                body: Excesses { query_id: msg.query_id }.toCell()
            });
        } else {
            require(ctx.sender == self.owner!!, "not owner");
            self.owner = msg.new_owner;  // change current owner to the new_owner
            if (msg.forward_amount > 0) {
                send(SendParameters{
                    to: msg.new_owner,
                    value: msg.forward_amount,
                    mode:  SendPayGasSeparately, 
                    bounce: true,
                    body: OwnershipAssigned{
                        query_id: msg.query_id,
                        prev_owner: ctx.sender,
                        forward_payload: msg.forward_payload
                    }.toCell()
                }); 
            }

            msgValue = msgValue - ctx.readForwardFee(); 
            if (msg.response_destination != null) { 
                send(SendParameters{ 
                    to: msg.response_destination!!,
                    value: msgValue - msg.forward_amount,
                    mode: SendPayGasSeparately,
                    bounce: true,
                    body: Excesses { query_id: msg.query_id }.toCell()
                });
            } 
        }
    }
    
    receive(msg: GetStaticData){ 
        let ctx: Context = context();
        send(SendParameters {
            to: ctx.sender,
            value: 0,
            mode: 64,  // (return msg amount except gas fees) 
            bounce: true,
            body: ReportStaticData{
                query_id: msg.query_id,
                index_id: self.item_index,
                collection: self.collection_address
            }.toCell()
        });
    }

    fun msgValue(value: Int): Int {
        let tonBalanceBeforeMsg: Int = myBalance() - value;
        let storageFee: Int = minTonsForStorage - min(tonBalanceBeforeMsg, minTonsForStorage);
        return value - (storageFee + gasConsumption);
    }

    // --------- Get Function  --------- //
    get fun get_nft_data(): GetNftData {
        let b: StringBuilder = beginString();
        let collectionData: String = (self.individual_content!!).asSlice().asString();
        b.append(collectionData);
        b.append(self.item_index.toString());
        b.append(".json");

        return GetNftData {
            is_initialized: self.is_initialized, 
            index: self.item_index, 
            collection_address: self.collection_address, 
            owner_address: self.owner!!,
            individual_content: b.toCell()
        };
    }
}


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/message.tact
message LogEventMintRecord {
    minter: Address;
    item_id: Int;
    generate_number: Int;
}


message(0x693d3950) GetRoyaltyParams {
    query_id: Int as uint64;
}
message(0xa8cb00ad) ReportRoyaltyParams {
    query_id: Int as uint64;
    numerator: Int as uint16;
    denominator: Int as uint16;
    destination: Address;
}
struct CollectionData {
    next_item_index: Int;
    collection_content: Cell;
    owner_address: Address;
}
struct RoyaltyParams {
    numerator: Int;
    denominator: Int;
    destination: Address;
}
message(0x5fcc3d14) Transfer {
    query_id: Int as uint64;
    new_owner: Address;
    response_destination: Address?;
    custom_payload: Cell?;
    forward_amount: Int as coins;
    forward_payload: Slice as remaining;
}
message(0x05138d91) OwnershipAssigned {
    query_id: Int as uint64;
    prev_owner: Address;
    forward_payload: Slice as remaining;
}
message(0xd53276db) Excesses {
    query_id: Int as uint64;
}
message(0x2fcb26a2) GetStaticData {
    query_id: Int as uint64;
}
message(0x8b771735) ReportStaticData {
    query_id: Int as uint64;
    index_id: Int;
    collection: Address;
}
struct GetNftData {
    is_initialized: Bool;
    index: Int;
    collection_address: Address;
    owner_address: Address;
    individual_content: Cell;
}

## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/test.spec.ts
import { toNano, beginCell } from "@ton/ton";
import {
    Blockchain,
    SandboxContract,
    TreasuryContract,
    printTransactionFees,
    prettyLogTransactions,
} from "@ton/sandbox";
import "@ton/test-utils";
import { printSeparator } from "./utils/print";
import { NftCollection, RoyaltyParams, loadLogEventMintRecord } from "./output/sample_NftCollection";
import { NftItem } from "./output/sample_NftItem";

describe("contract", () => {
    const OFFCHAIN_CONTENT_PREFIX = 0x01;
    const string_first = "https://s.getgems.io/nft-staging/c/628f6ab8077060a7a8d52d63/";
    let newContent = beginCell().storeInt(OFFCHAIN_CONTENT_PREFIX, 8).storeStringRefTail(string_first).endCell();

    let blockchain: Blockchain;
    let deployer: SandboxContract<TreasuryContract>;
    let collection: SandboxContract<NftCollection>;

    beforeAll(async () => {
        blockchain = await Blockchain.create();
        deployer = await blockchain.treasury("deployer");

        let royaltiesParam: RoyaltyParams = {
            $$type: "RoyaltyParams",
            numerator: 350n, // 350n = 35%
            denominator: 1000n,
            destination: deployer.address,
        };

        collection = blockchain.openContract(
            await NftCollection.fromInit(deployer.address, newContent, royaltiesParam)
        );

        const deploy_result = await collection.send(deployer.getSender(), { value: toNano(1) }, "Mint");
        expect(deploy_result.transactions).toHaveTransaction({
            from: deployer.address,
            to: collection.address,
            deploy: true,
            success: true,
        });
    });

    it("Test", async () => {
        console.log("Next IndexID: " + (await collection.getGetCollectionData()).next_item_index);
        console.log("Collection Address: " + collection.address);
    });

    it("Test Mint Record in detail", async () => {
        const deploy_result = await collection.send(deployer.getSender(), { value: toNano(1) }, "Mint"); // Send Mint Transaction
        printTransactionFees(deploy_result.transactions);
        prettyLogTransactions(deploy_result.transactions);
    });

    it("should deploy correctly", async () => {
        await collection.send(deployer.getSender(), { value: toNano(2) }, "Mint");

        let current_index = (await collection.getGetCollectionData()).next_item_index;
        const deploy_result = await collection.send(deployer.getSender(), { value: toNano(1) }, "Mint"); // Send Mint Transaction
        expect(deploy_result.transactions).toHaveTransaction({
            from: deployer.address,
            to: collection.address,
            success: true,
        });
        let next_index = (await collection.getGetCollectionData()).next_item_index;
        expect(next_index).toEqual(current_index + 1n);
        printSeparator();

        console.log("External Message(string - base64): " + deploy_result.externals[0].body.toBoc().toString("base64"));
        console.log("External Message(string - hex): " + deploy_result.externals[0].body.toBoc().toString("hex"));
        printSeparator();

        // Print the Log Event of the Mint Record
        let loadEvent = loadLogEventMintRecord(deploy_result.externals[0].body.asSlice());
        console.log("ItemId: " + loadEvent.item_id);
        console.log("The Random Number: " + loadEvent.generate_number);
    });
});


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/utils/deploy.ts
import { beginCell, Cell, contractAddress, storeStateInit } from "@ton/core";
import { prompt } from "enquirer";
import open from "open";
import base64url from "base64url";
import { printSeparator } from "./print";
import qs from "qs";

function getLink(
    prefix: string,
    init: { code: Cell; data: Cell },
    value: bigint,
    command: Cell | string,
    testnet: boolean
) {
    // Resolve target address
    let to = contractAddress(0, init);

    // Resovle init
    let initStr = base64url(beginCell().store(storeStateInit(init)).endCell().toBoc({ idx: false }));

    let link: string;
    if (typeof command === "string") {
        link =
            prefix +
            `transfer/` +
            to.toString({ testOnly: testnet }) +
            "?" +
            qs.stringify({
                text: command,
                amount: value.toString(10),
                init: initStr,
            });
    } else {
        link =
            prefix +
            `transfer/` +
            to.toString({ testOnly: testnet }) +
            "?" +
            qs.stringify({
                text: "Deploy contract",
                amount: value.toString(10),
                init: initStr,
                bin: base64url(command.toBoc({ idx: false })),
            });
    }
    return link;
}

export function getTonhubLink(
    init: { code: Cell; data: Cell },
    value: bigint,
    command: Cell | string,
    testnet: boolean
) {
    return getLink(`https://${testnet ? "test." : ""}tonhub.com/`, init, value, command, testnet);
}

export function getTonkeeperLink(
    init: { code: Cell; data: Cell },
    value: bigint,
    command: Cell | string,
    testnet: boolean
) {
    return getLink(`https://app.tonkeeper.com/`, init, value, command, testnet);
}

export function getLocalLink(
    init: { code: Cell; data: Cell },
    value: bigint,
    command: Cell | string,
    testnet: boolean
) {
    return getLink(`ton://`, init, value, command, testnet);
}

export function get(init: { code: Cell; data: Cell }, value: bigint, command: Cell | string, testnet: boolean) {
    // Resolve target address
    let to = contractAddress(0, init);

    // Resovle init
    let initStr = base64url(beginCell().store(storeStateInit(init)).endCell().toBoc({ idx: false }));

    let link: string;
    if (typeof command === "string") {
        link =
            `https://${testnet ? "test." : ""}tonhub.com/transfer/` +
            to.toString({ testOnly: testnet }) +
            "?" +
            qs.stringify({
                text: command,
                amount: value.toString(10),
                init: initStr,
            });
    } else {
        link =
            `https://${testnet ? "test." : ""}tonhub.com/transfer/` +
            to.toString({ testOnly: testnet }) +
            "?" +
            qs.stringify({
                text: "Deploy contract",
                amount: value.toString(10),
                init: initStr,
                bin: base64url(command.toBoc({ idx: false })),
            });
    }
    return link;
}

export async function deploy(
    init: { code: Cell; data: Cell },
    value: bigint,
    command: Cell | string,
    testnet: boolean = true
) {
    let kind = (
        await prompt<{ kind: "tonhub" | "tonkeeper" | "local" }>([
            {
                type: "select",
                name: "kind",
                message: "Way to deploy",
                initial: 0,
                choices: [
                    {
                        message: "Tonhub/Sandbox",
                        name: "tonhub",
                    },
                    {
                        message: "Tonkeeper",
                        name: "tonkeeper",
                    },
                    {
                        message: "Open local link",
                        name: "local",
                    },
                ],
            },
        ])
    ).kind;

    // Show tonhub link
    if (kind === "tonhub") {
        printSeparator();
        console.log("Deploy: " + getTonhubLink(init, value, command, testnet));
        printSeparator();
        return;
    }

    // Show tonkeeper link
    if (kind === "tonkeeper") {
        printSeparator();
        console.log("Deploy: " + getTonkeeperLink(init, value, command, testnet));
        printSeparator();
        return;
    }

    // Show tonkeeper link
    if (kind === "local") {
        // Create a link and display to the user
        let l = getLocalLink(init, value, command, testnet);
        printSeparator();
        console.log("Deploy: " + l);
        printSeparator();

        // Open link
        open(l);

        return;
    }
}


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/utils/print.ts
import { Address, beginCell, Cell, contractAddress, storeStateInit } from "@ton/ton";
import qs from "qs";
import base64url from "base64url";

export function printSeparator() {
    console.log("========================================================================================");
}

export function printHeader(name: string) {
    printSeparator();
    console.log("Contract: " + name);
    printSeparator();
}

export function printAddress(address: Address, testnet: boolean = true) {
    console.log("Address: " + address.toString({ testOnly: testnet }));
    console.log(
        "Explorer: " +
            "https://" +
            (testnet ? "testnet." : "") +
            "tonviewer.com/" +
            address.toString({ testOnly: testnet })
    );
    printSeparator();
}

export function printDeploy(
    init: { code: Cell; data: Cell },
    value: bigint,
    command: Cell | string,
    testnet: boolean = true
) {
    // Resolve target address
    let to = contractAddress(0, init);

    // Resovle init
    let initStr = base64url(beginCell().store(storeStateInit(init)).endCell().toBoc({ idx: false }));

    let link: string;
    if (typeof command === "string") {
        link =
            `https://${testnet ? "test." : ""}tonhub.com/transfer/` +
            to.toString({ testOnly: testnet }) +
            "?" +
            qs.stringify({
                text: command,
                amount: value.toString(10),
                init: initStr,
            });
    } else {
        link =
            `https://${testnet ? "test." : ""}tonhub.com/transfer/` +
            to.toString({ testOnly: testnet }) +
            "?" +
            qs.stringify({
                text: "Deploy contract",
                amount: value.toString(10),
                init: initStr,
                bin: base64url(command.toBoc({ idx: false })),
            });
    }
    console.log("Deploy: " + link);
    printSeparator();
}


## Beginning of file https://github.com/howardpen9/nft-template-in-tact/blob/tutorial/nft-template-in-tact-tutorial/sources/utils/transfer.ts
import { getHttpEndpoint } from "@orbs-network/ton-access";
import { mnemonicToWalletKey } from "ton-crypto";
import { TonClient, WalletContractV4, Address, beginCell, toNano, internal} from "ton";


async function main() {
  const NFT_OWNER = Address.parse("EQDND6yHEzKB82ZGRn58aY9Tt_69Ie_uz73e2VuuJ3fVVXfV"); //wallet contract address of current owner NFT
  const NFT_DST = Address.parse("EQC4hErTeLrqzY05eiwMK4Wpy92QxAfYbgtOP7MhOKNnGj8Z"); // destination wallet contract address
  const NFT_ITEM = Address.parse("EQA2D8ZV0EaoXsXCLvQb4J8PBfm_0lEIkNdtcn3-DGJSXmV1"); // NFT item contract address, that will be transfered


  // initialize ton rpc client on testnet
  const endpoint = await getHttpEndpoint({ network: "testnet" });
  const client = new TonClient({ endpoint });

  // open wallet v4 (notice the correct wallet version here)
  const mnemonic = "multiply voice predict..."; // your 24 secret words (replace ... with the rest of the words)
  const key = await mnemonicToWalletKey(mnemonic.split(" "));
  const wallet = WalletContractV4.create({ publicKey: key.publicKey, workchain: 0 });
  if (!await client.isContractDeployed(wallet.address)) {
    return console.log("wallet is not deployed");
  }

  // open wallet and read the current seqno of the wallet
  const walletContract = client.open(wallet);
  const seqno = await walletContract.getSeqno();
  const queryId = 0;
  const secretKey = key.secretKey;
  const msgvalue = toNano("0.05");
  const forwardfee = toNano(1); // TODO need figure out how it should calculate

      //TLB: transfer#5fcc3d14 query_id:uint64 new_owner:address response_destination:address custom_payload:Maybe ^cell forward_amount:coins forward_payload:remainder<slice> = Transfer
      let msg_transfer_body = beginCell()
        .storeBuffer(Buffer.from("5fcc3d14", "hex"))
        .storeUint(queryId, 64)
        .storeAddress(NFT_DST)
        .storeAddress(NFT_OWNER)
        .storeUint(0,1)
        .storeCoins(forwardfee)
        .endCell()


      console.log('🛠️Preparing transfer NFT = ',NFT_ITEM ,' from ', NFT_OWNER);
      await walletContract.sendTransfer({
          seqno,
          secretKey,
          messages: [internal({
              value: msgvalue,
              to: NFT_ITEM,
              body: msg_transfer_body
          })]
      });
      console.log('======Sending NFT =', NFT_ITEM, ' to ', NFT_DST, ' ======');




}
main();

function sleep(ms: number) {
  return new Promise(resolve => setTimeout(resolve, ms));
}