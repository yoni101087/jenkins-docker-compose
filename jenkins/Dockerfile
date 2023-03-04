FROM ubuntu:latest



# Install Python
RUN apt-get update 
ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Asia/Jerusalem
RUN apt-get install -y tzdata

    
RUN apt-get install software-properties-common -y && \
    add-apt-repository --yes ppa:deadsnakes/ppa && \
    apt-get install python3.8 -y && \
    apt-get install wget -y && \
    apt-get install git -y && \
    apt-get install default-jre -y && \
    update-alternatives --config java


# Install Jenkins
RUN wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | apt-key add - && \
    sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' && \
    apt-get update && \
    apt-get install -y jenkins

# Expose the default Jenkins port
EXPOSE 8080

# Start Jenkins when the container starts
CMD service jenkins start && tail -f /var/log/jenkins/jenkins.log

