# tekton-slack-message
This is a simple repository with Tekton tasks to use slack incoming webhooks to publish messages. Follow [this link](https://api.slack.com/messaging/webhooks) on how to create an incoming webhook URL for your slack workspace/channel.

### Steps

* Run the following command to create the task that uses incoming webhooks of slack to send the message:
```
kubectl apply -f https://raw.githubusercontent.com/tektoncd/catalog/v1beta1/slackmessage/send-to-webhook-slack.yaml
```

* Edit _webhook-secret.yaml_ to add your slack webhook URL and then execute the following:
```
kubectl apply -f webhook-secret.yaml
```

* Edit _run-send-to-webhook-slack.yaml_ to modify the message to be posted. Execute the following to create a taskrun:
```
kubectl apply -f run-send-to-webhook-slack.yaml
```


