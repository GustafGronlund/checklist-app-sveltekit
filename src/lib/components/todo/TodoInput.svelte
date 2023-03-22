<script>
	import { deleteTodo, toggleComplete, editTodo } from '../../store/TodoStore';

	export let todo;

	$: completeClass = todo.complete ? 'bg-green-three' : 'bg-leaf-one';
</script>

<div class="flex items-center justify-between rounded-md border-2 border-gray-one px-5 py-4">
	<div class="flex w-full max-w-lg items-center justify-start">
		<label for={`${todo.id}-checkbox`} class="sr-only">Complete todo</label>
		<input
			id={`${todo.id}-checkbox`}
			type="checkbox"
			checked={todo.complete}
			on:change={() => toggleComplete(todo.id)}
			class="h-4 w-4 rounded border border-gray-three bg-cream-four text-green-four focus:border-green-five focus:outline focus:outline-2 focus:outline-offset-2 focus:outline-green-five"
		/>
		<label for={`${todo.id}-text`} class="sr-only">Edit todo</label>
		<input
			id={`${todo.id}-text`}
			type="text"
			placeholder="Enter a todo"
			value={todo.text}
			on:input={(e) => editTodo(todo.id, e.target.value)}
			class="ml-5 flex-1 text-ellipsis rounded-none border-x-0 border-t-0 border-b border-dashed border-b-gray-two bg-cream-four px-0 pb-1 text-base font-normal text-gray-three placeholder:text-gray-two focus:border-gray-three focus:outline-none focus:ring-0"
		/>
		<span
			class="{completeClass} ml-5 hidden rounded-full py-0.5 px-2 text-sm font-normal text-gray-five md:block "
		>
			{todo.complete ? 'Complete' : 'In Progress'}
		</span>
	</div>
	<button
		class="group ml-4 flex item-center justify-center rounded-md bg-cream-four p-2 hover:bg-steel-one focus:outline-none focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-green-five"
		type="button"
		on:click={() => deleteTodo(todo.id)}
	>
		<span class="sr-only"> Delete todo </span>
		<svg
			class="h-5 w-5 text-steel-three group-hover:text-gray-five"
			width="17"
			height="19"
			viewBox="0 0 17 19"
			fill="none"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				d="M5.604 0.137207V1.13721H0.604004V3.13721H1.604V16.1372C1.604 16.6676 1.81472 17.1763 2.18979 17.5514C2.56486 17.9265 3.07357 18.1372 3.604 18.1372H13.604C14.1344 18.1372 14.6431 17.9265 15.0182 17.5514C15.3933 17.1763 15.604 16.6676 15.604 16.1372V3.13721H16.604V1.13721H11.604V0.137207H5.604ZM3.604 3.13721H13.604V16.1372H3.604V3.13721ZM5.604 5.13721V14.1372H7.604V5.13721H5.604ZM9.604 5.13721V14.1372H11.604V5.13721H9.604Z"
				fill="currentColor"
			/>
		</svg>
	</button>
</div>
