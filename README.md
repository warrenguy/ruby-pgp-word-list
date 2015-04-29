# pgp-word-list

Convert hex strings to PGP word lists and vice-versa.

See [PGP word list on WikiPedia](http://en.wikipedia.org/wiki/PGP_word_list]) for more information.

I've also written a JavaScript version: [javascript-pgp-word-list](https://github.com/warrenguy/javascript-pgp-word-list).

## Usage

Extends `String`, `Array`, and `Integer` with `.to_pgp_words`, and `String` and `Array` with `.to_pgp_hex`.

Available as a gem on [RubyGems](https://rubygems.org/gems/pgp-word-list).

````
require 'pgp-word-list'

> 'D1D4 64C0 04F0 0FB5 C9A4  C8D8 E433 E7FB 7FF5 6256'.to_pgp_words
=> "stairway souvenir flytrap recipe adrift upcoming artist positive spearhead Pandora spaniel stupendous tonic concurrent transit Wichita lockup visitor flagpole escapade"

> 0xD1D464C004F00FB5C9A4C8D8E433E7FB7FF56256.to_pgp_words
=> "stairway souvenir flytrap recipe adrift upcoming artist positive spearhead Pandora spaniel stupendous tonic concurrent transit Wichita lockup visitor flagpole escapade"

> "stairway souvenir flytrap recipe adrift upcoming artist positive spearhead Pandora spaniel stupendous tonic concurrent transit Wichita lockup visitor flagpole escapade".to_pgp_hex
=> "D1D464C004F00FB5C9A4C8D8E433E7FB7FF56256"                       

> ["stairway", "souvenir", "flytrap", "recipe"].to_pgp_hex
=> ["D1", "D4", "64", "C0"]

> ["D1", "D4", "64", "C0"].to_pgp_words
=> ["stairway", "souvenir", "flytrap", "recipe"]
````

## Author

Warren Guy <warren@guy.net.au>

https://warrenguy.me

The word list itself belongs to PGP Corporation.

## License

MIT license. See [LICENSE](https://github.com/warrenguy/ruby-pgp-word-list/blob/master/LICENSE)
