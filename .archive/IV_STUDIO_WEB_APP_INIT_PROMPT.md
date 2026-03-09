ARCHIVED IV STUDIO WEB APP PRD PROMPT:

I need help filling in the prompt from Step 1 of the attached CREATE_PRD_PROMPTS.md file from the following description that I would have sent it normally:

```
The main goal of this app is to improve the customer service functions of a board game company (IV Studio; Website: `https://shop.iv.studio/`) by automating some quick customer request functions like change address, check order status, and cancel duplicate orders. Eventually, we will try to automate more of the complex customer service functions as much as we can, but for now, we’ll focus on the easy to accomplish requests.

The current user flow of how a customer submits a support ticket is through the following link: `https://ivstudio.zendesk.com/hc/en-us/requests/new`. However, this link will eventually be deprecated since the IV Studio is moving away from using Zendesk. They are potentially moving to Gorgias, a different customer support software (`https://www.gorgias.com/ecommerce/shopify`), so the support ticket inflow system could originate there. They could also end up using an in-app support ticket inflow system to make the integration flow smoother. Regardless, a customer would click the support link from this web page: ` https://shop.iv.studio/pages/contact`.

To start, the main product feature flow of the app is as follows:
-	Use Claude Code as a base level AI to read incoming support tickets created in-app (or through the Gorgias API: `https://docs.gorgias.com/en-US/rest-api-208286`) [ANTHROPIC API INTEGRATION NEEDED, GORGIAS API INTEGRATION OPTIONAL]
-	If provided, look up matching order numbers from the support ticket to find the corresponding order using Shopify API requests. Fallback to using the requestor’s email if the order number is not provided. Fallback to reply to the request email to ask for more order details if order still can’t be found [SHOPIFY INTEGRATION NEEDED].
-	Based on preset rules (from the Rules module creating a Rules object), classify the request with a tag of commonly requested customer tasks to identify easy to complete tasks vs more manual and custom customer service tasks
-	Investigate what a solution would look like to resolve the customer support ticket based on the tag classification of the request
-	If the solution has a high confidence rating of being the correct course of action to resolve the support ticket automatically, complete the necessary step automatically based on the tag classification of the request (e.g. update customer address through Shopify API integration).
-	For solutions below a specific confidence rating threshold, flag it for review and present your proposed solution to resolve the support ticked for a IV Studio customer support agent to review
-	Provide in-app abilities for the IV Studio customer support agent to resolve support tickets within the app.

We’ll also need a GMAIL INTEGRATION for internal IV Studio employees to login to their account.

Who will use it (user roles): IV Studio employees, IV Studio customer support agents, IV Studio customers

Core features and capabilities:
-	Gmail Oauth Sign In Flow
-	Company Support Ticket Management Pages (CRUD)
-	Customer Facing Support Ticket Input Page
-	Claude Code Integration to Review Incoming Support Tickets for Classification
-	Shopify Integration to Sync with Existing Company Data

To just create a proof of concept for the app, start with just automating the process of someone wanting to change their email address and/or their physical address. Create just the access point for the support link found in the ` https://shop.iv.studio/pages/contact` web page so that a customer can create a support ticket directly in-app. However, still provide a plan for the access point through a webhook from the Gorgias API (`https://docs.gorgias.com/en-US/rest-api-208286`) triggering our app to create enhanced automations more than the capabilities that Gorgias can provide by itself.

DUE TO THE LARGE SCOPE OF THIS PROJECT, DECOMPOSE YOUR INITIAL PRD FILE INTO MULTIPLE SEPARATE PRD FILES TO BE RUN SEQUENTIALLY.
```
