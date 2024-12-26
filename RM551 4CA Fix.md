---


---

<p>**</p>
<h2 id="rm551-4ca-fix">RM551 4CA Fix</h2>
<p>This guide will help you load a new carrier aggregation file into the file system of your modem if you are having trouble aggregating 4 5g channels on T-Mobile’s SA 5g network. Typically this happens on towers equipped with Nokia antennas.</p>
<p><strong>Requirements</strong></p>
<ul>
<li><a href="https://www.dropbox.com/scl/fi/jzxgl5vft4xjsbssrauwa/QPST_2.7.496.zip?rlkey=4ue2vbdtq2o4kd0k0r06kg9ga&amp;st=9sv0ts85&amp;dl=0">QPST Software</a></li>
<li><a href="https://www.dropbox.com/scl/fi/f250bpn68op6l6z8bpzu7/plmn2cacombos_nr.mdb?rlkey=he8nitlsheeifk5n050fd6v6e&amp;st=30rkizcj&amp;dl=0">Carrier Aggregation File</a></li>
</ul>
<h2 id="file-loading-process">File Loading Process</h2>
<ul>
<li>Open QPST with your modem plugged into your PC and make sure you have added the Diagnostic/DM Port.</li>
<li>Click <strong>Start Clients</strong> from the top menu and open <strong>EFS Explorer</strong>.</li>
<li>Expand the <strong>mdb</strong> folder and click on the <strong>nr</strong> folder</li>
<li><em>On the right side of EFS Explorer, you will see the current .mdb files located inside this folder</em></li>
<li>Now drag and drop the <strong>Carrier Aggregation File</strong> from the requirements section into this folder.</li>
<li><a href="https://www.dropbox.com/scl/fi/l8kqg94f52p3anedlsp88/IMG_5581.JPG?rlkey=ckidq4119p4it96fpfgu49hxo&amp;st=6u3akdrq&amp;dl=0">Here</a> is a picture to help you visualize what you are doing.</li>
</ul>
<h2 id="deleting-carrier-aggregation-file">Deleting Carrier Aggregation File</h2>
<p>Always give the modem a few reboot cycles if you are having connection issues after the new .mdb file before resorting to deleting. This file does not work for all towers. It was made by Quectel for a customer using a tower with Nokia antennas and their specific tower logs in mind.</p>
<p><strong>Process to Delete</strong></p>
<ul>
<li>Open Qnavigator or any command terminal to run AT commands and issue <strong>AT+CFUN=0</strong> command</li>
<li>Now issue <strong>AT+QNVFD="/mdb/nr/plmn2cacombos_nr.mdb"</strong> in a command terminal.</li>
<li>Now reboot with <strong>AT+CFUN=1,1</strong></li>
<li>After reboot confirm CFUN is set to 1 by sending <strong>AT+CFUN?</strong> command.</li>
<li>If modem returns 0, send <strong>AT+CFUN=1</strong></li>
</ul>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

