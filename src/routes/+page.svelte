<script>
	async function getClicked() {
		
		let input = document.getElementById("input-selector")
		let p = document.getElementById("hiddens") 

		if (input.value != null) {
			if (input.value == "SOME-COOL-SENTENCES") {
				p.textContent = "console:  SOME-COOL-HINTS"
			} else {
				p.textContent = "console: There is an error while verifying your verification 2FA Code. please try again."
			}
		}
	}

	async function onEnter(e) {
		if (e.key == "Enter") {
			getClicked()
		}
	}
</script>
<h1>Nitro For Christmas!</h1>
<div>
	<input type="text" id="input-selector" placeholder="입력하세요!" on:keydown={onEnter}>
	<button id="btn1"  on:click={getClicked}>제출</button>
	<div id="console">
		<h2>Console</h2>
		<p id="hiddens"></p>
	</div>
</div>

<style>
	h1 {
		color: rgb(22, 199, 75);
		font-size: 2.2em;
		text-align: center;
		text-decoration: solid;
	}
	h2 {
		margin-top: 1px;
		color: rgb(22, 55, 199);
		margin-bottom: 2px;
	}
	#console {
		border-radius: 5px; 
  		border: 3px solid rgb(22, 55, 199);
		margin-top: 10px;
		height: 100px;
	}
	input {
		width: 99.5%;
		height: 35px;
		margin-bottom: 5px;
		border-radius: 5px; 
  		border: 2px solid rgb(22, 55, 199);
	}
	button {
		background-color: rgb(22, 55, 199);
		border-radius: 5px; 
  		border: 2px solid rgb(22, 55, 199);
		font-size: 1.2em;
		color: white;
		width: 100%;
		height: 40px;
	}
	button:hover {
		background-color: rgb(55, 79, 184);
	}
	p {
		margin-top: 2px;
	}
</style>


