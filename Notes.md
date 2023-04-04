# Deploy

gcloud functions deploy YOUR_FUNCTION_NAME \
[--gen2] \
--region=YOUR_REGION \
--runtime=YOUR_RUNTIME \
--source=YOUR_SOURCE_LOCATION \
--entry-point=YOUR_CODE_ENTRYPOINT \
TRIGGER_FLAGS

During upload of your source code, Cloud Functions excludes unnecessary files via the .gcloudignore file.

gcloud functions deploy NAME --runtime ruby30 --trigger-http

# Run local version of functions framework for testing
bundle exec functions-framework-ruby --source=foo.rb --target=hello
curl http://localhost:8080/

# Triggering the function
gcloud functions describe ruby-http-function --gen2 --region REGION --format="value(serviceConfig.uri)"

curl -m 70 -X POST URI \
    -H "Authorization: bearer $(gcloud auth print-identity-token)" \
    -H "Content-Type: application/json" \
    -d '{}'

## Calling functions directly
gcloud functions call YOUR_FUNCTION_NAME --data '{"name":"Keyboard Cat"}'

## Since PubSub messages are encoded, this is the proper way to test
DATA=$(printf 'Hello!'|base64) && gcloud functions call hello_pubsub --data '{"data":"'$DATA'"}'

# Delete the function
gcloud functions delete ruby-http-function --gen2 --region REGION

