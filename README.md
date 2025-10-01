# Standard-Dsa-Easy-Solutions-

Array Sorted ----->>>> Use Binary Search

1. Find First And Last Index Sorted Array.
2. Celebraty Problem
3. Maximum Sliding Windows
4. 


   1. valid parenthesis
  
-------------------------------------------------------------------------------------------------------
   2.                   Leet Code &&  Gfg
   3.                 class Solution {
    public boolean isBalanced(String s) {
        // code here
        Stack<Character> st=new Stack<>();
        int n=s.length();
        for(int i=0; i<n; i++){
            
            char ch=s.charAt(i);
            if(ch == '(' || ch == '{' || ch == '[') st.push(ch);
            else{
                // if stack is empty than no any opening parenthese respective closing
                 
                if(st.isEmpty() ) return false; 
                
                 char top=st.peek();
                  //  if respective parenthesis prasent than pop it 
                 if( (ch == ')' && top == '(' ) ||
                     (ch == '}' && top == '{' ) ||
                     (ch == ']' && top == '[')) st.pop();
                     else  return false ;
            }
        }
        // stack is empty than return true value
        return (st.isEmpty());  
    }
}
-------------------------------------------------------------------------------------------------
   

