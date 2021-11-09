<template>
	<div class="flex items-end  h-full pb-[1rem]">
		<div class="flex w-full justify-around">

			<label class="flex flex-col">
				<div class="flex flex-col">
					<span class="text-green-500" v-if="isOK">Congratulation!</span>
					<span>Input here: "{{validPhrase}}"</span> 
				</div>
				<input v-model="userInput" class="focus:outline-none w-[15rem] border rounded pl-[.5rem] border-blue-700" 
				type="text" placeholder="Type here">
			</label>
			<button  
			:disabled="isInValid"
			@click="isOK = !isOK"
			class="flex flex-grow-1 self-center focus:outline-none border py-[1rem] px-[2rem] rounded border-blue-700 text-blue-700 disabled:(opacity-50 cursor-not-allowed)">OK</button>
		</div>
	</div>
</template>

<script>
export default{
	props: {
		validPhrase: {
			type: String,
			required: true,
		}
	},
	data() {
		return{
			userInput: '',
			isOK: false,
		}
	},
	computed: {
		isInValid() {
			if(this.validPhrase === this.userInput){
				return false
			} else {
				return true
			}
			
		}
	}
}
</script>