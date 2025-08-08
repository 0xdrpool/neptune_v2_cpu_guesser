# **Neptune V2 CPU Guesser**  


---

## **📌 CPU Mining Tutorial**  

### **1️⃣ Mining Pool Address**  
```bash
-p stratum+tcp://neptune.drpool.io:30127
```

### **2️⃣ Latest Miner Releases**  
🔗 **[Download Here](https://github.com/0xdrpool/neptune_v2_cpu_guesser/blob/main/download.md)**  

### **3️⃣ Mining Guide**  

#### **Basic Command**  
```bash
./dr_neptune_prover -p stratum+tcp://neptune.drpool.io:30127 -w drpoolaccount.xxx
```

### **4️⃣ Register a DRPool Account​**  

[drpool register](https://drpool.io/user/register)

---

### **⚙️ Setup on Ubuntu (v18.04+)**  

1. **Get a Mining Address**
   
   **Option 1**
   - Download **[Neptune-Core](https://github.com/Neptune-Crypto/neptune-core/releases/latest)**  
   - Generate a wallet:`neptune-cli generate-wallet`
   
   **Option 2**
   
   [vxb_neptune_wallet](https://github.com/VxBlocks/vxb_neptune_wallet)

1. **Download the Miner**  
   - Get the latest `ubuntu-dr_neptune_prover-x.x.x.tar.gz` from **[Download](https://github.com/0xdrpool/neptune_v2_cpu_guesser/blob/main/download.md)**
     
3. **Extract & Prepare**  
   ```bash
   tar -zxvf ubuntu-dr_neptune_prover-x.x.x.tar.gz
   cd dr_neptune_prover && chmod +x inner_guesser.sh run_guesser.sh stop_guesser.sh dr_neptune_prover
   ```

4. **Configure Your Account**  
   - Edit `inner_guesser.sh` and update your **[drpool](https://drpool.io) account name**.  

5. **Start Mining**  
   ```bash
   ./run_guesser.sh
   ```
6. **View Mining Logs:**
  
7. **Stop Mining**
   ```bash
   ./stop_guesser.sh
   ```
   
