# Practical Introduction to Blockchain-based Remote Electronic Voting
Christian Killer, Bruno Rodrigues, Eder Scheid, Muriel Franco, Burkhard Stiller 
*Communication Systems Group (CSG), Department of Informatics (IfI) 
University of Zurich (UZH), Switzerland*

**This is the official repository for Tutorial 2 *Practical Introduction to Blockchain-based Remote Electronic Voting* presented at the [2020 IEEE International Conference on Blockchain and Cryptocurrency Conference](https://icbc2020.ieee-icbc.org/).**

### Disclaimer
- Even though the full tutorial code is dockerized, it takes (a) some Docker expertise and (b) sufficient RAM and CPU to make it run smoothly on Linux or Windows. 
- Unfortunately, macOS is not supported
- Thus, if you don't want to locally deploy it, simply follow the tutorial and read the code as you see fit.
- The practical part of the tutorial is [based on the code of Provotum 2.0](https://github.com/christiankiller/master-project-evoting), which was developed by [Moritz Eck](https://github.com/meck93), [Alex Scheitlin](https://github.com/alexscheitlin) and [Nik Zaugg](https://github.com/nikzaugg/) in the scope of their Master Project with the CSG@IfI.  

### Prerequisites
- [Docker](https://docs.docker.com/)
- Make sure you create a github.json with a valid access token, otherwise you won't be able to pull from GitHub packages

### Setting up a short demo election on your local OS
1. ```git clone git@github.com:christiankiller/master-project-evoting.git```
2. Set up your [github.json](https://github.com/christiankiller/master-project-evoting)
3. ```./docker-prebuilt-up.sh```
4. ```docker ps```and verify all components are running by visiting the links provided below 

[Voting Authority on http://172.1.1.41:4001/](http://172.1.1.41:4001/)  
[Sealer 1 on http://172.1.1.141:4011/](http://172.1.1.141:4011/)  
[Sealer 2 on http://172.1.1.142:4012/](http://172.1.1.142:4012/)  
[Sealer 3 on http://172.1.1.143:4013](http://172.1.1.143:4013/)  
[Voter Frontend on http://172.1.1.30:3000/](http://172.1.1.30:3000/)

If everything is running smoothly so far, you can continue by following the tutorial steps. 


