## MongoDB Shell Bling

The `mongo` shell includes an embedded JavaScript interpreter which allows 

More on working with the shell:

 - standard
 - keyboard nav
 - writing extensions


### Installing

This repo includes some common extensions and functions for the `mongo` shell. There is currently no standard way to package or install shell extensions, so you will have to check the README in the relevant repo.

To check out all extensions, you can clone this repository using: `git clone --recursive ...`

### Updating

```git submodule update --remote```

### Caveats

 - most of the shell extensions have been independently developed, so functionality may overlap and/or conflict
 - some extensions override built-in `mongo` shell API (as opposed to augment), and may inadvertently cause different behaviour from the default shell
 - run `mongo --norc` to start a shell session without loading any startup scripts

### Bundles

These extensions include a grab-bag of improvements.

| Extension                | Author     | Purpose                    |
|--------------------------|------------|----------------------------|
| [mongo-hacker](https://github.com/TylerBrock/mongo-hacker) | TylerBrock | MongoDB Shell Enhancements for Hackers: colorized query output, custom prompt, API additions (eg. fluent aggregation) ... |
| [mongodb-shell-extensions](https://github.com/gabrielelana/mongodb-shell-extensions) | gabrielelana| A bundle of utility libraries and API additions including: MomentJS, LoDash, JSONPath, and sprintf.js|
| [mongorcd](https://github.com/devkev/mongorcd) | devkev | Automatically load multiple mongo shell startup scripts from the ~/.mongorc.d directory. Includes a great set of [example scripts](https://github.com/devkev/mongorcd/tree/master/.mongorc.d).

### Shell Helpers

These extensions provide discrete features which extend built-in objects.

| Extension                | Author     | Purpose                    |
|--------------------------|------------|----------------------------|
| [mongodb-schema](https://github.com/skratchdot/mongodb-schema) | skratchdot| Schema analysis tool; adds `db.collection.schema()` |
| [mongo-views](https://github.com/mongodb-js/mongo-views) | mongodb-js | Virtual collections - aka views with joins - in the MongoDB shell; adds `db.collection.createView()`, `show views`, and related hlepers.
| [mongo-table-view](https://github.com/cswanson310/mongo-table-view) | cswanson310 | Display results of a cursor in a table view; adds `.table()` method for `find()` and `aggregate()`.
| [mongodb-distinct-types](https://github.com/skratchdot/mongodb-distinct-types) | skratchdot| Similar to the db.myCollection.distinct() function, distinctTypes() will return "types" rather than "values"; adds `db.collection.distinctTypes()`. |
| [mongodb-wild](https://github.com/skratchdot/mongodb-wild) | skratchdot | Adds a wildcard search to collection or query results; adds `db.collection.wild()`, `db.collection.find().wild()`.

### Function Libraries

Additional functions designed to be invoked in the `mongo` shell.

| Library                | Author     | Purpose                    |
|--------------------------|------------|----------------------------|
| [uuidhelpers.js](https://github.com/mongodb/mongo-csharp-driver/blob/master/uuidhelpers.js) | mongo-csharp-driver| Javascript helper functions for parsing and displaying historical UUID variations in the MongoDB shell; includes `HexToBase64()`, `Base64ToHex()`, `UUID()`, `JUUID()`, `CSUUID()`, `PYUUID()` |



### Third Party Libraries

Third party JavaScript libraries which are compatible with the `mongo` shell (but not specifically designed for it).

| Library                | Purpose                    |
|--------------------------|----------------------------|
| [Moment.js](http://momentjs.com/)|Parse, validate, manipulate, and display dates in JavaScript.|
| [JSONPath](https://github.com/s3u/JSONPath)|Analyse, transform, and selectively extract data from JSON documents (and JavaScript objects) using JSONPath.|
| [Underscore](http://underscorejs.org/)|Underscore provides over 100 functions that support both your favorite workaday functional helpers: map, filter, invoke — as well as more specialized goodies: function binding, javascript templating, creating quick indexes, deep equality testing, and so on.|
| [Lo-Dash](https://lodash.com/)|A utility library that began as a fork of Underscore and has since become a superset of Underscores features.
| [sprintf.js](https://github.com/alexei/sprintf.js)|A complete open source JavaScript `sprintf` implementation.
