# ChangeLog

## 0.next

* BC: `minimumEvaluationRatio` is now a method to be called, not a private field. Defaults to 0.5.

## 0.8.0

* Updated dependency on `icomefromthenet/reverse-regex` to solve warnings on PHP 7.
* `bind` Generator.
* Default string dump for `Listener\collectFrequencies()`.
* Optionally logging generations with `hook(Listener\log($filename))`.
* `disableShrinking()` option.
* `limitTo()` accepts a `DateInterval` too.
* Configurability of randomness: choice between `rand`, `mt_rand`, and a pure PHP Mersenne Twister.
* `suchThat` Generator accepts PHPUnit constraints like `when()`.
* `Generator\constant()` utility function.
* Fixed bug of size not being fully explored due to slow growth.
* Switched to PSR-2 coding standards and PSR-4 autoloading.
* BC: `frequency` generator only accepts variadics args, not an array anymore.
* BC: removed `strictlyPos` and `strictlyNeg` Generators as duplicated of `pos` and `neg` ones.
* BC: removed `andAlso`, `theCondition`, `andTheCondition`, `implies`, `imply` aliases which no one uses. Added `and` for multiple preconditions.

## 0.7.0

* `associative`, `map`, `subSet`, `suchThat` Generators.
* Optionally limiting the number of generations with `limitTo()`.
* Optionally collecting generated data with `hook(Listener\collectFrequencies())`.
* Support for listeners with `startPropertyVerification`, `newGeneration` and `endPropertyVerification` events.
* BC: changed Generators API to use `GeneratedValue` objects.
* BC: requiring PHP 5.5 or newer.
* BC: dropped array single parameter in `forAll()`.

## 0.6.0

* PHP 7 compatibility.
* Renaming all Generator classes to *Generator.

## 0.5.0

* Generators are now based on size, an increasing random parameter.
* `choose()` new Generator to get integers inside a fixed range.
* PHPUnit 5.x is supported.
* `set` new Generator.
* Differentiating `pos`, `nat`, `neg` Generators.
* GeneratorSampleTest to get sample output from Generators.

## 0.4.0

* Showing generated input with `ERIS_ORIGINAL_INPUT=1`.
* `names` and `date` (DateTime) new Generators.
* `tuple` Generator supports variadic arguments.
* Shrinking respects `when()` clauses.
* Dates and sorting examples.

## 0.3.1

* `forAll()` accepts multiple arguments instead of an array.
* `byte` Generator.

## 0.3.0

* `frequency` and `oneOf` Generators that combine other Generators. 
* `sequence` Generator for lists of constant type and variable size.
* `char` Generators with `printableCharacter` Antecedent.
* `int`, `pos`, `neg` and `float` Generators.
* `regex` Generator to build strings satisfying a regular expression.
* Shrinking respects an optional maximum time limit (`$this->shrinkingtimeLimit`).

## 0.2.0

* Generators now use the Generator\nat(...) syntax.
* Added `bool`, `constant`, `elements`, `string`, `tuple` Generators.
* Improved shrinking by performing it on all involved Generators.
* Reproducibility with ERIS_SEED.

## 0.1.0

* `forAll()` and `then()` syntax.
* `natural` and `vector` Generators.
* `when()` for constraints.
* Basic best-effort shrinking.
* `sample()` and `sampleShrink()` for Generators.
