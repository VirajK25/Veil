<!DOCTYPE html>
<html lang="en">
<head>

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
