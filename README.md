# **Neptune V2 CPU Guesser**  

The current version of ​drpool​ only supports ​CPU-based operation.

**​Hardware Requirements**:​

- ​RAM: Minimum ​45GB​ (the software requires ​40GB​ to run).
- CPU: Recommended ​32 cores or more.

**How to Verify Hardware Compatibility**

Check the log for the entry: ​​"guess preprocess use time"​.
If this time exceeds ​120 seconds, your hardware ​may not meet the requirements, and performance will be degraded.

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
   ```bash
   wget https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu-dr_neptune_prover-2.0.0.tar.gz
   ```
     
3. **Extract & Prepare**  
   ```bash
   tar -zxvf ubuntu-dr_neptune_prover-x.x.x.tar.gz
   cd dr_neptune_prover && chmod +x inner_guesser.sh run_guesser.sh stop_guesser.sh dr_neptune_prover
   ```

4. **Configure Your Account**  
   - Edit `inner_guesser.sh` and update your **[drpool](https://drpool.io) account name**.  

5. **Start Mining**  
   ```bash
   ./start_guesser.sh
   ```
6. **View Mining Logs:**
   ```bash
   tail -n 100 -f guesser.log
   ```
   ![alt text](image.png)
   **Part1**
   1. ​Create the guesser_buffer for later guessing​
   2. The guesser_buffer generation took ​65 seconds.
   
   **Part2**
   
   Mined a valid nonce after proof generation

   **Last 1m speed(KP/s)**

   The proof generation speed per second in the last minute
  
7. **Stop Mining**
   ```bash
   ./stop_guesser.sh
   ```
   
