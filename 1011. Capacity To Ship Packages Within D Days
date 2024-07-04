class Solution {
    public int shipWithinDays(int[] weights, int days) {
        int lo = getMax(weights);
        int hi = getSum(weights);

        while (lo <= hi) {
            int mid = (lo + hi) / 2;
            if (daysNum(mid, weights) <= days) {
                hi = mid - 1;
            } else {
                lo = mid + 1;
            }
        }
        return lo;
    }

    private int daysNum(int mid, int[] weights) {
        int d = 1, temp = 0;
        for (int weight : weights) {
            if (weight > mid) {
                return Integer.MAX_VALUE;
            }
            temp += weight;
            if (temp > mid) {
                d++;
                temp = weight;
            }
        }
        return d;
    }

    private int getMax(int[] weights) {
        int max = weights[0];
        for (int weight : weights) {
            if (weight > max) {
                max = weight;
            }
        }
        return max;
    }

    private int getSum(int[] weights) {
        int sum = 0;
        for (int weight : weights) {
            sum += weight;
        }
        return sum;
    }
}
