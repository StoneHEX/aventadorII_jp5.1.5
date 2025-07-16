# aventadorII_jp5.1.5

JETPACK 5.1.5 build system for AventadorII.<br>
The <b>compile_kernel</b> script creates a new kernel with camera, spi can and audio.<br><br>
This script download the compiler if not available and all the requested modules.<br>
The devel machine must have a running http server.<br>
The <b>aventadorII_flash</b> flashes the newly created kernel and modules on the AventadorII Orin module.<br>
In order to downgrade a previously installed JP6 from $JETPACK you can issue :<br>
<b> sudo ./flash.sh -c ./bootloader/t186ref/cfg/flash_t234_qspi.xml jetson-orin-nano-devkit mmcblk0p1</b>
where $JETPACK is, for example, <sdk_manager_installation_path>/JetPack_5.1.5_Linux_JETSON_ORIN_NX_TARGETS/Linux_for_Tegra


