# pull-request-it
Please make as many pull requests on this repo as you can!

Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Tap on a clip to paste it in the text box.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Use the edit icon to pin, add or delete clips.Tap on a clip to paste it in the text box.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Tap on a clip to paste it in the text box.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Tap on a clip to paste it in the text box.Use the edit icon to pin, add or delete clips.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Tap on a clip to paste it in the text box.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Tap on a clip to paste it in the text box.Use the edit icon to pin, add or delete clips.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Use the edit icon to pin, add or delete clips.Welcome to Gboard clipboard, any text that you copy will be saved here.Tap on a clip to paste it in the text box.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.Welcome to Gboard clipboard, any text that you copy will be saved here.Tap on a clip to paste it in the text box.// STYLE
const style = document.createElement("style");
style.textContent = `
  body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: #e5e5e5;
  }

  .scanner {
    background: #111;
    color: #0f0;
    padding: 10px;
    height: 200px;
    overflow-y: auto;
    border-bottom: 3px solid red;
  }

  .scanner h3 {
    color: #fff;
    margin-top: 0;
  }

  .explorer {
    display: flex;
    flex-direction: column;
    background: #fff;
    height: calc(100vh - 200px);
    border-top: 1px solid #ccc;
  }

  .toolbar {
    padding: 5px;
    background: #f1f1f1;
    border-bottom: 1px solid #ccc;
  }

  .toolbar button {
    margin-right: 10px;
  }

  .breadcrumb {
    padding: 10px;
    font-size: 14px;
    color: #555;
    background: #fafafa;
    border-bottom: 1px solid #ddd;
  }

  .files {
    padding: 10px;
    display: flex;
    flex-direction: column;
    gap: 8px;
    overflow-y: auto;
  }

  .file {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 16px;
  }

  .file img {
    width: 24px;
    height: 24px;
  }

  .popup {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: #fff;
    border: 3px solid red;
    padding: 20px;
    z-index: 9999;
    box-shadow: 0 0 15px red;
    text-align: center;
    width: 300px;
  }

  .popup h2 {
    color: red;
    font-size: 20px;
  }

  .popup p {
    margin: 10px 0;
  }

  .popup button {
    padding: 10px 20px;
    font-size: 16px;
    background: red;
    color: white;
    border: none;
    cursor: pointer;
    border-radius: 4px;
  }
`;
document.head.appendChild(style);

// VIRUS SCANNER on top
const scanner = document.createElement("div");
scanner.className = "scanner";
scanner.innerHTML = `<h3>Virus Scanner</h3><div id="log"></div>`;
document.body.appendChild(scanner);

// FILE EXPLORER
const explorer = document.createElement("div");
explorer.className = "explorer";
explorer.innerHTML = `
  <div class="toolbar">
    <button>Organize</button>
    <button>Open</button>
    <button>New Folder</button>
  </div>
  <div class="breadcrumb">Computer > Local Disk (C:) > Users > John</div>
  <div class="files">
    <div class="file"><img src="https://img.icons8.com/windows/32/folder-invoices.png"/> Documents</div>
    <div class="file"><img src="https://img.icons8.com/windows/32/folder-pictures.png"/> Pictures</div>
    <div class="file"><img src="https://img.icons8.com/windows/32/file.png"/> important.docx</div>
    <div class="file"><img src="https://img.icons8.com/windows/32/file.png"/> strange_file.scr</div>
    <div class="file"><img src="https://img.icons8.com/windows/32/folder-music.png"/> Music</div>
  </div>
`;
document.body.appendChild(explorer);

// POPUP
const popup = document.createElement("div");
popup.className = "popup";
popup.innerHTML = `
  <h2>Your device is infected with 918 viruses!</h2>
  <p>Fix them immediately for a smoother experience!</p>
  <a href="https://www.avast.com" target="_blank">
    <button>FIX NOW</button>
  </a>
`;
document.body.appendChild(popup);

// LOGIC
const logContainer = document.getElementById("log");
let virusCount = 0;
const maxViruses = 918;
const virusNames = [
  'Trojan.GenericKD', 'Worm.AutoRun.fg', 'Backdoor.Win32.Pinkslip',
  'Spyware.Agent.AA', 'Rootkit.HiddenProc', 'Adware.PopMe', 
  'PUA.Bundler.Gen', 'Keylogger.TrackMe'
];

function logVirus() {
  if (virusCount >= maxViruses) {
    popup.style.display = "block";
    return;
  }
  const div = document.createElement("div");
  div.textContent = `Detected: ${virusNames[Math.floor(Math.random() * virusNames.length)]} [Threat Level: High]`;
  logContainer.appendChild(div);
  logContainer.scrollTop = logContainer.scrollHeight;
  virusCount++;
  setTimeout(logVirus, 20);
}

logVirus();
