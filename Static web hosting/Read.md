# Follow these steps to host your static website on AWS S3:
1. Access AWS Console
2. Go to your AWS console and search v    for "S3" in the search bar, then       select "S3" when it appears.
3. Create a Bucket
4. Click on "Create bucket."
   Provide a unique "Bucket name" for     your website.
   Configure Bucket Settings
5. Unselect "Block all public             access" to allow internet users.       to access your website.
6. Click on "Create bucket" at the        bottom.
   Select Your Bucket
7. Once created, select your bucket.      from the list.
8. Configure Static Web Hosting
9. Under the "Properties" tab, scroll.    down to "Static web hosting" and.      click on "Edit."
10. Click on "Enable" and select "Host     a static website." Choose the         default home page (index document)     for your site.
11. Set Up Error Handling (Optional)
12. Enter the names of the index.          document and error document (if.       needed), then click "Save changes."
13. Endpoint Creation
   When "Static website hosting" is       enabled, the bucket endpoint is.        created.
14. Bucket Policy for File Access
    Create a bucket policy to enable.      access to the files.
    Navigate to the "Permissions" tab.     and under the "Bucket policy"          section, enter the provided.           policy, ensuring to change the.        Resource to your bucket's ARN.         followed by "/*".
15. Upload Your Website
    Create and upload your website.        files, including the "index.html"      file as specified in step 8.
16. Final Configuration
    Navigate to the "Properties" tab.      and load the bucket's endpoint.        The "index.html" file will serve as the home page.
In case of an error (e.g., the index file is not available), the "error.html" page will be returned at the endpoint.
