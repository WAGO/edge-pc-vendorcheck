<p align="left">
<img src="images/wago.png"
     alt="wago logo"
     title="wago logo"/>

# Debian package to activate CoDeSys [WAGO] libraries on the Edge Computer
- Debian Package for Edge PC equals 752-94xx<br>
- Working for nativ and virtual CoDeSys Runtimes<br><br>

</p>
<p align="left">
<img src="images/Edge-PC.jpg"
     alt="Edge-PC"
     title="Edge-PC"/>
</p>
- Howto use<br><br>

1.  Open ssh connection, use putty or integratet terminal inside cockpit<br>
1a. On older devices <FW4 please install "sudo":<pre><code>apt-get install sudo</code></pre>
2.  Goto home folder: <pre><code>cd /home</code></pre>
3.  If you device had internet access, download the package direct to your device:<br>
3a. Download directly: <pre><code>wget https://github.com/WAGO/edge-pc-vendorcheck/raw/main/debian%20package/vendorcheck-0.1.3.deb</code></pre>
3b. If not, download from repo via Laptop and copy package via scp to the home folder<br>
4.  Install package: <pre><code>apt-get install /home/vendorcheck-0.1.3.deb</code></pre>  <H4>OR</h4>  <pre><code>dpkg -i /home/vendorcheck-0.1.3.deb</code></pre>
5.  Check installation: <pre><code>apt list | grep vendorcheck</code></pre> <H4>OR</h4>  <pre><code>dpkg -l | grep vendorcheck</code></pre>
6.  Check service is running: <pre><code>systemctl status vendor_daemon.service</code></pre>

7. In case of use a virtual runtime<br>
7a.  Mount "tmp" folder to your docker container: <H4>/tmp:/tmp,</H4><br>
7b.  (re)start your container via CoDeSys IDE<br>

</p>
<p align="left">
<img src="images/CAA.jpg"
     alt="CAA"
     title="CAA"/>
</p>

8. In case of use a nativ runtime<br>
8a. Restart your runtime: <pre><code>/etc/init.d/codesyscontrol restart</code></pre>
9.  Dowload CoDeSys library from this repo and install inside your IDE<br>
https://github.com/WAGO/edge-pc-vendorcheck/tree/main/codesys%20library<br>
10. Use the library inside your CoDeSys project
<br><br>
- If you like to uninstall the package:<br>
<pre><code>dpkg -r vendorcheck</code></pre>


