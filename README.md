# PouchDB Sublime snippets [![Build Status](https://travis-ci.org/brenopolanski/pouchdb-sublime-snippets.svg?branch=master)](https://travis-ci.org/brenopolanski/pouchdb-sublime-snippets)

<img src="https://raw.githubusercontent.com/brenopolanski/pouchdb-sublime-snippets/gh-assets/pouchdb-sublime-snippets.png" alt="CSS Comments snippets" align="right" />

PouchDB snippets for [Sublime Text](http://www.sublimetext.com/).

[PouchDB](http://pouchdb.com/) is an open-source JavaScript database inspired by Apache [CouchDB](http://couchdb.apache.org) that is designed to run well within the browser. Was created to help web developers build applications that work as well offline as they do online.

To install through Package Control, search for [**PouchDB**](https://sublime.wbond.net/packages/PouchDB%20Snippets). If you still don't have Package Control in Sublime Text, [go get it](http://wbond.net/sublime_packages/package_control/installation). If you insist to not install it, you can download the package and put it manually inside your Pacakages directory. It should work but will not update automatically.

## Snippets

To trigger a snippet just put a **pdb-** followed by it's name, like so:

## Create a database

**trigger:** pdb-new⇥

```javascript
var db = new PouchDB('dbName', options);
```

## Delete a database

**trigger:** pdb-destroy⇥

```javascript
db.destroy('dbName', function(err, res) {
	// your code goes here
});
```

## Create a new document or update an existing document

**trigger:** pdb-put⇥

```javascript
db.put(doc, function(err, res) {
	// your code goes here
});
```

## Create a new document and let PouchDB generate an `_id` for it

**trigger:** pdb-post⇥

```javascript
db.post(doc, function(err, res) {
	// your code goes here
});
```

## Fetch a document

**trigger:** pdb-get⇥

```javascript
db.get('doc', function(err, res) {
	// your code goes here
});
```

## Delete a document

**trigger:** pdb-remove⇥

```javascript
db.remove('doc', function(err, res) {
	// your code goes here
});
```

## Create/update a batch of documents

**trigger:** pdb-bulkDocs⇥

```javascript
db.bulkDocs(docs, function(err, res) {
	// your code goes here
});
```

## Fetch multiple documents

**trigger:** pdb-allDocs⇥

```javascript
db.allDocs(options, function(err, res) {
	// your code goes here
});
```
## Listen to database changes

**trigger:** pdb-changes⇥

```javascript
db.changes(options);
```

## Replicate a database

**trigger:** pdb-replicate⇥

```javascript
db.replicate.type(remoteDB, options);
```
## Sync a database

**trigger:** pdb-sync⇥

```javascript
var sync = PouchDB.sync(src, target, options);
```

## Save an attachment

**trigger:** pdb-putAttachment⇥

```javascript
db.putAttachment(docId, attachmentId, rev, doc, type, function(err, res) {
	// your code goes here
});
```

## Get an attachment

**trigger:** pdb-getAttachment⇥

```javascript
db.getAttachment(docId, attachmentId, options, function(err, res) {
	// your code goes here
});
```

## Delete an attachment

**trigger:** pdb-removeAttachment⇥

```javascript
db.removeAttachment(docId, attachmentId, rev, function(err, res) {
	// your code goes here
});
```

## Query the database

**trigger:** pdb-query⇥

```javascript
db.query(fun, options, function(err, res) {
	// your code goes here
});
```

## Get database information

**trigger:** pdb-info⇥

```javascript
db.info(function(err, res) {
	// your code goes here
});
```

## Compact the database

**trigger:** pdb-compact⇥

```javascript
db.compact(options, function(err, res) {
	// your code goes here
});
```

## Document revisions diff

**trigger:** pdb-revsDiff⇥

```javascript
db.revsDiff(diff, function(err, res) {
	// your code goes here
});
```

## Events

**trigger:** pdb-event⇥

```javascript
PouchDB.on('event', function(dbName) {
	// your code goes here
});
```

## Plugins

**trigger:** pdb-plugin⇥

```javascript
PouchDB.plugin({
	methodName: myFunction
});
```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m "Add some feature"`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request  :)

English is the universal language nowadays, so please don't create or comment on issues using another language.

## History

For detailed changelog, see [Releases](https://github.com/brenopolanski/pouchdb-sublime-snippets/releases).

## License

[MIT License](https://brenopolanski.mit-license.org/) © Breno Polanski
