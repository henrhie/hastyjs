# 
# Hastyjs👩‍💻

Hastyjs is the cli tool for you if you quickly want to add npm libraries to your
experimental javascript project.

Hastyjs internally uses custom esbuild plugins to fetch bundled versions of javascript libraries from 
unpkg.com on demand and bundles them alongside your local modules.

This tool is not meant to replace your traditional node js production pipeline but to allow you to quickly
experiment with your ideas without the need for a package.json file and node modules.




## Features

- Harnesses Esbuild's speed ⚡⚡⚡ bundling capabilities
- Caches fetched libraries for faster execution
- Use popular libraries such as lodash without `npm install`
- Execute complex javascript code with a simple command



## Installation

Installing Hastyjs with npm

```bash
  npm install -g hastyjs
```
## Usage
```bash
hastyjs run --input=<EntryFile> | -i <EntryFile> --output=<OutputFile> | -i <OutputFile>

-> EntryFile is the entry file passed to esbuild for bundling - default=index.js
-> OutputFile is the file bundled file - default=output.js
```

```bash
hastyjs clear-cache

-> Clears cache
```



## Examples

```javascript
//index.js

import _ from 'lodash';

console.log(_.merge({ java: '13', cpp: '32', rust: '23' }));
```

```bash
hastyjs run --input=index.js --output=output.js && node output.js
```

```bash
✅✅✅ bundle successful
{ java: '13', cpp: '32', rust: '23' }
```

```bash
//clears cache

hastyjs clear-cache
```
## Credits
- Several references were made from Stephen Griders React with Typescript course on Udemy

## Contributing

Contributions are always welcome!

See `contributing.md` for ways to get started.


## License

[MIT](https://choosealicense.com/licenses/mit/)

