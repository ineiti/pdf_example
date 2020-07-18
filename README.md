# pdf-example

This is to get typescript bindings in mozilla's pdf.js library

https://github.com/mozilla/pdf.js/pull/12102

The pdf.js and pdf_example need to be in the same directory:

```bash
mkdir tmp; cd tmp
git clone --depth=1 https://github.com/ineiti/pdf.js -b add_types_annotations
( cd pdf.js && npm ci && gulp generic && npx tsc -p . )
git clone --depth=1 https://github.com/ineiti/pdf_example
cd pdf_example && npm ci && npm run start
```

The entry point is in `src/app/home/home.component.ts`
