# leetcode 557 反转字符串中的单词 III
## edited by 王少锐
## c++



```cpp
class Solution {
public:
    // void f(string s,int i,int j){
    //     char c;
    //     c=s[i];
    //     s[i]=s[j];
    //     s[j]=c;
    // }
    string reverseWords(string s) {
        //char a[100000];
        int flag=0,a,b;
        for(int i=0;i<s.length();i++){
            if(s[i]==' '||i==s.length()-1){
                if(i==s.length()-1) b=i;
                else b=i-1;
                a=flag;
                while(a<b){
                    char c=s[a];
                    s[a]=s[b];
                    s[b]=c;
                    a++;
                    b--;
                }
                flag=i+1;
            }
        }
        return s;
    }
};

```

