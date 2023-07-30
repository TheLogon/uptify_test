<template>
	<div>
		<the-header />
		<div class="home">
			<div class="container">
				<div class="home__inner">
					<div class="home__top">
						<h1 class="home__title">Start connecting your world</h1>
						<p class="home__subtitle">Save time and money by making the internet work for you! We believe you might like...</p>
					</div>
					<div class="home__search">
						<button class="home__search_btn">
							<img src="/images/icons/search.svg" alt="" />
						</button>
						<input type="text" placeholder="Search Services" class="home__search_input" name="search" />
					</div>
				</div>
				<the-services />
				<the-form />
			</div>
		</div>
	</div>
</template>
