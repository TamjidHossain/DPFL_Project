# DPFL_Project
**Summary:**
This project implements the local differential privacy (LDP) mechanism in the federated learning (FL) process. We find that the differential privacy can be exploited to conduct data/model poisoning attacks in FL process, which in turn can degrade the FL model performance. Sub-optimal model can be generated due to this DP-exploited attacks. This project also shows the evaluation of our DP-exploited attack and proves that the attack is stealthy. It has been done through the computational cost analysis of the process in terms of CPU and RAM usage for three different scenarios: (a) No DP (b) DP included but no attack (b) DP-exploited attack

**Run instruction:**
(1) Download all the files and folder in a single directory
(2) run the "code1.ipynb" file from a jupyter notebook. Before running, you can change following parameters according to your preference:


            dpFlag = [1].  # 0 = No DP, 1= DP
            FDIFlag = [1]. # 0 = No attack, 1 = Attack
            TclientList = [100] # total number of clients = 100
            PclientList = [30] # total number of participating clients (randomly selected) in a round = 30
            epsList = [1.0]. # value of privacy loss, epsilon = 1.0
            deltaList = [0.005] # value of privacy leakage probability, delta = 0.005
            gammaList = [8.0] # value of attacker's tolerance, gamma = 8.0
            sigmaList = [] # It will be calculated automatically; no need to change anything in this line
            patience = 7  # It is related to early stop the process
            malModel = [[5]] # which model we are treating as malicious. In this case, model 5 is the malicious model.


(3) find out the "process id" of this code1.ipynb script through below command (in OSX/mac):
  ps -ax | awk '/[J]upyter/{print $1}'
(4) open "cpu_ram.ipynb" in another jupyter notebook tab
(5) edit the following line of the "cpu_ram.ipynb" file with the process id of code1.ipynb file:
  pr = psutil.Process("PROCESS ID of code1.ipynb")
(6) run "code1.ipynb" and "cpu_ram.ipynb" side by side to see the computational analysis

**Please contact mdtamjidh@nevada.unr.edu for more information**
