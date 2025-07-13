1 - Reverse String 

class Solution {
    func reverseString(_ s: inout [Character]) {
  var left = 0
    var right = s.count - 1

    while left < right {
        let temp = s[left]
        s[left] = s[right]
        s[right] = temp

        left += 1
        right -= 1
    }
    }
}

Explaination : Use two pointer approach one for iterate through left and another from right and only iterate till both index is not overlapping using while loop
--------------------------
2 - Best time to Buy and Sell stock 
class Solution {
    func maxProfit(_ prices: [Int]) -> Int {
    var minPrice = Int.max
    var maxProfit = 0

    for price in prices {
        if price < minPrice {
            minPrice = price
        } else if price - minPrice > maxProfit {
            maxProfit = price - minPrice
        }
    }

    return maxProfit
}
}

Explaination : set min price to the max possible int value and max to minimum (0) iterating whole array and checking if else condition 
------------------------
