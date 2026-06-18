# 🚨 Incident Forensic Report: TC06_Contact_Us_Form

## 📊 Executive Summary
- **Test Case ID:** TC06_Contact_Us_Form 
- **Browser Engine:** firefox
- **Timestamp (UTC):** 2026-06-18T17:12:01.526Z
- **Status:** FAILED ❌
- **Severity:** HIGH · **Clasificación:** NETWORK_INFRASTRUCTURE

## 🔍 Context of the Failure (The "Why")
**System Error Triggered:**
```text
Error: [2mexpect([22m[31mlocator[39m[2m).[22mtoContainText[2m([22m[32mexpected[39m[2m)[22m failed

Locator: locator('#contact-page')
Timeout: 5000ms
[32m- Expected substring  -  1[39m
[31m+ Received string     + 57[39m

[32m- [7mSuccess! Your details [27mha[7mv[27me [7mbeen submitted successfully.[27m[39m
[31m+[39m
[31m+ [43m    	[49m[39m
[31m+ [43m	    	[49m[39m
[31m+ [43m	    		    			   			[49m[39m
[31m+ 					Contact Us[39m
[31m+ [43m					[49m[39m
[31m+ [43m							 		[49m[39m
[31m+ [43m			    	[49m[39m
[31m+ [43m    		  	[49m[39m
[31m+ [43m	    		[49m[39m
[31m+ [43m	    			[49m[39m
[31m+ 						Note: Below contact form is for testing purpose.[39m
[31m+ 	    				Get In Touch[39m
[31m+ [43m						[49m[39m
[31m+[39m
[31m+ [43m						[49m[39m
[31m+ [43m						[49m[39m
[31m+ [43m				            [49m[39m
[31m+ [43m							[49m[39m
[31m+ [43m				                [49m[39m
[31m+ [43m				            [49m[39m
[31m+ [43m				            [49m[39m
[31m+ [43m				                [49m[39m
[31m+ [43m				            [49m[39m
[31m+ [43m				            [49m[39m
[31m+ [43m				                [49m[39m
[31m+ [43m				            [49m[39m
[31m+ [43m				            [49m[39m
[31m+ [43m				                [49m[39m
[31m+ [43m				            [49m[39m
[31m+ [43m							[49m[39m
[31m+ [43m				                [49m[39m
[31m+ [43m				            [49m[39m
[31m+[39m
[31m+ [43m				            [49m[39m
[31m+ 				                Submit[39m
[31m+ [43m				            [49m[39m
[31m+ [43m				        [49m[39m
[31m+ [43m						[49m[39m
[31m+ [43m	    			[49m[39m
[31m+ [43m	    		[49m[39m
[31m+ [43m	    		[49m[39m
[31m+ [43m	    			[49m[39m
[31m+ 	    				Feedback For Us[39m
[31m+ [43m	    				[49m[39m
[31m+ 	    					We really appreciate your response to our website.[39m
[31m+ [43m							[49m[39m
[31m+ [7m							Kindly s[27mha[7mr[27me [7myour feedback with us at feedback@automationexercise.com.[27m[39m
[31m+ [43m							[49m[39m
[31m+ 							If you have any suggestion areas or improvements, do let us know. We will definitely work on it.[39m
[31m+ [43m							[49m[39m
[31m+ 							Thank you[39m
[31m+ [43m	    				[49m[39m
[31m+ [43m	    			[49m[39m
[31m+ [43m    			    			[49m[39m
[31m+ [43m	    	  [49m[39m
[31m+ [43m    	[49m[39m

Call log:
[2m  - Expect "toContainText" with timeout 5000ms[22m
[2m  - waiting for locator('#contact-page')[22m
[2m    - locator resolved to <div id="contact-page" class="container">…</div>[22m
[2m    - unexpected value "[22m
[2m    	[22m
[2m	    	[22m
[2m	    		    			   			[22m
[2m					Contact Us[22m
[2m					[22m
[2m							 		[22m
[2m			    	[22m
[2m    		  	[22m
[2m	    		[22m
[2m	    			[22m
[2m						Note: Below contact form is for testing purpose.[22m
[2m	    				Get In Touch[22m
[2m						[22m
[2m[22m
[2m						[22m
[2m						[22m
[2m				            [22m
[2m							[22m
[2m				                [22m
[2m				            [22m
[2m				            [22m
[2m				                [22m
[2m				            [22m
[2m				            [22m
[2m				                [22m
[2m				            [22m
[2m				            [22m
[2m				                [22m
[2m				            [22m
[2m							[22m
[2m				                [22m
[2m				            [22m
[2m[22m
[2m				            [22m
[2m				                Submit[22m
[2m				            [22m
[2m				        [22m
[2m						[22m
[2m	    			[22m
[2m	    		[22m
[2m	    		[22m
[2m	    			[22m
[2m	    				Feedback For Us[22m
[2m	    				[22m
[2m	    					We really appreciate your response to our website.[22m
[2m							[22m
[2m							Kindly share your feedback with us at [email protected].[22m
[2m							[22m
[2m							If you have any suggestion areas or improvements, do let us know. We will definitely work on it.[22m
[2m							[22m
[2m							Thank you[22m
[2m	    				[22m
[2m	    			[22m
[2m    			    			[22m
[2m	    	  [22m
[2m    	"[22m
[2m    12 × locator resolved to <div id="contact-page" class="container">…</div>[22m
[2m       - unexpected value "[22m
[2m    	[22m
[2m	    	[22m
[2m	    		    			   			[22m
[2m					Contact Us[22m
[2m					[22m
[2m							 		[22m
[2m			    	[22m
[2m    		  	[22m
[2m	    		[22m
[2m	    			[22m
[2m						Note: Below contact form is for testing purpose.[22m
[2m	    				Get In Touch[22m
[2m						[22m
[2m[22m
[2m						[22m
[2m						[22m
[2m				            [22m
[2m							[22m
[2m				                [22m
[2m				            [22m
[2m				            [22m
[2m				                [22m
[2m				            [22m
[2m				            [22m
[2m				                [22m
[2m				            [22m
[2m				            [22m
[2m				                [22m
[2m				            [22m
[2m							[22m
[2m				                [22m
[2m				            [22m
[2m[22m
[2m				            [22m
[2m				                Submit[22m
[2m				            [22m
[2m				        [22m
[2m						[22m
[2m	    			[22m
[2m	    		[22m
[2m	    		[22m
[2m	    			[22m
[2m	    				Feedback For Us[22m
[2m	    				[22m
[2m	    					We really appreciate your response to our website.[22m
[2m							[22m
[2m							Kindly share your feedback with us at feedback@automationexercise.com.[22m
[2m							[22m
[2m							If you have any suggestion areas or improvements, do let us know. We will definitely work on it.[22m
[2m							[22m
[2m							Thank you[22m
[2m	    				[22m
[2m	    			[22m
[2m    			    			[22m
[2m	    	  [22m
[2m    	"[22m

```

## 📍 Point of Failure (Stack Trace)
```javascript
Error: [2mexpect([22m[31mlocator[39m[2m).[22mtoContainText[2m([22m[32mexpected[39m[2m)[22m failed

Locator: locator('#contact-page')
Timeout: 5000ms
[32m- Expected substring  -  1[39m
[31m+ Received string     + 57[39m
```

## 🛡️ Security & Network Telemetry
- **Network Errors (400+):** 3 endpoints failed during execution.
- **Missing CSP Headers:** 126 assets loaded without Content-Security-Policy.

## 📁 Attached Evidence
- **Visual Capture:** `screenshot.png`
- **Forensic Video:** `video.webm`
- **Raw Telemetry:** `telemetry.json`
- **Folder:** `evidence/bug-reports/firefox/TC06__contact_us_form_*/`