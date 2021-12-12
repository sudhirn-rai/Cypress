# Cypress
Test BY Pierce
Let's assume that the test subjects are two domains www.24mx.pl and www.24mx.ie. 
Please create design of automatic tests using the Cypress tool https://www.cypress.io/, which will allow you to perform 5 the same (freely selected) test cases on both domains. Place the code in the public repository on GitHub.



Solution:

INstall NPM node, cypress and Microsoft visual studio
Created package.json file
create your project java script file in code

Use this command to run test runner  - node_modules/.bin/cypress open

// Test
describe('Pierce official web page', function(){
    it('Verify title of the page-potitive', function(){
        cy.visit('https://www.24mx.ie/')
        cy.title().should('eq', "Ireland's Largest Online Motocross Store! - 24mx.ie")
        
    })
    it('Verify title of the page-negative', function(){
        cy.visit('https://www.24mx.ie/')
        cy.title().should('eq', "Ireland's smallest Online Motocross Store! - 24mx.ie")
    })

    //Click menu item
    it('Click meny buttoverify search tablet', function () {
        cy.visit('https://www.24mx.ie/')
            cy.get('#search-tablet').click();
        })

     // searvch mobile   
        it('verify search mobile', function () {
            cy.visit('https://www.24mx.ie/')
            cy.get('#search-mobile').click();
        })

     // class usage
       it('Verify mobile header hutton icon', function () {
        cy.visit('https://www.24mx.ie/')
        cy.get('.m-header-button_number').click();
    })   
})
