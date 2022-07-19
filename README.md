# k8s-mongo
mongoDB and mongo express application setup with k8s components



1> create a secret for mongo deployment

2> create mongodb deployment (port: 27017)

3> create a service to talk with mongodb pod (cluster ip or internal service)

4> create a configmap having the db-url (the service url that attached to db pod)

5> create mongo-express deployment(port: 8081)
	> Need to to specify, which db to connect to?
		>mongoDB Address /Internal service, (...MONGODB_SERVER) (refer from configmap)
	
	> Which credentials to authenticate?
		> ...ADMINUSERNAME  (refer from secret)
		> ...ADMINPASSWORD

5> create an external service (type: LoadBalancer, and a NodePort: 30000~327667) for mongo-express.

6> Now take the public-ip:port and open in browser!

DONE!!!
