words = []
with open("sai.txt", "r") as f:
    for line in f:
        words.extend(line.split())

from collections import Counter
counts = Counter(words)
top10 = counts.most_common(10)
print(top10)
