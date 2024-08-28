<script>
	let name='Harshit';
	let age = 30;

	function incrementAge(){
		age+=1
	}

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name} aged {age}!</h1>
<button on:click="{incrementAge}">Increase Age</button>
