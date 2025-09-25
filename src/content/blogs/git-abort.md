---
title: "git merge --abor"
tag: ["githup"]
---

**git merge --abort**: ពាក្យបញ្ជានេះប្រើដើម្បីបោះបង់ (cancel) ដំណើរការសម្រាប់ merge ដែលមាន conflict ឬមិនទាន់បញ្ចប់។ វាទាមទារឱ្យមានឯកសារមួយហៅថា MERGE\_HEAD ដែលបង្ហាញថាមាន merge កំពុងដំណើរការ។

### តើត្រូវធ្វើដូចម្តេចបន្ទាប់?

ព្រោះអ្នកចង់ "ត្រឡប់ទៅមុន pull" ប៉ុន្តែ git merge --abort មិនដំណើរការ អ្នកអាចប្រើវិធីដទៃដើម្បីត្រឡប់ស្ថានភាព។ នេះជាជំហាន៖

1.  **ពិនិត្យស្ថានភាពបច្ចុប្បន្ន**:
    ```bash
    git status
```
        
    *   បើមានឯកសារដែលផ្លាស់ប្តូរបន្ទាប់ពី pull អ្នកអាចឃើញនៅក្នុង "Changes not staged for commit" ឬ "Untracked files"។
        
2.  **ត្រឡប់ទៅ Commit មុន Pull**:
```bash    
git log --oneline
git reset --hard abc123
```
    *   **ចំណាំ**: នេះនឹងលុបការផ្លាស់ប្តូរទាំងអស់បន្ទាប់ពី commit នោះ។
        
3.  **ប្រើ Git Reflog (ប្រសិនមិនដឹង Commit ID)**:
```bash
git reflog
git reset --hard HEAD@{1}
```

4.  **ប្រសិនបើមានការផ្លាស់ប្តូរមុន Pull**:
    
```bash
git stash list
git stash pop
```
        
5.  **ប្រសិនបើធ្លាក់ចូល GitHub**:
```bash
git push origin main --force
```        
    *   ប៉ុន្តែសូមជួនកាលជាមួយក្រុមអ្នក ព្រោះវាអាចប៉ះពាល់អ្នកដទៃ។
        

### ហេតុផលនៃកំហុស

*   ការបញ្ជា git merge --abort មានប្រយោជន៍តែនៅពេលមាន merge conflict ដែលមិនទាន់បញ្ចប់ (មាន MERGE\_HEAD)។ បើ git pull បានបញ្ចប់ដោយស្វ័យប្រវត្តិ (គ្មាន conflict) ឬអ្នកមិនបាន merge ទេ វាមិនអាច abort បាន។
    

### គន្លឹះ

*   **ពិនិត្យមុន Pull**: ប្រើ git status និង commit ឬ stash ការផ្លាស់ប្តូរមុន pull ដើម្បីជៀសវាងបញ្ហា។
    
*   **Backup**: បង្កើតច្បាប់គម្រោងមុនធ្វើអ្វីក៏ដោយ។
    
*   **សួរក្រុម**: បើមានការផ្លាស់ប្តូរសំខាន់នៅលើ GitHub ពិនិត្យជាមួយក្រុមអ្នក។