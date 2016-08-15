# Jekyll-Dec-to-Hex
A simple Jekyll Liquid filter plugin for hexadecimal conversion.

While it could be done through liquid itself by reimplementing the conversion,
it would be unwieldy, since it doesn't support functions.

## Installation

Copy `dec_to_hex.rb` into your `_plugins` directory (create it if needed).

You will have to restart jekyll for it to notice the plugin.

## Usage
You now have a `dec_to_hex` filter you can use as any other. Pass it a decimal
integer or string and it will output a "0x" prefixed hexadecimal representation.

The string version is idempotent if you pass a number that is already hex.

## Examples
    {{ 7 | dec_to_hex }}
    # => 0x7

    {{ "17" | dec_to_hex }}
    # => 0x11

    {{ "0x12" | dec_to_hex }}
    # => 0x12

    {{ 0x12 | dec_to_hex }}
    # => ERROR
