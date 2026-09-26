# 58. Length of Last Word
# Given a string s consisting of words and spaces, return the length of the last word in the string.
# A word is a maximal substring consisting of non-space characters only.

class Solution {
public:
    int lengthOfLastWord(string s) {
        int count = 0;
        for (int i = s.size() - 1; i >= 0; i--) {
            if (s[i] != ' ')
                count++;
            else if (count > 0)
                break;
        }
        return count;
    }
};


# Length of Last Word Using stringstream
class Solution {
public:
    int lengthOfLastWord(string s) {
        string word;
        stringstream ss(s);
        while (ss >> word) {
             // Keep reading until the last word
        }
        return word.length();
    }
};

