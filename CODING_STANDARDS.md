# MeldCE Opensource Coding Standards

## File Formatting

### Line Endings
All files (unless required), must have Unix (LF) line endings.

### Indentation and Line Wrapping
Hard tabs must be used for indentation. A tab width of two characters should be
used. Lines should be hard wrapped at 80 characters.

## Coding Formatting

### Curly Braces and Square Brackets
Curly braces must be on the same as that which they are associated with (for
example an if statement, or function call) (the one true brace style
[[1TBS](https://en.wikipedia.org/wiki/Indent_style#Variant:_1TBS)]). 
For example:
```javascript
if (true) {
	start({
		greatThings: true
	});
}
```
Squares brackets used to define arrays and curly braces used to define objects
should follow the same style. A single space should be put after each `,`.
If an object is being declared a single line, one space should be put in
between the curly braces and the contents, eg `func({ var: true })`.

### Line Continuations
If lines, for example function calls and their parameters, are longer than the
80 character wrap limit, they should be hard wrapped to the next line and
indented by two tabs.
For example:
```javascript
if(thisReallyReallyReallyLongVarName == 'something that is really long'
		&& anotherLongVarName == 'something else that is really long') {
	runThisFunctionWithALongName(thisReallyReallyReallyLongVarName,
			anotherLongVarName,{
				someParam: true
			});
}
```
Lines should be wrapped using the following preferences:
1. After a comma used to separate function arguments, eg
   ```javascript
	 someFunc('longArg',
	     'longArg2');
	 ```
2. Before the `.` on chaining functions, eg
   ```javascript
	 someVar
	     .someFunc('longArg')
			 .anotherFunc('longArg');
	 ```
3. Before Logical operators
   ```javascript
	 if (someReallyLongVar === anotherReallyLongVar
	     && anotherVar !== somethingElse) {
	 ```
3. Before comparison operators
   ```javascript
	 if (somethingReallyLong
	     === something) {
	 ```

### Naming
Constants should be named using uppercase characters and underscores,
`MY_CONSTANT`.

[CamelCase](https://en.wikipedia.org/wiki/CamelCase) should be used for all
names (variables, functions, prototypes, CSS classes, and script classes)
except where not allowed. Script prototype and class names should start with
a capital letter. All others should start with a lower case letter.

Names should shed some light on what their use and functionality is instead of
being cryptic, eg `deleteObject()` rather than `dO()` (a code minimiser can be
used for minimising names).

Counters, such as those used in `for` statements can be single letters, for
example `for (o in objects)`.

### Other
Strict comparison operators should be used.
