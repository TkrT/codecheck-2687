# Hash generator for the bot
----

This module generate hash from command-data pair.

## Usage
1. Import Bot class from "bot.py".
2. Create dictionary which contains two keys, "command" and "data", and store command string and data string.
3. Pass this dictionary to Bot constructor and create instance.
4. Call generate_hash method.
5. Get hash from member variable "hash".

## How to work
1. Initialize member variables "command" and "data" by parameter dictionary.
2. In generate_hash method, convert "command" and "data" following steps.
    1. Convert string into ascii code list and concatenate this list in convert_to_ascii method.
    2. If this value is larger than 10^20, convert into scientific notation in scientific_notation method.
    3. If value converted in previous step, extract decimal part of fraction and exponent and concatenate them in extract_value method.
3. Adding command value and data value.
4. Convert this value into hex.
