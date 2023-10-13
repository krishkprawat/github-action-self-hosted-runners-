# github-action-self-hosted-runners-

this repo is for the self hosted runner test project
we have to configure inbound and outbound rules
open http and https ports because aws/github needs to be conenct with each other.
becaues both cant be in same network, github can be public hosted and aws can be in vpc.
Inbound traffic - http - ipv4- port 80 - https -ipv4-
outbound traffic - http - ipv4- port 80 - https -ipv4-

1. open github project - settings- action - runners- + new self hosted runner
2. select runner image (linux)
3. select architecture - amd/arm
4. execute the steps mentioned on the screen (run all commands on ec2)

thanks for reading...
