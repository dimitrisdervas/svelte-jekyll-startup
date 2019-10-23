<script>
	import Folder from './Folder.svelte';
import Yaml from './Yaml.svelte';


	let root = [
		{
			type: 'folder',
			name: 'Section',
			form: '',
			files: [
				{
					type: 'folder',
					name: 'data',
					files: [
							{ type: 'file',
							 name: 'htmlelement',
							 info: 'choose the html element to choose div, section, article,…',
							 options: [
									option: "<article>",
									option: "<aside>",
									option: "<details>",
									option: "<figcaption>",
									option: "<figure>",
									option: "<footer>",
									option: "<header>",
									option: "<main>",
									option: "<mark>",
									option: "<nav>",
									option: "<section>",
									option: "<summary>",
									option: "<time>"
							 ] }
						]
				},
				{
					type: 'file',
					name: 'theme'
				},
				{
					type: 'folder',
					name: 'seoTitle',
					info: 'Create title plus',
					files: [
							{
							type: 'folder',
							name: 'data',
							files: [
								{ type: 'file', name: 'label', info: 'what to print' },
								{ type: 'file', name: 'separator', info: 'separate with the seoSubtitle' },
								{ type: 'file', name: 'link', info: 'where to link' }
								]
							}
						]
				},
				{
					type: 'folder',
					name: 'seoSubtitle',
						files: [
							{
							type: 'folder',
							name: 'data',
							files: [
								{ type: 'file', name: 'label', info: 'what to print' },
								{ type: 'file', name: 'separator', info: 'separate with the seoSubtitle' },
								{ type: 'file', name: 'link', info: 'where to link' }
								]
							}
						]
				},
				{
					type: 'folder',
					name: 'wrapperSection',
					info: 'wrap the section in a div and theme it',
					files: [
						{
							type: 'folder',
							name: 'theme',
							files: [
									{ type: 'file', name: 'class' },
									{ type: 'file', name: 'id' }
								]
						}
					]
				}
		]
		}
	];
</script>

<div class="flex flex-no-wrap justify-around w-full">
	<div class="flex-1 flex-col border m-2 p-2 bg-gray-200">
		<Folder name="Home" files={root} expanded/>tet
	</div>

	<div class="flex-1 border m-2 p-2 bg-blue-200">
		<Yaml/>
	</div>
</div>