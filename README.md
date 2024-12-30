# A simple encryption scheme available in ResNet

Users of the [ResNet app](https://resnet.me) have the option to use a simple but effective encryption scheme to send messages, i.e., a subject of maximum length of 200 characters and a message text of maximum length of 3000 characters.

The encryption scheme applies the Blum-Blum-Shub algorithm [1] to generate a pseudo-random sequence $x, x^2, x^4, x^8, \ldots\pmod{n}$, where $x$ and $n$ are based on a nonce (a number only used once) and a shared secret (a password transmitted over a secure channel, e.g., at a face-to-face meeting), and that is used as a binary one-time pad XOR-ed (the ^ operator in Python) with the subject and the message text. This notebook is a Python translation of the used Kotlin code for Android devices and Swift code for iOS.

To demonstrate the strength of this encryption scheme - and also for fun 😊 - we created a PHP version of the encryption scheme available [here](https://resnet.me/bbs/BBS.php). The message text is the private key of the Solana address [CSfT8di8n1mP7KHQaHXniEGdKsWaqkyifsVVAokFbw3x](https://solscan.io/account/CSfT8di8n1mP7KHQaHXniEGdKsWaqkyifsVVAokFbw3x) and we therefore offer 133 USD for cracking this encryption scheme.

[1] Blum, L.; Blum, M.; Shub, M. (1986). "A Simple Unpredictable Pseudo-Random Number Generator". SIAM Journal on Computing. 15 (2). Society for Industrial & Applied Mathematics (SIAM): 364–383, doi:10.1137/0215025
