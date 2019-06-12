# IOLO-crackme & Bomblab. My take on finding the exploits on UCR CS 165 Security Instructor:Zhiyun Qian

Crackme
0x00
Answer:250382
*simple x/s addr
*tbreak *0x0804845b

0x01
Answer:5274
*look at hexadecimal value 0x149a

0x02
Answer:338724
*look at 0x8[ebp] = eax; result is stored

0x03
Answer:338724
*arguments are passed in "test"
*shift-> decodes string
*void shift(const char *str) { char buf[120]; size_t i;

for (i = 0; i < strlen(str); i++) { buf[i] = str[i] - 3;
}
buf[i] = 0;
printf("%s", buf); 
}

0x04
Answer: Any number that can be broken up and add up to 15.
*example 771-> 7+7+1=15
*look at check function to see how string input is the sum of digits and equal to 0xf.

0x05
Answer: even number that is equal to 16.
*similar to previous
*parell is input string that checks while input to see if its even

0x06
Answer:LOLO 16
*env variable + 0x05

bomblab
1.What is your mother's maiden name?
2.paper
3.P@s$wOrd (case sensitive)
4.six numbers : where first value is greater than 0. and then adds to it(loop)
