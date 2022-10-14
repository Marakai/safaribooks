### Get cookie in Chrome

(must user Chrons for ANZ SSO to work)

- Login as usual to https://learning.oreilly.com/
- Open the developer tools with F12
- Go to Network tab in the developer tools
- Access the profile page in the browser: https://learning.oreilly.com/profile/
- Open Chrome DevTools console
- Paste this script into console of Chrome DevTools and get cookies.

```
console.log(JSON.stringify(document.cookie.split(';').map(c => c.split('=')).map(i => [i[0].trim(), i[1].trim()]).reduce((r, i) => {r[i[0]] = i[1]; return r;}, {})))
```

- Copy-paste result into `cookies.json` inside the script directory
