# rabitmq-local

local syystem rabit mq

## docker commands

### Spin rabbitmq server docker

`docker run --name rabbitmq -p 5672:5672 -d rabbitmq`

### Publish Command

`npm run publish {number}`

### Consume Command

`npm run consume`

### Spin rabbitmq server HTTP server docker

`docker run --name rabbitmq -p 5672:5672 -p 15672:15672 -d rabbitmq:3-management`

HTTP
fetch("http://localhost:15672/api/vhosts”, {headers: {"Authorization" : `Basic ${btoa('guest:guest')}`}}).then(a=>a.json()).then(console.log)

fetch("http://localhost:15672/api/channels", {headers: {"Authorization" : `Basic ${btoa('guest:guest')}`}}).then(a=>a.json()).then(console.log)

fetch("http://localhost:15672/api/queues", {headers: {"Authorization" : `Basic ${btoa('guest:guest')}`}}).then(a=>a.json()).then(console.log)

Ref - [hnasr/javascript_playground/rabbitmq](https://github.com/hnasr/javascript_playground/tree/master/rabbitmq)
