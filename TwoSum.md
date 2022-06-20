// Input: nums = [2,7,11,15], target = 9
// Output: [0,1]
// Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

// Input: nums = [3,2,4], target = 6
// Output: [1,2]

// Input: nums = [3,3], target = 6
// Output: [0,1]

//Time Complexity ---> O(n^2)
```
const TwoSum = (nums, target) => {
  for (let i = 0; i < nums.length; i++){
    for (let j = i+1; j< nums.length; j++){
      if (nums[i] + nums[j] == target){
        return [i, j];
      }  
    }
  } 
};

//Time Complexity ---> O(n)
const TwoSum2 = (nums, target) => {
  for (let i = 0; i < nums.length; i++){
    let compliment = target - nums[i];
    if (nums.includes(compliment) && nums.indexOf(compliment) !== i){
      return [i, nums.indexOf(compliment)];
    }
  } 
};

TwoSum2([3,3], 6);
```
