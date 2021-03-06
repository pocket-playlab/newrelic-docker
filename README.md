# newrelic-docker

This is a Docker container to run the newrelic agent on CoreOS. It is inspired 
from [this page][1]. 
The difference with the original solution presented in the previous topic is 
that it reads variables from etcd using the [etcd-env gem][2] so you don't need 
to write your newrelic key in your Dockerfile.

## Installation 

This is specific for running in EC2.

You need to set your `NEWRELIC_KEY` environment variable in the /global dir in 
etcd.

Follow the instructions at [this page][1] to download the nrsysmond beta and 
nrsysmond.cfg files and add them to this repo. Then run docker build. Or get the
 container on the hub by running docker pull pocketplaylab/newrelic-docker.

[1]: https://discuss.newrelic.com/t/how-to-try-out-the-docker-beta/19478
[2]: https://rubygems.org/gems/etcd-env