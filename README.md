# Demo Application.
## Demo Application Architecture
![image](https://github.com/user-attachments/assets/c28faf2b-7127-4d2f-98d0-954c095ebe1f)

## Application information
            | Service                                            | Language      |
            | ---------------------------------------------------| ------------- | 
            | frontend                                           | Go            | 
            | cartservice                                        | C#            | 
            | productcatalogservice                              | Go            | 
            | currencyservice                                    | Node.js       |   
            | paymentservice                                     | Node.js       | 
            | shippingservice                                    | Go            | 
            | emailservice                                       | Python        | 
            | checkoutservice                                    | Go            | 
            | recommendationservice                              | Python        |
            | loadgenerator                                      | Python/Locust | 


## Training Demo Steps.

### Logining into Cloud Shell from CCE Console.
<img width="1919" height="693" alt="image" src="https://github.com/user-attachments/assets/f43ae849-44f3-4beb-a21d-6116c9c92bf5" />
<br/><br/>

### Cloning Github Repository to Cloud Shell Instance.

```
git clone https://github.com/canberkglr/cce-demo-app.git
```

<img width="845" height="147" alt="image" src="https://github.com/user-attachments/assets/d4ad97db-f606-404b-9d1c-11fd1ae88670" />
<br/><br/>

### Create Namespace and Apply Application Manifest files.
```
kubectl create ns demo-app
kubectl apply -f cce-demo-app/kubernetes-manifests/ -n demo-app
```
<img width="882" height="432" alt="image" src="https://github.com/user-attachments/assets/6bfa103f-3c7c-4377-a14b-cbfaaa5bf514" />
<br/><br/>

### Check Deployment Statuses from Console and Make Sure All Deployments are Running.
<img width="1870" height="980" alt="image" src="https://github.com/user-attachments/assets/6d74ce76-d46c-4d18-b660-331a8c9f822a" />
<br/><br/>

### Install NGINX Ingress Controller Addon.
<img width="1912" height="1003" alt="image" src="https://github.com/user-attachments/assets/d4e986f7-5e8f-4459-a7f1-b85b06b982dd" />

<img width="1299" height="989" alt="image" src="https://github.com/user-attachments/assets/00fd257d-e89b-442c-a75e-3a7c96ea4dfe" />
<br/><br/>

### Configure Ingress Object and Expose Application to Public.
<img width="1918" height="697" alt="image" src="https://github.com/user-attachments/assets/f0e5a2d5-79b1-48e9-b122-e7fed51525d8" />

<img width="1170" height="1014" alt="image" src="https://github.com/user-attachments/assets/66414417-6015-4077-8b16-f463f28d46f9" />

<br/><br/>

### Access Application Through Web Browser
<img width="1893" height="419" alt="image" src="https://github.com/user-attachments/assets/e60c1b48-2b98-4205-a0b6-3b1569830bfd" />
<br/><br/>

<img width="1915" height="1171" alt="image" src="https://github.com/user-attachments/assets/64750583-ad5b-45a3-8c62-b7f425015cea" />

