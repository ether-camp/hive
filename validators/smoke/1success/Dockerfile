# Docker container spec defining and running a simple smoke test consisting of a
# genesis state definition and a short chain to import.
FROM alpine:3.4

# Install curl to allow querying the HTTP-RPC endpoint
RUN apk add --update curl

# Inject the chain definition
ADD genesis.json /genesis.json

# Inject the tester and set the entrypoint
ADD test.sh /test.sh
RUN chmod +x /test.sh

ENTRYPOINT ["/test.sh"]
