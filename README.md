# Optimizing Branch Prediction in Processors

This project explores **branch prediction techniques** in computer architecture and proposes an **optimized method** to reduce control hazards and mispredictions. It was developed as part of the **Computer Organization & Architecture (COA) course project**.

---

## 📌 Project Overview

* **Problem**: Control hazards (branch/jump instructions) cause instruction pipeline stalls, reducing processor performance.
* **Solution**: Use branch prediction to guess branch outcomes in advance, minimizing stalls.
* **Goal**: Compare existing prediction strategies and propose an **optimized hybrid technique**.

---

## 🧩 Techniques Studied

1. **Static Branch Prediction**

   * Always Taken / Always Not Taken (simple but less accurate).

2. **Dynamic Branch Prediction**

   * **1-Bit Predictor**: Flips prediction after a wrong guess.
   * **2-Bit Predictor**: Uses a saturating counter for more stability.

3. **Correlating Branch Prediction**

   * Uses the history of multiple branches to predict the next one.

4. **Optimized Branch Prediction (Proposed)**

   * Combines **Static**, **2-Bit**, and **Correlating** predictors using a **2×1 Multiplexer (MUX)**.
   * Dynamically selects the most accurate prediction source.

---

## ⚙️ Example Results

For branch history patterns tested:

* **1-Bit Prediction** → 7 mispredictions
* **2-Bit Prediction** → 6 mispredictions
* **Correlating Prediction** → 6 mispredictions
* **Static Prediction** → 5 mispredictions
* **Optimized Technique** → **1 misprediction** ✅

Another test case showed:

* Optimized method reduced mispredictions to **3**, compared to 4–7 in traditional methods.

---

## 📊 Conclusion

* Traditional predictors work but often fail in complex patterns.
* The **optimized MUX-based predictor** dynamically adapts and achieves **fewer mispredictions**, improving instruction throughput.
* This approach demonstrates a balance between **accuracy and efficiency** in modern processor design.

---

## 👩‍💻 Team Members

* **N. Priyadarshini (CS22B1009)**
* **G. Satya Priya (CS22B1012)**
* **K. Sri Harsha Priya (CS22B1017)**

---
