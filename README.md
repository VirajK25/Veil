<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Veil: lock files with your fingerprint. Free and open source.</title>
<meta name="description" content="Veil encrypts files and folders on your Mac with AES-256 and opens them only with Touch ID. Free, open source, no account, no network.">
<meta name="color-scheme" content="light dark">
<link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🔒</text></svg>">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{--bg:#eef1f6;--surface:#fff;--ink:#14213d;--muted:#56657f;--line:#d5dbe6;--accent:#3a5bff;--accent-ink:#fff;--ok:#16805a;--sans:"Bricolage Grotesque",ui-sans-serif,system-ui,-apple-system,"Segoe UI",sans-serif;--mono:"IBM Plex Mono",ui-monospace,SFMono-Regular,Menlo,monospace}
@media(prefers-color-scheme:dark){:root{--bg:#0f1626;--surface:#17203a;--ink:#e8ecf6;--muted:#9aa8c4;--line:#2a3555;--accent:#7f95ff;--accent-ink:#0f1626;--ok:#4cc79b}}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;background:var(--bg);color:var(--ink);font:400 1.0625rem/1.6 var(--sans)}
a{color:inherit}
:focus-visible{outline:3px solid var(--accent);outline-offset:3px;border-radius:4px}
.wrap{max-width:62rem;margin:0 auto;padding:0 1.5rem}
header{display:flex;justify-content:space-between;align-items:center;padding:1.25rem 0}
header b{font-weight:700;font-size:1.25rem}
header nav{display:flex;gap:1.5rem}
header nav a{text-decoration:none;color:var(--muted)}
header nav a:hover{color:var(--ink)}
.hero{display:grid;grid-template-columns:1.1fr 1fr;gap:3rem;align-items:center;padding:3rem 0 4rem}
h1{font-weight:700;font-size:clamp(2.4rem,5.5vw,4rem);line-height:1.05;letter-spacing:-.02em;margin:0 0 1.25rem}
h2{font-weight:700;font-size:1.9rem;letter-spacing:-.01em;margin:0 0 1rem}
.lede{font-size:1.2rem;color:var(--muted);max-width:32rem;margin:0 0 1.75rem}
.btns{display:flex;flex-wrap:wrap;gap:.75rem;margin-bottom:1rem}
.btn{display:inline-block;padding:.8rem 1.4rem;border-radius:999px;font-weight:700;text-decoration:none;border:2px solid var(--ink)}
.btn.primary{background:var(--accent);border-color:var(--accent);color:var(--accent-ink)}
.small{font-size:.9rem;color:var(--muted);margin:0}
.demo{background:var(--surface);border:1px solid var(--line);border-radius:18px;padding:1.5rem;box-shadow:0 20px 50px -30px rgba(20,33,61,.5)}
.row{display:flex;align-items:center;gap:1rem;padding:1rem;border:1px solid var(--line);border-radius:12px}
.row .ico{font-size:1.8rem}
.row .name{font-family:var(--mono);font-size:.95rem;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;flex:1;min-width:0}
.row .name.enc{color:var(--accent)}
.state{margin:1rem 0 1.25rem;color:var(--muted);font-size:.95rem;min-height:1.5em}
.state.ok{color:var(--ok)}
.demo button{font:700 1rem var(--sans);width:100%;padding:.85rem;border-radius:12px;border:0;background:var(--ink);color:var(--bg);cursor:pointer}
section{padding:3rem 0;border-top:1px solid var(--line)}
dl{display:grid;grid-template-columns:14rem 1fr;gap:1.25rem 2rem;margin:0}
dt{font-weight:700}
dd{margin:0;color:var(--muted);max-width:40rem}
.tw{overflow-x:auto}
table{border-collapse:collapse;width:100%;min-width:34rem;background:var(--surface);border:1px solid var(--line);border-radius:12px}
th,td{padding:.8rem 1rem;text-align:left;border-bottom:1px solid var(--line);vertical-align:top}
th{font-weight:700}
td:first-child{color:var(--muted)}
th.us,td.us{background:color-mix(in srgb,var(--accent) 10%,transparent);font-weight:500}
ol{padding-left:1.25rem;max-width:42rem}
li{margin-bottom:.75rem}
code{font-family:var(--mono);font-size:.9em;background:var(--surface);border:1px solid var(--line);padding:.1em .4em;border-radius:6px}
footer{padding:2.5rem 0 3.5rem;color:var(--muted);border-top:1px solid var(--line);font-size:.95rem}
@media(max-width:760px){.hero{grid-template-columns:1fr;gap:2rem}dl{grid-template-columns:1fr;gap:.25rem}dd{margin-bottom:1rem}header nav{gap:1rem}}
</style>
</head>
<body>
<div class="wrap">
<header><b>Veil</b><nav><a href="#compare">Compare</a><a href="#install">Install</a><a href="https://github.com/YOUR_USER/veil">GitHub</a></nav></header>

<main>
<div class="hero">
<div>
<h1>Lock files with your fingerprint. Free, and open to read.</h1>
<p class="lede">Veil encrypts the files and folders you pick, hides them from Finder and Spotlight, and opens them only with Touch ID. It runs entirely on your Mac.</p>
<div class="btns">
<a class="btn primary" href="https://github.com/YOUR_USER/veil/releases/latest/download/Veil.dmg">Download for Mac</a>
<a class="btn" href="https://github.com/YOUR_USER/veil">View the source</a>
</div>
<p class="small">Needs macOS 13 or later. MIT licensed. No account.</p>
</div>

<div class="demo" aria-live="polite">
<div class="row"><span class="ico" aria-hidden="true">📄</span><span class="name" id="fname">Tax-return-2026.pdf</span></div>
<p class="state" id="fstate">Visible in Finder. Anyone using your Mac can open it.</p>
<button id="fbtn" type="button">Lock with Veil</button>
</div>
</div>

<section>
<h2>What it does</h2>
<dl>
<dt>Real encryption</dt><dd>AES-256-GCM with a fresh random key for every item. Tampering or truncation is detected, not ignored.</dd>
<dt>Fingerprint only</dt><dd>Your key is tied to the Secure Enclave and Touch ID. Your Mac login password unlocks nothing.</dd>
<dt>A way back in</dt><dd>A 256-bit recovery key is shown once at setup, with an optional password as a second way in.</dd>
<dt>Locks itself</dt><dd>Re-locks on sleep, screen lock, inactivity or quit. Press ⌃⌥⌘L to lock everything instantly.</dd>
<dt>Verified before deleting</dt><dd>The original is removed only after the encrypted copy is fully read back and every chunk checks out.</dd>
<dt>Nothing leaves your Mac</dt><dd>No account, no cloud, no telemetry. The app contains no network code, and you can read all of it.</dd>
</dl>
</section>

<section id="compare">
<h2>How Veil compares</h2>
<div class="tw"><table>
<thead><tr><th></th><th class="us">Veil</th><th>Cloak</th><th>Shoo!</th></tr></thead>
<tbody>
<tr><td>Price</td><td class="us">Free</td><td>$9.99 to $24.99, one time</td><td>Paid, one time</td></tr>
<tr><td>Source code</td><td class="us">Open, MIT</td><td>Proprietary</td><td>Proprietary</td></tr>
<tr><td>Encrypts files and folders</td><td class="us">Yes</td><td>Yes</td><td>Not listed</td></tr>
<tr><td>Locks apps</td><td class="us">No</td><td>Yes</td><td>Yes</td></tr>
<tr><td>Network use</td><td class="us">None</td><td>License activation and update checks</td><td>Not stated</td></tr>
</tbody></table></div>
<p class="small" style="margin-top:1rem">Based on each product’s public pages in November 2026. Cloak does more today, including apps, websites and schedules. Veil does one job, in the open, for free.</p>
</section>

<section id="install">
<h2>Install</h2>
<ol>
<li>Download <code>Veil.dmg</code> and drag Veil into Applications.</li>
<li>Veil isn’t notarized by Apple, so macOS blocks the first launch. Open Veil once, then go to System Settings, Privacy &amp; Security and click <b>Open Anyway</b>.</li>
<li>Create your vault and store the recovery key somewhere offline.</li>
</ol>
<p class="small">Prefer to build it? Clone the repo and run <code>./build.sh</code>. Every release lists a SHA-256 checksum.</p>
</section>

<section>
<h2>Know the limits</h2>
<dl>
<dt>Not audited</dt><dd>Nobody independent has reviewed Veil yet. Keep backups and read the code before trusting it with anything irreplaceable.</dd>
<dt>Turn on FileVault</dt><dd>Snapshots and Time Machine can keep copies of a file from before you locked it.</dd>
<dt>Unlocked means plaintext</dt><dd>An unlocked item is a normal file until it re-locks.</dd>
</dl>
</section>
</main>

<footer>Veil is free software under the MIT license. <a href="https://github.com/YOUR_USER/veil">Source on GitHub</a>. Not affiliated with Cloak or Shoo!.</footer>
</div>

<script>
(function () {
  var name = document.getElementById('fname'), state = document.getElementById('fstate'), btn = document.getElementById('fbtn');
  var plain = 'Tax-return-2026.pdf', locked = false, busy = false;
  var calm = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  function hex(n) { var s = ''; for (var i = 0; i < n; i++) s += Math.floor(Math.random() * 16).toString(16); return s; }
  function finish() {
    busy = false;
    if (locked) {
      name.textContent = 'a41f9c07e2b83d55c1.veil'; name.className = 'name enc';
      state.textContent = 'Encrypted and gone from Finder. Only your fingerprint brings it back.'; state.className = 'state ok';
      btn.textContent = 'Unlock with Touch ID';
    } else {
      name.textContent = plain; name.className = 'name';
      state.textContent = 'Visible in Finder. Anyone using your Mac can open it.'; state.className = 'state';
      btn.textContent = 'Lock with Veil';
    }
  }
  btn.addEventListener('click', function () {
    if (busy) return;
    locked = !locked; busy = true;
    if (calm) { finish(); return; }
    var steps = 0, t = setInterval(function () {
      name.textContent = hex(plain.length); name.className = 'name enc';
      if (++steps > 12) { clearInterval(t); finish(); }
    }, 50);
  });
})();
</script>
</body>
</html>
