Semantic Versioning
===

The Semantic Versioning documentation can be found at their site. http://semver.org/

Versions are formatted as follows:

   `MCVERSION`-`MAJOR`-`MINOR`-`PATCH`-`BUILD`

`MCVERSION` - This is the minecraft version for which this release is built; EX: 1.6.4, 1.7.10, 1.8.0, 1.9.X

`MAJOR` - This number increments when API changes are performed. These changes are not backwards-compatible and often require mods to perform a change to their code to accommodate the change. Changes can be modifications/subtractions of:
	* classes or class names
	* a class's functions or function names

`MINOR` - This number increments when changes are made which are backwards-compatible. These changes do not affect the compatibility with other mods. Changes can be:
	* additions of:
		* classes
		* class functions
	* deprecation of:
		* classes
		* class functions

`PATCH` - This number increments when bugs are patched. No updates are required in another mod's code. Changes can be:
	* modification of:
		* a class's constructor's internal code
		* a class's function's internal code

`BUILD` - This number is used to indicate test builds on a build server.
