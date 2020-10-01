FPGA Labview Library Usage:

Setting Chip Select Pins:
1.) Navigate to SPI/SPI_CS.vi
2.) Select the device in the outer case structure
3.) Select the MXP port (A or B) in the inner case structure
4.) Edit the FPGA I/O constant to the desired port

Setting SPI Pins:
1.) Navigate to SPI/SPI_RW_A.vi or SPI/SPI_RW_B.vi depending on which MXP port you want to configure
2.) Find the cluster constant in the bottom left corner of the VI block diagram
3.) Change the MISO/MOSI/SCLK FPGA I/O constants to the desired ports

Setting SPI Frequencies:
1.) Navigate to SPI/SPI_FREQ.vi
2.) Select the device in the case structure
3.) Enter the desired SPI SCLK frequency for that device (in KHz)

VESC:
1.) Call VESC/startVESC.vi with desired CAN rate and MXP port
	Note: Selection of CAN rates has been reduced to save FPGA space
	Additional CAN rate options can be added if needed
2.) Pass the SPI Config Out to VESC/writeVESC.vi and call