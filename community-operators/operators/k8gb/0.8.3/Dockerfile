FROM scratch

LABEL alm-examples="[{"apiVersion":"k8gb.absa.oss/v1beta1","kind":"Gslb","metadata":{"name":"test-gslb-failover","namespace":"test-gslb"},"spec":{"ingress":{"rules":[{"host":"failover.cloud.example.com","http":{"paths":[{"backend":{"serviceName":"frontend-podinfo","servicePort":"http"},"path":"/"}]}}]},"strategy":{"type":"failover","primaryGeoTag":"eu"}}},{"apiVersion":"k8gb.absa.oss/v1beta1","kind":"Gslb","metadata":{"name":"test-gslb","namespace":"test-gslb"},"spec":{"ingress":{"rules":[{"host":"notfound.cloud.example.com","http":{"paths":[{"backend":{"serviceName":"non-existing-app","servicePort":"http"},"path":"/"}]}},{"host":"unhealthy.cloud.example.com","http":{"paths":[{"backend":{"serviceName":"unhealthy-app","servicePort":"http"},"path":"/"}]}},{"host":"roundrobin.cloud.example.com","http":{"paths":[{"backend":{"serviceName":"frontend-podinfo","servicePort":"http"},"path":"/"}]}}]},"strategy":{"type":"roundRobin","splitBrainThresholdSeconds":300,"dnsTtlSeconds":30}}}]"
LABEL capabilities="Seamless Upgrades"
LABEL categories="Networking"
LABEL certified="false"
LABEL containerImage="absaoss/k8gb:v0.8.2"
LABEL createdAt="2021-09-24 12:00:00"
LABEL description="A cloud native Kubernetes Global Balancer"
LABEL namespace="placeholder"
LABEL operatorframework.io/suggested-namespace="k8gb"
LABEL operators.operatorframework.io/builder="operator-sdk-v1.12.0+git"
LABEL operators.operatorframework.io/project_layout="go.kubebuilder.io/v2"
LABEL repository="https://github.com/k8gb/k8gb"
LABEL support="cncf-k8gb-maintainers@lists.cncf.io"

COPY manifests /manifests/
COPY metadata /metadata/
