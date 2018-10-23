# HKemoji for CKEditor 4x 

This plugin integrates the custom png/gif emoji and smiley for ckeditor 4 (with exists 4 example emoji package) . Similar with plugin emojione.
### Download this plugin : [CKEditor-hkemoji.zip](https://ckeditor.com/cke4/addon/hkemoji)

<img align="center" width="800px" src="https://linx.li/selif/fqy6n5f2.png">

# Check our [demo](http://git-html.byethost9.com/hkemoji/) (tested in CKeditor v4.10.1)

# Install

1. Download source and extract to "ckeditor/plugins" folder.
2. in `config.toolbarGroups` (`groups`) add "HKemoji"
3. in `config.extraPlugins` add "hkemoji"

And you're done. 

Now, you want to change smiley to your self? I got it, because i'm just like you. And finally found the way, happy to share with you:




# Manage your emoji/smiley
Not too hard , not much easy , 3 step to add or remove emoji smiley, just focus to the name. You can do that without developer skill.

### I. Emoji files
Create folder (for example): `folder_emoji_1` and `folder_emoji_2`, `folder_emoji_n` ... inside `sricker` directory and storage list of emoji files on their folder.

### II. Edit: `plugin.js` & array files list
Find `CKEDITOR.config.hkemoji` and do with example below

You need some trick to list all of emoji image and array that. If don't have any, you can try to use Excel or Chrome ( to list files in folder) and Notepad (find and replace) to array format:
`['file_1.png','file_2.png','file_3.png',...]`

```
CKEDITOR.config.hkemoji = {
    tabs: {
		folder_emoji_1: 'Name of emoji package 1', // make tab clickable and register files in "folder_emoji_1" for this tab
		folder_emoji_2: 'Name of emoji package 2',
		folder_emoji_n: 'Name of emoji package n'
        	},
    emojis: {
		folder_emoji_1: ['emoji_1.png','emoji_2.png',...], // list all files (png/gif/etc..) with array format, inside "folder_emoji_1". 
		folder_emoji_2: ['emoji_1.png','emoji_2.png',...], 
		folder_emoji_n: ['emoji_1.png','emoji_2.png',...] 
    
    }

}
```


### III. Edit : `dialogs\hkemoji.js` from line `175`
Find and do with example below

Note with `folder_emoji_x`, need match with what you created before.
```
contents: [
			{
				id: 'tab-folder_emoji_1', 
				label: editor.config.hkemoji.tabs.folder_emoji_1,
				elements: [
					emojis('folder_emoji_1')
				]
			}, {
				id: 'tab-folder_emoji_2',
				label: editor.config.hkemoji.tabs.folder_emoji_2,
				elements: [
					emojis('folder_emoji_2')
				]
			}, {
				id: 'tab-folder_emoji_n',
				label: editor.config.hkemoji.tabs.folder_emoji_n,
				elements: [
					emojis('folder_emoji_n')
				]
			}
		]

```



# Thanks
- braune-digital [emojione](https://ckeditor.com/cke4/addon/emojione)

# _
Hope you like this function, let the star or comment at [hkemoji](https://ckeditor.com/cke4/addon/hkemoji) or email to [develop@execs.com](develop@execs.com) if you have issue. I'm happy to resolove.


