# localStorageDBAsync

An asynchronous version of https://github.com/knadh/localStorageDB

Works with chrome.storage or localStorage

Tests not yet converted

```coffee-script

    chromeStorageDB name, localStorage, (db) =>
      @db = db
      if db.isNew()
        db.createTable 'preferences', ['name', 'value']
        for key, value of preferences
          db.insert 'preferences', name: key, value: value
        db.commit()

```