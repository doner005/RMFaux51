---


---

<h2 id="fm190w-gl-to-rm551e-gl-firmware-conversion-guide">FM190W-GL to RM551E-GL firmware conversion guide</h2>
<p><strong>Requirements</strong></p>
<ul>
<li>Fibocom FM190W-GL modem</li>
<li>m.2 adapter with usb</li>
<li>PC with windows</li>
<li>Fibocom <a href="https://www.dropbox.com/scl/fi/veni1yp97axjrp10dn46y/FbUSBDeviceSetup_v2.1.2.5-2.7z?rlkey=dtbw82bb5qjhjd1y71q0z62bz&amp;st=3cby476k&amp;dl=0">usb drivers</a></li>
<li>Quectel <a href="https://mega.nz/file/bdUWiKSQ#7RPymUcm7Rgdjf9mRsWjuf9zXia5qxV7NZWMLruvb5A">Qflash</a> software</li>
<li>Quectel RM551E-GL <a href="https://mega.nz/file/aAdVHTST#dOzRfehUUbcUFH3Yoo-n58m68wgHcEXhcnKYuo2nMo4">firmware</a></li>
<li><a href="https://www.dropbox.com/scl/fi/jzxgl5vft4xjsbssrauwa/QPST_2.7.496.zip?rlkey=4ue2vbdtq2o4kd0k0r06kg9ga&amp;st=o3r9rkht&amp;dl=0">QPST software</a></li>
<li>RM551 .xqcn restore <a href="https://www.dropbox.com/scl/fi/7fkljc2ayfibegclcqq6l/551.xqcn?rlkey=m89k76e7gxue54fmdk27goplw&amp;st=254l7diw&amp;dl=0">file</a></li>
</ul>
<h2 id="firmware-flashing-process">Firmware Flashing Process</h2>
<p>Make sure you have downloaded and installed all software and drivers from requirements section above.</p>
<ul>
<li>Plug modem into PC via usb and open device manager. If the Fibocom usb drivers have been installed successfully, you should see <strong>”Ports”</strong> populate in your device manager list a few seconds after plugging in the modem. Click on ports to reveal the list of all available modem ports. Make note of the number of your <strong>Diagnotics/DM port</strong>. This is the port we are going to use to flash the firmware.</li>
<li>Open <strong>Qflash</strong>  software, select the <strong>COM port</strong> number that corresponds with the <strong>Diagnostics/DM port</strong> from device manager and set <strong>Baudrate</strong> to 460800.</li>
<li>Click <strong>Load FW Files</strong> and navigate to where you have the RM551 firmware update folder saved.</li>
<li>The file you need is located at <strong>update&gt;firehose&gt;</strong>  prog_firehose_sdx7x.elf</li>
<li>Click <strong>Start</strong> once the progress bar finishes the modem is now flashed with Quectel firmware.</li>
</ul>
<h2 id="nv-restore-process">NV Restore Process</h2>
<ul>
<li>Make sure Qflash is closed and modem is still plugged in.</li>
<li>Open <strong>QPST software</strong></li>
<li>I’m linking this <a href="https://www.dropbox.com/scl/fi/pofi5g7lz3jcelh6howwx/Qpst-Restore-QCN-20191206.pdf?rlkey=myqimvlsh3a54qy0pbau3bhqo&amp;st=uet6w623&amp;dl=0">guide</a> to help you follow along with the instructions.</li>
<li>If the DM port isn’t automatically detected by QPST, select <strong>Add New Port</strong> from the <strong>Ports</strong> tab.</li>
<li>Under the <strong>Start Clients</strong> menu, select <strong>Software Download</strong></li>
<li>Select the <strong>Restore</strong> tab, make sure your <strong>Diagnostics/DM port</strong> is selected and load in the RM551 <strong>.xqcn</strong> file that you saved.</li>
<li>Make sure Allow ESN mismatch is selected and click <strong>Start</strong></li>
<li>Wait until status says **Memory Restore **</li>
</ul>
<h2 id="congratulations-you-are-now-the-proud-owner-of-an-rmfaux51">Congratulations you are now the proud owner of an RMFaux51</h2>

