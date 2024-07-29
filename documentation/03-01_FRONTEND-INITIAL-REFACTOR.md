# 🔥 Initial Refactorization of Frontend Application (NextJS Version)

## Changes in `frontend/src/app/layout.tsx`

![Refactored Layout Code](/documentation/images/layout-refactored.png)

## Image Refactorization

1. Remove the `favicon.ico` file  from the `src/app` folder

2. Navigate to [Favicon Icon Generator](https://www.silisoftware.com/tools/favicon.php)

3. Upload Your Image by clicking `Choose File` Button

4. Select Dimension Size

5. Click `Create Icon` Button

6. Select `Download` Button to download the `favicon.ico` file

7. Place the `favicon.ico` file in the `public` folder as this need to be displayed as the Browser Icon

8. Remove `next.svg` file from `public` folder

9. Remove `vercel.svg` file from `public` folder

## Change in `page.tsx`

1. Remove every child HTML Elements inside `<main>` HTML Semantic Tag Element

2. Remove Unnecessary Imports

3. Remove `className` attribute from `<main>` HTML Semantic Tag Element

![Refactored Page Code](/documentation/images/page-refactored.png)