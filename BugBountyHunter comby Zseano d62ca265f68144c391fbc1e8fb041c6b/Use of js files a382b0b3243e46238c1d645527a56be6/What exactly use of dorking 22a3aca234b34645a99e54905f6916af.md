# What exactly use of dorking ?

# Google :

**Just Ask right Question** 

Use of public search engines to find  the public data about your target. They do spidering for you.

1. `**site:example.com inurl:&**` - find parameters, scrape and try on every endpoint you discover.
2. **Site:example.com ext:php** `[jsp, asp, aspx, xhtml, txt]`  - Discovering  content on their sites, maybe sometimes old files that are indexed sometimes ago. Helpful if to get an insight into what types of payloads or bugs you should focus on [ex - Seeing a lots of php ? probably going to find xss quite easily]
3.  **Site:example.com inrul:admin [ login ,  register, signup , redirect , return URL GET creative!!! The possibilities  are endless . Ask and you you should receive] Finding functionality to play with. The common wordlist from seclist.** 

New is **gdpr stuff for managing your cookies.**

 ****

# GitHub :

**Just Ask Right Questions**

- Searching through devs code finding potential exposed staging servers, internal api's (think swagger) Even test code sometimes.

**"Company" stage** ( staging, stg, dev, prod, qa, swagger) - Have any devs pushed code containing staging information or any swagger uri exposed ? Even if those domains can't be accessed from their network save if for SSRF in future ?

 **"Company" apiKey** (api Secret, x-api-key, apidocs, /api/ /internal/api/)  - Any exposed api Keys? Find API docs and see what key is used for. Maybe an internal key is leaked Which bypasses rate limiting for example (Had a case in which login flow is used ?client_id= which was always same. Found another on github which bypassed 2FA).

**"Company"** [Keyword] - Looking for specific features/services such as login, signup, registration, admin, adminstartor , appspot (staging Servers ?) , firebase , password , testuser, testing )