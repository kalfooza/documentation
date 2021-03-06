# Creating Providers

A Provider can be created by sending a POST request to the `/providers` endpoint, specifing a JSON document.
Again we can use `curl` to do this, but this time pass in different parameters.

The JSON document is sent using an HTTP POST request.
However we need to specify that we are sending JSON in the HTTP HEADER information of the `curl` request using
the `-H` switch.
The actual JSON document is specified using the `-d` switch. Finally the `\` allows us to write the command on multiple lines in our computer's terminal. For example:

    curl -X POST -u <appId>:<appKey> \
      -d '{"xid":"company_id","name":"my_company", ...}' \
      https://papi-sandbox.makeitsocial.com/providers \
      -H "Content-Type: application/json"


