<script>
	import { addTodo } from '../../store/TodoStore';
</script>

<section class="flex justify-between ">
	<h3 class="text-xl font-bold text-gray-three">Checklist</h3>
	<button
		class="group flex items-center rounded-md border-cream-four bg-green-one px-6 py-3 text-lg font-semibold text-gray-five outline outline-2 outline-offset-2 outline-green-one hover:text-green-five focus-visible:text-green-five focus-visible:outline-green-five"
		type="button"
		on:click={addTodo}
		>Add task <svg
			class="ml-3 h-4 w-4 text-gray-five group-hover:text-green-five group-focus-visible:text-green-five"
			width="21"
			height="21"
			viewBox="0 0 21 21"
			fill="none"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				d="M10.9927 18.8628C6.58268 18.8628 2.99268 15.2728 2.99268 10.8628C2.99268 6.45279 6.58268 2.86279 10.9927 2.86279C15.4027 2.86279 18.9927 6.45279 18.9927 10.8628C18.9927 15.2728 15.4027 18.8628 10.9927 18.8628ZM10.9927 0.862793C9.67946 0.862793 8.3791 1.12145 7.16584 1.624C5.95259 2.12654 4.85019 2.86314 3.92161 3.79173C2.04624 5.66709 0.992676 8.21063 0.992676 10.8628C0.992676 13.515 2.04624 16.0585 3.92161 17.9339C4.85019 18.8624 5.95259 19.599 7.16584 20.1016C8.3791 20.6041 9.67946 20.8628 10.9927 20.8628C13.6448 20.8628 16.1884 19.8092 18.0637 17.9339C19.9391 16.0585 20.9927 13.515 20.9927 10.8628C20.9927 9.54957 20.734 8.24921 20.2315 7.03596C19.7289 5.8227 18.9923 4.72031 18.0637 3.79173C17.1352 2.86314 16.0328 2.12654 14.8195 1.624C13.6063 1.12145 12.3059 0.862793 10.9927 0.862793ZM11.9927 5.86279H9.99268V9.86279H5.99268V11.8628H9.99268V15.8628H11.9927V11.8628H15.9927V9.86279H11.9927V5.86279Z"
				fill="currentColor"
			/>
		</svg>
	</button>
</section>
