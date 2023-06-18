<script>
	import { AppBar, AppShell } from '@skeletonlabs/skeleton';
	let output_title = "Rick Astley - Never Gonna Give You Up (Official Music Video)"
	let output_text = "The Never Gonna Give You Up music video is a cultural artifact synonymous with the late 80s, showcasing Rick Astleys breakthrough as a musician and the enduring legacy he crafted. The videos simplicity combined with Astleys inimitable style and energetic performance results in a captivating, unpretentious watch that became a defining piece of pop culture.\nThe video opens with Astley strolling out in a cinematic blend of low lighting and an atmospheric mist, dressed in his signature casual style - a neat trench coat paired with his iconic hairdo. This entrance has become emblemic of Astley himself, setting the tone for the infectious rhythm and soulful delivery that follows.\nThroughout the music video, Astley performs against a variety of backdrops, including an underpass and a fence, which adds a degree of dynamism to the visual narrative. The use of contrasting hues of blue and red throughout the video conveys a range of emotional tonalities while maintaining its 80s aesthetic. Additionally, the choreography executed by the accompanying dancers embodies the spirit of the times, a fusion of energy and optimism, creating a lively ambiance that augments the musical composition.\nAstleys performance in the video is a powerful testament to his vocal prowess. His passionate delivery, tinged with a soulful blend of pop and dance-pop, elevates the song to a captivating auditory experience. From the catchy chorus to the smooth verses, the video perfectly complements the lyrical narrative of commitment and unyielding love.\nNever Gonna Give You Up isnt just a music video; its a symbol of an era. Its unpretentiousness and charm typify the spirit of the 80s, and its subsequent memetic resurgence as Rickrolling in the late 2000s has only cemented its place in internet folklore. The video, although simple in its execution, managed to create an iconic image of Astley, resonating with generations and transcending cultural and temporal barriers.\nWhile the videos production value may not stand up to the high-definition, multi-million-dollar music videos of today, it does not detract from its appeal. The videos strength lies in its simplicity, and the focus on Astleys vocals and performance style, which offer a refreshing breather from the overproduced music videos of contemporary times.\nThe Never Gonna Give You Up music video is more than just a music video; it is a cultural phenomenon. The videos influence extends beyond music, influencing internet culture and standing as a testament to the power of simplicity in music video production. From its catchy tune to its iconic choreography, the video continues to captivate audiences, serving as a testament to Astleys enduring influence and the timeless appeal of his music."
	let input_dynamic = ""

	async function handleSubmit() {

	}
</script>

<AppShell>

	<svelte:fragment slot="pageHeader">
		<AppBar gridColumns="grid-cols-3" slotTrail="place-content-end">
			<svelte:fragment slot="lead">
				<div class="flex">
					<img src="src/images/7862-telescope.png" alt="" width="50" height="50" class="space-x-20"/>
					<h1 class="text-4xl space-x-20">VibeScope</h1>
				</div>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<button type="button" class="btn variant-filled">Login</button>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>

	<slot>
		<div class="space-y-8 ml-32 mr-32 mt-24 mb-12">
			<div class="grid grid-cols-2 gap-4">
				<img src="src/images/youtubelogo_fluffy.png" alt="" width="400" height="400" class="ml-18"/>
				<div class="space-y-6 mt-14">
					<h1 class="text-6xl">Analyze user sentiment in a flash!</h1>
					<p class="text-lg">Simply copy and paste in the URL to your desired YouTube video and submit 
										it to VibeScope to recieve an AI powered sentiment analysis of user reviews.
										Effectiveley determine the validity of your content with a simple click.
					</p>
				</div>
			</div>
		</div>

		<div class="ml-96 mr-96 space-y-12">
			<div class="space-y-4 flex flex-col items-center">
				<h1 class="text-3xl text-center">Input Url</h1>
				<input class="input" title="Input (url)" type="url" multiple="true" placeholder=" eg. https://www.youtube.com/watch?v=dQw4w9WgXcQ" bind:value={input_dynamic}/>
				<button type="button" class="btn variant-filled-primary btn-lg" on:click={handleSubmit}>Submit</button>
			</div>
		</div>
		<div>
			<div class="card p-4 max-h-[200px] overflow-auto space-y-4 mt-14 ml-24 mr-24">
				<h3 class="h3" data-toc-ignore>{output_title}</h3>
				<p>
					{output_text}
				</p>
			</div>
		</div>
	</slot>
	<svelte:fragment slot="footer">

	</svelte:fragment>	

</AppShell>
