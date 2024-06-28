# 27/06/2024

1. Learnt how to use git commands and created a branch in the forked repo.
2.  Started learning simple markdown commands.
3. Started with the edx coursework! 


### EDX Notes
#### Learning TL-Verilog in makerchip.com website

1. TL-Verilog Syntax for each op:
	1.  ![[Pasted image 20240628220510.png]]
2. ![[Pasted image 20240628221928.png]]
3. ![[Pasted image 20240628221949.png]]
4. ![[Pasted image 20240628222136.png]]
5. Other vector operators are supported, including comparison operators like  ==, !=, >, >=, <, <=. We will only cover the operators needed for this course.

#### NOTE:
you will, as a convenience, not bother declare the input vectors. As such, there is no definition of their width. In this circumstance, you can define their widths by using bit ranges on the right-hand side as such:
$out[7:0] = $in1[6:0] + $in2[6:0];

Values of vector signals are represented in the waveform viewer in hexadecimal. There are many online conversion tools, such as [[https://www.rapidtables.com/convert/number/hex-to-decimal.html]] if you need help finding a decimal or binary equivalent.


6. ![[Pasted image 20240628223718.png]] 
##### A simple 2:1 MUX implementation

7. Verilog provides 6 syntaxes for coding a mux, but TL-verilog favors ternary operators.
		EX: ```
```bash
$out = $sel ? $in1 : $in0;
```

An example that implements ternary operators chained to form a 8:1 MUX (here, ```$in0, $in1, $in2, $in3 ``` must be 8-bit vectors.)


```bash
$out[7:0] =  
   $sel[3]  
      ? $in3 :  
   $sel[2]  
      ? $in2 :   $sel[1]  
      ? $in1 :  
   //default  
        $in0;
```

![[Pasted image 20240628224601.png]]

