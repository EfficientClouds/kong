To add auth0 token validation to kong api gateway you need to do the following:

1. Run the following command:
   curl https://your auth0Domain/pem | openssl x509 -pubkey -noout
2. Copy the public key and paste it into the public key area in jwt_auth0.yml
3. run kubectl apply -f jwt_auth0.yml -n your_kong_api_gateway_namespace
