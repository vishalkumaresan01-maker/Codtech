module RAM_tb;

reg clk, we;
reg [2:0] addr;
reg [7:0] din;
wire [7:0] dout;

RAM uut (.clk(clk), .we(we), .addr(addr), .din(din), .dout(dout));

always #5 clk = ~clk;

initial begin
    clk = 0;
    we = 1;

    addr = 3'b001; din = 8'b10101010; #10;
    addr = 3'b010; din = 8'b11001100; #10;

    we = 0;
    addr = 3'b001; #10;
    addr = 3'b010; #10;

    $stop;
end

endmodule
