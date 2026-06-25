# Longest Common Subsequence (LCS)

# Define the input strings directly
str1 = "abcde"
str2 = "ace"

m = len(str1)
n = len(str2)

# Initialize a 2D list (matrix) with zeros
dp = [[0] * (n + 1) for _ in range(m + 1)]

# Build the dp table
for i in range(1, m + 1):
    for j in range(1, n + 1):
        if str1[i - 1] == str2[j - 1]:
            dp[i][j] = dp[i - 1][j - 1] + 1
        else:
            dp[i][j] = max(dp[i - 1][j], dp[i][j - 1])

# The result is stored in the bottom-right corner of the matrix
lcs_length = dp[m][n]

print(f"Length of LCS is {lcs_length}")