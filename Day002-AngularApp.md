# ២). របៀបសរសេរ Component
 
 តាមរយះការបង្កើតគ្រោងកម្មវិធីដោយប្រើប្រាស់ `Angular Cli` យើងសង្កេតឃើញថា នៅក្នុងនោះមានទៅដោយ ហ្វិល(file) នឹង ហ្វូដឺ(folder) ជាច្រើន។
 ហ្វិល (files) រួមទាំង ហ្វូដឺ (folders) ទាំងអស់នោះគឺជាគ្រោងនៃកម្មវិធីរបស់យើងដែលត្រូវសរសេរ។ អូខេ!! ដើម្បីកុំអោយខាតពេលវេលា! យើងនឹងចាំផ្ដើមពី ហ្វូដឺ `src`ដែលនៅក្នុងនោះរួមមាន ហ្វិល `index.html` ដែលកន្លែងដែល `root Angular` ចាំផ្ដើមនៅក្នុងនោះ។
 
 ```
 <!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>NgxDatepickerCustom</title>
  <base href="/">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
<body>
   // បន្ទាត់កូដដែលជា root angular
  <app-root></app-root> 
</body>
</html>

 ```
 បន្ដទៅទៀតយើងនឹងអាចសង្កេតឃើញ ហ្វីល(files) ជាច្រើនដែល កន្ទុយជា ហ្វម៉ាត់ (format) `ts` ដែលយើងហៅហ្វីលទាំងអស់នោះជាភាសាអង់គ្លេសថា `TypeScript (TS)` ។
 
 ហ្វិលទាំងអស់នោះមានមុខងារផ្សេងៗ គ្នាដូចជា:
 - `app.component.html` កន្លែងដែលយើងអាចសរសេរ `HTML`
 - `app.component.scss` កន្លែងដែលអនុញ្ញាតអោយយើងសរសេរ `style scss`
 - `app.component.spec.ts` កន្លែងដែលអនុញ្ញាតអោយយើងសរសេរ `unit test`
 - `app.component.ts` កន្លែងដែលអនុញ្ញាតអោយយើងសរសេរកូដ `angular` ហើយថា `Commponent`
 - `app.module.s` កន្លែងដែលប្រមូលផ្ដុំនៃ `components`, `services` ដែលគេហៅកន្លែងនោះថា `Module`
 
 ## និយមន័យរបស់ Component
 
`Component` ជាបន្ដុំនៃប្លកកូដ `HTML` ដែលកកើតឡើងដោយ `Angular` ។ តែបើយើងនិយាយពីគេហទំព័រវិញ `Component` ជាផ្នែកតូចមួយនៃគេហទំព័រនោះ ។ គឺវាមានន័យ គេហទំព័រទាំងមូល អាចកកើតឡើងបានដោយបន្ដុំនៃ `Commponent` តូចៗ ជាច្រើន។

ឧទារហ៍ណ: [youtube.com](https://www.youtube.com/) វាកកើតដោយ `Component`មានដូចជា:

- `Left Menu`
- `Header`
- `Flooter`
-  ...
 
 ## របៀបបង្កើត Component
 
 ការបង្កើត `Commponent` មួយបានយើងអាចប្រើប្រាស់វិធីយ៉ាងងាយ:
 - ប្រើប្រាស់ ពាក្យគន្លឺះដើម្បី អោយវាធ្វើការបង្កើតដោយខ្លួនអែង (auto)
```
ng generate component <ឈ្មោះ-component>
ng g component <ឈ្មោះ-component>
```
 ឧទារហណ៍: `ng g component hello`
 ```
 src/app/hello/hello.component.scss
 src/app/hello/hello.component.html
 src/app/hello/hello.component.spec.ts
 src/app/hello/hello.component.ts
 ```
 យើងសង្កេតឃើញថា វាធ្វើបង្កើតអោយយើងនៅ ហ្វិលចំនួន ៤ដែលមានមុខងារស្រដៀងទៅនឹងហ្វិលដែលបានរៀបរាប់ខាងដើម។ តោះយើងបន្ដដំនើររបស់យើងទៅកាន់ ហ្វិលដែលចំាបាច់របស់ហៅថា `Component` នោះគឺ ហ្វិល `src/app/hello/hello.component.ts` ។ នៅក្នុងហ្វិល នេះយើងអាចសង្កេតឃេីញថាវាមានទំរង់ដូចខាងក្រោម:
```
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-hello',
  templateUrl: './hello.component.html',
  styleUrls: ['./hello.component.scss']
})
export class HelloComponent {}
```
- `selector` គឺថា `tag`នៃ`component`វាមានទំរង់ដូចខាងក្រោមនេះ
```
<tag-name></tag-name>
```
- `templateUrl` សម្រាប់កំនត់ ទីតាំងរបស់ហ្វិល `HTML`
- `styleUrls` សម្រាប់កំនត់ ទីតាំងរបស់ហ្វិល `style`

រួចហើយយើងត្រូវតែដាក់បញ្ចូល `HelloComponent` ចូលទៅកាន់ `app.module.ts` នេះគឺច្បាប់របស់ `Angular` ។ ជាធម្មតារាល់ គ្រប់`Component` ទំាងអស់ដើម្បីអោយវាមានដំនើរកើតយើងត្រូវដាក់វាចូលទៅដាក់ `module` ណាមួយ ។ដូច្នោះហើយយើងនឹងដាក់ `HelloComponent` ចូលទៅកាន់ `app.module.ts`
```
import { HelloComponent } from './hello/hello.component';

...

declarations: [
  AppComponent,
  HelloComponent,
],
```

រួចហើយនៅក្នុង `src/app/hello/hello.component.html` យើងអាចសរសេរបន្ថែមនៅបន្ទាត់កូដដូចខាងក្រោម:

```
<app-hello></app-hello>
```

## ឯកសារយោង
- [https://angular.io/guide/architecture-components](https://angular.io/guide/architecture-components)
- [https://angular.io/guide/architecture](https://angular.io/guide/architecture)
