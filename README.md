imap-message-stream
====================

Use with [node-imap](https://github.com/mscdex/node-imap)'s [ImapMessage](https://github.com/mscdex/node-imap#data-types). Pipe like a pro.

Install
-------
stable
```bash
npm install imap-message-stream
```
edge
```bash
npm install https://github.com/daxxog/imap-message-stream/tarball/master
```

Example
-------
```javascript
ImapMessageStream = require('imap-message-stream');
```

```javascript
fetch.on('message', function(msg) {
    var ws = fs.createWriteStream('raw.email'),
        ims = ImapMessageStream(msg);
    
    ims.pipe(ws);
});
```