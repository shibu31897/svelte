<script>
	let name='Harshit';
	let age = 30;
	// let upperCaseName not required
	$: upperCaseName = name.toUpperCase();
	$: console.log(age)
	$: if (name == 'Shibu'){
		age = 27;
	}
	function incrementAge(){
		age+=1;
	}

	function changeName(){
		name = 'Shibu';
	}

</script>

<style>
	h1 {
		color: purple;
	}
</style>
<!-- markup -->
<h1>Hello {upperCaseName} aged {age}!</h1>
<button on:click="{incrementAge}">Increase Age</button>
<button on:click={changeName}>Change Name</button>
