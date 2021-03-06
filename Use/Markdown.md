<link rel="stylesheet" type="text/css" href="/{{ site.title }}/css/stylesheet.css" media="screen">
<link rel="stylesheet" href="/{{ site.title }}/css/simplemde.min.css">
<script src="/{{ site.title }}/js/simplemde.min.js"></script>
<!--代码高亮-->
<script src="https://cdn.jsdelivr.net/highlight.js/latest/highlight.min.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/highlight.js/latest/styles/github.min.css">
	
<section class="main-content">
  <a href="https://lcfu1.github.io/Note/Use/Markdown_editor.html" target="_blank"><h2>Markdown在线编辑器</h2></a>
  <textarea id="demo2" style="display: none;"># Welcome to use</textarea>
</section>
<script>
  new SimpleMDE({
	element: document.getElementById("demo2"),
	spellChecker: false,
	autosave: {
		enabled: true,
		unique_id: "demo2",
		delay: 1000,
	},
	forceSync: true,
	//代码高亮
	renderingConfig: {
		singleLineBreaks: false,
		codeSyntaxHighlighting: true,
	},
	insertTexts: {
		image: ["![](", ")"],
		link: ["[", "]()"],
	},
	toolbar: [{
			name: "bold",
			action: SimpleMDE.toggleBold,
			className: "fa fa-bold",
			title: "粗体",
		},
		{
			name: "italic",
			action: SimpleMDE.toggleItalic,
			className: "fa fa-italic",
			title: "斜体",
		},
		{
			name: "strikethrough",
			action: SimpleMDE.toggleStrikethrough,
			className: "fa fa-strikethrough",
			title: "删除线",
		},
		{
			name: "heading",
			action: SimpleMDE.toggleHeadingSmaller,
			className: "fa fa-header",
			title: "标题",
		},"|", 
		{
			name: "code",
			action: SimpleMDE.toggleCodeBlock,
			className: "fa fa-code",
			title: "代码",
		},
		{
			name: "quote",
			action: SimpleMDE.toggleBlockquote,
			className: "fa fa-quote-left",
			title: "引用",
		},
		{
			name: "horizontal-rule",
			action: SimpleMDE.drawHorizontalRule,
			className: "fa fa-minus",
			title: "横线",
		},
		{
			name: "unordered-list",
			action: SimpleMDE.toggleUnorderedList,
			className: "fa fa-list-ul",
			title: "无序列表",
		},
		{
			name: "ordered-list",
			action: SimpleMDE.toggleOrderedList,
			className: "fa fa-list-ol",
			title: "有序列表",
		},"|", 
		{
			name: "link",
			action: SimpleMDE.drawLink,
			className: "fa fa-link",
			title: "链接",
	    },
		{
			name: "image",
			action: SimpleMDE.drawImage,
			className: "fa fa-picture-o",
			title: "图片",
		},
		{
			name: "table",
			action: SimpleMDE.drawTable,
			className: "fa fa-table",
			title: "表格",
		},"|", 
		{
			name: "preview",
			action: SimpleMDE.togglePreview,
			className: "fa fa-eye no-disable",
			title: "预览模式",
		},
		{
			name: "fullscreen",
			action: SimpleMDE.toggleFullScreen,
			className: "fa fa-arrows-alt no-disable no-mobile",
			title: "全屏模式",
		},
		{
			name: "side-by-side",
			action: SimpleMDE.toggleSideBySide,
			className: "fa fa-columns no-disable no-mobile",
			title: "边写边看",
		},"|", 
		{
			name: "clean-block",
			action: SimpleMDE.cleanBlock,
			className: "fa fa-eraser fa-clean-block",
			title: "清除格式",
		},
		{
			name: "guide",
			action: function link(link){
				window.open('/{{ site.title }}/Markdown/markdown.html','_blank')
			},
			className: "fa fa-star",
			title: "Markdown指南",
		},
		{
			name: "custom",
			action: function customFunction(editor){
				window.open('/{{ site.title }}/Use/markdown-help.html','_blank')
			},
			className: "fa fa-question-circle",
			title: "帮助",
		},
		],
		shortcuts: {
			"toggleBold": "Ctrl-B",
			"toggleItalic": "Ctrl-I",
			"toggleStrikethrough": "Ctrl-S",
			"toggleHeadingSmaller": "Ctrl-H",
			"toggleCodeBlock": "Ctrl-Alt-C",
			"toggleBlockquote": "Ctrl-Q",
			"drawHorizontalRule": "Ctrl--",
			"toggleUnorderedList": "Ctrl-L",
			"toggleOrderedList": "Ctrl-Alt-L",
			"drawLink": "Ctrl-K",
			"image": "Ctrl-Alt-I",
			"table": "Ctrl-Alt-T",
			"togglePreview": "Ctrl-P",
			"toggleFullScreen": "F11",
			"toggleSideBySide": "F9",
			"cleanBlock": "Ctrl-E"
			},
		});
</script>