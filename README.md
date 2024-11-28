# THE-VERILOG-CODE-FOR-AND-GATE-WITH-TESTBENCH

TESTBENCH:
// step1 write the module without port
module tb;
  //step2 input of dut -reg,output-
  reg a,b;
  wire y;
  //step3 dut inetantion
  and_gate dut(a,b,y);//positional port mapzing
  //step 4 stimuli generation
  initial
    begin
      a=1'b0 ; b=1'b0;
   #2 a=1'b0 ; b=1'b1;
   #2 a=1'b1 ; b=1'b0; 
   #2 a=1'b1 ; b=1'b1;
    end
  //step5 capturing the output
  initial
    begin
      $monitor("a=%b  b=%b  y=%b",a,b,y);
    end
endmodule
