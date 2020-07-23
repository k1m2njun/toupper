#include <cs50.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main(void)
{
    //문자열을 입력받는다
    string s = get_string("Before: ");
    
    //After 출력
    printf("After:  ");
    
    //입력받은 문자열(s)의 길이(strlen)만큼
    for (int i = 0, n = strlen(s); i < n; i++)
    {
        //문자열이 'a'이상 그리고 'z'이하라면(c)
        if (s[i] >= 'a' && s[i] <= 'z')
        {
            //각 문자에서 32를 빼고 문자(c)로 출력해라(ASCII 코드)
            printf("%c", s[i] - 32);
        }
        else
        {
            //아니면 그냥 출력
            printf("%c", s[i]);
        }
        
        
        
            //위 if의 기능은 toupper로 대신할 수 있다(ctype.h)
            printf("%c", toupper(s[i]));
    }
    printf("\n");
}
