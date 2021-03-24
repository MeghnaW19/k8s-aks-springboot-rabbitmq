## Exercise: Deploy a Spring Boot microservice that uses RabbitMQ on K8s cluster in Azure AKS.

* In this exercise, you will deploy a Spring Boot application on K8s Cluster in Azure AKS. This application will produce and consume data using RabbitMQ.

This exercise contains the following:

	- producer-service - A Spring Boot microservice that publishes the message to the direct exchange with a routing key.
	- consumer-service - A Spring Boot microservice which consumes the message asynchronously.
	- k8s-manifests - A folder that contains manifest files.

  

This exercise contains the following files in k8s-manifests folder:  

		- rabbitsecret.yml - To create a K8 Secret.
		- rabbitmq.yml - To create the StatefulSet, and two services, one to expose the management HTTP port on each node and second for StatefulSets.
		- producer.yml - To create a Service of type NodePort for producer-app microservice.
		- consumer.yml - To create a Service of type NodePort for consumer-app microservice.

**Note**: You need to go through the comments thoroughly and complete the application.

Understand and perform following steps to complete the exercise:

	1. Verify that the AKS cluster is created and is ready.
	2. Implement `rabbitsecret.yml` to define a Secret.
	3. Define `rabbitmq.yml` to define StatefulSet and two services.
	4. Test the deployed RabbitMQ management UI from the browser.
	5. Modify `application.yml` of `producer-service` and `consumer-service` following the comments given in the respective files.
	6. Push the docker images of both applications to DockerHub.
	7. Implement `producer.yml` to define Deployment and Service.
	8. Implement `consumer.yml` to define Deployment and Service.
	9. To produce data in RabbitMQ, test the POST endpoint in POSTMAN.
	10. Verify the consumption of message by `consumer-service`.
	11. You can also verify the production and consumption of data through the RabbitMQ management UI opened in Step 4.

  

### Instructions 

- Take care of whitespace/trailing whitespace
- Do not change the provided code unless instructed
- Ensure your code compiles without any errors/warning/deprecations
- Follow best practices while coding
