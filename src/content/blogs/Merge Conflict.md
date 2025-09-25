---
title: "Merge Conflict"
tag: ["githup"]
---

ជំហានដើម្បីដោះស្រាយ **Merge Conflict**

ជម្រើសទី **1:** ដោះស្រាយតាម **Web Editor** នៅលើ **GitHub**

1.  ចុច **"Resolve conflicts"**:
    
    *   នៅលើផ្ទាំង GitHub ដែលអ្នកបានផ្ទុកមក ចុចប៊ូតុង **"Resolve conflicts"**។
        
2.  កែប្រែ **Conflict**:
    
    *   GitHub នឹងបង្ហាញឯកសារដែលមាន conflict ជាមួយនឹងសញ្ញា <<<<<<<, =======, >>>>>>> ដែលបង្ហាញភាពខុសគ្នារវាង branch របស់អ្នក និង branch ដែលអ្នកចង់ merge ទៅ។
        
    *   ជ្រើសយកកូដដែលអ្នកចង់រក្សា (អាចជាកូដពី branch របស់អ្នក ឬ branch ផ្សេង) ហើយលុបសញ្ញាទាំងនេះ។
        
    *   ឧទាហរណ៍៖ text<<<<<<< HEAD
        
    *   // កូដពី branch របស់អ្នក
        
    *   \=======
        
    *   // កូដពី branch ផ្សេង
        
    *   \>>>>>>> branch-nameកែជា៖ text// កូដដែលអ្នកជ្រើស
        
3.  រក្សាទុក:
    
    *   បន្ទាប់ពីកែរួច ចុច **"Mark as resolved"** សម្រាប់ឯកសារនីមួយៗ។
        
4.  **Commit** នៅលើ **Web**:
    
    *   ចុច **"Commit merge"** ដើម្បីរក្សាទុកការផ្លាស់ប្តូរនៅលើ branch របស់អ្នក។
        
5.  **Merge Pull Request**:
    
    *   វិលទៅផ្ទាំង Pull Request ហើយចុច **"Merge pull request"** បន្ទាប់ពី conflict ត្រូវបានដោះស្រាយ។
        

ជម្រើសទី **2:** ដោះស្រាយតាម **Command Line (**ផ្អែកលើកុំព្យូទ័រ**)**

1.  **Pull** ដើម្បីទាញ **Conflict** មក **Local**:
    
    *   បើ branch របស់អ្នកនៅលើ local (ឧ. restor-login-page) ធ្វើ pull ដើម្បីទាញ conflict មក៖ 
    ```bash
    git pull origin restor-login-page
    ```    
    *   បើ branch ផ្សេង (ឧ. dev) ដែលអ្នកចង់ merge ទៅ ធ្វើ៖ 
    ```bash
    git pull origin dev
    ```    
2.  ដោះស្រាយ **Conflict**:
    
    *   Git នឹងបង្ហាញឯកសារដែលមាន conflict។ បើកឯកសារ (ឧ. src/App.jsx, src/routes/AdminRoutes.jsx) ដោយ editor របស់អ្នក។
        
    *   កែប្រែផ្នែកដែលមានសញ្ញា <<<<<<<, =======, >>>>>>> ដូចឧទាហរណ៍ខាងលើ។
        
    *   សន្សំ (save) ឯកសារបន្ទាប់ពីកែ។
        
3.  **Mark Conflict** ថាបានដោះស្រាយ:
    
    *   បញ្ជូលឯកសារទៅ staging area៖ 

    ```bash
    git add src/App.jsx src/pages/adminDashboard/layout/AuthLayout.jsx src/routes/AdminRoutes.jsx
    ```    
    *   ឬបញ្ជូលរាល់ឯកសារ៖ bashgit add .
        
4.  **Complete Merge**:
    
    *   បញ្ចប់ដំណើរការសម្រាប់ merge៖ 
    ```bash
    git commit
    ```    
    *   Git នឹងប្រើសារដែលបានរៀបចំរួច (merge commit message)។
        
5.  **Push** ទៅ **GitHub**:
    
    *   Push ការផ្លាស់ប្តូរទៅ branch របស់អ្នក៖ 
    ```bash
    git push origin restor-login-page
    ```    
    *   បន្ទាប់មកអ្នកអាចផ្ទុក Pull Request ឡើងវិញ ឬ merge ដោយផ្ទាល់នៅលើ GitHub។
        

ឧទាហរណ៍ជាក់ស្តែង **(Command Line)**

សន្មត់ថាអ្នកស្ថិតនៅ branch restor-login-page និងចង់ merge ទៅ dev៖

1.  Pull ពី dev: bashgit pull origin dev
    
2.  កែឯកសារ (ឧ. src/App.jsx) ដោះស្រាយ conflict៖
    
    *   លុបសញ្ញា <<<<<<<, =======, >>>>>>> និងជ្រើសកូដ។
        
3.  Add ឯកសារ៖ bashgit add src/App.jsx
    
4.  Commit និង Push: bashgit commit
    
5.  git push origin restor-login-page
    

ការពិភាក្សា

*   ជ្រើសកូដណា**?**: បើមិនប្រាកដថាត្រូវរក្សាកូដណា (ពី branch អ្នក ឬ dev) សួរក្រុមអ្នក ឬប្រើកូដថ្មីបំផុតដែលអ្នកបានជួសជុល។
    
*   **Backup**: បង្កើតច្បាប់គម្រោងមុនដោះស្រាយ conflict ដើម្បីជៀសវាយប្រហាត់។
    

••សួរជំនួយ: បើមិនសម្រេចចិត្តបាន សួរក្រុមអ្នកឬអ្នកអភិវឌ្ឍន៍ដែលមានបទពិសោធន៍។