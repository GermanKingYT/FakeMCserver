FakeMCServer
==
Run `shadow` with Gradle to compile. Output is in `build/libs`.
Run as `java -jar FakeMCserver-0.1-shadow.jar <port (optional)>`.

Config
--
Configuration is autogenerated on startup as `server.properties`.
* version/protocol: MC version and protocol, check http://wiki.vg/Protocol#Protocol_Version
* max/online: how many max players and online players you have
* description: also known as motd, use standard color codes and `\n` for newline
* engine: how to output the description, can be `json` or `classic`

Engines
--
* Using `engine: json`:
```json
{"version":{"name":"1.7.9","protocol":5},"players":{"max":42070,"online":9001},"description":{"text":"Bl","bold":false,"italic":false,"underlined":false,"strikethrough":false,"obfuscated":false,"extra":[{"text":"aze it\n","bold":false,"italic":false,"underlined":false,"strikethrough":false,"obfuscated":false,"color":"aqua"},{"text":"maggots","bold":false,"italic":false,"underlined":false,"strikethrough":false,"obfuscated":false,"color":"white"}],"color":"red"}}
```
* Using `engine:classic`:
```json
{"version":{"name":"1.7.9","protocol":5},"players":{"max":42070,"online":9001},"description":{"text":"\u00A7cBl\u00A7baze it\n\u00A7fmaggots","bold":false,"italic":false,"underlined":false,"strikethrough":false,"obfuscated":false}}
```