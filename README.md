# @heavy-duty/spl-utils

The `@heavy-duty/spl-utils` package is a comprehensive collection of utility functions designed to simplify and enhance the development experience with Solana's SPL tokens. This package aims to provide developers with a set of tools that abstract away the complexities involved in interacting with SPL token contracts on the Solana blockchain, allowing for more efficient and streamlined development processes.

## Features

Currently, the package includes the following utility function:

- **createTransferInstructions**: Generates a list of transaction instructions for transferring SPL tokens. This function supports a variety of scenarios including basic transfers, transfers with memos, and optionally funding the recipient's associated token account if it doesn't exist. The flexibility of this function makes it suitable for a wide range of applications, from simple token transfers to more complex financial transactions.

## Usage

To use the `@heavy-duty/spl-utils` package in your project, you need to install it via npm or yarn:

```bash
npm install @heavy-duty/spl-utils
# or
yarn add @heavy-duty/spl-utils
```

Once installed, you can import and use the available utility functions in your project. For example, to create transfer instructions:

```typescript
import { createTransferInstructions } from '@heavy-duty/spl-utils';
import { PublicKey } from '@solana/web3.js';

const transferInstructions = createTransferInstructions({
  sender: new PublicKey('SenderPublicKeyHere'),
  receiver: new PublicKey('ReceiverPublicKeyHere'),
  mint: new PublicKey('TokenMintAddressHere'),
  amount: 100, // Amount of tokens to transfer
  memo: 'Optional memo',
  fundReceiver: true, // Optionally fund the receiver's associated token account
});
```

## Future Additions

The `@heavy-duty/spl-utils` package is actively under development, and we plan to extend its functionality with more utility functions over time. Our goal is to cover a broader range of SPL token functionalities, making it the go-to library for developers looking to build on the Solana ecosystem. We welcome contributions and suggestions from the community to help us expand this package.

## Contributing

We encourage contributions from the community! If you have suggestions for new utilities or improvements to existing ones, please feel free to submit an issue or pull request on our GitHub repository.

## License

This project is licensed under the [MIT License](LICENSE).
