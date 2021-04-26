# springboot-helm


Helm is an Package manager

![image](https://user-images.githubusercontent.com/54719289/116109764-00ecbd00-a6ad-11eb-9252-4833a147812d.png)




# helm 2 and helm 3 differences:

![image](https://user-images.githubusercontent.com/54719289/116110544-b1f35780-a6ad-11eb-94d6-cb5e349f02a4.png)


# Helm Installation procedure:

    curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
    chmod 700 get_helm.sh
    ./get_helm.sh

Note : {HELM_INSTALL_DIR:="/usr/local/bin"

# Note For helm 3 : curl https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 | bash


![image](https://user-images.githubusercontent.com/54719289/116116773-6c398d80-a6b3-11eb-8999-9de8a25a1534.png)

# update the insatlled location as usr/bin if required

![image](https://user-images.githubusercontent.com/54719289/116117688-6ee8b280-a6b4-11eb-86a4-e4725708e4a7.png)


# Now create helm chart for deploy application

        helm create springboot-application
        
![image](https://user-images.githubusercontent.com/54719289/116129518-1b7d6100-a6c2-11eb-8e3f-5d817217419e.png)

![image](https://user-images.githubusercontent.com/54719289/116129652-42d42e00-a6c2-11eb-8bcf-5711d2a32c9b.png)

# To check the file structure of helm chart, install tree

        yum install -y tree
 
 ![image](https://user-images.githubusercontent.com/54719289/116130103-bf670c80-a6c2-11eb-9072-7a7a66fa3fb7.png)


        >> Charts.yml have below details (meta data information)
                >> type: application ==> type of application
                >> version : 0.10.0   ==> chart version
                >> appVersion : "1.16.0" ==> version no of application being deployed

        >> _helpers.pl ==under this file, will define the values of deployment.yml variables.

# _helpers.tpl
![image](https://user-images.githubusercontent.com/54719289/116131481-5a141b00-a6c4-11eb-96d5-e5c06939640c.png)

# deployment.yml
![image](https://user-images.githubusercontent.com/54719289/116131600-7f088e00-a6c4-11eb-8eef-d44e8f045d5a.png)

# values.yml   -- if we dont update fullOverride then it will take default value (want to update imagename during runtime we can use it)

![image](https://user-images.githubusercontent.com/54719289/116131967-e8889c80-a6c4-11eb-9e3e-d262442dc456.png)


# By default, the port no is 80 in deployment.yml, in case of changes in your application,we can update.

        Before:
![image](https://user-images.githubusercontent.com/54719289/116133565-c4c65600-a6c6-11eb-847c-ef7e185f92a3.png)

        After:
 ![image](https://user-images.githubusercontent.com/54719289/116133652-dc054380-a6c6-11eb-9b62-775a2584def8.png)


# Update your image in values.yml

    Before:
![image](https://user-images.githubusercontent.com/54719289/116133997-49b16f80-a6c7-11eb-8fec-76f6ea86eb74.png)

    After
![image](https://user-images.githubusercontent.com/54719289/116134426-c7757b00-a6c7-11eb-8698-826ce2a4ca5e.png)


 



# The process of label updation is similar as name updation

![image](https://user-images.githubusercontent.com/54719289/116132458-811f1c80-a6c5-11eb-99be-17630b77b3ac.png)





 

