basic-calculator/
│
├── index.html         ← (from task 2.txt)
├── styles.css         ← (you need to include this if not provided)
├── script.js          ← (you need to include this if not provided)
├── README.md          ← (project info)
└── LICENSE            ← (optional)
# Basic Calculator

This is a simple, responsive calculator built using HTML, CSS, and JavaScript. It includes a clean user interface with number and operator buttons, real-time input display, and basic arithmetic operations like addition, subtraction, multiplication, and division. The calculator also supports clearing and backspace functions. Ideal for learning basic DOM manipulation and event handling, this project is perfect for beginners exploring frontend web development.

code here -

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Basic Calculator</title>
    <link rel="stylesheet" href="styles.css" />
</head>
<body>
    <div class="calculator">
        <input type="text" class="display" id="display" disabled />
        <div class="buttons">
            <button class="btn" data-action="clear">C</button>
            <button class="btn" data-action="backspace">⌫</button>
            <button class="btn" data-action="divide">÷</button>
            <button class="btn" data-action="multiply">×</button>

            <button class="btn" data-number="7">7</button>
            <button class="btn" data-number="8">8</button>
            <button class="btn" data-number="9">9</button>
            <button class="btn" data-action="subtract">−</button>

            <button class="btn" data-number="4">4</button>
            <button class="btn" data-number="5">5</button>
            <button class="btn" data-number="6">6</button>
            <button class="btn" data-action="add">+</button>

            <button class="btn" data-number="1">1</button>
            <button class="btn" data-number="2">2</button>
            <button class="btn" data-number="3">3</button>
            <button class="btn equal" data-action="equals">=</button>

            <button class="btn zero" data-number="0">0</button>
            <button class="btn" data-number=".">.</button>
        </div>
    </div>
    <script src="script.js"></script>
<!-- Code injected by live-server -->
<script>
	// <![CDATA[  <-- For SVG support
	if ('WebSocket' in window) {
		(function () {
			function refreshCSS() {
				var sheets = [].slice.call(document.getElementsByTagName("link"));
				var head = document.getElementsByTagName("head")[0];
				for (var i = 0; i < sheets.length; ++i) {
					var elem = sheets[i];
					var parent = elem.parentElement || head;
					parent.removeChild(elem);
					var rel = elem.rel;
					if (elem.href && typeof rel != "string" || rel.length == 0 || rel.toLowerCase() == "stylesheet") {
						var url = elem.href.replace(/(&|\?)_cacheOverride=\d+/, '');
						elem.href = url + (url.indexOf('?') >= 0 ? '&' : '?') + '_cacheOverride=' + (new Date().valueOf());
					}
					parent.appendChild(elem);
				}
			}
			var protocol = window.location.protocol === 'http:' ? 'ws://' : 'wss://';
			var address = protocol + window.location.host + window.location.pathname + '/ws';
			var socket = new WebSocket(address);
			socket.onmessage = function (msg) {
				if (msg.data == 'reload') window.location.reload();
				else if (msg.data == 'refreshcss') refreshCSS();
			};
			if (sessionStorage && !sessionStorage.getItem('IsThisFirstTime_Log_From_LiveServer')) {
				console.log('Live reload enabled.');
				sessionStorage.setItem('IsThisFirstTime_Log_From_LiveServer', true);
			}
		})();
	}
	else {
		console.error('Upgrade your browser. This Browser is NOT supported WebSocket for Live-Reloading.');
	}
	// ]]>
</script>
</body>
</html>
