### i18next
---
https://github.com/i18next/i18next

```sh
npm install i18next --save
yarn add i18next
```

```js
import i18next from 'i18next';
i18next.init({
  lng: 'en',
  debug: true,
  resources: {
    en: {
      translation: {
        "key": "hello world"
      }
    }
  }, function(err, t){
   document.getElementById().innerHTML = i18next.t('key');
  }
});

i18next.init({
  fallbackLng: 'en',
  ns: ['file1', 'file2'],
  defaultNS: 'file1',
  debug: true
}, (err, t) => {
  if(err) return console.log('something went wrong loading', err);
  t.('key');
});

import i18next from 'i18next';
import Backend from 'i18next-xhr-backend';
import Cache from 'i18next-localstorage-cache';
import postProcessor from 'i18next-sprintf-postprocessor';
import LanguageDetector from 'i18next-browser-languagedetector';
i18next
  .user(Backend)
  .use(Cache)
  .use(LanguageDetector)
  .use(postProcessor)
  .init(options, callback);
  
i18next.t('my.key');
i18next.t(['unknown.key', 'my.key']);

i18next.exists('my.key');

const de = i18next.getFiexedT('de');
de('myKey');
const anotherNamespace = i18next.getFiexedT(null, 'anotherNamespace');
anotherNamespace('anotherNamespaceKey');

i18next.changeLanguage('en', (err, t) => {
  if(err) return console.log('something went wrong loading', err);
  t.('key');
});

i18next.init({
  fallbackLng: ["es", "fr", "en-US", "dev"]
});
i18next.changeLanguage("en-US-xx");
i18next.languages;
i18next.changeLanguage("de-DE");
i18next.languages;

i18next.loadNamespaces('myNamespace', (err, t) => { /* */ });
i18next.loadNamespaces(['myNamespace1', 'myNamespace2'], (err, t) => { /* */ });

i18next.loadLanguages('de', (err, t) => {/**/});
i18next.loadLanguages(['de', 'fr'], (err, t) => {/**/})

const newInstance = i18next.createInstance({
  fallbacklng: 'en',
  ns: ['file1', 'file2'],
  defaultNS: 'file1',
  debug: true
}, (err, t) => {
  if(err) return console.log('someghing went wrong loading', err);
  t('key');
});
const newInstance = i18next.createInstance();
newInstance.init({
  fallbackLng: 'en',
  ns: ['file1', 'file2'],
  defaultNS: 'file1',
  debug: true
}, (err, t) => {
  if(err) return console.log('something went wrong loading', err);
  t('key');
});
```

```
```


