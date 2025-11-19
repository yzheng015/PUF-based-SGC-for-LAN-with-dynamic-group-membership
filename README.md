# PUF-based-SGC-for-LAN-with-dynamic-group-membership
This repository contains the official release of (1) the ProVerif scripts and verification results; (2) the demonstration video of a 16-node prototype LAN, for "A Lightweight PUF-based Secure Group Communication Scheme for Low Altitude Network With Dynamic Group Membership", accepted by IEEE Transactions on Mobile Computing in 2025. 

This paper introduced a novel PUF-based lightweight secure group communication protocol. The proposed protocol utilizes a combination of the device’s PUF and the one-time pad (OTP) to eliminate secure key storage at both group verifier and prover nodes, and achieves perfect forward secrecy (PFS) by eliminating dependence on static long-term secrets. The proposed protocol also supports efficient group key renewal by using a full binary tree as a secret vault for sharing and updating distributed secrets with Chinese Remainder Theorem (CRT). Meantime, this data structure also reduces the computation and communication complexity  for key renewal to $O(\log_2N)$ at the cluster head and $O(1)$ at the sensor nodes. A comparative analysis shows that the proposed protocol surpasses related protocols in terms of security features and overheads in computation, communication as well as secret storage requirements. The proposed protocol was also validated by formal security analyse and a physical LAN implementation using Ultra96-V2 boards as cluster nodes.

================Automatic Security Analysis Tool by ProVerif===================== 

GKM_ProVerif.text-----> the ProVerif code to describe GKM process in Fig. 5 in the manuscript
GMM_ProVerif.text -----> the ProVerif code to describe the GMM process in Fig. 6 in the manuscript 

To verify the security of the proposed work, please copy the scripts in above two files directly to http://proverif24.paris.inria.fr/ (the online demo for Proverif), click the "verify" button

GKM_verification summary.jpg -----> verifies the security of our proposed GKM process 
GMM_verification summary.jpg -----> verifies the security of our proposed GMM process 


================================Implementation==================================

group_key_demo.mp4 -----> shows the protype of our work in a demonstrative video. The network can support 16 nodes. Due to limited FPGA availability, we present the procedures of key establishment and update among 5 devices. 
