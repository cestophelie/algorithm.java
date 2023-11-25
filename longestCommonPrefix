class Solution {
    public String longestCommonPrefix(String[] strs) {
        // 1. find the shortest string
        // 2. check with the first half of the shortest string as a prefix
        // Time complexity : N^2
        // Space complexity : N
        int idx = 0;
        int min = 200;
        int i, j, flag = 0;
        String prefix = "";
        
        // Step1) Find the shortest string
        for (i = 0; i < strs.length; i++) {
            if (strs[i].length() < min) {
                idx = i;
                min = strs[i].length();
            }
        }
        
        System.out.println(strs[idx]);

        if(strs.length == 1){
            return strs[idx];
        }
        // Step2)
        for (i = 1; i <= strs[idx].length(); i++){
            prefix = strs[idx].substring(0, i);
            
            for(j = 0; j< strs.length; j++){
                if (strs[j].substring(0, i).equals(prefix)){
                    if(j == strs.length-1){
                        // when reached the end of the array
                        flag = 1;
                    }
                    //pass;
                }
                else{ //when did not reached the end
                    return strs[idx].substring(0,i-1);
                }
                
            }
            j = 0;
        }

        // when reached the end
        if (flag == 1) {
            return strs[idx].substring(0,i-1);
        }
        else {
            return "";
        }
    }
}

/*
public class Solution {
    public String longestCommonPrefix(String[] strs) {
        if (strs == null || strs.length == 0) return "";
        String prefix = strs[0];
        for (String s : strs)
            while (s.indexOf(prefix) != 0)
                prefix = prefix.substring(0, prefix.length() - 1);
        return prefix;
    }
}
*/
