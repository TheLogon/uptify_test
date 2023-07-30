<template>
	<div class="home__form">
		<div class="home__form_top">
			<h2 class="home__form_title">Suggest Your own Integration</h2>
			<button class="home__form_btn">Close</button>
		</div>
		<div class="home__form_inputs">
			<div class="home__form_wrapper">
				<label class="home__form_label">Integration name:</label>
				<input type="text" name="text" placeholder="Type Web Service name here..." class="home__form_input" />
			</div>
			<div class="home__form_wrapper">
				<label class="home__form_label">Triggers that you wanna have:</label>
				<input type="text" name="text" placeholder="Type here triggers that you wanna use..." class="home__form_input" />
			</div>
		</div>
		<button class="home__form_submit">Submit</button>
	</div>
</template>

<script>
	export default {
		name: "form",
	}
</script>

<style></style>
