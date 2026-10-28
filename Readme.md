
# Vue DataTables playground

This app is a simple Vue application which is used for development and testing of the [Vue DataTables component](https://github.com/DataTables/Vue).

You can clone this repo and use:

```
npm install
npm run dev
```

to start the application and be able to see a few simple DataTables in Vue.


## Local development

For development with the [Vue DataTables component](https://github.com/DataTables/Vue), clone that repo as well, then:

```
npm install
npm run build
npm link
```

Next in this playground repo you can:

```
npm link datatables.net-vue3
npm run dev
```

That will use your local development version of the DataTables Vue component and run the app with those files.


## General use

You will not need this repo for general use of the DataTables Vue component! Instead, follow the [instructions in the documentation](https://datatables.net/manual/components/vue/) to install and use in your own Vue applications. This repo is intended for local development and testing only.
