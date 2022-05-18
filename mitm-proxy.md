## General
1. Certificates are located in ~/.mitmproxy
2. Listen on a specific port
`mitmproxy -p <port>`
3. Focus on a request, Press `Enter` for additional details and modification, q to return back to the proxy list.

## All of the below commands are to be used in the cli interface of mitmproxy i.e after launching the client.
1. Intercept request:
Press `i` then enter desired regex. ( `.*` for all requests and responses)
2. Resume flow (Send the intercepted request): `a`
3. Intercept only requests: `~q`. (Press i, between set intercept enter `.* & ~q` to intercept all the requests and no response)
4. Kill the flow: `X`
5. Edit a request: Focus and select a request, press `e`, select the field, mdify value, press `Enter`, press `Esc`, press `q` and then Resume the flow.
6. Replay request: Focus a request and press `r`.
