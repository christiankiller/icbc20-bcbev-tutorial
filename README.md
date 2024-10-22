# Practical Introduction to Blockchain-based Remote Electronic Voting
Christian Killer, Bruno Rodrigues, Eder Scheid, Muriel Franco, Burkhard Stiller 
*Communication Systems Group (CSG), Department of Informatics (IfI) 
University of Zurich (UZH), Switzerland*

**This is the official repository for Tutorial 2 *Practical Introduction to Blockchain-based Remote Electronic Voting* presented at the [2020 IEEE International Conference on Blockchain and Cryptocurrency Conference](https://icbc2020.ieee-icbc.org/).**

### Tutorial Materials
- [Tutorial Slides (PDF, 1-up)](/assets/ICBC20-BCBEV-Tutorial-v8.pdf)
- [Provotum 2.0 Code (different repository)](https://github.com/christiankiller/master-project-evoting) 
- [Provotum 2.0 Voting Protocol Steps (Videos)](/videos/)

### Disclaimer
- Even though the full tutorial code is dockerized, it takes (a) some Docker expertise and (b) sufficient RAM and CPU to make it run smoothly on Linux or Windows. 
- Unfortunately, macOS is not supported
- Thus, **if you don't want to locally deploy it, simply follow the tutorial and [read the code](https://github.com/christiankiller/master-project-evoting) as you see fit.**
- The practical part of the tutorial is [based on the code of Provotum 2.0](https://github.com/christiankiller/master-project-evoting), which was developed by [Moritz Eck](https://github.com/meck93), [Alex Scheitlin](https://github.com/alexscheitlin) and [Nik Zaugg](https://github.com/nikzaugg/) in the scope of their Master Project with the CSG@IfI.  

### Prerequisites
- [Docker](https://docs.docker.com/) and [Docker Compose](https://docs.docker.com/compose/)
- Make sure you create a [github.json](https://github.com/christiankiller/master-project-evoting#github-packages--github-config-json-important) with a valid access token, otherwise you won't be able to pull from GitHub packages

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

### Setting up a demo election on a remote VPS
1. Make sure the image is [Docker-ready](https://marketplace.digitalocean.com/apps/docker), which saves you some time
2. Follow the steps above for the local OS
3. Use `ssh -D 5000 -C -q -N [REMOTE-IP]` to enable `-D` Dynamic application-level port forwarding, `-C` use compression, `-q` quiet mode, `-N` macOS specific (Do not execute a remote command.  This is useful for just forwarding ports.)
4. Set up a proxy in your browser as shown in [the screenshot here](/assets/vps-local-firefox-proxy.jpg).

# References

- **[KRM20]** C. Killer, B. Rodrigues, R. Matile, E. Scheid, B. Stiller: Design and Implementation of Cast-as-Intended Verifiability for a Blockchain-based Voting System. In: Proceedings of the 2020 ACM Symposium on Applied Computing. SAC ’20, Association for Computing Machinery, New York, NY, USA, 2020. Paper: http://bcbev.ch/uciv

- **[KS19]** C. Killer, B. Stiller: The Swiss Postal Voting Process and Its System and Security Analysis. In: R. Krimmer, M. Volkamer, V. Cortier, B. Beckert, R. Küsters, U. Serdült, D.Duenas-Cid (eds.) Electronic Voting. Springer International Publishing, Cham, 2019, p. 134–149, Paper: http://pvpf.ch/paper

- **[MK18]** R. Matile, C. Killer: Privacy, Verifiability, and Auditability in Blockchain-based E-Voting, 2018, Master’s Project, University of Zurich, http://bcbev.ch/pv

- **[BT94]** Josh Benaloh and Dwight Tuinstra. Receipt-Free Secret-Ballot Elections. In Proceedings of the Twenty-Sixth Annual ACM Symposium on Theory of Computing, STOC ’94, pages544–553, New York,NY, USA,1994. Association for Computing Machinery. 

- **[CGS97]** Ronald Cramer, Rosario Gennaro, and Berry Schoenmakers. A secure andoptimally efficient multi- authority election scheme. InLecture Notes inComputer Science (including subseries Lecture Notes in Artificial Intelligenceand Lecture Notes in Bioinformatics), 1997.

- **[Cha81]** David L. Chaum. Untraceable Electronic Mail, Return Addresses, and Digital Pseudonyms.Communications of the ACM, 1981.

- **[Cha04]** David Chaum. Secret-Ballot Receipts: True Voter-Verifiable Elections,2004.

- **[DH76]** Whitfield Diffie and Martin E. Hellman. New Directions in Cryptography. IEEE Transactions on Information Theory, 1976.

- **[Elg85]** T. Elgamal. A public key cryptosystem and a signature scheme based on discrete logarithms. IEEE Transactions on Information Theory, 31(4):469–472,71985.

- **[FOO92]** Atsushi Fujioka, Tatsuaki Okamoto, and Kazuo Ohta. A Practical SecretVoting Scheme for Large Scale Elections. In Proceedings of the Workshop on the Theory and Application of Cryptographic Techniques: Advances in Cryptology, ASIACRYPT ’92, pages 244–251, Berlin, Heidelberg, 1992. Springer-Verlag.

- **[JCJ05]** Ari Juels, Dario Catalano, and Markus Jakobsson. Coercion-ResistantElectronic Elections. InProceedings of the 2005 ACM Workshop on Privacy in the Electronic Society, WPES ’05, page 61–70, New York, NY, USA, 2005. Association for Computing Machinery.

### Further Materials
- [Provotum 2.0 Project Report](https://github.com/christiankiller/master-project-evoting/blob/master/assets/report.pdf)
- [Crypto Library Dependency](https://github.com/meck93/evote-crypto/)
