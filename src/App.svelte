<script>
	import ContactCard from "./ContactCard.svelte";
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

	function nameInput(event) {
		const enteredValue = event.target.value;
		name = enteredValue;
	}

</script>

<style>
	h1 {
		color: purple;
	}
</style>̀
<!-- markup -->
<h1>Hello {upperCaseName} aged {age}!</h1>
<button on:click="{incrementAge}">Increase Age</button>
<!-- <button on:click={changeName}>Change Name</button> -->
 <!-- <input value="{name}" on:input="{nameInput}"> to achive this 2 way binding we can use -->
 <input type="text" bind:value={name}>
 <ContactCard userName=name jobTitle='SDE-1' description="Some story"/>