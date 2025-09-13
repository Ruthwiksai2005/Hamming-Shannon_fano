# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.4,0.19,0.16,0.15,0.15} for its output. 
Apply the Huffman to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
Google Colab 
# Program:
```
import math
p = [0.4,0.19,0.16,0.15,0.15]
# Corresponding Huffman/Shannon-Fano code lengths
lk = [1,3,3,3,3]
n = len(p)
# Average Codeword Length
L = sum(p[k] * lk[k] 
for k in range(n))
# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2)
 for k in range(n))
hs = round(hs, 3)
# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)
# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2 
for k in range(n))
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:

![Huffmann ](https://github.com/user-attachments/assets/cb700a91-f57f-4f5d-9f2f-4ca017ed1976)

# Output
<img width="321" height="101" alt="image" src="https://github.com/user-attachments/assets/6a3f4cd3-1d4a-4f62-881a-fb9060542b2a" />
# Results:
```
Thus,the average code word length, entropy, variance, redundancy, and efficiency was calculated and verified with observed values.
```
