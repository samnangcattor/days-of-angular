# ១. ការរៀបចំដំឡើង (PREPARE THE WORKING ENVIROMENT)

## សេចក្ដីផ្ដើម

រយះពេលច្រើនឆ្នាំកន្លងមកនេះ, Angular បានធ្វើការផ្លាស់ប្ដូរ នឹងកែទំរង់ ជាច្រើនទៅលើមុខងារនឹង ល្បឿននៃដំនើរការ(Performance) ។ ដូច្នោះហើយបាន ជាមានក្រុមហ៊ុនច្រើន

បានជ្រើរើស Angularមកសរសេរ ក្នុងកម្មវិធី គេហទំព័ររបស់ពួកគេ ស្របពេលជាមួយគ្នានេះ Google ខ្លួនអែងផ្ទាល់ក៏កកំពុងតែធ្វើការកែទំរង់ នៃ Angularពីជំនាន់មួយទៅ ជំនាន់មួយ

កាន់តែប្រសើរឡើង ។ ហេតុដូចនេះ យើងក៏បាន ចាប់ផ្ដើមរៀបចំ ជាមេរៀនជាលំដាប់ លំដោយដែល បានសរសេរជាខេមរះភាសា ដើម្បីអោយនិសិត្ស ឬមួយអ្នកពេញនិយមប្រើប្រាស់ Angular

និយាយជារួម អាចសិក្សាស្រាវជ្រាវបាន ។ យើងសង្ឃឹមថា អត្ថបទមេរៀននេះអាចជាគន្លឹះ ដែលអាច ផ្ដល់អោយអ្នករៀន ពី Angular កាន់តែងាយស្រួលឡើង ។ទោះបី ជាយ៉ាងណាក៏ដោយ

អត្ថបទសរសេររបស់យើង និមួយៗ អាចនឹង មានកំហុសឆ្គងទៅលើពាក្យពេជច្យ ឬ ការខ្វះខាត ទៅការពន្យល់ ហេតុដូច្នោះ សូមអោយអ្នកអាន ទាំងអស់មេត្ដា អាជាស្រ័យមកខាងយើងផង

ឬមួយក៏អាចផ្ញើជាមតិដើម្បីអោយខាងយើងធ្វើការកែប្រែ អោយកាន់តែប្រសើរឡើង។

## រៀបចំ

ដើម្បីសរសេរកូដ Angular ទៅរួចយើងត្រូវការ តំឡើងកម្មវិធីមួយចំនួនក្នុង កំុំព្យូទ័ររបស់យើងជាមុនសិន។ ហើយកម្មវីធីនោះរួមមានដូចខាង:

- IDE/Editor: យើងត្រូវការកម្មវិធីដែលអាចអោយយើង ធ្វើការសរសេរ កូដAngular កើតក្នុងនោះរួមមាន [Visual Studio Code](https://code.visualstudio.com/),

[WebStorm](https://www.jetbrains.com/webstorm/), [Sublime](https://www.sublimetext.com/), [Atom](https://atom.io/) ...

- តំឡើង [NodeJS](https://nodejs.org/en/)
- តំឡើង [TypeScript](https://www.typescriptlang.org/)
- តំឡើង [Angular Cli](https://cli.angular.io/)

### NODEJS

មុនដំបូងបង្អស់ យើងត្រូវការតំឡើង `NodeJS` តាមរយះ ការដោនឡូត វាពីគេហទំព័រ [https://nodejs.org/en/download/](https://nodejs.org/en/download/) ។ ក្នុងការ

ជ្រើរើសយើងសង្គេតឃើញថា `NodeJS` របស់យើងមាន ២ប្រភេទ:

- Long Term Support(LTS)
- Current Version

យើងសូមណែនាំអោយជ្រើរើស Long Term Support.

ក្រោយពីការដំឡើង `NodeJs` រួចរាល់យើងការធ្វើការពិនិត្យ `NodeJS` ថាតើវាបានតំឡើងរួចរាល់ហើយរឺនៅក្នុងម៉ាសុីនរបស់យើងដោយវាយនៅពាក្យគន្លឹះដូចខាងក្រោម:

```
node -v
npm -v
```
### Angular Cli

ដើម្បីសរសេរកូដ Angular អាចទៅកើតយើង ត្រូវតែចាំបាច់តំឡើង `Angular Cli` ។ ដំនើរការតំឡើងនៃវាមានលំដាប់លំដោយដូចខាងក្រោយនេះ: (យើងត្រូវការតំឡើងវាតាមរយះ `Terminal`)

```
npm install -g @angular/cli@latest
```

ក្រោយពីយើងបានធ្វើការដំឡើងវារួចរាល់ហើយ យើងអាចធ្វើការពិនិត្យវាបានដោយវាយពាក្យគន្លឹះ `ng version` 

### របៀបបង្កើតគ្រោងនៃកម្មវីធី

អោយពីយើងបានធ្វើការដំឡើង `Angular Cli` រួចរាល់ហើយយើងអាចធ្វើការបង្កើត គ្រោងកម្មវិធីបានដោយងាយស្រួលបំផុតតាមរយះវាយ ពាក្យគន្លឹះ

```
ng new <ឈ្មោះ គ្រោងកម្មវីធីរបស់អ្នក>
```

ឧទារហណ៍: `ng new angular001-d`

អំឡុងពេលយើងបង្កើតគ្រោងនៃកម្មវិធី `Angular Cli` បានសួរយើងសួរយើងថា:

- Would you like to add Angular routing? កន្លែងនេះយើង ជាជ្រើរើសថា យល់ព្រមក៏បានឬមិនត្រូវការ (យើងនឹងធ្វើការលំអិតទាក់ទងទៅនឹង `Angular routing` នៅពេលក្រោយ)
- Which stylesheet format would you like to use? ជាធម្មតា យើងបានដឹងហើយថា ការរចនាគេហទំព័រគឺវា ចាំបាច់ទៅដល់ កូដ `CSS` ។ ហេតុដូចនេះ `Angular Cli` បានបង្កើតអោយយើងជាស្រាច់នៃ `style` កូដដែលយើងចង់ប្រើប្រាស់ អាច `CSS, SCSS, SASS`
- ក្រោយពីដំឡើងរួចរាល់ហើយ យើង ប្រើប្រាស់ `ng serve` ដើម្បីដំណើរការកម្មវិធីរបស់យើង ។ ជាធម្មតា វានឹងដំណើរនៅលើ `port` ៤២០០ ក៏បុ៉ន្ដែយើងអាចធ្វើការកែប្រែវាបានដោយប្រើប្រាស់ពាក្យគន្លឺះ

```
ng serve --port=<other-port>
```
ឧទារហណ៍ `ng serve --port=9000` រួចហើយយើងអាចចូលទៅកាន់លីងមួយនេះ [http://localhost:9000/](http://localhost:9000/)

## ឯកសារយោង
- [https://angular.io/guide/setup-local](https://angular.io/guide/setup-local)
- [https://angular.io/tutorial/toh-pt0](https://angular.io/tutorial/toh-pt0)

## អ្នករៀបរៀងអត្ថបទសរសេរ
- [ដាំ សំណាង](https://github.com/samnangcattor)

## កំនែនទំរង់អត្ថបទសរសេរ

ទោះបីយ៉ាងណាអត្ថបទនេះអាចនឹងធ្វើការកែប្រែទៅតាម ជំនាន់របស់ `Angular`