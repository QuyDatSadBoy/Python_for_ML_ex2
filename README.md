# Python for Machine Learning - Exercise 2

A collection of Python programming exercises focused on NumPy operations and text processing fundamentals for machine learning applications.

## 📋 Overview

This repository contains solutions to various Python exercises that demonstrate fundamental concepts used in machine learning and data science, including array manipulation with NumPy and text processing techniques.

## 🚀 Exercises

### Exercise 1: Array Reversal
**Objective**: Write a NumPy program to reverse an array (first element becomes last).

**Input**: `[12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37]`

### Exercise 2: Array Element Comparison
**Objective**: Write a NumPy program to test whether each element of a 1-D array is also present in a second array.

**Input**: 
- Array1: `[0 10 20 40 60]`
- Array2: `[10, 30, 40]`

### Exercise 3: Min/Max Indices
**Objective**: Write a NumPy program to find the indices of the maximum and minimum values along the given axis of an array.

**Input**: `[1, 6, 4, 8, 9, -4, -2, 11]`

### Exercise 4: Text Analysis
**Objective**: Read the entire file `story.txt` and write a program to print out the top 100 words that occur most frequently and their corresponding appearance count. Ignore all punctuation characters such as comma, dot, semicolon, etc.

**Sample Output**:
```
            Word | Count           
===================================
           House | 453             
             Dog | 440             
          People | 312             
             ... | ...             
```

## 📁 Repository Structure

```
Python_for_ML_ex2/
├── README.md           # This file
├── ex2.py             # Exercise descriptions and requirements
├── 2_4_solution.py    # Solution for Exercise 4 (Text Analysis)
└── story.txt          # Text file containing "Alice's Adventures in Wonderland"
```

## 🔧 Requirements

- Python 3.x
- NumPy library
- Collections module (built-in)
- Regular expressions (re module, built-in)

## 🏃‍♂️ How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/QuyDatSadBoy/Python_for_ML_ex2.git
   cd Python_for_ML_ex2
   ```

2. **Install dependencies**:
   ```bash
   pip install numpy
   ```

3. **Run the text analysis solution**:
   ```bash
   python 2_4_solution.py
   ```

## 💡 Key Features

### Exercise 4 Solution Highlights:
- **Text Preprocessing**: Converts text to lowercase and removes punctuation
- **Word Tokenization**: Uses regex to split text into individual words
- **Frequency Analysis**: Utilizes Python's `Counter` class for efficient word counting
- **Formatted Output**: Displays results in a clean, table format
- **Top 100 Filter**: Shows only the most frequently occurring words

### Code Example (Exercise 4):
```python
from collections import Counter
from re import split

def main():
    counter = Counter()
    with open("story.txt", "r") as f:
        for line in f:
            line = line.strip().lower()
            if not line:
                continue
            counter.update(x for x in split("[^a-z]+", line) if x)
    
    freqSorted = sorted(counter, key=counter.get, reverse=True)
    
    count = 0
    print("Word".rjust(16), "|", "Count".ljust(16))
    print("=" * 35)
    for word in freqSorted:
        print(word.title().rjust(16), "|", str(counter[word]).ljust(16))
        count += 1
        if count >= 100:
            break
```

## 📚 Learning Objectives

This repository helps you learn:
- **NumPy Array Operations**: Array manipulation, indexing, and comparison
- **Text Processing**: String handling, regex patterns, and text cleaning
- **Data Analysis**: Frequency analysis and statistical operations
- **Python Best Practices**: File I/O, error handling, and clean code structure

## 📖 Data Source

The text analysis exercise uses "Alice's Adventures in Wonderland" by Lewis Carroll, sourced from Project Gutenberg.

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for:
- Additional exercise solutions
- Code optimizations
- Documentation improvements
- New related exercises

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**QuyDatSadBoy**
- GitHub: [@QuyDatSadBoy](https://github.com/QuyDatSadBoy)

---

⭐ **Star this repository if you find it helpful!**
