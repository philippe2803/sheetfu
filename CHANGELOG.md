# CHANGELOG



## v1.0.0 (2024-05-08)

### Breaking

* feat(Table): Add sort method and full table syncro commits.

Full syncro commits will be useful once deleting items is added to the table object.

BREAKING CHANGE: The values, notes, backgrounds and font_colors attributes from Table have been removed. All this information is now purely encapsulated within the Item object. They have been replaced with boolean attributes that only indicate if the table was built with these information. ([`f8941c4`](https://github.com/philippe2803/sheetfu/commit/f8941c485c88fb6b23ae2b130110695d3e262ca4))

### Documentation

* docs: Add datetime explanation in the README ([`cb21f86`](https://github.com/philippe2803/sheetfu/commit/cb21f863ec29e05e03fa29393d5adf1ca43545d4))

* docs(Table): typo ([`1f4897c`](https://github.com/philippe2803/sheetfu/commit/1f4897c35897284bf4ea32ddb0c3501a3c4db037))

* docs(Table): Formatting. ([`4e3380b`](https://github.com/philippe2803/sheetfu/commit/4e3380be7bfc0d13e3197af5fa68bd495f168474))

* docs(Table): Remove irrelevant content ([`6cd4455`](https://github.com/philippe2803/sheetfu/commit/6cd445572c5849e58a2e1cd63502b7291fbc0955))

* docs(Table): Adding documentation for the Table object. ([`d42678e`](https://github.com/philippe2803/sheetfu/commit/d42678e6eb2bccdf13e92cfab2f96ec62cd7033b))

* docs(setup): simply adding long description for Pypi. ([`3b77e27`](https://github.com/philippe2803/sheetfu/commit/3b77e27fe3295f3168c8361f495eb873c2ac3bf3))

* docs(README): Fixed link. ([`0288835`](https://github.com/philippe2803/sheetfu/commit/028883515c29f38bf09813305464a41cc876e048))

* docs(Range): Added documentation for missing methods, added new methods at range level. ([`9cf53f6`](https://github.com/philippe2803/sheetfu/commit/9cf53f6120caa836fd51bcee4f2cbe1b51396507))

* docs: Add documentation for initializing ENV vars ([`2a4b487`](https://github.com/philippe2803/sheetfu/commit/2a4b487d1e7796e7eec0b3094e1ff6d686387186))

* docs(CI): Add documentation on semantic releases ([`f02ddab`](https://github.com/philippe2803/sheetfu/commit/f02ddabe2f560f191705a6468706ffce3c3ab52b))

* docs(Spreadsheet): Update documentation of the new clone/create sheet functions ([`4a4f9cf`](https://github.com/philippe2803/sheetfu/commit/4a4f9cf18549f4d409d7958a69d386d808c9772f))

### Feature

* feat: Add formulas integration

We can now get formulas with method Range.get_formulas.
To set formulas, we can simply set_values with formulas as string. If a string starts with &#39;=&#39; it will be interpreted as a formula.
The method Range.set_formulas now raise an error when used. ([`590df68`](https://github.com/philippe2803/sheetfu/commit/590df68221c580c33a0c5e4c564dca71e569aceb))

* feat(Range): Add datetime python conversion ([`fe664b6`](https://github.com/philippe2803/sheetfu/commit/fe664b614b6eb17bbe1b469fcc94efdc39be5ef9))

* feat(Item): Add to_dict method to convert Item object to simple dictionary ([`210d10e`](https://github.com/philippe2803/sheetfu/commit/210d10edd5ae4fafd289ca1683a211c28c5bca5c))

* feat(Range): Added coordinates getters at Range level for syntactic sugar. ([`c8e72e9`](https://github.com/philippe2803/sheetfu/commit/c8e72e956e91626b43124e684e314e0385de7657))

* feat(Service): Load service with env variables if they exist ([`6e88b42`](https://github.com/philippe2803/sheetfu/commit/6e88b429248962e0f0316be5a19290028a7e34fe))

* feat(Table): Add the delete method. ([`dec2fdb`](https://github.com/philippe2803/sheetfu/commit/dec2fdb675b355d1e38b6afad1c2a22654f97264))

* feat(Table): Returning the created item on add_one function ([`d973256`](https://github.com/philippe2803/sheetfu/commit/d9732564029dbdfe4f58df96b453e208eb6df1dd))

* feat(Sheet): Add get_max_rows/columns methods. ([`7fbdc5d`](https://github.com/philippe2803/sheetfu/commit/7fbdc5d4bc6ddc33e0731da2d1648849e88e7d26))

* feat(Table): Add delete_add method and remove full_table_syncro parameter from sort ([`6dc6b60`](https://github.com/philippe2803/sheetfu/commit/6dc6b605e976d1425a1af8357cb0145a41ca2a97))

* feat(Selector): Adds &#39;selector&#39; class to implement CNF notation on select ([`da416e2`](https://github.com/philippe2803/sheetfu/commit/da416e2d7dfd6c4bffe748ec038c8f0bf4058b8f))

* feat(Table): Add &#39;select&#39; method ([`b472d0b`](https://github.com/philippe2803/sheetfu/commit/b472d0bb4d7a3625264fc4e83c139b128128aa32))

* feat(Table): Add &#39;get_table_from_sheet&#39; option ([`5acb909`](https://github.com/philippe2803/sheetfu/commit/5acb90968b20c8ed5175c26ecac11495ae78f64c))

* feat(Model): Replace the trim/expand methods by the offset method. ([`d30d6a4`](https://github.com/philippe2803/sheetfu/commit/d30d6a4cab644adacb136f6b8dc5c3bb8123ed0e))

* feat(Table): Trim empty bottom rows on table construction and support header_row.
Now empty rows at the bottom of the table will be trimmed from its full range. A new header_row parameter also allows the construction of tables where the header row is not on the top of the specified range.
BREAKING CHANGE: Any Table being built with a custom-build range (not using get_data_range() from Sheet) can potentially behave differently when adding items, as they will be added on the next row without values instead at the end of the range specified in the constructor. ([`02a746d`](https://github.com/philippe2803/sheetfu/commit/02a746d62149f95ac702e2429e0e6508ccb1b140))

* feat(Range): Add trim/expand methods to Range object. ([`b29c0e4`](https://github.com/philippe2803/sheetfu/commit/b29c0e4dcfa164ea34ecaac463f49f88e178c608))

* feat(Spreadsheet): Add new functions to create and duplicate sheets ([`e67b030`](https://github.com/philippe2803/sheetfu/commit/e67b0303277977bd81c5f74332cf074f19316b75))

* feat(CI): Final version of semantic releases Sheetfu ([`71b0ce8`](https://github.com/philippe2803/sheetfu/commit/71b0ce8c7d2b5d7c5ce3d2638b775051ad919a3d))

* feat(CI): Final version of semantic releases Sheetfu ([`ab88cff`](https://github.com/philippe2803/sheetfu/commit/ab88cffec8392b1330a09a7498b994abc5344400))

* feat(CI): Add semantic versioning (#9) ([`c4e8f40`](https://github.com/philippe2803/sheetfu/commit/c4e8f40337f7bec564f4be06b6f5ffed2557a0ae))

### Fix

* fix(Range): enforce userEnteredFormat as a field mask ([`1e77f6b`](https://github.com/philippe2803/sheetfu/commit/1e77f6b449d18b9ee7c6bffdd0d680db7d402494))

* fix: PEP8 formatting ([`04a74f9`](https://github.com/philippe2803/sheetfu/commit/04a74f9b657670be6aa1fe07ad802af78e071017))

* fix(Sheet): Fixes missing sheet name in a1 notation when using get_range method ([`4770fb1`](https://github.com/philippe2803/sheetfu/commit/4770fb142e4d4a19e18d4eff8899f58c673befeb))

* fix: remove ugly print ([`105ec78`](https://github.com/philippe2803/sheetfu/commit/105ec78cf5c8de0d8fe7969829edc8e50aa58937))

* fix: dummy to test python semantic release ([`342d49d`](https://github.com/philippe2803/sheetfu/commit/342d49d37800c7c0a3103aa06816cf14bb44fe6b))

* fix(Sheet): Addng custom error when using row=0 or column=0 ([`a8f4f43`](https://github.com/philippe2803/sheetfu/commit/a8f4f43b968880a9611b416ac8f38c8ad2ccb535))

* fix(travis): Update supported python versions (#51)

* fix: Update supported python versions

* Remove dist specification ([`d3b5a3a`](https://github.com/philippe2803/sheetfu/commit/d3b5a3aa74aa5a9899ef984884fd8803f38ce09d))

* fix(requirements): update six library version. ([`cfbe527`](https://github.com/philippe2803/sheetfu/commit/cfbe527dcd167049f8f4ae8069b3ba09ed9243f5))

* fix(Range): Fix when setting notes in sheet. ([`d5a0a24`](https://github.com/philippe2803/sheetfu/commit/d5a0a24a28d7b6adf3f9a170212828bd6989a423))

* fix(Travis): Fix PRs from forks triggering semantic release travis job (#39) ([`51f2245`](https://github.com/philippe2803/sheetfu/commit/51f224504017e9fd3b2e4acbee27755cae30650a))

* fix(Range): Assert that number of columns is an integer ([`c62b1c6`](https://github.com/philippe2803/sheetfu/commit/c62b1c6a0cf98214b1a3139566a777e879250da0))

* fix(README): missing commit in README example. ([`47fc0df`](https://github.com/philippe2803/sheetfu/commit/47fc0dffedec87a6557e82d1e2d5930fdba66a70))

* fix(Spreadsheet): Removed irrelevant print. ([`1943e43`](https://github.com/philippe2803/sheetfu/commit/1943e43a48c9c0cff8ef1d41f21d49c25625e986))

* fix(Spreadsheet): Quick renaming and cleaning in tests. ([`9ba874f`](https://github.com/philippe2803/sheetfu/commit/9ba874f8bd9ba2801ba4511cdceea064ddc611c0))

* fix(Spreadsheet): Method creating sheets now return the sheets created. ([`14ecbcd`](https://github.com/philippe2803/sheetfu/commit/14ecbcd69fa957a9cdc11a1913fc3bb7e1ab03ab))

* fix(Spreadsheet): Matching sheet names ignoring case, as GSheets ignores case for sheet names internally. ([`62dca9c`](https://github.com/philippe2803/sheetfu/commit/62dca9c1f7a15a4b22a04813292d7ed5d31b87b9))

* fix(service): Add missing parameters to docstring and fix for Python 2.7 ([`477d6d3`](https://github.com/philippe2803/sheetfu/commit/477d6d3f678592d5770497b53d098970f7acbfc9))

* fix(Table): Sepparate delete polymorphism into two sepparate methods ([`dd2e727`](https://github.com/philippe2803/sheetfu/commit/dd2e727097129e755be8d23af5250a8598b87fbf))

* fix(Table): Fix adding items without specifying a value for each field. ([`3a03f93`](https://github.com/philippe2803/sheetfu/commit/3a03f93c5ae15c2302d243476a78ebd300b0a066))

* fix(Helpers): Fix wrong error being raised in python 2.7 ([`9f71b98`](https://github.com/philippe2803/sheetfu/commit/9f71b9886ef850151ed1a38d4c636457a0312aa8))

* fix(Table): Fix updating row_index in items after sorting ([`8cbca6b`](https://github.com/philippe2803/sheetfu/commit/8cbca6b46e4538b484d4ffec87918e2f702dfcd2))

* fix(Sheet): Add sheet name to A1 notation when getting range from A1 notation ([`29b4ec3`](https://github.com/philippe2803/sheetfu/commit/29b4ec32f6c19e6bbf0b90176bd2004de921fb2f))

* fix(Selector): moved &#39;Selector&#39; class to it&#39;s own module. ([`6e36168`](https://github.com/philippe2803/sheetfu/commit/6e361684215c61217ff72bd73261d55f73974522))

* fix(Table): Fix commit of table/spreadsheet with empty batches. ([`62bfa21`](https://github.com/philippe2803/sheetfu/commit/62bfa21fb8ee884fe1bd53ec02b1ec7e9a5941c5))

* fix(Table): Fix sorting of empty table ([`f6d56bc`](https://github.com/philippe2803/sheetfu/commit/f6d56bc9f9deee7bfd067d0d1c44c89eee095281))

* fix(Model): Fix format being overwritten when setting values. ([`782aa3a`](https://github.com/philippe2803/sheetfu/commit/782aa3a9b6f92f529d7ffda8d1db747a22ffa463))

* fix(Parsers): Fix 0 and False values not being written to tables. ([`edc5c14`](https://github.com/philippe2803/sheetfu/commit/edc5c1499a92b96042687042440ca10740927625))

* fix(Table): Fix font_colors boolean value and less parameter passing to parse_items ([`22d50a2`](https://github.com/philippe2803/sheetfu/commit/22d50a20159a29e9bc4b00944e004e627384454b))

* fix(Parsers): Support to writing python datetime objects and fix writing bool values ([`9fb0bdf`](https://github.com/philippe2803/sheetfu/commit/9fb0bdf41e84f4bf09dd503b56e02351f245043c))

* fix(Table): Fix table construction and add_one breaking when building off a table with only a header ([`2017390`](https://github.com/philippe2803/sheetfu/commit/2017390e66a4717d9b3b115f2a2ed673eadeabb9))

* fix(CI): Fix sheetfu modules not being deployed to Pypi ([`36c2e5e`](https://github.com/philippe2803/sheetfu/commit/36c2e5eb83850bcc5b6747213079a59d294e4a80))

* fix(Table): Fix emptying of batches list after commit ([`b19e6b8`](https://github.com/philippe2803/sheetfu/commit/b19e6b8b42b364141fa2cc301031cd22d76b344c))

* fix(Spreadsheet): Fix emptying of batches list after commit ([`d1c5995`](https://github.com/philippe2803/sheetfu/commit/d1c59954c6e226cae6e6a58d1641b7162d8b52d9))

* fix(CI): Fixed semantic releases ([`37d7029`](https://github.com/philippe2803/sheetfu/commit/37d70298b4f3ac7d2aaa974bb4544e3228503d8f))

* fix(CI): Rely on the correct git branch on semantic release ([`755b11b`](https://github.com/philippe2803/sheetfu/commit/755b11ba90c7eedf8cb55bc08ce5517469a54e9d))

### Refactor

* refactor(Table): Clarified the purpose of the notes/backgrounds/font attributes. ([`cd934a5`](https://github.com/philippe2803/sheetfu/commit/cd934a5db9da98cf013efa6b4a614c976b3f2b2b))

### Style

* style(Helpers): Improved code style of append_sheet_name ([`c997d3a`](https://github.com/philippe2803/sheetfu/commit/c997d3a1c60483c93239a444e26a4c8b80a868c2))

* style(Table): Improve code style of Table ([`5150a2e`](https://github.com/philippe2803/sheetfu/commit/5150a2e804a41ab4825da500e4af57e800a4f86e))

### Test

* test(Table): Removed unused fixtures ([`1f398ce`](https://github.com/philippe2803/sheetfu/commit/1f398cea3c11bb2541984cba234c1087fdb41580))

* test(Table): Tests for the new trimming behaviour of tables. ([`3026721`](https://github.com/philippe2803/sheetfu/commit/302672149affaed2e7c0ce3cfcd813fb232c4290))

* test(Table): Add tests for the Table model ([`02a6986`](https://github.com/philippe2803/sheetfu/commit/02a69866c1aec506c6bc148f4fab30c91baccec0))

### Unknown

* Create CODEOWNERS ([`d3a2ee5`](https://github.com/philippe2803/sheetfu/commit/d3a2ee5f37de5fb26e09542ee0c637a28004777c))

* Merge pull request #61 from socialpoint-labs/hotfix/format-for-new-dates

fix(Range): enforce userEnteredFormat as a field mask ([`4d0e746`](https://github.com/philippe2803/sheetfu/commit/4d0e746e1864de03cec693db17c958456a3849ef))

* Merge pull request #58 from socialpoint-labs/datetime-conversion

Adding datetime conversion, to_dict for table item, and formulas integration ([`1c81c1a`](https://github.com/philippe2803/sheetfu/commit/1c81c1a70006bd3299861db55166cbc0585c32ef))

* Remove unused config ([`97ecb8a`](https://github.com/philippe2803/sheetfu/commit/97ecb8ae1538c96ce5f06cb9d112b34989a14fee))

* PEP8 ([`b0b5c37`](https://github.com/philippe2803/sheetfu/commit/b0b5c371791d18deb82b865cbfb5b144b3ccbfe2))

* Merge branch &#39;master&#39; into datetime-conversion ([`31f8ac0`](https://github.com/philippe2803/sheetfu/commit/31f8ac0eb9a28b35919c79244eca865c174a91a0))

* Merge pull request #59 from socialpoint-labs/feature/github-actions-ci

Adding quickstart github action to experiment ([`899ad70`](https://github.com/philippe2803/sheetfu/commit/899ad702189ee774415c104e17e87a4be9d6df4b))

* Setting python semantic release ([`a31f92e`](https://github.com/philippe2803/sheetfu/commit/a31f92ea177cef3804243765dea288ec2364dc27))

* Adding quickstart github action to experiment ([`d6f9ad2`](https://github.com/philippe2803/sheetfu/commit/d6f9ad26fad69e201906a3a7255b7221b0132492))

* Merge pull request #48 from socialpoint-labs/feature/raise-error-when-0

Adding custom error when using row=0 or column=0 ([`f0bc098`](https://github.com/philippe2803/sheetfu/commit/f0bc098420496f35852b25eaa5bb4e47b1132dc5))

* Merge pull request #55 from GeorgiyDemo/master

fix(convert_letter_to_column): column_number in int type ([`25dcf96`](https://github.com/philippe2803/sheetfu/commit/25dcf96c0712d68bf0a3b9981ef4ca22a3da582d))

* fix(convert_letter_to_column) column_number in int type

column_number was in double type when column&#39;s letter was more then “Z” (&#34;AA&#34;, &#34;AB&#34;, &#34;AC&#34;, etc..) ([`1e7378a`](https://github.com/philippe2803/sheetfu/commit/1e7378a5c117b24fc173e8b5686454e01e616761))

* Merge pull request #45 from socialpoint-labs/hotfix/set-notes-not-values

Hotfix/set notes not values ([`571eb0a`](https://github.com/philippe2803/sheetfu/commit/571eb0a1c5fd1924b7664965eb213f844809684e))

* Update six requirements. ([`fb99e20`](https://github.com/philippe2803/sheetfu/commit/fb99e209e0a63f0c5d7fb4966f1c023244886310))

* Merge pull request #44 from socialpoint-labs/hotfix/set-notes-not-values

Hotfix/set notes not values ([`102e8a2`](https://github.com/philippe2803/sheetfu/commit/102e8a20c141b233cdbe536cae7553bcc90ade08))

* Fix when setting notes. ([`3d1e99a`](https://github.com/philippe2803/sheetfu/commit/3d1e99ae65dd5643c157685b83cda3664ae7aa1b))

* Quick fix on Table documentation.

The docs for get_field_range was missing a line of code. ([`6c7109d`](https://github.com/philippe2803/sheetfu/commit/6c7109df1cb7ebacd70047ac3f72cf067fd0d4b1))

* Merge pull request #40 from socialpoint-labs/docs/table

Documentation for Table module ([`54bed48`](https://github.com/philippe2803/sheetfu/commit/54bed487e4fa50f4d1f8a1a9f9ec2952b577bfad))

* Slightly improved README and small edit fix in auth doc. ([`6fda8bd`](https://github.com/philippe2803/sheetfu/commit/6fda8bd7fba82a736bc4bc861909187556623533))

* Need to merge master to get updated README.

Merge branch &#39;master&#39; into docs/table ([`b5e9b75`](https://github.com/philippe2803/sheetfu/commit/b5e9b7503bb3c4379beba1f3d69e9357c1d6fc36))

* Merge pull request #33 from luchinke/master

fix(Range): Assert that number of columns is an integer ([`a1b9bb5`](https://github.com/philippe2803/sheetfu/commit/a1b9bb5a7e320f51efc41c1a6625f6bc67ba74d4))

* Removed the commit mention in example. ([`d6d2a71`](https://github.com/philippe2803/sheetfu/commit/d6d2a7158e4e246f83b0206539d26eb8996afb49))

* Merge pull request #30 from socialpoint-labs/max-row-column

feat(Range): Max row and max column methods at range level. ([`6f91b0f`](https://github.com/philippe2803/sheetfu/commit/6f91b0f9a09bab9998bd431a106e4ca7163e35bf))

* Merge branch &#39;master&#39; into max-row-column ([`6184fcc`](https://github.com/philippe2803/sheetfu/commit/6184fccd9164d3220042e2f5369eddb6abb674e3))

* Merge pull request #31 from socialpoint-labs/returns-fix

fix(Spreadsheet): Method creating sheets now return the sheets created. ([`9fe43a7`](https://github.com/philippe2803/sheetfu/commit/9fe43a7263401ed5c924984dd2e34f67d6f716cf))

* Documentation and python 3.3 removal from travis (#28)

* SpreadsheetApp usage doc

* Added self references into docs.

* Started docs for Spreadsheet object

* Changed filename.

* Added methods for every objects.

* Get range doc.

* Finished documentation of sheetfu api

* Added link to documentation from README.

* removed 3.3 python version from travis as one of our dependency required minimum 3.4 ([`0290e19`](https://github.com/philippe2803/sheetfu/commit/0290e1965ba92802b835d304fd0fc6aec20f25b9))

* Merge pull request #26 from socialpoint-labs/ignoreCase

Matching sheet names ignoring case ([`8ae27e6`](https://github.com/philippe2803/sheetfu/commit/8ae27e688f60c1170ef9b2991c651a5a98e98dbc))

* Merge pull request #25 from socialpoint-labs/feat/env_variable_login

Feat/env variable login ([`3aba33e`](https://github.com/philippe2803/sheetfu/commit/3aba33e1c15c32bd660eb31e267a86fbda377934))

* WIP env varaibles login ([`d313647`](https://github.com/philippe2803/sheetfu/commit/d313647047eae9794d7f6769e4323e736bc6789b))

* Merge pull request #24 from socialpoint-labs/dev_amuelas

Delete method for Table ([`d67d86f`](https://github.com/philippe2803/sheetfu/commit/d67d86f76c865d1c96b0f6bc17b77e1c67de39e5))

* Merge pull request #22 from socialpoint-labs/dev_amuelas

Delete_all / Sort fix / get_range_from_a1 fix ([`7bed854`](https://github.com/philippe2803/sheetfu/commit/7bed854046b2872e43b9f76ac2b9cbafec4743d1))

* Merge pull request #21 from socialpoint-labs/feat/table-select

Table select method ([`47961fb`](https://github.com/philippe2803/sheetfu/commit/47961fbfe164417286a5d97e938e022d6254bbe6))

* Merge pull request #20 from socialpoint-labs/dev_amuelas

fix(Table): Fix commit of table/spreadsheet with empty batches. ([`28f22c9`](https://github.com/philippe2803/sheetfu/commit/28f22c9bfeb525ddb3302ae532d0224a9a64cd1a))

* Merge pull request #19 from socialpoint-labs/dev_amuelas

fix(Table): Fix sorting of empty table ([`da8a001`](https://github.com/philippe2803/sheetfu/commit/da8a0017ebac693d08330d652024f082f1a1b88f))

* Merge pull request #18 from socialpoint-labs/dev_amuelas

feat(Table): Add sort method and full table syncro commits. ([`b069b4b`](https://github.com/philippe2803/sheetfu/commit/b069b4baf0cd4a80c697ee969e8a98f1f98eb0d3))

* Merge pull request #15 from socialpoint-labs/dev_amuelas

Trimming empty rows on the bottom of Tables ([`0cb425c`](https://github.com/philippe2803/sheetfu/commit/0cb425c60c3de7d43f0a1a9c01f3bfb5a9755f15))

* Merge branch &#39;dev_amuelas&#39; of github.com:socialpoint-labs/sheetfu into dev_amuelas ([`0114b8f`](https://github.com/philippe2803/sheetfu/commit/0114b8fb9e7184c60909363be3b22d1f3ab35d91))

* Merge pull request #13 from socialpoint-labs/dev_amuelas

docs(CI): Add documentation on semantic releases ([`dcdcdd6`](https://github.com/philippe2803/sheetfu/commit/dcdcdd6268fb66e29f138690982427fe5e5cb2b6))

* Merge branch &#39;master&#39; into dev_amuelas ([`0b1af66`](https://github.com/philippe2803/sheetfu/commit/0b1af66ff198f20cc7934553feb8460c6dfcb80b))

* Merge pull request #11 from socialpoint-labs/sortByTable

Fix emptying of batches when commiting ([`35a3e92`](https://github.com/philippe2803/sheetfu/commit/35a3e9290dc69a96959a12bdfc601c0d46ff1580))

* Merge pull request #10 from socialpoint-labs/createSheet

feat(Spreadsheet): Add new functions to create and duplicate sheets ([`c5457e1`](https://github.com/philippe2803/sheetfu/commit/c5457e15a3be6caaea86a3412dadf05713084371))

* updated version ([`8c5cceb`](https://github.com/philippe2803/sheetfu/commit/8c5ccebae152b1375a3a54120621b4217d1ef383))

* Table Module (#8)

* Organized fixtures and first draft of table object

* added dimension getters at item level

* added couple of get range methods for item.

* added small description of table module in readme

* Table MVP completed + refacto on get/set values at range level.

* gridRange fixes in requests.

* fix on grid range attribute for set requests

* added possibility to add new entry in table. ([`a2be15b`](https://github.com/philippe2803/sheetfu/commit/a2be15b61274fbe4629fb151863e80d53757375f))

* readme fix ([`036c07b`](https://github.com/philippe2803/sheetfu/commit/036c07b53504e2dcc6d940b917e4f0ce2adbb498))

* Create CODE_OF_CONDUCT.md (#6) ([`5bed0a8`](https://github.com/philippe2803/sheetfu/commit/5bed0a8460d1b515f094cebbcd74970f6bf299e4))

* Cell (#5)

* Change batches level (on spreadsheet level opposed to range level ([`dffa5fe`](https://github.com/philippe2803/sheetfu/commit/dffa5fe9830386a079891a603eba4b5b1c12731f))

* all pyc files removed ([`6f568ee`](https://github.com/philippe2803/sheetfu/commit/6f568ee0a17a41a696ac4d9539aedf0552e543a5))

* Documentation (#4)

* maj

* First version of README completed.

* First draft for authentication docs.

* Maj.

* a bit more documentation.

* Completed auth documentation.

* Added contributing documentation.

* More contrib docs.

* adding changes for 2.7 compatibility

* first documentation completed

* updated readme

* added reference to sheetfu apps script ([`beeff0c`](https://github.com/philippe2803/sheetfu/commit/beeff0c72a9fe45e043189c67ec3702e9e56465e))

* Merge pull request #3 from socialpoint-labs/2.7

added changes to work with 2.7. ([`b8fcd22`](https://github.com/philippe2803/sheetfu/commit/b8fcd225ac3f1de2691ab7c5ce8ab9e373006145))

* added changes to work with 2.7. ([`3480c53`](https://github.com/philippe2803/sheetfu/commit/3480c535013d98ced55eb200986060f02e57eb50))

* version 0.3 (#2)

* fxed set backgrounds

* Added get and set font colors.

* Testing new structure.

* New structure completed.

* Added command to Makefile

* Cleaning with the field masks.

* added set background and set font color methods

* changed version

* maj

* deleting useless files

* added very quick travis config

* cleaning ([`93a1ea8`](https://github.com/philippe2803/sheetfu/commit/93a1ea835f49758aac933ee80526f8f5d4e3d6c2))

* Added small comparison with Google Apps script. ([`7be644a`](https://github.com/philippe2803/sheetfu/commit/7be644a9113fc89a127f27484543bc363561dba5))

* Added first draft for why Sheetfu over other libraries. ([`76402c9`](https://github.com/philippe2803/sheetfu/commit/76402c92a4131fe39d9d67c26be50f72e1e55bc5))

* Merge pull request #1 from socialpoint-labs/dev

Initial code ([`83d0bd3`](https://github.com/philippe2803/sheetfu/commit/83d0bd3e140eacb7d5b137d3a450453e0d8af3f7))

* Added testing libraries in requirements. ([`db667b8`](https://github.com/philippe2803/sheetfu/commit/db667b8dd6d77bbbbe1438f351626311d2ccfee8))

* 0.01 dev version ([`9b1b3e8`](https://github.com/philippe2803/sheetfu/commit/9b1b3e819cd60ea8507e0e24f7bf3d2aafd1f8a6))

* testing local config ([`581aa0d`](https://github.com/philippe2803/sheetfu/commit/581aa0dddc13207cee0b08046ea429ea581611a4))

* Added link to Google apps script version ([`da0f9dc`](https://github.com/philippe2803/sheetfu/commit/da0f9dc93c197c40bbfbca203b88f743980ccd24))

* Initial commit ([`05e8ba0`](https://github.com/philippe2803/sheetfu/commit/05e8ba0d462957e012046430e662249a355f4b63))
