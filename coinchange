# The Coin Change Problem (Dynamic Programming)

def get_total_ways(coins: list, amount: int) -> int:
    """Calculates how many different combinations of coins sum up to the amount."""
    # Initialize a DP array of size (amount + 1) with zeros
    dp = [0] * (amount + 1)
    
    # Base case: There is exactly 1 way to make a sum of 0 (use no coins)
    dp[0] = 1
    
    # Build the DP table
    for coin in coins:
        for i in range(coin, amount + 1):
            dp[i] = dp[i] + dp[i - coin]
            
    return dp[amount]


def get_minimum_coins(coins: list, amount: int) -> int:
    """Calculates the minimum number of coins needed to make the amount."""
    # Initialize the DP array with infinity, since we are looking for the minimum
    dp = [float('inf')] * (amount + 1)
    
    # Base case: 0 coins are needed to make a sum of 0
    dp[0] = 0
    
    # Build the DP table
    for i in range(1, amount + 1):
        for coin in coins:
            if i - coin >= 0:
                dp[i] = min(dp[i], dp[i - coin] + 1)
                
    # If the amount is still infinity, it means no combination works
    return dp[amount] if dp[amount] != float('inf') else -1


# --- Execution Block ---
coins_list = [1, 2, 5, 10]
target_sum = 10

ways = get_total_ways(coins_list, target_sum)
min_coins = get_minimum_coins(coins_list, target_sum)

print(f"Target Sum: {target_sum}")
print(f"Available Coins: {coins_list}")
print("-" * 30)
print(f"Total different ways to make {target_sum}: {ways}")
print(f"Minimum coins needed to make {target_sum}: {min_coins}")