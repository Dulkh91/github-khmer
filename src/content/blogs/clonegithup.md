---
title: "ដើម្បី Update កូដពី GitHub ទៅម៉ាស៊ីនអ្នក"
tag: ["githup"]
---

ជំហានដើម្បី Update កូដពី GitHub ទៅម៉ាស៊ីនអ្នក
---

ដើម្បីទទួលបានកូដថ្មីដែលក្រុមបាន push ទៅ GitHub អ្នកត្រូវទាញ (pull) ការផ្លាស់ប្តូរពី Remote Repository មកកាន់ Local Repository របស់អ្នក។ នេះជាជំហាន៖
ត្រូវប្រាកដថាអ្នកនៅក្នុង Repository ត្រឹមត្រូវ:
បើក Terminal (ឬ Command Prompt) ហើយចូលទៅក្នុងថតគម្រោងរបស់អ្នក៖
```bash
cd /path/to/your/repository
```

បើអ្នកមិនទាន់មាន Repository នៅលើម៉ាស៊ីនអ្នក សូមទាញ (clone) វាពី GitHub៖
```bash
git clone <repository-url>
```

ប្តូរទៅសាខាចម្បង (Main Branch):
ជាធម្មតា កូដថ្មីរបស់ក្រុមនឹងត្រូវបាន merge ទៅសាខាចម្បង (ឧ. main ឬ develop)។
ប្តូរទៅសាខាចម្បង៖
 ```bash
git checkout main
```

បើអ្នកមិនប្រាកដថាសាខាណាជាសាខាចម្បង សូមពិនិត្យជាមួយក្រុមអ្នក។
ទាញកូដថ្មីពី GitHub:
ប្រើពាក្យបញ្ជា git pull ដើម្បីទាញការផ្លាស់ប្តូរចុងក្រោយពី Remote Repository៖
 ```bash
git pull origin main
```

ពាក្យបញ្ជានេះនឹងទាញកូដថ្មីទាំងអស់ដែលក្រុមបាន push ទៅសាខា main មកកាន់ម៉ាស៊ីនអ្នក។
ពិនិត្យការផ្លាស់ប្តូរ:
បន្ទាប់ពី git pull អ្នកអាចពិនិត្យឯកសារនៅលើម៉ាស៊ីនអ្នក ដើម្បីឃើញកូដថ្មីដែលបានធ្វើបច្ចុប្បន្នភាព។
បើចង់ឃើញប្រវត្តិការផ្លាស់ប្តូរ ប្រើ៖
 ```bash
git log --oneline
```

បើអ្នកកំពុងធ្វើការលើ Branch ផ្សេង:
បើអ្នកកំពុងធ្វើការលើ Branch ផ្ទាល់ខ្លួន (ឧ. feature/add-something) ហើយចង់ធ្វើបច្ចុប្បន្នភាព Branch នោះជាមួយកូដថ្មីពី main សូមធ្វើដូចនេះ៖
ប្តូរទៅ Branch របស់អ្នក៖
 ```bash
git checkout feature/add-something
```

Merge កូដពី main ទៅ Branch របស់អ្នក៖
 ```bash
git merge main
```

បើមាន conflict (ការប៉ះទង្គិចកូដ) អ្នកនឹងត្រូវដោះស្រាយវាដោយកែឯកសារដែលមានបញ្ហា ហើយបន្ត៖
 ```bash
git add .
git commit
```

បង្ហោះ Branch របស់អ្នក (បើចាំបាច់):
បន្ទាប់ពីធ្វើបច្ចុប្បន្នភាព Branch របស់អ្នក អ្នកអាចបង្ហោះវាទៅ GitHub៖
 ```bash
git push origin feature/add-something
```

បន្ទាប់មកបង្កើត Pull Request នៅលើ GitHub ដើម្បីស្នើសុំបញ្ចូលកូដរបស់អ្នក។

ឧទាហរណ៍ជាក់ស្តែង
សន្មត់ថាក្រុមអ្នកបាន push កូដថ្មីទៅសាខា main នៅលើ GitHub៖
ចូលទៅក្នុងថតគម្រោង៖
 ```bash
cd /path/to/your/repository
```

ប្តូរទៅសាខា main:
 ```bash
git checkout main
```

ទាញកូដថ្មី៖
 ```bash
git pull origin main
```

នេះនឹងធ្វើបច្ចុប្បន្នភាព Local Repository របស់អ្នកជាមួយកូដថ្មីទាំងអស់។
បើអ្នកកំពុងធ្វើការលើ Branch feature/add-login-page:
ប្តូរទៅ Branch នោះ៖
 ```bash
git checkout feature/add-login-page
```

Merge កូដពី main:
 ```bash
git merge main
```

បើមាន conflict សូមកែឯកសារដែលមានបញ្ហា ហើយបន្ត៖
 ```bash
git add .
git commit
```

បង្ហោះ Branch ទៅ GitHub៖
 ```bash
git push origin feature/add-login-page
```

ចូលទៅ GitHub បង្កើត Pull Request សម្រាប់ feature/add-login-page។

គន្លឹះបន្ថែម
ពិនិត្យសាខាមុននឹង Pull:
បើក្រុមបាន push កូដទៅសាខាផ្សេង (ឧ. develop ជំនួសឱ្យ main) សូមប្រាកដថាអ្នកប្រើសាខាត្រឹមត្រូវ៖
 ```bash
git pull origin develop
```

ដោះស្រាយ Conflict:
បើមាន conflict នៅពេល merge កម្មវិធីនឹងប្រាប់អ្នកពីឯកសារដែលមានបញ្ហា។ បើកឯកសារទាំងនោះ កែសម្រួលកូដដែលប៉ះទង្គិច ហើយបន្តដំណើរការ។
ឧបករណ៍ដូចជា VS Code អាចជួយបង្ហាញ conflict និងជួយដោះស្រាយ។
ទាញកូដជាប្រចាំ:
ដើម្បីជៀសវាង conflict ច្រើន សូម git pull ជាប្រចាំមុននឹងចាប់ផ្តើមធ្វើការលើ Branch របស់អ្នក។
ប្រើ GitHub Desktop ឬ VS Code:
បើអ្នកមិនចូលចិត្តប្រើ Terminal អ្នកអាចប្រើ GitHub Desktop ឬ VS Code ដើម្បីទាញកូដ និងគ្រប់គ្រង Branch។

សរុប
ដើម្បី update កូដដែលក្រុមបាន push ទៅ GitHub៖
ប្តូរទៅសាខាចម្បង (ឧ. main) ហើយប្រើ git pull origin main ដើម្បីទាញកូដថ្មី។
បើអ្នកធ្វើការលើ Branch ផ្ទាល់ខ្លួន បញ្ចូលកូដពី main ទៅ Branch របស់អ្នកដោយប្រើ git merge main។
ដោះស្រាយ conflict (បើមាន) ហើយបន្ត push Branch របស់អ្នកទៅ GitHub និងបង្កើត Pull Request។
