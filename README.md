# aventadorII_jp5.1.5
# JETPACK 5.1.5 build system for AventadorII
# Prerequisites
The scripts in this repo run on a completely running sdkmanager created system and modify the standard sdkmanager installed system to include some new drivers described below.<br>
If you plan to use both NANO and NX modules you have to install both targets.<br>
# Installation notes
Download or clone the repo and expand in the <sdk_manager_installation_path> ( the one where you find JetPack_5.1.5_Linux_JETSON_ORIN_NX_TARGETS or JetPack_5.1.5_Linux_JETSON_ORIN_NANO_TARGETS directories)<br><br>
# How to use<br>
The <b>compile_kernel</b> script creates a new kernel with camera, spi can and audio as separately loadable overlays.<br>
Example : <br>
<b>./compile_kernel ORIN_NX</b> creates a ORIN NX kernel <br>
<b>./compile_kernel ORIN_NANO</b> creates a ORIN NANO kernel <br><br>
This script download the compiler if not available and all the requested modules.<br><br>
The <b>./aventadorII_flash ORIN_NX</b> flashes the newly created kernel and modules on the AventadorII Orin NX module.<br>
The <b>./aventadorII_flash ORIN_NANO</b> flashes the newly created kernel and modules on the AventadorII Orin NANO module.<br><br>
# Additional Notes
In order to downgrade a previously installed JP6 from $JETPACK you can issue :<br>
<b> sudo ./flash.sh -c ./bootloader/t186ref/cfg/flash_t234_qspi.xml jetson-orin-nano-devkit mmcblk0p1</b>
where $JETPACK is, for example:<br>
<sdk_manager_installation_path>/JetPack_5.1.5_Linux_JETSON_ORIN_NX_TARGETS/Linux_for_Tegra<br>
# SanDisk on board disk
AventadorII can be equipped with an on board PCIe disk up to 1TB.<br>
The disk is connected to the PCIe1 bus, on the two lanes available.<br>
The folder <b>Sandisk</b> contains the test script using fio and the results on a 256GB disk.<br>
The system must have a JetPack 5.1.5 installed on the M.2 disk and the tests are done on the whole Sandisk disk.<br>
To run the tests the command is:<br>
<b>sudo fio <test_name></b>



