# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: tests\regression\TC06_Contact_Us_Form.js >> TC06_Contact_Us_Form
- Location: automation-scripts\tests\regression\TC06_Contact_Us_Form.js:20:1

# Error details

```
Error: expect(locator).toContainText(expected) failed

Locator: locator('#contact-page')
Timeout: 5000ms
- Expected substring  -  1
+ Received string     + 57

- Success! Your details have been submitted successfully.
+
+     	
+ 	    	
+ 	    		    			   			
+ 					Contact Us
+ 					
+ 							 		
+ 			    	
+     		  	
+ 	    		
+ 	    			
+ 						Note: Below contact form is for testing purpose.
+ 	    				Get In Touch
+ 						
+
+ 						
+ 						
+ 				            
+ 							
+ 				                
+ 				            
+ 				            
+ 				                
+ 				            
+ 				            
+ 				                
+ 				            
+ 				            
+ 				                
+ 				            
+ 							
+ 				                
+ 				            
+
+ 				            
+ 				                Submit
+ 				            
+ 				        
+ 						
+ 	    			
+ 	    		
+ 	    		
+ 	    			
+ 	    				Feedback For Us
+ 	    				
+ 	    					We really appreciate your response to our website.
+ 							
+ 							Kindly share your feedback with us at feedback@automationexercise.com.
+ 							
+ 							If you have any suggestion areas or improvements, do let us know. We will definitely work on it.
+ 							
+ 							Thank you
+ 	    				
+ 	    			
+     			    			
+ 	    	  
+     	

Call log:
  - Expect "toContainText" with timeout 5000ms
  - waiting for locator('#contact-page')
    5 × locator resolved to <div id="contact-page" class="container">…</div>
      - unexpected value "
    	
	    	
	    		    			   			
					Contact Us
					
							 		
			    	
    		  	
	    		
	    			
						Note: Below contact form is for testing purpose.
	    				Get In Touch
						

						
						
				            
							
				                
				            
				            
				                
				            
				            
				                
				            
				            
				                
				            
							
				                
				            

				            
				                Submit
				            
				        
						
	    			
	    		
	    		
	    			
	    				Feedback For Us
	    				
	    					We really appreciate your response to our website.
							
							Kindly share your feedback with us at [email protected].
							
							If you have any suggestion areas or improvements, do let us know. We will definitely work on it.
							
							Thank you
	    				
	    			
    			    			
	    	  
    	"
    8 × locator resolved to <div id="contact-page" class="container">…</div>
      - unexpected value "
    	
	    	
	    		    			   			
					Contact Us
					
							 		
			    	
    		  	
	    		
	    			
						Note: Below contact form is for testing purpose.
	    				Get In Touch
						

						
						
				            
							
				                
				            
				            
				                
				            
				            
				                
				            
				            
				                
				            
							
				                
				            

				            
				                Submit
				            
				        
						
	    			
	    		
	    		
	    			
	    				Feedback For Us
	    				
	    					We really appreciate your response to our website.
							
							Kindly share your feedback with us at feedback@automationexercise.com.
							
							If you have any suggestion areas or improvements, do let us know. We will definitely work on it.
							
							Thank you
	    				
	    			
    			    			
	    	  
    	"

```

```yaml
- heading "Contact Us" [level=2]:
  - text: Contact
  - strong: Us
- text: "Note: Below contact form is for testing purpose."
- heading "Get In Touch" [level=2]
- textbox "Name"
- textbox "Email"
- textbox "Subject"
- textbox "Your Message Here"
- button "Choose File"
- button "Submit"
- heading "Feedback For Us" [level=2]
- paragraph: We really appreciate your response to our website.
- paragraph:
  - text: Kindly share your feedback with us at
  - link "feedback@automationexercise.com":
    - /url: mailto:feedback@automationexercise.com
  - text: .
- paragraph: If you have any suggestion areas or improvements, do let us know. We will definitely work on it.
- paragraph: Thank you
```

# Test source

```ts
  1  | // @sentinel-codegen-clean
  2  | // ─────────────────────────────────────────────────────────────────────────────
  3  | // TC06 — Contact Us Form
  4  | //
  5  | // INFRASTRUCTURE NOTE — do NOT add dialog handlers to this file.
  6  | //   page.on('dialog', accept)  is registered globally by the Nexus page fixture
  7  | //   (automation-scripts/utils/base-fixture.js) before any test body runs.
  8  | //   Adding page.once('dialog', dismiss) here creates a conflicting second handler
  9  | //   that attempts dialog.dismiss() after the infrastructure already called
  10 | //   dialog.accept().  The dismiss() will throw "Dialog already handled" — even
  11 | //   with .catch(() => {}), this indicates a broken pattern and confuses tracing.
  12 | //
  13 | // LINTER NOTE — if your editor auto-inserts unused POM imports or a dismiss
  14 | //   handler, check your VS Code snippet library and remove the conflicting entry,
  15 | //   or add this file to your formatter's ignore list.
  16 | // ─────────────────────────────────────────────────────────────────────────────
  17 | import { test }   from '../../utils/base-fixture.js';
  18 | import { expect } from '@playwright/test';
  19 | 
  20 | test('TC06_Contact_Us_Form', async ({ page }) => {
  21 |     await page.goto('https://automationexercise.com/');
  22 |     await page.getByRole('link', { name: /Contact us/i }).click();
  23 |     await page.getByRole('textbox', { name: 'Name' }).fill('sentinel');
  24 |     await page.getByRole('textbox', { name: 'Email', exact: true }).fill('sentinel@gmail.com');
  25 |     await page.getByRole('textbox', { name: 'Subject' }).fill('nothing');
  26 |     await page.getByRole('textbox', { name: 'Your Message Here' }).fill('hi');
  27 |     await page.getByRole('button', { name: 'Submit' }).click();
  28 |     await expect(page.locator('#contact-page'))
> 29 |         .toContainText('Success! Your details have been submitted successfully.');
     |          ^ Error: expect(locator).toContainText(expected) failed
  30 | });
  31 | 
```