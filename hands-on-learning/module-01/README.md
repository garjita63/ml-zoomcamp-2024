## Setting up the Environment
_Source_ : **https://github.com/DataTalksClub/machine-learning-zoomcamp/blob/master/01-intro/06-environment.md**

### Linux
- VMWare
- Linux Mint 21 (Ubuntu)
- Install Anaconda
  ```
  $ wget https://repo.anaconda.com/archive/Anaconda3-2024.06-1-Linux-x86_64.sh
  ```
- Craeate envronment for course
  ```
  conda create -n ml-zoomcamp python=3.11
  ```
- Activate environment
  ```
  conda activate ml-zoomcamp
  ```
- Installing libraries
  ```
  conda install numpy pandas scikit-learn seaborn jupyter
  ```
  Later in the course you will also need to install XGBoost and Tensorflow, but we can skip this part for now.

### Cloud (AWS)
- [Creating an AWS account](https://mlbookcamp.com/article/aws)
  
- [Renting an ec2 instance](https://mlbookcamp.com/article/aws-ec2)


  **Setup**
  
  <img width="140" alt="image" src="https://github.com/user-attachments/assets/7fbde986-a0b3-4500-b182-65d508b3126a">  
  <img width="301" alt="image" src="https://github.com/user-attachments/assets/5d303557-207f-4a0e-8353-ddd4b972fe51">
  <img width="475" alt="image" src="https://github.com/user-attachments/assets/5c1e4fe4-d983-462c-83a8-d85260bdeb8f">
  <img width="506" alt="image" src="https://github.com/user-attachments/assets/2dbb08fe-08cd-4c0b-8d5a-e372a9751724">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/eb8488df-bbfc-4c47-ab42-5816c79d8269">
  <img width="499" alt="image" src="https://github.com/user-attachments/assets/e782de3c-7046-4959-8b78-26fa9968ac89">
  <img width="387" alt="image" src="https://github.com/user-attachments/assets/56c3be95-dbab-41af-8cf7-a733ce9d4210">
  <img width="387" alt="image" src="https://github.com/user-attachments/assets/340e1cf4-c620-4a78-bbc1-92652d9f00de">
  <img width="503" alt="image" src="https://github.com/user-attachments/assets/c46a0354-749f-43e0-90a0-b9f03eaaf603">
  <img width="509" alt="image" src="https://github.com/user-attachments/assets/5910d146-d2de-4d55-a708-5fec472d2d6f">
  <img width="235" alt="image" src="https://github.com/user-attachments/assets/23b39df2-2f46-4bf9-8083-d76f935de16d">


  **Instance Status & Summary**

  <img width="674" alt="image" src="https://github.com/user-attachments/assets/0aa57877-bed1-42d4-ba4a-6470614f8467">
  <img width="529" alt="image" src="https://github.com/user-attachments/assets/55430d9c-0b50-4ef4-8875-556d122f8954">

  
  **Configure EC2 instance Server in Linux**  

  <img width="521" alt="image" src="https://github.com/user-attachments/assets/1c29cfd4-ff03-4626-83a9-620992adb1a2">

  - Copy key to ~/.ssh
 
    <img width="448" alt="image" src="https://github.com/user-attachments/assets/5e7c5982-4069-47d1-a56f-a2582de34ede">

  - Make config file
 
    Use Public IPv4 address
    
    ```
    cd ~/.ssh
    vi coonfig
    ```
    ```
      Host ml-zoomcamp
        HostName 108.137.91.254
        User ubuntu
        IdentityFile /home/hduser/.ssh/ml-zoomcamp-gar-key.pem
        StrictHostKeyChecking no
     ```
 
    Note: HostName will change when instance restart


  **Login to EC2 Instance Server**
  
    ``` 	
    ssh ml-zoomcamp
    ```
    
    <img width="529" alt="image" src="https://github.com/user-attachments/assets/b9281ad5-9568-4c67-8755-9648e668a26c">


  **Clone machine-learning-zoomcamp repository**

  <img width="296" alt="image" src="https://github.com/user-attachments/assets/da1b3a42-61d3-4e45-9272-eded6692427b">

  ```
  git clone https://github.com/DataTalksClub/machine-learning-zoomcamp.git
  ```

  **Install Anaconda3 in EC2 Instance Server**

    https://www.anaconda.com/download/success
  
    <img width="218" alt="image" src="https://github.com/user-attachments/assets/b4aac9fe-e47e-4092-b153-a24a72fa4b7d">

    Copy link
  
    ```
    wget https://repo.anaconda.com/archive/Anaconda3-2024.06-1-Linux-x86_64.sh

    bash Anaconda3-2024.06-1-Linux-x86_64.sh
    ```

  **Install docker-compose**
  
    ```
    mkdir soft
    cd soft
    ```   
    Open browser
  
    https://github.com/docker/compose/releases
  
    <img width="508" alt="image" src="https://github.com/user-attachments/assets/0cb73ba8-b02b-4c09-ba7a-723074b8a3c6">
  
    Copy link
  
    ```
    wget https://github.com/docker/compose/releases/download/v2.29.7/docker-compose-linux-x86_64
    ```
    ```
    chmnod +x docker-compose
    ```

    **Login using Visual Studio Code (code) via Linux**

    ```
    which code
    code
    ```

    <img width="178" alt="image" src="https://github.com/user-attachments/assets/eed48fcd-3f00-4c3d-a036-8f6cbbfb7279">

    <img width="293" alt="image" src="https://github.com/user-attachments/assets/948dd97b-fcbd-4628-8392-732deca9b455">

    <img width="212" alt="image" src="https://github.com/user-attachments/assets/2e16a72e-86cb-4ef1-b405-a2f8bfa4f1a1">

    <img width="384" alt="image" src="https://github.com/user-attachments/assets/6f899e2f-8940-4922-a6d0-1d8403ac0e81">
	
    
