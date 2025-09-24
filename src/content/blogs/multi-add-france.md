---
title: "Pull Request ដំណើរការយ៉ាងណា នៅពេលអ្នក Push Branch ច្រើន?"
tag: ["githup"]
---

### **តើ Pull Request ដំណើរការយ៉ាងណា នៅពេលអ្នក Push Branch ច្រើន?**

នៅពេលអ្នកប្រើពាក្យបញ្ជា៖

```bash
git push origin feature/add-login-page
git push origin feature/add-user-profile
```
នេះមានន័យថាអ្នកបានបង្ហោះ Branch ទាំងពីរនេះ (feature/add-login-page និង feature/add-user-profile) ទៅ Remote Repository នៅលើ GitHub។ ប៉ុន្តែ នៅពេលអ្នកបង្កើត **Pull Request** នេះជាអ្វីដែលអ្នកត្រូវយល់៖

1.  **Pull Request ត្រូវបានបង្កើតជាលក្ខណៈបុគ្គលសម្រាប់ Branch នីមួយៗ**:
    
    *   Pull Request នីមួយៗគឺភ្ជាប់ជាមួយ **Branch មួយ** និងស្នើសុំឱ្យបញ្ចូល (merge) កូដពី Branch នោះទៅសាខាចម្បង (ឧ. main ឬ develop)។
        
    *   ឧទាហរណ៍៖
        
        *   បើអ្នកបង្កើត Pull Request សម្រាប់ feature/add-login-page វានឹងរួមបញ្ចូលតែកូដនៅក្នុង Branch នោះប៉ុណ្ណោះ។
            
        *   បើអ្នកបង្កើត Pull Request សម្រាប់ feature/add-user-profile វានឹងរួមបញ្ចូលតែកូដនៅក្នុង Branch នោះ។
            
    *   **ចម្លើយចំពោះសំណួររបស់អ្នក**: កូដទាំងអស់នៅក្នុង Branch ទាំងពីរនឹងមិនទៅជាមួយ Pull Request **តែមួយ** នោះទេ។ អ្នកត្រូវបង្កើត Pull Request **ដាច់ដោយឡែក** សម្រាប់ Branch នីមួយៗ។
        
2.  **ករណីដែលកូដទាំងអស់អាចទៅជាមួយគ្នា**:
    
    *   បើអ្នកចង់ឱ្យកូดនៅក្នុង feature/add-login-page និង feature/add-user-profile ត្រូវបញ្ចូលទៅសាខាចម្បងជាមួយគ្នា អ្នកត្រូវ៖
        
        *   បញ្ចូល (merge) Branch ទាំងនេះទៅក្នុង Branch មួយផ្សេងទៀត (ឧ. Branch ដែលប្រមូលផ្តុំគ្រប់មុខងារទាំងអស់ ដូចជា feature/combined-changes) មុននឹងបង្កើត Pull Request។
            
        *   ឬបង្កើត Pull Request ដាច់ដោយឡែកសម្រាប់ Branch នីមួយៗ ហើយ merge ពួកវាទៅ main ម្តងមួយៗ។
            
3.  **បើអ្នកបង្កើត Pull Request បន្ទាប់ពី Push**:
    
    *   នៅលើ GitHub នៅពេលអ្នកបង្ហោះ Branch (ឧ. feature/add-login-page) អ្នកនឹងឃើញជម្រើស **Compare & pull request** សម្រាប់ Branch នោះ។ អ្នកត្រូវបង្កើត Pull Request ដាច់ដោយឡែកសម្រាប់ feature/add-login-page និង feature/add-user-profile។
        
    *   កូដនៅក្នុង Branch នីមួយៗនឹងនៅដាច់ដោយឡែក ហើយមិនមានការលាយឡំជាមួយគ្នាទេ លុះត្រាតែអ្នក merge Branch ទាំងនេះទៅក្នុង Branch តែមួយមុននឹងបង្កើត Pull Request។
        

### **ឧទាហរណ៍ជាក់ស្តែង**

សន្មត់ថាអ្នកបាន push Branch ទាំងពីរ៖

```bash
git push origin feature/add-login-page
git push origin feature/add-user-profile
```
#### **ជំហានបង្កើត Pull Request:**

