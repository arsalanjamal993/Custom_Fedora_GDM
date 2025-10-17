<h1 align="center">Custom GDM Theme for Fedora & GNOME-Based Systems</h1>

<p align="center">
A sleek, modern, and professional <strong>GDM (GNOME Display Manager)</strong> theme built to enhance the Fedora login and lock screen experience.<br/>
Designed for maintainability, accessibility, and visual harmony.
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT"></a>
  <a href="#"><img src="https://img.shields.io/badge/GNOME-45--47-green.svg" alt="GNOME Versions"></a>
  <a href="#"><img src="https://img.shields.io/badge/Supported%20Distros-Fedora%20%7C%20RHEL%20%7C%20openSUSE-orange.svg" alt="Supported Distros"></a>
</p>

<hr/>

<h2>Project Overview</h2>

<ul>
  <li>Custom <strong>Dark</strong> and <strong>Light</strong> GDM themes</li>
  <li>Complete <code>SCSS</code> source files for customization</li>
  <li>Precompiled <code>.gresource</code> file for quick installation</li>
  <li>Automated build and installation scripts</li>
</ul>

<hr/>

<h2>Prerequisites</h2>

<ul>
  <li>GNOME Shell 45 or higher</li>
  <li><code>glib2</code> and <code>sassc</code> installed</li>
  <li>Administrative privileges (sudo access)</li>
</ul>

<hr/>

<h2>Installation</h2>

<pre><code>git clone https://github.com/&lt;your-username&gt;/gdm-theme.git
cd gdm-theme
chmod +x install.sh
sudo ./install.sh
</code></pre>

<p>
The installer automatically backs up your existing GDM theme before applying the new one.
</p>

<h3>Restart GDM</h3>
<pre><code>sudo systemctl restart gdm
</code></pre>

<hr/>

<h2>Features</h2>

<table>
  <tr>
    <th>Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Dark & Light Variants</td>
    <td>Optimized for both dark and light environments with accessible contrast ratios.</td>
  </tr>
  <tr>
    <td>Simple Installation</td>
    <td>Fully automated installer — no manual file copying required.</td>
  </tr>
  <tr>
    <td>Backup & Restore</td>
    <td>Automatically creates and stores a backup of your original theme for easy rollback.</td>
  </tr>
  <tr>
    <td>Cross-Distro Support</td>
    <td>Compatible with Fedora, RHEL, openSUSE, and other GNOME-based RPM systems.</td>
  </tr>
  <tr>
    <td>Modern GNOME Compatibility</td>
    <td>Tested on GNOME Shell versions 45, 46, and 47.</td>
  </tr>
</table>

<hr/>

<h2>Reverting to Default Theme</h2>

<pre><code>sudo cp /usr/share/gnome-shell/gnome-shell-theme.gresource.backup \
         /usr/share/gnome-shell/gnome-shell-theme.gresource
sudo systemctl restart gdm
</code></pre>

<p>
Backup files are automatically created as <code>gnome-shell-theme.gresource.backup</code> in <code>/usr/share/gnome-shell/</code>.
</p>

<hr/>

<h2>How It Works</h2>

<ol>
  <li><strong>Source Files:</strong> SCSS files in <code>gnome-shell-sass/</code> define the visual styling.</li>
  <li><strong>Build Process:</strong> <code>make_gresource.sh</code> compiles SCSS into a single <code>.gresource</code> file.</li>
  <li><strong>Theme Application:</strong> The compiled file replaces GNOME’s default <code>gnome-shell-theme.gresource</code>.</li>
</ol>

<hr/>

<h2>File Structure</h2>

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

<h2>Development Notes</h2>

<ul>
  <li>Edit <code>.scss</code> files in <code>gnome-shell-sass/</code> to adjust visuals.</li>
  <li>Rebuild using:
    <pre><code>./make_gresource.sh</code></pre>
  </li>
  <li>Test changes in a live GNOME Shell session before deploying to GDM.</li>
</ul>

<hr/>

<h2>Screenshots</h2>

<p align="center">
  <img src="screenshots/dark-preview.png" width="48%" alt="Dark Theme Preview">
  <img src="screenshots/light-preview.png" width="48%" alt="Light Theme Preview">
</p>

<hr/>

<h2>Compatibility</h2>

<table>
  <tr>
    <th>Distro</th>
    <th>Status</th>
    <th>GNOME Version</th>
  </tr>
  <tr>
    <td>Fedora 40+</td>
    <td>Tested</td>
    <td>45–47</td>
  </tr>
  <tr>
    <td>RHEL 9</td>
    <td>Compatible</td>
    <td>45</td>
  </tr>
  <tr>
    <td>openSUSE Tumbleweed</td>
    <td>Tested</td>
    <td>46</td>
  </tr>
</table>

<hr/>

<h2>License</h2>
<p>This project is released under the <strong>MIT License</strong>. You are free to use, modify, and distribute it with proper attribution.</p>

<hr/>

<h2>Contributions</h2>
<p>
Contributions, bug reports, and pull requests are welcome.<br/>
To improve the design, fix bugs, or add variants, please open an issue or PR on GitHub.
</p>

<hr/>

<h2>Author</h2>
<p>
Developed by <strong>Arsalan Jamal</strong> — passionate about Linux, UI design, and crafting clean, open-source experiences.
</p>
