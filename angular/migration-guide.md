
# Angular migration guide

1. Open https://angular.dev/update-guide
2. Select `from` and `to` versions
3. Select `Advanced` application complexity
4. Check `I use Angular Material`
5. Click `Show` button
6. Go over each item executing if needed

### Vesrions conflict issues
Note that some of the steps proposed by the angular upgrade guide might not work as expected. 

For example the following update line didn't work on my local environemnt because of version conflicts:
`npx @angular/cli@10 update @angular/core@10 @angular/cli@10`

The workaround (example of migratin from version 9 to 10):
1. npm i --save-dev @angular/cli@10
2. commit
3. npm i --save-dev @angular-devkit/build-angular@0.1002.3 // older builder-angular version was blocking the typescrit update
4. commit
5. ng update @angular/core@10
6. commit
7. ng update @angular/material@10
8. commit

### 'Automatic' update issue
Pay attention to the lines in the migration guide like 
`Angular now requires TypeScript 4.2. ng update will update you automatically`

It **might NOT** update automatically! You might need to increase the mentioned version manually.