1.  **ចូលទៅ GitHub**:
    
    *   នៅលើ Repository របស់អ្នក អ្នកនឹងឃើញសារថា feature/add-login-page និង feature/add-user-profile ត្រូវបានបង្ហោះ។
        
    *   ចុចលើ **Compare & pull request** សម្រាប់ feature/add-login-page។
        
    *   បំពេញព័ត៌មាន (ឧ. ពន្យល់ថា Branch នេះធ្វើអ្វី) ហើយបង្កើត Pull Request។
        
    *   ធ្វើដូចគ្នាសម្រាប់ feature/add-user-profile។
        
2.  **លទ្ធផល**:
    
    *   អ្នកនឹងមាន Pull Request ពីរ៖
        
        *   Pull Request ទី 1: សម្រាប់ feature/add-login-page → បញ្ចូលទៅ main។
            
        *   Pull Request ទី 2: សម្រាប់ feature/add-user-profile → បញ្ចូលទៅ main។
            
    *   កូដទាំងអស់នៅក្នុង Branch ទាំងពីរនឹង**មិនទៅជាមួយ Pull Request តែមួយ** នោះទេ។ ពួកវាត្រូវបានគ្រប់គ្រងដាច់ដោយឡែក។
        
3.  **បើចង់បញ្ចូលកូដទាំងអស់ជាមួយគ្នា**:
    
    *   បង្កើត Branch ថ្មីមួយ (ឧ. feature/combined-changes)៖ 
```bash
git checkout -b feature/combined-changes
```        

Merge Branch ទាំងពីរទៅក្នុង Branch ថ្មីនេះ៖ 
```bash
git merge feature/add-login-page
```
*   git merge feature/add-user-profile
    
*   ដោះស្រាយ **conflict** (បើមាន)។
    
*   Push Branch ថ្មី៖ 
```bash
git push origin feature/combined-changes
```    
*   បង្កើត Pull Request មួយសម្រាប់ feature/combined-changes ដែលនឹងរួមបញ្ចូលកូដទាំងអស់ពី Branch ទាំងពីរ។
    

### **សរុប**

*   បើអ្នក **push** Branch ច្រើន (ឧ. feature/add-login-page និង feature/add-user-profile) ហើយបង្កើត Pull Request នោះ Pull Request នីមួយៗនឹងភ្ជាប់ជាមួយ Branch មួយៗ។ កូដទាំងអស់នឹង**មិនទៅជាមួយ Pull Request តែមួយ** ទេ លុះត្រាតែអ្នក merge Branch ទាំងនោះទៅក្នុង Branch តែមួយមុននឹងបង្កើត Pull Request។
    
*   បើអ្នកចង់ឱ្យកូដទាំងអស់នៅក្នុង Branch ទាំងពីរទៅជាមួយ Pull Request តែមួយ អ្នកត្រូវបញ្ចូល Branch ទាំងនោះទៅ Branch ថ្មីមួយសិន។
    
*   បើ Branch ទាំងនេះត្រូវបាន **merge** ទៅ main ដោយ Pull Request ដាច់ដោយឡែក កូដទាំងអស់នឹងនៅតែទៅដល់ main ដែរ ប៉ុន្តែតាមរយៈ Pull Request ផ្សេងគ្នា។
    

### **គន្លឹះបន្ថែម**

**បន្ទាប់ពី merge** Pull Request នីមួយៗ ជាទម្លាប់ល្អ គួរលុប Branch នោះ៖ 
```bash
git push origin --delete feature/add-login-page
git push origin --delete feature/add-user-profile
```
    
*   បើមាន **conflict** នៅពេល merge Branch ច្រើនទៅ Branch តែមួយ អ្នកត្រូវដោះស្រាយ conflict ដោយកែកូដដោយផ្ទាល់ ឬប្រើឧបករណ៍ដូចជា VS Code។
    
*   ប្រើឈ្មោះ Branch ដែលច្បាស់លាស់ (ឧ. feature/add-login-page ជំនួសឱ្យ feature/login) ដើម្បីជៀសវាងការភាន់ច្រឡំ។