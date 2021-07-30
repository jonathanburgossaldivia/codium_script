# codium_script
Solve the problem "Cannot connect to Extensions marketplace" on Open Suse

Save as sh script and Run:

```console
data='"serviceUrl": "https://marketplace.visualstudio.com/_apis/public/gallery",
"cacheUrl": "https://vscode.blob.core.windows.net/gallery/index",
"itemUrl": "https://marketplace.visualstudio.com/items"'

sudo sed -i '/itemUrl/d' /usr/share/codium/resources/app/product.json
perl -spe 's/.serviceUrl.*/$var/' -- -var="$data"  /usr/share/codium/resources/app/product.json
```
