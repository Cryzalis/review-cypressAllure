#### Review cypressAllure project

- `cyAllureRun.yml`
```yml
    - name: Deploy report
    uses: JamesIves/github-pages-deploy-action@3.1.0
    if: always()     
    with:
        ACCESS_TOKEN: ${{'secrets.ACCESS_TOKEN'}}
        BRANCH: master
```
        Usually a report is deployed to a non-master branch
<br/>
<br/>

- `config/config.config.ts`

```js
    baseUrl: 'http://automationpractice.com/index.php',
```
        baseUrl must contain root address only
<br/>
<br/>

- `login.test.ts`
```js
    loginPage.validateLoginError('Invalid email addressssss.')
```
        spelling mistake
<br/>
<br/>

- `myAccount.test.ts`
```js
    import { loginPage } from "../pages/loginPage";

    describe('My Account Functionality', () => {
        beforeEach(() => {
            cy.visit('https://google.com');
            //loginPage.launchApplication()
        })
        it('Sample Test', () => {
            console.log("This is a sample test")
        })
    })
```
        import is not used
        trash file with no meaningful tests
<br/>
<br/>

- `users.json`
```json
    "valid_credentials": {
        "emailId": "testautomation@cypresstest.com",
        "password": "Test@1234"
    },
```
        snake case and camel case 

