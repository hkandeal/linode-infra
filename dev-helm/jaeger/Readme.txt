helm repo add jaegertracing https://jaegertracing.github.io/helm-charts

helm install jaeger jaegertracing/jaeger --set cassandra.config.max_heap_size=1024M --set cassandra.config.heap_new_size=512M --set cassandra.resources.requests.memory=1024Mi --set cassandra.resources.requests.cpu=0.4 --set cassandra.resources.limits.memory=2048Mi --set cassandra.resources.limits.cpu=0.4 -n monitoring --values=values.yml


helm install jaeger jaegertracing/jaeger -n monitoring --values=values.yaml