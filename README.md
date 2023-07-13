# open-telemetry

An investigation project to do code instrumentation.

Prerequsite:

1. Run "docker run --rm -d -p 9411:9411 --name zikin openzipkin/zipkin" to install and run zipkin on your local docker. Zipkin is the telemetry data backend to help show the data.

Steps:

1. npm install
2. npx ts-node --require ./tracing.ts app.ts

Then hit the http://localhost:8080/rolldice a few times and go to the
http://localhost:9411/zipkin/?lookback=15m&endTs=1689216670445&limit=10 and hit "run query" button and you should see the data.

Have fun.
