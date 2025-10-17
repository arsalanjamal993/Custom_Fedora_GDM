<h1 align="center">Custom GDM Theme for Fedora & GNOME-Based Systems</h1>

<p align="center">
A sleek, modern, and professional <strong>GDM (GNOME Display Manager)</strong> theme designed to enhance the Fedora login and lock screen experience.  
Built with maintainability, accessibility, and visual balance in mind.
</p>

<hr/>

<h2>📁 Project Overview</h2>

<ul>
  <li>Custom <strong>Dark</strong> and <strong>Light</strong> GDM themes</li>
  <li>Complete <code>SCSS</code> source files for customization</li>
  <li>Precompiled <code>.gresource</code> file for quick installation</li>
  <li>Automated build and installation scripts</li>
</ul>

<hr/>

<h2>🧩 Features</h2>

<table>
  <tr>
    <th>Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Dark & Light Variants</td>
    <td>Designed for clarity and accessibility across all lighting conditions.</td>
  </tr>
  <tr>
    <td>Simple Installation</td>
    <td>Quick setup with included scripts — no manual steps required.</td>
  </tr>
  <tr>
    <td>Backup & Restore</td>
    <td>Automatically creates a backup of your original theme before applying changes.</td>
  </tr>
  <tr>
    <td>Cross-Distro Support</td>
    <td>Compatible with Fedora, RHEL, openSUSE, and other GNOME-based RPM distributions.</td>
  </tr>
  <tr>
    <td>Modern GNOME Compatibility</td>
    <td>Tested on GNOME versions 45, 46, and 47.</td>
  </tr>
</table>

<hr/>

<h2>⚙️ Installation</h2>

<pre><code>git clone https://github.com/&lt;your-username&gt;/gdm-theme.git
cd gdm-theme
chmod +x install.sh
sudo ./install.sh
</code></pre>

<p>
The installer automatically backs up your original GDM theme before applying the new one.
</p>

<h3>Restart GDM</h3>
<pre><code>sudo systemctl restart gdm
</code></pre>

<hr/>

<h2>🔄 Reverting to Default Theme</h2>

<pre><code>sudo cp /usr/share/gnome-shell/gnome-shell-theme.gresource.backup \
         /usr/share/gnome-shell/gnome-shell-theme.gresource
sudo systemctl restart gdm
</code></pre>

<hr/>

<h2>🧠 How It Works</h2>

<ol>
  <li><strong>Source Files:</strong> SCSS files in <code>gnome-shell-sass/</code> define the interface styling.</li>
  <li><strong>Build Process:</strong> The <code>make_gresource.sh</code> script compiles SCSS into a single <code>.gresource</code> file.</li>
  <li><strong>Theme Application:</strong> The compiled file replaces GNOME’s default <code>gnome-shell-theme.gresource</code>.</li>
</ol>

<hr/>

<h2>📂 File Structure</h2>

<pre><code>gdm-theme/
├── gnome-shell-sass/
│   ├── _colors.scss
│   ├── _widgets.scss
│   └── widgets/
├── theme/
├── make_gresource.sh
├── install.sh
└── gnome-shell-theme.gresource.xml
</code></pre>

<hr/>

<h2>🧾 Development Notes</h2>

<ul>
  <li>Edit <code>.scss</code> files in <code>gnome-shell-sass/</code> to customize visuals.</li>
  <li>Rebuild using:
    <pre><code>./make_gresource.sh</code></pre>
  </li>
  <li>Test changes in a GNOME Shell session before applying them to GDM.</li>
</ul>

<hr/>

<h2>🖼️ Screenshots</h2>

<p align="center">Add your screenshots here (before and after).</p>

<hr/>

<h2>🧩 Compatibility</h2>

<table>
  <tr>
    <th>Distro</th>
    <th>Status</th>
    <th>GNOME Version</th>
  </tr>
  <tr>
    <td>Fedora 40+</td>
    <td>✅ Tested</td>
    <td>45–47</td>
  </tr>
  <tr>
    <td>RHEL 9</td>
    <td>⚙️ Compatible</td>
    <td>45</td>
  </tr>
  <tr>
    <td>openSUSE Tumbleweed</td>
    <td>✅ Tested</td>
    <td>46</td>
  </tr>
</table>

<hr/>

<h2>📜 License</h2>
<p>This project is released under the <strong>MIT License</strong>. You are free to use, modify, and distribute it with proper attribution.</p>

<hr/>

<h2>🙌 Contributions</h2>
<p>
Contributions, bug reports, and pull requests are welcome.  
If you’d like to improve the design or add new theme variants, please submit a pull request or open an issue.
</p>

<hr/>

<h2>🧭 Author</h2>
<p>
Developed by <strong>Arsalan Jamal</strong> — passionate about Linux, UI design, and clean open-source projects.
</p>

<style>
table {
  border-collapse: collapse;
  width: 100%;
}
th, td {
  border: 1px solid #ccc;
  padding: 8px 12px;
  text-align: left;
}
th {
  background-color: #f5f5f5;
}
code {
  background-color: #f4f4f4;
  padding: 2px 5px;
  border-radius: 3px;
}
pre {
  background-color: #f8f8f8;
  border: 1px solid #ddd;
  padding: 10px;
  border-radius: 4px;
}
h1, h2, h3 {
  color: #333;
}
</style>
