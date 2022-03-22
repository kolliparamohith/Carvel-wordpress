# Wordpress Package

WordPress is the world's most popular blogging and content management platform. Powerful yet simple, everyone from students to global corporations use it to build beautiful, functional websites.

## Configuration Reference

You can configure the following:

### WordPress Image parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|imagePullPolicy|WordPress image pull policy|string|IfNotPresent|

### WordPress Configuration parameters

|Parameter|Description|Type|Deafult|
|---------|-----------|----|-------|
|wordpressUsername|WordPress username|string|user|
|wordpressPassword|WordPress user password|string|" "|
|wordpressEmail|WordPress user email|string|user@example.com|
|wordpressFirstName|WordPress user first name|string|FirstName|
|wordpressLastName|WordPress user last name|string|LastName|
|wordpressBlogName| Blog name|string|User's Blog!|
|wordpressTablePrefix|Prefix to use for WordPress database tables|string|wp_|
|wordpressScheme|Scheme to use to generate WordPress URLs|string|http|

### WordPress deployment parameters

|Parameter|Description|Type|Deafult|
|---------|-----------|----|-------|
|replicas|Number of WordPress replicas to deploy|integer|1|
|containerPorts.http|WordPress HTTP container port|integer|8080|
|containerPorts.https|WordPress HTTPS container port|integer|8443|
|podSecurityContext.fsGroup|Set WordPress pod's Security Context fsGroup|integer|1001|
|containerSecurityContext.runAsUser|Set WordPress container's Security Context runAsUser|integer|1001|
|containerSecurityContext.runAsNonRoot|Set WordPress container's Security Context runAsNonRoot|string|true|
|livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|120|
|livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|10|
|livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
|livenessProbe.failureThreshold| Failure threshold for livenessProbe|integer|6|
|livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|30|
|readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|10|
|readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|5|
|readinessProbe.failureThreshold|Failure threshold for readinessProbe|integer|6|
|readinessProbe.successThreshold| Success threshold for readinessProbe|integer|1|

### Traffic Exposure Parameters

|Parameter|Description|Type|Deafult|
|---------|-----------|----|-------|
|ports.http|WordPress service HTTP port|integer|80|
|ports.https|WordPress service HTTPS port|integer|443|
|ingress.enabled|Enable ingress record generation for WordPress|string|false|
|ingress.pathType|Ingress path type|string|ImplementationSpecific|

### Other Parameters

|Parameter|Description|Type|Deafult|
|---------|-----------|----|-------|
|automountServiceAccountToken|Allows auto mount of ServiceAccountToken on the serviceAccount created|string|true|
|autoscaling.minReplicas|Minimum number of WordPress replicas|integer|1|
|autoscaling.maxReplicas|Maximum number of WordPress replicas|integer|11|
|autoscaling.targetCPU|Target CPU utilization percentage|integer|50|
|autoscaling.targetMemory|Target Memory utilization percentage|integer|50|

### Metrics Parameters

|Parameter|Description|Type|Deafult|
|---------|-----------|----|-------|
|metrics.enabled|Enable livenessProbe on Prometheus exporter containers|string|false|
|metrics.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|15|
|metrics.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|10|
|metrics.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
|metrics.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|3|
|metrics.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|metrics.readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|5|
|metrics.readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|10|
|metrics.readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|3|
|metrics.readinessProbe.failureThreshold|Failure threshold for readinessProbe|integer|3|
|metrics.readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|
|metrics.serviceMonitor.enabled|Create ServiceMonitor Resource for scraping metrics using Prometheus Operator|string|false|
|metrics.serviceMonitor.honorLabels|Specify honorLabels parameter to add the scrape endpoint|string|false|



