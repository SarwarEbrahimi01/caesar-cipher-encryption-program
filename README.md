# Caesar Cipher — Simple Encryption Program

## Overview

This repository contains small Python programs that demonstrate the Caesar Cipher — a simple substitution cipher that shifts letters by a fixed number of positions.

The Caesar Cipher replaces each letter in the plaintext with a letter some fixed number of positions down the alphabet. For example, with a shift of 3, `A` becomes `D`, `B` becomes `E`, and so on. When the end of the alphabet is reached it wraps around (e.g., `Z` shifted by 1 becomes `A`).

## Files

- `caesar_cipher_1.py` — Minimal interactive implementation.
- `caesar_cipher_2.py` — Variation with preserving case and punctuation.
- `caesar_cipher_3.py` — Batch encrypt/decrypt helper (example).
- `caesar_cipher_4.py` — Additional utilities and examples.
- `art.py` — Decorative ASCII art used in demos.

## How the algorithm works

1. Choose a shift amount `n` (commonly 1–25).
2. For each letter in the input:
   - If it is an uppercase letter, shift within `A-Z` by `n` positions.
   - If it is a lowercase letter, shift within `a-z` by `n` positions.
   - Leave non-alphabet characters (numbers, punctuation, spaces) unchanged.
3. The result is the ciphertext.

Mathematically, for a letter with 0-based index $x$ and shift $n$, the cipher letter index is $(x + n) \bmod 26$.

## Usage

Run the simplest script from the repository root. Example (Windows PowerShell):

```powershell
python caesar_cipher_1.py
```

The program will typically prompt for text and a shift number, then print the encrypted (or decrypted) result.

## Example run (ASCII "picture")

Below is a representative terminal output showing the program running. This serves as the "picture" of the final running program:

```
---------------------------------------------
 C:\> python caesar_cipher_1.py
 Welcome to Caesar Cipher encrypt/decrypt!
 Enter text: Hello, World!
 Enter shift (0-25): 3
 Encrypted text: Khoor, Zruog!
 ---------------------------------------------
```

If your script prompts for encrypt/decrypt mode, choose as needed. The output above demonstrates a shift of 3 (standard Caesar).

## Notes & Tips

- Shifts of 13 (ROT13) are symmetric — applying ROT13 twice returns the original text.
- This cipher is not secure for real-world encryption; it is valuable for learning and simple obfuscation.
- Want a real screenshot image added instead of the ASCII example? I can add a PNG screenshot if you provide one, or I can generate one for you.

## Extra Info

- To preserve punctuation and spacing, the implementations here only shift alphabetic characters.
- Case is preserved in `caesar_cipher_2.py` and later scripts.

## License

Feel free to reuse and modify these simple demos for learning and teaching purposes.
