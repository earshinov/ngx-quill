# ngx-quill
Angular (>=2) component for rich text editor Quill

<img src="https://cloud.githubusercontent.com/assets/2264672/20601381/a51753d4-b258-11e6-92c2-1d79efa5bede.png" width="200px">

ngx-quill is the new angular (>=2) implementation of ngQuill.
This project was generated with [angular-cli](https://github.com/angular/angular-cli) version 1.0.0-beta.24.

## Examples
[demo-page](https://killercodemonkey.github.io/ng2-quill)

## Installation
- install QuillJS 1.1.9 `npm install ngx-quill`
- include bubble.css, snow.css in your index.html
- add `QuillModule` to your own NgModule: `node_modules/ng2-quill/src/quill/quill.module.ts`
- use `<quill-editor></quill-editor>` in your templates to add a default quill editor

## Config
- ngModel - set initial value or allow two-way databinding
- readOnly (true | false) if user can edit content
- formats - array of allowed formats/groupings
- modules - configure/disable quill modules, e.g toolbar or add custom toolbar via html element default is
```
{
  toolbar: [
    ['bold', 'italic', 'underline', 'strike'],        // toggled buttons
    ['blockquote', 'code-block'],

    [{ 'header': 1 }, { 'header': 2 }],               // custom button values
    [{ 'list': 'ordered'}, { 'list': 'bullet' }],
    [{ 'script': 'sub'}, { 'script': 'super' }],      // superscript/subscript
    [{ 'indent': '-1'}, { 'indent': '+1' }],          // outdent/indent
    [{ 'direction': 'rtl' }],                         // text direction

    [{ 'size': ['small', false, 'large', 'huge'] }],  // custom dropdown
    [{ 'header': [1, 2, 3, 4, 5, 6, false] }],

    [{ 'color': [] }, { 'background': [] }],          // dropdown with defaults from theme
    [{ 'font': [] }],
    [{ 'align': [] }],

    ['clean'],                                         // remove formatting button

    ['link', 'image', 'video']                         // link and image, video
  ]
};
```
- theme - bubble/snow, default is `snow`
- placeholder - placeholder text, default is `Insert text here ...`

## Outputs
- onEditorCreated - editor instance
- onContentChanged - text is updated
```
{
  editor: this.quillEditor,
  html: html,
  text: text
}
```
