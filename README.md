# Aim
To Stimulate and Synthesis JK FLIP FLOP using Vivado.
# Software Required
Vivado
# JK_FLIPFLOP
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/094e9d55-5f30-4984-90b9-dd51d5297974)
# Circuit Diagram
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/5b973ee8-9ee2-402d-8cba-1adfa2e4d5f2)
# Truth Table
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/04d4ff52-ae20-4e08-bd70-58137b129890)
# Program
```
module JK_flipflop (q, q_bar, j,k, clk, reset);
  input j,k,clk, reset;
  output reg q;
  output q_bar;
  
  always@(posedge clk) begin 
    if(!reset)        q <= 0;
    else 
  begin
      case({j,k})
        2'b00: q <= q;  
        2'b01: q <= 1'b0; 
        2'b10: q <= 1'b1; 
        2'b11: q <= ~q; 
      endcase
    end
  end
  assign q_bar = ~q;
endmodule
```
# Output
![jk flip flop](https://github.com/j-gugan/JK_FLIPFLOP/assets/163828735/5eb8b556-06a0-46b2-bf87-565ba9676758)
# Result
Thus,JK FLIP FLOP using Vivado is simulated and synthesised.
