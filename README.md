# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
    import math

    p = [0.4, 0.19, 0.16, 0.15, 0.15]
    lk = [3, 4, 2, 4, 3, 3, 2]
    n = len(p)

     L = sum(p[k] * lk[k] for k in range(n))
    hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
    hs = round(hs, 3)

    eff = round(hs / L, 3)
    red = round(1 - eff, 3)

    var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
    var = round(var, 3)

    print(f"Average Codeword Length is : {L}")
    print(f"Entropy is : {hs}")
    print(f"Efficiency is : {eff * 100}%")
    print(f"Redundancy is : {red}")
    print(f"Variance is : {var}")


# Calculation:
<img width="1233" height="1600" alt="image" src="https://github.com/user-attachments/assets/7cf3f535-287c-4c5c-a45b-061a123815ec" />

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/3c2a6926-f580-46f5-be3c-73a851f4a5e8" />

<img width="1285" height="1600" alt="image" src="https://github.com/user-attachments/assets/59191854-ce39-4090-8804-6648c414e888" />



# Output
<img width="477" height="108" alt="image" src="https://github.com/user-attachments/assets/829c796c-8174-4d35-bb89-48d7414c1f8a" />

# Results:
The Huffman and Shannon-Fano of the given statistics {0.4, 0.19, 0.16, 0.15, 0.15} using python are verified.
