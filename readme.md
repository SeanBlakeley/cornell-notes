=== Cornell Notes ===
Contributors: sean-blakeley
Tags: Cornell Notes, notes, learning, note-taking, Gutenberg, study, note taking, study-aid, development, block
Requires at least: 5.3.4
Requires PHP: 7.1
Tested up to: 5.4.2
Stable tag: 1.0

Create perfect study notes with the Cornell Notes Gutenberg Block.

== Description ==

[Cornell Notes](https://en.wikipedia.org/wiki/Cornell_Notes) provides an excellent structure for organising and summarized your notes, ideas and concepts - this logical approach is an invaluable way to help learning and retention for students of all ages. This plugin provides a new, dedicated Cornell Notes Gutenberg block to enable you to quickly and easily take your notes within WordPress.

= How to Use Cornell Notes =
1. Add your title at the top of the note - this is a summary of context of the notes - for example: `ES6 Main Concepts from Kyle Simpson` or `American Civil War Lecture: 06-20-2020`.
2. Take long-form notes in the right-hand column - you can take notes during a class, lecture, video tutorial or WordCamp Talk, it doesn't matter. Add as many ideas as you need - click the 'Add Idea' indicator to add a new idea.
3. Once you've finished your notes, review them and summarise the concepts with key ideas in the left-hand column - for example: `Arrow Functions` or `Supply and Demand`.
4. Finally, summarize all the notes in a sentence or two at the bottom of the page.
5. To fully benefit from Cornell Notes, you should consider adding [Spaced Repetition](https://en.wikipedia.org/wiki/Spaced_repetition) to your learning plan.

Cornell Notes contains a second block - an *Idea* block - this block is only made available as a child of the Cornell Note block - and enables you to add as many ideas (key ideas and long-form notes) you require.

There are currently no specific settings required by the Cornell Notes Block.

== How to Extend This Plugin ==
`npm install ` -- install all required dependencies.  
`npm start` -- serve the development version of the block.  
`npm run build` -- build the production-ready version of the block.  

== Localization ==
* English (default)

== Installation ==
1. Upload the entire `cornell-notes` folder to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Navigate to any Gutenberg-enabled editing screen and select the 'Cornell Note' block from the `Common Blocks` tab
4. Create your Cornell Note
5. Learn and grow :)

== Frequently Asked Questions ==
= How can I style the block? = 
The Cornell Notes Block contains minimalist styling - it should inherit the styles from you existing theme. Overriding the styles is straightforward (for reference, the Sass stylesheet can be found at: `cornell-notes/src/blocks/cornell-notes/styles.scss`

> **Note**: The Summary section is forced to the bottom of the Cornell Note via Flexbox (`order: 1`) - this only affects the display - in the DOM, the Summary sits below the first key idea and long-form note.

= Style via CSS Variables =
CSS Variables are used with default settings - you can override these in your theme by setting the variables in the `root`
```
:root{
    --note-border-style: dotted;  
	--note-border-width: 2px;
	--note-border-color: #f00;  
	--note-body-padding: 30px;  
	--note-padding: 20px;  
}
```

= Style via Classes =
The structure to the Cornell Notes Block:
```
.wp-block-cornell-notes-cornell-note
	.cornell-note-title
	.wp-block-cornell-notes-cornell-idea
		.cornell-note-key-idea
		.cornell-note-long-form
	.cornell-note-summary /* forced to the bottom of the note via Flexbox */
```
(This structure is simplified - you will find additional classes added via Gutenberg)

> **Note**: The block requires this class structure to display correctly

= Why am I getting some different styling at different device sizes? =
By default, The Cornell Note Block is responsive and has a small amount of styling which changes at 600px width.  if you want to override these styles, try adding this [breakpoint](https://www.w3schools.com/css/css_rwd_mediaqueries.asp) to your styles.

= How do I add new ideas and concepts? = 
Simply click the 'Add Idea' button which is located directly above the notes summary section (see screenshot)

= Is there a limit to the number of ideas I can add? = 
No, you can keep adding as many ideas as you like

= Will I be able to search for the ideas via the WordPress Search Box? = 
Yes, your Cornell Note ideas will be searchable via the standard WordPress search or any other search tool which searches your content.

= Can I tag the notes? = 
No, not yet - this is a feature we're looking to add later.

= Is the block likely to be well supported? = 
The Cornell Notes block is a composite of core blocks - so you get all the usual editing, support, security and functional options of core WordPress blocks baked-in :)

= Are there any ambitions to extend the plugin to incorporate Spaced Repetition? = 
It's funny you should ask that - yes, definitely maybe.

== Screenshots ==
1. Cornell Notes adds a new block to the editor
2. Cornell Notes contains an 'Idea' block - only available as a child of the Cornell Note block
3. The Cornell Note Block on the frontend (inheriting the theme styles)
4. Simply add another concept to your Cornell Notes

== Changelog ==
= 1.0 =
Initial release into the wild

== Upgrade Notice ==
= 1.0 =
Release

== Translations ==
* English - default
This plugin is translation-ready

==How to Contribute to This Project==
All contributions are welcome - make a Pull Request or raise an issue on the [Github Repo](https://github.com/SeanBlakeley/cornell-notes/)

==Plugin Creator==
[Sean Blakeley](https://github.com/SeanBlakeley)

== Credits ==
This project was bootstrapped with [Create Guten Block](https://github.com/ahmadawais/create-guten-block).
