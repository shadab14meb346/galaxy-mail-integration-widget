### How to use the widget?

- Include the this script tag in your application

```javascript
<script
	type="text/javascript"
	src="https://cdn.jsdelivr.net/gh/shadab14meb346/galaxy-mail-integration-widget/widget-entry.js"></script>
```

- Now when your Dapp gets connected to Metamask then just post a message to window like below.
- If the wallet address is not yet registered with Galaxy mail it will open the modal and onboarding flow will start
- If it is already registered then no action will happen.

```javascript
useEffect(() => {
	if (account) {
		window?.top?.postMessage({type: "WALLET_CONNECTED", account}, "*");
	}
}, [account]);
```
