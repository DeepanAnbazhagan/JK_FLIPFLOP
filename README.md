# JK_FLIPFLOP
# AIM:
To simulate and synthesis JK FLIPFLOP using Vivado software.
# APPARATUS REQUIRED:
Vivado 2023.1 software.
# Pin Diagram:
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/094e9d55-5f30-4984-90b9-dd51d5297974)
# Circuit Diagram
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/5b973ee8-9ee2-402d-8cba-1adfa2e4d5f2)
# Truth Table
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/04d4ff52-ae20-4e08-bd70-58137b129890)
# Program:
     module jk_ff (q, q_bar, j,k, clk, reset);        
  input j,k,clk, reset;
  output reg q;
  output q_bar;
  always@(posedge clk) begin
    if(!reset)
      q <= 0;
    else 
  begin
      case({j,k})              
      2'b00: q <= q; // No change
      2'b01: q <= 1'b0; // reset
      2'b10: q <= 1'b1; // set
      2'b11: q <= ~q; // Toggle                       
      endcase
    end
  end
  assign q_bar = ~q;
endmodule

# Elaborated Design:
<img width="960" alt="Screenshot 2024-03-30 115309" src="https://github.com/DeepanAnbazhagan/JK_FLIPFLOP/assets/164902865/5d75ac70-3177-49bb-9919-ab572e93b0dd">

# Output: 
<img width="960" alt="Screenshot 2024-03-30 115237" src="https://github.com/DeepanAnbazhagan/JK_FLIPFLOP/assets/164902865/b37d6d59-9f11-4a65-b255-db459cce9227">

# RESULT:
Thus the simulate and synthesis of JK FLIPFLOP is verified successfully by using Vivado software.


