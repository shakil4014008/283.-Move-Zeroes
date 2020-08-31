# 283.-Move-Zeroes

```c#

/////using in memory


////using additonal memory
 public void MoveZeroes(int[] nums) {
     
        List<int> zero = new List<int>();
        List<int> nonzero = new List<int>();
        
        
        for(int i=0; i<nums.Length; i++){
            if(nums[i] == 0){
                zero.Add(nums[i]);
            }else{
                nonzero.Add(nums[i]);
            } 
        }
        
        int [] arr = new int[zero.Count + nonzero.Count];
        
        int index = 0;
        foreach(var i in nonzero){
            arr[index] = i;
            index++;
        }
        
        foreach(var j in zero){
            arr[index] = j;
            index++;
        }
        
        foreach(var t in arr){
            Console.Write(t +" ");
        }
        
        
        
    }


````
