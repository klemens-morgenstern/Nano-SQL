<p align="center">
  <a href="https://github.com/ClickSimply/Nano-SQL/tree/master/packages/Core">
    <img src="https://github.com/ClickSimply/Nano-SQL/raw/master/graphics/logo.png" alt="nanoSQL Logo">
  </a>
</p>
<p align="center">
  <a href="https://badge.fury.io/js/%40nano-sql%2Fadapter-sqlite">
    <img src="https://badge.fury.io/js/%40nano-sql%2Fadapter-sqlite.svg" alt="nanoSQL Logo">
  </a>
  <a href="https://github.com/ClickSimply/@nano-sql/core/blob/master/LICENSE">
    <img src="https://img.shields.io/npm/l/express.svg?style=flat-square" alt="nanoSQL Logo">
  </a>
</p>

<h1 align="center">nanoSQL 2 SQLite Adapter</h1>
<p align="center">
  <strong>Allows you to run SQLite in NodeJS with <a href="https://www.npmjs.com/package/@nano-sql/core">nanoSQL 2</a></strong>
</p>

[Documentation](https://nanosql.io/adapters/sqlite-nodejs.html) | [Bugs](https://github.com/ClickSimply/Nano-SQL/issues) | [Chat](https://gitter.im/nano-sql/community)

# Installation

```sh
npm i @nano-sql/adapter-sqlite --save
```

# Usage

```ts
import { SQLite } from "@nano-sql/adapter-sqlite";
import { nSQL } from "@nano-sql/core";

nSQL().createDatabase({
    id: "my_db",
    mode: new SQLite(),
    tables: [...]
}).then(...)
```

# API

The `SQLite` class accepts two optional arguments in it's constructor.

### Filename
The first argument is the filename to the SQLite database to connect to, if no filename is provided or an empty string if provided the nanoSQL database ID will be used instead.

### Database Arguments

Passed into the underlying database constructor for SQLite, fully documented [here](https://github.com/JoshuaWise/better-sqlite3/blob/master/docs/api.md#new-databasepath-options).

# MIT License

Copyright (c) 2019 Scott Lott

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

# Changelog

## [2.0.8]
- Database/table Id is now the filename if no filename is provided.
- Fixed memory property issue.

## [2.0.7]
- Switched to better-sqlite3 https://github.com/JoshuaWise/better-sqlite3.
- Dependency updates.

## [2.0.6]
- Documentation & Dependency updates.

## [2.0.5]
- Updated dependencies.
- Updated readme.

## [2.0.4]
- Moved to SQLite streaming API.
- Fixed dependencies.

## [2.0.3]
- Added git repo

## [2.0.1] & [2.0.2]
- Readme tweak

## [2.0.0]
- First release