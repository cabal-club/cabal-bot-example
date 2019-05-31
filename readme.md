# cabal-bot-example

simple example cabal bot that upper cases any text that follows a `!uc` command

```
20:21:00 <substack> !uc this is a test bot that upper cases the text you type
20:21:00 <ucbot> THIS IS A TEST BOT THAT UPPER CASES THE TEXT YOU TYPE
20:22:11 <cblgh-windsor> !uc bots r cool
20:29:11 <ucbot> BOTS R COOL
```

If the bot is down or the network disconnects the messages can still eventually
go through. But watch out that you don't accidentally process the whole history
of bot commands if you reset the local database. It will probably make sense to
check the clock skew and reject commands that are more than some latency threshold.

# install and run

```
$ npm install
$ npm start
```

