1. C+Shift+P > Create Project > Account Customization Project
2. to manifest.xml add the below (to allow access to some accounting list records like Transaction Status if we are creating a field which will source that list)
   `<dependencies>`
   `<features>`
   `<feature required="true">`ACCOUNTING `</feature>`
   `</features>`
   `</dependencies>`
3. C+Shift+P > Setup relevant netsuite account (will auto create/update project.json)
4. C+Shift+P > Deploy Project

Note - if there are any custom dependenacies like:

1. customlist_pr_status (a sources value for custbody_pr_status_pf) then C+Shift+P > Import Objects >customlist > customlist_pr_status - this will create customlist_pr_status.xml in the Object folder (this will be pushed back so don't change it if not required)
2. custom subtab then C+Shift+P > Import Objects > subtab > custtab_234_5046553_447 - this will create custtab_234_5046553_447.xml in the object folder (this will be pushed back so don't change it if not required))


-----------UPDATE-----------
Ignore the above, auto add dependencies: simply do CTRL+P suitecloud: Add Dependency References to the Manifest and all detected dependencies will be auto added!
