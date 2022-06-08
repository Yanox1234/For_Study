### Cluster for broetli

### Before starting

```
docker login
```

### Start

```
docker compose up -d
```
After the launching:

1) you may open `http://localhost:4200` to reach a UI.
2) you may open `http://localhost:8080/` to reach an Apache Kafka UI.

### Start with logs

```
docker-compose up --build -V
```

### Stop

```
docker compose down
```

### Monitor the Resource Usage of Docker Containers

```
docker stats
```

### Deployment
```
mvn clean package -Dspring.profiles.active=prod  -Pspring.profiles.active=prod 
```

# Stripe

https://stripe.com/docs/payments/handling-payment-events
### Start listener 
```
stripe listen --forward-to http://localhost:8080/api/v1/stripe-webhooks
```
### Trigger an event
```
stripe trigger payment_intent.succeeded
```

### Migrate to kubernetes
```
https://kubernetes.io/docs/tasks/configure-pod-container/translate-compose-kubernetes/
```


### Clear artifacts in Gitlab
```
curl --request DELETE --header "PRIVATE-TOKEN: glpat-C2YoepZ7qAPdnYojzQzf" \
"https://gitlab.com/api/v4/projects/35275961/artifacts"
```

# Articles

`https://javascript.plainenglish.io/a-beginners-introduction-to-kafka-with-typescript-using-nestjs-7c92fe78f638`
