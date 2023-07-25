# Smart Talk


Steps to run the same example
###### Setup Docker-desktop and enable Kubernetes

1. Clone the podinfo using the following command

        git clone https://github.com/stefanprodan/podinfo/

2. if you would like to build the image from scratch use the following (Optional)

        docker build . -t USERNAME/REPO-NAME:VERSION

3. Push the newly created image to your Repo (Optional)
    
        docker push USERNAME/REPO-NAME:VERSION

4. Use the doployment files as is

        cd kustomiz

        kubectl apply -f deployment.yaml
        kubectl apply -f service.yaml


5. Modify the doployment files to have your image
    
        vi deployment.yaml 

replace this         image: ghcr.io/stefanprodan/podinfo:6.4.0 with your image uri






