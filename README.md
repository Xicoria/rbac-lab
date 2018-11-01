# RBAC on Kubernetes workshop

This workshop provides you basic hands on Kubernetes RBAC. It should be enough to get a grasp on access control.

##### Exercise:
 
- Create a namespace: user0
- Create a serviceaccount: sa-user0
- Create a role: full access inside the ns: user0
- Create a cluster-role: get/list access to nodes
- Bind the role, and cluster-role to the sa
- Start a pod which is assigned to the newly created sa
- Verify that inside of that pod you should have limited access to only the user1 ns and listing nodes

*Check that from dev environment you can get nodes and manage resources whithin the namespace.*


##### As a proof of concept, create another namespace named user1 with all the access controls and verify that it cannot access user0 namespace:

- Create a namespace: user1
- Create a serviceaccount: sa-user1
- Create a role: full access inside the ns: user1
- Create a cluster-role: get/list access to nodes
- Bind the role, and cluster-role to the sa
- Start a pod which is assigned to the newly created sa
- Verify that inside of that pod you should have limited access to only the user1 ns and listing nodes


*Check that the dev environment on user0 cannot access resources on user1.*

*Check that the dev environment on user1 cannot access resources on user0.*
