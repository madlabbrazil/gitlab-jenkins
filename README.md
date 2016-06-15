# gitlab-jenkins

Description:
![alt slider](http://cdn.madlabbrazil.com/ex06.jpg)

[Full Presetation](https://docs.google.com/presentation/d/1DReA_GDzy6HvG0TJ1Ry-CQlmVhuNZsEbXi7VGO3-f3k/edit?usp=sharing)


```
useradd -c "Jenkins User" -d /home/jenkins -m -u 1000  jenkins
su jenkins
mkdir -p /home/jenkins/docker_jenkins_home
```

Create Jenkins Home Volume
```
docker run --name ci-jenkins -p 8080:8080 -p 50000:50000 -v /home/jenkins/docker_jenkins_home:/var/jenkins_home  -u jenkins jenkins:2.0

docker run -d  --name ci-gitlab -p 8888:80 -p 4444:443  -p 2222:22 gitlab/gitlab-ce
```
