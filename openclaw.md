# 安装过程
## 下载
zgq@docker01:~$ clear
zgq@docker01:~$ mkdir -p ~/openclaw-assistant
zgq@docker01:~$ cd ~/openclaw-assistant
zgq@docker01:~/openclaw-assistant$ ls -l
total 0
zgq@docker01:~/openclaw-assistant$ git clone https://github.com/openclaw/openclaw.git
Cloning into 'openclaw'...
fatal: unable to access 'https://github.com/openclaw/openclaw.git/': gnutls_handshake() failed: The TLS connection was non-properly terminated.
zgq@docker01:~/openclaw-assistant$ env | grep -i proxy
no_proxy=localhost,127.0.0.1,.local,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16
https_proxy=https://10.126.126.5:10808
NO_PROXY=localhost,127.0.0.1,.local,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16
HTTPS_PROXY=https://10.126.126.5:10808
HTTP_PROXY=http://10.126.126.5:10808
http_proxy=http://10.126.126.5:10808
ALL_PROXY=socks5://10.126.126.5:10808
all_proxy=socks5://10.126.126.5:10808
zgq@docker01:~/openclaw-assistant$ git clone https://github.com/openclaw/openclaw.git
Cloning into 'openclaw'...
fatal: unable to access 'https://github.com/openclaw/openclaw.git/': gnutls_handshake() failed: The TLS connection was non-properly terminated.
zgq@docker01:~/openclaw-assistant$ git config --global http.sslBackend
zgq@docker01:~/openclaw-assistant$ curl -x http://10.126.126.5:10808 -I https://github.com
HTTP/1.1 200 Connection established

HTTP/2 200 
date: Wed, 25 Feb 2026 08:55:53 GMT
content-type: text/html; charset=utf-8
vary: X-PJAX, X-PJAX-Container, Turbo-Visit, Turbo-Frame, X-Requested-With, Accept-Language, Sec-Fetch-Site,Accept-Encoding, Accept, X-Requested-With
content-language: en-US
etag: W/"561173cbb183a41fcc3c54379da5e9e4"
cache-control: max-age=0, private, must-revalidate
strict-transport-security: max-age=31536000; includeSubdomains; preload
x-frame-options: deny
x-content-type-options: nosniff
x-xss-protection: 0
referrer-policy: origin-when-cross-origin, strict-origin-when-cross-origin
content-security-policy: default-src 'none'; base-uri 'self'; child-src github.githubassets.com github.com/assets-cdn/worker/ github.com/assets/ gist.github.com/assets-cdn/worker/; connectbusercontent.com api.github.com github-cloud.s3.amazonaws.com github-production-repository-file-5c1aeb.s3.amazonaws.com github-production-upload-manifest-file-7fdce7.s3.amazonaws.com githu wss://*.rel.tunnels.api.visualstudio.com github.githubassets.com objects-origin.githubusercontent.com copilot-proxy.githubusercontent.com proxy.individual.githubcopilot.com proxy.businesscom wss://*.actions.githubusercontent.com productionresultssa0.blob.core.windows.net/ productionresultssa1.blob.core.windows.net/ productionresultssa2.blob.core.windows.net/ productionresuonresultssa5.blob.core.windows.net/ productionresultssa6.blob.core.windows.net/ productionresultssa7.blob.core.windows.net/ productionresultssa8.blob.core.windows.net/ productionresultssa9ultssa11.blob.core.windows.net/ productionresultssa12.blob.core.windows.net/ productionresultssa13.blob.core.windows.net/ productionresultssa14.blob.core.windows.net/ productionresultssa15ultssa17.blob.core.windows.net/ productionresultssa18.blob.core.windows.net/ productionresultssa19.blob.core.windows.net/ github-production-repository-image-32fea6.s3.amazonaws.com github-ithub.com wss://alive-staging.github.com api.githubcopilot.com api.individual.githubcopilot.com api.business.githubcopilot.com api.enterprise.githubcopilot.com edge.fullstory.com rs.fullstub.com copilot-workspace.githubnext.com objects-origin.githubusercontent.com; frame-ancestors 'none'; frame-src viewscreen.githubusercontent.com notebooks.githubusercontent.com www.youtubecontent.com camo.githubusercontent.com identicons.github.com avatars.githubusercontent.com private-avatars.githubusercontent.com github-cloud.s3.amazonaws.com objects.githubusercontent.comser-images.githubusercontent.com/ private-user-images.githubusercontent.com opengraph.githubassets.com marketplace-screenshots.githubusercontent.com/ copilotprodattachments.blob.core.windos3.amazonaws.com customer-stories-feed.github.com spotlights-feed.github.com objects-origin.githubusercontent.com *.githubusercontent.com images.ctfassets.net/8aevphvgewt8/; manifest-src '.githubusercontent.com/ private-user-images.githubusercontent.com github-production-user-asset-6210df.s3.amazonaws.com gist.github.com github.githubassets.com assets.ctfassets.net/8aevphvge-src 'unsafe-inline' github.githubassets.com; upgrade-insecure-requests; worker-src github.githubassets.com github.com/assets-cdn/worker/ github.com/assets/ gist.github.com/assets-cdn/wor
server: github.com
accept-ranges: bytes
set-cookie: _gh_sess=ngUz7weVAlj2H4%2FsckU%2BfeEiKGAo4h7prin1er3NXABaLdnLu9%2B2FZnkCRMoI2rEOxl8xyMpAm1sKQ1KlWRpe6i%2ByilddrqJn61T%2FYA2TVJ8mEqdE3z0cXI91yY%2BD7ZO6SUZZNBWPgxXpMg0ylOVElndlzPg2GWRKHZPZ8qpX%2FVGTi9gMA5yw6yQ0J0QwmDcyeOw%3D%3D--XpuE2qXIPB2Z0bEP--GLBSnkpN6rHESBG4LOQvig%3D%3D; Path=/; HttpOnly; Secure; SameSite=Lax
set-cookie: _octo=GH1.1.2027230677.1772009760; Path=/; Domain=github.com; Expires=Thu, 25 Feb 2027 08:56:00 GMT; Secure; SameSite=Lax
set-cookie: logged_in=no; Path=/; Domain=github.com; Expires=Thu, 25 Feb 2027 08:56:00 GMT; HttpOnly; Secure; SameSite=Lax
x-github-request-id: 14B9:38B90A:C59B39:E1FA00:699EB91F

zgq@docker01:~/openclaw-assistant$ git config --global http.sslBackend openssl
zgq@docker01:~/openclaw-assistant$ git config --global http.sslBackend
openssl
zgq@docker01:~/openclaw-assistant$ curl -x http://10.126.126.5:10808 -I https://github.com
HTTP/1.1 200 Connection established

HTTP/2 200 
date: Wed, 25 Feb 2026 08:56:23 GMT
content-type: text/html; charset=utf-8
vary: X-PJAX, X-PJAX-Container, Turbo-Visit, Turbo-Frame, X-Requested-With, Accept-Language, Sec-Fetch-Site,Accept-Encoding, Accept, X-Requested-With
content-language: en-US
etag: W/"adae07719ec10210e325c8dd59ffd138"
cache-control: max-age=0, private, must-revalidate
strict-transport-security: max-age=31536000; includeSubdomains; preload
x-frame-options: deny
x-content-type-options: nosniff
x-xss-protection: 0
referrer-policy: origin-when-cross-origin, strict-origin-when-cross-origin
content-security-policy: default-src 'none'; base-uri 'self'; child-src github.githubassets.com github.com/assets-cdn/worker/ github.com/assets/ gist.github.com/assets-cdn/worker/; connectbusercontent.com api.github.com github-cloud.s3.amazonaws.com github-production-repository-file-5c1aeb.s3.amazonaws.com github-production-upload-manifest-file-7fdce7.s3.amazonaws.com githu wss://*.rel.tunnels.api.visualstudio.com github.githubassets.com objects-origin.githubusercontent.com copilot-proxy.githubusercontent.com proxy.individual.githubcopilot.com proxy.businesscom wss://*.actions.githubusercontent.com productionresultssa0.blob.core.windows.net/ productionresultssa1.blob.core.windows.net/ productionresultssa2.blob.core.windows.net/ productionresuonresultssa5.blob.core.windows.net/ productionresultssa6.blob.core.windows.net/ productionresultssa7.blob.core.windows.net/ productionresultssa8.blob.core.windows.net/ productionresultssa9ultssa11.blob.core.windows.net/ productionresultssa12.blob.core.windows.net/ productionresultssa13.blob.core.windows.net/ productionresultssa14.blob.core.windows.net/ productionresultssa15ultssa17.blob.core.windows.net/ productionresultssa18.blob.core.windows.net/ productionresultssa19.blob.core.windows.net/ github-production-repository-image-32fea6.s3.amazonaws.com github-ithub.com wss://alive-staging.github.com api.githubcopilot.com api.individual.githubcopilot.com api.business.githubcopilot.com api.enterprise.githubcopilot.com edge.fullstory.com rs.fullstub.com copilot-workspace.githubnext.com objects-origin.githubusercontent.com; frame-ancestors 'none'; frame-src viewscreen.githubusercontent.com notebooks.githubusercontent.com www.youtubecontent.com camo.githubusercontent.com identicons.github.com avatars.githubusercontent.com private-avatars.githubusercontent.com github-cloud.s3.amazonaws.com objects.githubusercontent.comser-images.githubusercontent.com/ private-user-images.githubusercontent.com opengraph.githubassets.com marketplace-screenshots.githubusercontent.com/ copilotprodattachments.blob.core.windos3.amazonaws.com customer-stories-feed.github.com spotlights-feed.github.com objects-origin.githubusercontent.com *.githubusercontent.com images.ctfassets.net/8aevphvgewt8/; manifest-src '.githubusercontent.com/ private-user-images.githubusercontent.com github-production-user-asset-6210df.s3.amazonaws.com gist.github.com github.githubassets.com assets.ctfassets.net/8aevphvge-src 'unsafe-inline' github.githubassets.com; upgrade-insecure-requests; worker-src github.githubassets.com github.com/assets-cdn/worker/ github.com/assets/ gist.github.com/assets-cdn/wor
server: github.com
accept-ranges: bytes
set-cookie: _gh_sess=Xwb9k7NBdThXlZG6t%2Fg6xwWr6Q9QpD9cKPepf6v%2Bpobt6D14VdB4VABBljXl5gs%2B8drdlieMwDI4vhXJzSV%2F70veqghwBafb3U3qKYzBUnbjqVJIebtYrkEqODm69yi0IvZNKmWdpdNxVzKasDlu7Yzxv%2BnCP1LWfbQD4DNL1RQE%2FAElhhSVK6Cscpjyr0fZevCA%3D%3D--uXVeyXrAzcHiNfcp--swZRWd78Zbou5WbRG%2BxbMg%3D%3D; Path=/; HttpOnly; Secure; SameSite=Lax
set-cookie: _octo=GH1.1.299186171.1772009793; Path=/; Domain=github.com; Expires=Thu, 25 Feb 2027 08:56:33 GMT; Secure; SameSite=Lax
set-cookie: logged_in=no; Path=/; Domain=github.com; Expires=Thu, 25 Feb 2027 08:56:33 GMT; HttpOnly; Secure; SameSite=Lax
x-github-request-id: 14EE:E6A30:C4E342:E14589:699EB940

zgq@docker01:~/openclaw-assistant$ git clone https://github.com/openclaw/openclaw.git
Cloning into 'openclaw'...
fatal: Unsupported SSL backend 'openssl'. Supported SSL backends:
	gnutls
zgq@docker01:~/openclaw-assistant$ git config --global http.proxy socks5://10.126.126.5:10808
zgq@docker01:~/openclaw-assistant$ git config --global https.proxy socks5://10.126.5:10808
zgq@docker01:~/openclaw-assistant$ git clone https://github.com/openclaw/openclaw.git
Cloning into 'openclaw'...
fatal: Unsupported SSL backend 'openssl'. Supported SSL backends:
	gnutls
zgq@docker01:~/openclaw-assistant$ git config --global --unset http.sslBackend
zgq@docker01:~/openclaw-assistant$ git clone https://github.com/openclaw/openclaw.git
Cloning into 'openclaw'...
remote: Enumerating objects: 186195, done.
remote: Counting objects: 100% (101/101), done.
remote: Compressing objects: 100% (77/77), done.
remote: Total 186195 (delta 37), reused 24 (delta 24), pack-reused 186094 (from 3)
Receiving objects: 100% (186195/186195), 219.21 MiB | 4.01 MiB/s, done.
Resolving deltas: 100% (120790/120790), done.
zgq@docker01:~/openclaw-assistant$ ls -l
total 4
drwxrwxr-x 22 zgq zgq 4096 Feb 25 17:02 openclaw
zgq@docker01:~/openclaw-assistant$ cd openclaw
zgq@docker01:~/openclaw-assistant/openclaw$ ls -l
total 1260
-rw-rw-r--  1 zgq zgq  23396 Feb 25 17:02 AGENTS.md
-rw-rw-r--  1 zgq zgq  62453 Feb 25 17:02 appcast.xml
drwxrwxr-x  6 zgq zgq   4096 Feb 25 17:02 apps
drwxrwxr-x  3 zgq zgq   4096 Feb 25 17:02 assets
-rw-rw-r--  1 zgq zgq 409510 Feb 25 17:02 CHANGELOG.md
lrwxrwxrwx  1 zgq zgq      9 Feb 25 17:02 CLAUDE.md -> AGENTS.md
-rw-rw-r--  1 zgq zgq   6794 Feb 25 17:02 CONTRIBUTING.md
-rw-rw-r--  1 zgq zgq   1399 Feb 25 17:02 docker-compose.yml
-rw-rw-r--  1 zgq zgq   2525 Feb 25 17:02 Dockerfile
-rw-rw-r--  1 zgq zgq    445 Feb 25 17:02 Dockerfile.sandbox
-rw-rw-r--  1 zgq zgq    730 Feb 25 17:02 Dockerfile.sandbox-browser
-rw-rw-r--  1 zgq zgq   1801 Feb 25 17:02 Dockerfile.sandbox-common
-rwxrwxr-x  1 zgq zgq   8603 Feb 25 17:02 docker-setup.sh
drwxrwxr-x 28 zgq zgq   4096 Feb 25 17:02 docs
-rw-rw-r--  1 zgq zgq   5223 Feb 25 17:02 docs.acp.md
drwxrwxr-x 40 zgq zgq   4096 Feb 25 17:02 extensions
-rw-rw-r--  1 zgq zgq   1166 Feb 25 17:02 fly.private.toml
-rw-rw-r--  1 zgq zgq    773 Feb 25 17:02 fly.toml
drwxrwxr-x  2 zgq zgq   4096 Feb 25 17:02 git-hooks
-rw-rw-r--  1 zgq zgq   1074 Feb 25 17:02 LICENSE
-rwxrwxr-x  1 zgq zgq   1414 Feb 25 17:02 openclaw.mjs
-rw-rw-r--  1 zgq zgq    889 Feb 25 17:02 openclaw.podman.env
-rw-rw-r--  1 zgq zgq  12496 Feb 25 17:02 package.json
drwxrwxr-x  4 zgq zgq   4096 Feb 25 17:02 packages
drwxrwxr-x  2 zgq zgq   4096 Feb 25 17:02 patches
-rw-rw-r--  1 zgq zgq 427454 Feb 25 17:02 pnpm-lock.yaml
-rw-rw-r--  1 zgq zgq    274 Feb 25 17:02 pnpm-workspace.yaml
-rw-rw-r--  1 zgq zgq   5323 Feb 25 17:02 PR_STATUS.md
-rw-rw-r--  1 zgq zgq    193 Feb 25 17:02 pyproject.toml
-rw-rw-r--  1 zgq zgq 113954 Feb 25 17:02 README.md
-rw-rw-r--  1 zgq zgq    480 Feb 25 17:02 render.yaml
drwxrwxr-x 11 zgq zgq   4096 Feb 25 17:02 scripts
-rw-rw-r--  1 zgq zgq  16151 Feb 25 17:02 SECURITY.md
-rwxrwxr-x  1 zgq zgq   9300 Feb 25 17:02 setup-podman.sh
drwxrwxr-x 54 zgq zgq   4096 Feb 25 17:02 skills
drwxrwxr-x 51 zgq zgq   4096 Feb 25 17:02 src
drwxrwxr-x  7 zgq zgq   4096 Feb 25 17:02 Swabble
drwxrwxr-x  6 zgq zgq   4096 Feb 25 17:02 test
-rw-rw-r--  1 zgq zgq    889 Feb 25 17:02 tsconfig.json
-rw-rw-r--  1 zgq zgq    463 Feb 25 17:02 tsconfig.plugin-sdk.dts.json
-rw-rw-r--  1 zgq zgq   1139 Feb 25 17:02 tsdown.config.ts
drwxrwxr-x  4 zgq zgq   4096 Feb 25 17:02 ui
drwxrwxr-x  3 zgq zgq   4096 Feb 25 17:02 vendor
-rw-rw-r--  1 zgq zgq   4637 Feb 25 17:02 VISION.md
-rw-rw-r--  1 zgq zgq   5338 Feb 25 17:02 vitest.config.ts
-rw-rw-r--  1 zgq zgq   1144 Feb 25 17:02 vitest.e2e.config.ts
-rw-rw-r--  1 zgq zgq    407 Feb 25 17:02 vitest.extensions.config.ts
-rw-rw-r--  1 zgq zgq    408 Feb 25 17:02 vitest.gateway.config.ts
-rw-rw-r--  1 zgq zgq    467 Feb 25 17:02 vitest.live.config.ts
-rw-rw-r--  1 zgq zgq    621 Feb 25 17:02 vitest.unit.config.ts
-rw-rw-r--  1 zgq zgq    524 Feb 25 17:02 zizmor.yml
## 安装
### 2.1 环境设置
zgq@docker01:~/openclaw-assistant/openclaw$ env | grep -i proxy
no_proxy=localhost,127.0.0.1,.local,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16
https_proxy=https://10.126.126.5:10808
NO_PROXY=localhost,127.0.0.1,.local,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16
HTTPS_PROXY=https://10.126.126.5:10808
HTTP_PROXY=http://10.126.126.5:10808
http_proxy=http://10.126.126.5:10808
ALL_PROXY=socks5://10.126.126.5:10808
all_proxy=socks5://10.126.126.5:10808
zgq@docker01:~/openclaw-assistant/openclaw$ unset http_proxy https_proxy HTTP_PROXY HTTPS_PROXY 
zgq@docker01:~/openclaw-assistant/openclaw$ env | grep -i proxy
no_proxy=localhost,127.0.0.1,.local,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16
NO_PROXY=localhost,127.0.0.1,.local,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16
ALL_PROXY=socks5://10.126.126.5:10808
all_proxy=socks5://10.126.126.5:10808
### 2.2 执行安装
zgq@docker01:~/openclaw-assistant/openclaw$ ./docker-setup.sh
==> Building Docker image: openclaw:local
[+] Building 253.1s (20/20) FINISHED                                                                                                                                                        
 => [internal] load build definition from Dockerfile                                                                                                                                        
 => => transferring dockerfile: 2.56kB                                                                                                                                                      
 => [internal] load metadata for docker.io/library/node:22-bookworm@sha256:cd7bcd2e7a1e6f72052feb023c7f6b722205d3fcab7bbcbd2d1bfdab10b1e935                                                 
 => [internal] load .dockerignore                                                                                                                                                           
 => => transferring context: 891B                                                                                                                                                           
 => [ 1/15] FROM docker.io/library/node:22-bookworm@sha256:cd7bcd2e7a1e6f72052feb023c7f6b722205d3fcab7bbcbd2d1bfdab10b1e935                                                                 
 => => resolve docker.io/library/node:22-bookworm@sha256:cd7bcd2e7a1e6f72052feb023c7f6b722205d3fcab7bbcbd2d1bfdab10b1e935                                                                   
 => => sha256:58b82c7153457434610289a1f61c4326cc9ea77b996a8e9b3cdd92c9814bd7e6 2.49kB / 2.49kB                                                                                              
 => => sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6 64.40MB / 64.40MB                                                                                            
 => => sha256:cd7bcd2e7a1e6f72052feb023c7f6b722205d3fcab7bbcbd2d1bfdab10b1e935 6.41kB / 6.41kB                                                                                              
 => => sha256:a08c488a9779570021138dacddb3138542f6632362b21bb14a7e5d5621e34258 6.74kB / 6.74kB                                                                                              
 => => sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c 48.48MB / 48.48MB                                                                                            
 => => sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c 24.04MB / 24.04MB                                                                                            
 => => sha256:4925cf9d8be888d2b942e0479d921815942727632813c006bad6a067e6363663 211.49MB / 211.49MB                                                                                          
 => => sha256:357cb6974fa00f5868ed182a039825412fca969c0988eb54c7114136aba26f0b 3.32kB / 3.32kB                                                                                              
 => => extracting sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c                                                                                                   
 => => extracting sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c                                                                                                   
 => => sha256:a6174c95fe7408545d8621aba806a8dce153306ae7f114bf6cfc66854efa5494 58.30MB / 58.30MB                                                                                            
 => => extracting sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6                                                                                                   
 => => sha256:737aff54b15787f7e024f1e1a146d3d7677be2f217565c88152937be519722ec 1.25MB / 1.25MB                                                                                              
 => => sha256:5e9e90c62a56b42994131b60a9afcd3851a32cabafa66d482444ab1dcbdbc620 446B / 446B                                                                                                  
 => => extracting sha256:4925cf9d8be888d2b942e0479d921815942727632813c006bad6a067e6363663                                                                                                   
 => => extracting sha256:357cb6974fa00f5868ed182a039825412fca969c0988eb54c7114136aba26f0b                                                                                                   
 => => extracting sha256:a6174c95fe7408545d8621aba806a8dce153306ae7f114bf6cfc66854efa5494                                                                                                   
 => => extracting sha256:737aff54b15787f7e024f1e1a146d3d7677be2f217565c88152937be519722ec                                                                                                   
 => => extracting sha256:5e9e90c62a56b42994131b60a9afcd3851a32cabafa66d482444ab1dcbdbc620                                                                                                   
 => [internal] load build context                                                                                                                                                           
 => => transferring context: 46.08MB                                                                                                                                                        
 => [ 2/15] RUN curl -fsSL https://bun.sh/install | bash                                                                                                                                    
 => [ 3/15] RUN corepack enable                                                                                                                                                             
 => [ 4/15] WORKDIR /app                                                                                                                                                                    
 => [ 5/15] RUN chown node:node /app                                                                                                                                                        
 => [ 6/15] RUN if [ -n "" ]; then       apt-get update &&       DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends  &&       apt-get clean &&       rm -rf /var/lib/
 => [ 7/15] COPY --chown=node:node package.json pnpm-lock.yaml pnpm-workspace.yaml .npmrc ./                                                                                                
 => [ 8/15] COPY --chown=node:node ui/package.json ./ui/package.json                                                                                                                        
 => [ 9/15] COPY --chown=node:node patches ./patches                                                                                                                                        
 => [10/15] COPY --chown=node:node scripts ./scripts                                                                                                                                        
 => [11/15] RUN pnpm install --frozen-lockfile                                                                                                                                              
 => [12/15] RUN if [ -n "" ]; then       apt-get update &&       DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends xvfb &&       mkdir -p /home/node/.cache/ms-playw
 => [13/15] COPY --chown=node:node . .                                                                                                                                                      
 => [14/15] RUN pnpm build                                                                                                                                                                  
 => [15/15] RUN pnpm ui:build                                                                                                                                                               
 => exporting to image                                                                                                                                                                      
 => => exporting layers                                                                                                                                                                     
 => => writing image sha256:555d0fddd4916c9b1a1e511a242814fd35411cfae2423b66c0f61ad7cf33a5de                                                                                                
 => => naming to docker.io/library/openclaw:local                                                                                                                                           
                                                                                                                                                                                            
==> Onboarding (interactive)                                                                                                                                                                
When prompted:
  - Gateway bind: lan
  - Gateway auth: token
  - Gateway token: 7fd85aa17c771bf75752c2c89b7a7f677c7b07543029118640a1f9160808ee22
  - Tailscale exposure: Off
  - Install Gateway daemon: No

WARN[0000] The "CLAUDE_AI_SESSION_KEY" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_WEB_SESSION_KEY" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_WEB_COOKIE" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_AI_SESSION_KEY" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_WEB_SESSION_KEY" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_WEB_COOKIE" variable is not set. Defaulting to a blank string. 
[+] Creating 1/1
 ✔ Network openclaw_default  Created                                                                                                                                                        

🦞 OpenClaw 2026.2.25 (unknown) — I don't judge, but your missing API keys are absolutely judging you.

▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
██░▄▄▄░██░▄▄░██░▄▄▄██░▀██░██░▄▄▀██░████░▄▄▀██░███░██
██░███░██░▀▀░██░▄▄▄██░█░█░██░█████░████░▀▀░██░█░█░██
██░▀▀▀░██░█████░▀▀▀██░██▄░██░▀▀▄██░▀▀░█░██░██▄▀▄▀▄██
▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀
                  🦞 OPENCLAW 🦞                    
 
┌  OpenClaw onboarding
│
◇  Security ──────────────────────────────────────────────────────────────────────────────╮
│                                                                                         │
│  Security warning — please read.                                                        │
│                                                                                         │
│  OpenClaw is a hobby project and still in beta. Expect sharp edges.                     │
│  This bot can read files and run actions if tools are enabled.                          │
│  A bad prompt can trick it into doing unsafe things.                                    │
│                                                                                         │
│  If you’re not comfortable with basic security and access control, don’t run OpenClaw.  │
│  Ask someone experienced to help before enabling tools or exposing it to the internet.  │
│                                                                                         │
│  Recommended baseline:                                                                  │
│  - Pairing/allowlists + mention gating.                                                 │
│  - Sandbox + least-privilege tools.                                                     │
│  - Keep secrets out of the agent’s reachable filesystem.                                │
│  - Use the strongest available model for any bot with tools or untrusted inboxes.       │
│                                                                                         │
│  Run regularly:                                                                         │
│  openclaw security audit --deep                                                         │
│  openclaw security audit --fix                                                          │
│                                                                                         │
│  Must read: https://docs.openclaw.ai/gateway/security                                   │
│                                                                                         │
├─────────────────────────────────────────────────────────────────────────────────────────╯
│
◇  I understand this is powerful and inherently risky. Continue?
│  Yes
│
◇  Onboarding mode
│  QuickStart
│
◇  QuickStart ─────────────────────────╮
│                                      │
│  Gateway port: 18789                 │
│  Gateway bind: Loopback (127.0.0.1)  │
│  Gateway auth: Token (default)       │
│  Tailscale exposure: Off             │
│  Direct to chat channels.            │
│                                      │
├──────────────────────────────────────╯
│
◇  Model/auth provider
│  Moonshot AI (Kimi K2.5)
│
◇  Moonshot AI (Kimi K2.5) auth method
│  Kimi API key (.cn)
│
◇  Enter Moonshot API key (.cn)
│  sk-zHPF7qWUIFQizRrYjzaVKYOhE9MQiYSiO364fJaTj7VrEPZq
│
◇  Model configured ────────────────────────╮
│                                           │
│  Default model set to moonshot/kimi-k2.5  │
│                                           │
├───────────────────────────────────────────╯
│
◇  Default model
│  Keep current (moonshot/kimi-k2.5)
│
◇  Channel status ────────────────────────────╮
│                                             │
│  Telegram: needs token                      │
│  WhatsApp (default): not linked             │
│  Discord: needs token                       │
│  Slack: needs tokens                        │
│  Signal: needs setup                        │
│  signal-cli: missing (signal-cli)           │
│  iMessage: needs setup                      │
│  imsg: missing (imsg)                       │
│  IRC: not configured                        │
│  Google Chat: not configured                │
│  Feishu: install plugin to enable           │
│  Google Chat: install plugin to enable      │
│  Nostr: install plugin to enable            │
│  Microsoft Teams: install plugin to enable  │
│  Mattermost: install plugin to enable       │
│  Nextcloud Talk: install plugin to enable   │
│  Matrix: install plugin to enable           │
│  BlueBubbles: install plugin to enable      │
│  LINE: install plugin to enable             │
│  Zalo: install plugin to enable             │
│  Zalo Personal: install plugin to enable    │
│  Synology Chat: install plugin to enable    │
│  Tlon: install plugin to enable             │
│                                             │
├─────────────────────────────────────────────╯
│
◇  How channels work ───────────────────────────────────────────────────────────────────────╮
│                                                                                           │
│  DM security: default is pairing; unknown DMs get a pairing code.                         │
│  Approve with: openclaw pairing approve <channel> <code>                                  │
│  Public DMs require dmPolicy="open" + allowFrom=["*"].                                    │
│  Multi-user DMs: run: openclaw config set session.dmScope "per-channel-peer" (or          │
│  "per-account-channel-peer" for multi-account channels) to isolate sessions.              │
│  Docs: channels/pairing              │
│                                                                                           │
│  Telegram: simplest way to get started — register a bot with @BotFather and get going.    │
│  WhatsApp: works with your own number; recommend a separate phone + eSIM.                 │
│  Discord: very well supported right now.                                                  │
│  IRC: classic IRC networks with DM/channel routing and pairing controls.                  │
│  Google Chat: Google Workspace Chat app with HTTP webhook.                                │
│  Slack: supported (Socket Mode).                                                          │
│  Signal: signal-cli linked device; more setup (David Reagans: "Hop on Discord.").         │
│  iMessage: this is still a work in progress.                                              │
│  Feishu: 飞书/Lark enterprise messaging with doc/wiki/drive tools.                        │
│  Nostr: Decentralized protocol; encrypted DMs via NIP-04.                                 │
│  Microsoft Teams: Bot Framework; enterprise support.                                      │
│  Mattermost: self-hosted Slack-style chat; install the plugin to enable.                  │
│  Nextcloud Talk: Self-hosted chat via Nextcloud Talk webhook bots.                        │
│  Matrix: open protocol; install the plugin to enable.                                     │
│  BlueBubbles: iMessage via the BlueBubbles mac app + REST API.                            │
│  LINE: LINE Messaging API bot for Japan/Taiwan/Thailand markets.                          │
│  Zalo: Vietnam-focused messaging platform with Bot API.                                   │
│  Zalo Personal: Zalo personal account via QR code login.                                  │
│  Synology Chat: Connect your Synology NAS Chat to OpenClaw with full agent capabilities.  │
│  Tlon: decentralized messaging on Urbit; install the plugin to enable.                    │
│                                                                                           │
├───────────────────────────────────────────────────────────────────────────────────────────╯
│
◇  Select channel (QuickStart)
│  Feishu/Lark (飞书)
│
◇  Install Feishu plugin?
│  Download from npm (@openclaw/feishu)
Downloading @openclaw/feishu…
Extracting /tmp/openclaw-npm-pack-8SYKfx/openclaw-feishu-2026.2.24.tgz…
Installing to /home/node/.openclaw/extensions/feishu…
Installing plugin dependencies…
13:09:38 [plugins] plugins.allow is empty; discovered non-bundled plugins may auto-load: feishu (/home/node/.openclaw/extensions/feishu/index.ts). Set plugins.allow to explicit trusted ids
│
◇  Feishu credentials ──────────────────────────────────────────────────────────────╮
│                                                                                   │
│  1) Go to Feishu Open Platform (open.feishu.cn)                                   │
│  2) Create a self-built app                                                       │
│  3) Get App ID and App Secret from Credentials page                               │
│  4) Enable required permissions: im:message, im:chat, contact:user.base:readonly  │
│  5) Publish the app or add it to a test group                                     │
│  Tip: you can also set FEISHU_APP_ID / FEISHU_APP_SECRET env vars.                │
│  Docs: feishu                 │
│                                                                                   │
├───────────────────────────────────────────────────────────────────────────────────╯
│
◇  Enter Feishu App ID
│  cli_a9144b21e6f99bcd
│
◇  Enter Feishu App Secret
│  WKKsteuIoiwAwOfuFLeOHgLSOMhEaw3B
[info]: [ 'client ready' ]
│
◇  Feishu connection test ────────────────────────────╮
│                                                     │
│  Connection failed: API error: app do not have bot  │
│                                                     │
├─────────────────────────────────────────────────────╯
│
◇  Which Feishu domain?
│  Feishu (feishu.cn) - China
│
◇  Group chat policy
│  Allowlist - only respond in specific groups
│
◇  Group chat allowlist (chat_ids)
│  oc_da6ce73451a8486b298cb7f30b53b975
[info]: [ 'client ready' ]
│
◇  Selected channels ──────────────────────────────────────────╮
│                                                              │
│  Feishu — 飞书/Lark enterprise messaging. Docs:              │
│  feishu  │
│                                                              │
├──────────────────────────────────────────────────────────────╯
Config warnings:
- plugins.entries.feishu: plugin feishu: duplicate plugin id detected; later plugin may be overridden (/app/extensions/feishu/index.ts)
Updated ~/.openclaw/openclaw.json
Workspace OK: ~/.openclaw/workspace
Sessions OK: ~/.openclaw/agents/main/sessions
│
◇  Skills status ─────────────╮
│                             │
│  Eligible: 7                │
│  Missing requirements: 41   │
│  Unsupported on this OS: 7  │
│  Blocked by allowlist: 0    │
│                             │
├─────────────────────────────╯
│
◇  Configure skills now? (recommended)
│  Yes
│
◇  Install missing skill dependencies
│  Skip for now
│
◇  Set GOOGLE_PLACES_API_KEY for goplaces?
│  No
│
◇  Set GEMINI_API_KEY for nano-banana-pro?
│  No
│
◇  Set NOTION_API_KEY for notion?
│  No
│
◇  Set OPENAI_API_KEY for openai-image-gen?
│  No
│
◇  Set OPENAI_API_KEY for openai-whisper-api?
│  No
│
◇  Set ELEVENLABS_API_KEY for sag?
│  No
│
◇  Hooks ──────────────────────────────────────────────────────────────────╮
│                                                                          │
│  Hooks let you automate actions when agent commands are issued.          │
│  Example: Save session context to memory when you issue /new or /reset.  │
│                                                                          │
│  Learn more: https://docs.openclaw.ai/automation/hooks                   │
│                                                                          │
├──────────────────────────────────────────────────────────────────────────╯
│
◇  Enable hooks?
│  Skip for now
Config warnings:
- plugins.entries.feishu: plugin feishu: duplicate plugin id detected; later plugin may be overridden (/app/extensions/feishu/index.ts)
Config overwrite: /home/node/.openclaw/openclaw.json (sha256 ab0e67615a56cb5a68494ea66889412363076e7bf27ccc6666785f8225441234 -> 431a7af507904db034e96ee4bc40cf5b5c368b8fc91029bcc169f07e3e9
│
◇  Systemd ───────────────────────────────────────────────────────────────────────────────╮
│                                                                                         │
│  Systemd user services are unavailable. Skipping lingering checks and service install.  │
│                                                                                         │
├─────────────────────────────────────────────────────────────────────────────────────────╯
Config warnings:\n- plugins.entries.feishu: plugin feishu: duplicate plugin id detected; later plugin may be overridden (/app/extensions/feishu/index.ts)
│
◇  
Health check failed: gateway closed (1006 abnormal closure (no close frame)): no close reason
  Gateway target: ws://127.0.0.1:18789
  Source: local loopback
  Config: /home/node/.openclaw/openclaw.json
  Bind: loopback
│
◇  Health check help ────────────────────────────────╮
│                                                    │
│  Docs:                                             │
│  https://docs.openclaw.ai/gateway/health           │
│  https://docs.openclaw.ai/gateway/troubleshooting  │
│                                                    │
├────────────────────────────────────────────────────╯
│
◇  Optional apps ────────────────────────╮
│                                        │
│  Add nodes for extra features:         │
│  - macOS app (system + notifications)  │
│  - iOS app (camera/canvas)             │
│  - Android app (camera/canvas)         │
│                                        │
├────────────────────────────────────────╯
│
◇  Control UI ───────────────────────────────────────────────────────────────────────────────╮
│                                                                                            │
│  Web UI: http://127.0.0.1:18789/                                                           │
│  Web UI (with token):                                                                      │
│  http://127.0.0.1:18789/#token=23f002a81976e14b315ec9889b911300a62fdc95b18a4872            │
│  Gateway WS: ws://127.0.0.1:18789                                                          │
│  Gateway: not detected (gateway closed (1006 abnormal closure (no close frame)): no close  │
│  reason)                                                                                   │
│  Docs: https://docs.openclaw.ai/web/control-ui                                             │
│                                                                                            │
├────────────────────────────────────────────────────────────────────────────────────────────╯
│
◇  Workspace backup ────────────────────────────────────────╮
│                                                           │
│  Back up your agent workspace.                            │
│  Docs: https://docs.openclaw.ai/concepts/agent-workspace  │
│                                                           │
├───────────────────────────────────────────────────────────╯
│
◇  Security ──────────────────────────────────────────────────────╮
│                                                                 │
│  Running agents on your computer is risky — harden your setup:  │
│  https://docs.openclaw.ai/security                              │
│                                                                 │
├─────────────────────────────────────────────────────────────────╯
│
◇  Shell completion ───────────────────────────────────────────────────────╮
│                                                                          │
│  Shell completion installed. Restart your shell or run: source ~/.zshrc  │
│                                                                          │
├──────────────────────────────────────────────────────────────────────────╯
│
◇  Dashboard ready ────────────────────────────────────────────────────────────────╮
│                                                                                  │
│  Dashboard link (with token):                                                    │
│  http://127.0.0.1:18789/#token=23f002a81976e14b315ec9889b911300a62fdc95b18a4872  │
│  Copy/paste this URL in a browser on this machine to control OpenClaw.           │
│  No GUI detected. Open from your computer:                                       │
│  ssh -N -L 18789:127.0.0.1:18789 user@<host>                                     │
│  Then open:                                                                      │
│  http://localhost:18789/                                                         │
│  http://localhost:18789/#token=23f002a81976e14b315ec9889b911300a62fdc95b18a4872  │
│  Docs:                                                                           │
│  https://docs.openclaw.ai/gateway/remote                                         │
│  https://docs.openclaw.ai/web/control-ui                                         │
│                                                                                  │
├──────────────────────────────────────────────────────────────────────────────────╯
│
◇  Web search (optional) ─────────────────────────────────────────────────────────────────╮
│                                                                                         │
│  If you want your agent to be able to search the web, you’ll need an API key.           │
│                                                                                         │
│  OpenClaw uses Brave Search for the `web_search` tool. Without a Brave Search API key,  │
│  web search won’t work.                                                                 │
│                                                                                         │
│  Set it up interactively:                                                               │
│  - Run: openclaw configure --section web                                                │
│  - Enable web_search and paste your Brave Search API key                                │
│                                                                                         │
│  Alternative: set BRAVE_API_KEY in the Gateway environment (no config changes).         │
│  Docs: https://docs.openclaw.ai/tools/web                                               │
│                                                                                         │
├─────────────────────────────────────────────────────────────────────────────────────────╯
│
◇  What now ─────────────────────────────────────────────────────────────╮
│                                                                        │
│  What now: https://openclaw.ai/showcase ("What People Are Building").  │
│                                                                        │
├────────────────────────────────────────────────────────────────────────╯
│
└  Onboarding complete. Use the dashboard link above to control OpenClaw.


==> Provider setup (optional)
WhatsApp (QR):
  docker compose -f /home/zgq/openclaw-assistant/openclaw/docker-compose.yml run --rm openclaw-cli channels login
Telegram (bot token):
  docker compose -f /home/zgq/openclaw-assistant/openclaw/docker-compose.yml run --rm openclaw-cli channels add --channel telegram --token <token>
Discord (bot token):
  docker compose -f /home/zgq/openclaw-assistant/openclaw/docker-compose.yml run --rm openclaw-cli channels add --channel discord --token <token>
Docs: https://docs.openclaw.ai/channels

==> Starting gateway
WARN[0000] The "CLAUDE_AI_SESSION_KEY" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_WEB_SESSION_KEY" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_WEB_COOKIE" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_AI_SESSION_KEY" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_WEB_SESSION_KEY" variable is not set. Defaulting to a blank string. 
WARN[0000] The "CLAUDE_WEB_COOKIE" variable is not set. Defaulting to a blank string. 
[+] Running 1/1
 ✔ Container openclaw-openclaw-gateway-1  Started                                                                                                                                           

Gateway running with host port mapping.
Access from tailnet devices via the host's tailnet IP.
Config: /home/zgq/.openclaw
Workspace: /home/zgq/.openclaw/workspace
Token: 7fd85aa17c771bf75752c2c89b7a7f677c7b07543029118640a1f9160808ee22

Commands:
  docker compose -f /home/zgq/openclaw-assistant/openclaw/docker-compose.yml logs -f openclaw-gateway
  docker compose -f /home/zgq/openclaw-assistant/openclaw/docker-compose.yml exec openclaw-gateway node dist/index.js health --token "7fd85aa17c771bf75752c2c89b7a7f677c7b07543029118640a1f9

# 配置
## 配置文件格式验证
zgq@docker01:~/openclaw-assistant/openclaw$ 
zgq@docker01:~/openclaw-assistant/openclaw$ cat ~/.openclaw/openclaw.json | python3 -m json.tool > /dev/null && echo "JSON 格式正确"
JSON 格式正确
zgq@docker01:~/openclaw-assistant/openclaw$ 
zgq@docker01:~/openclaw-assistant/openclaw$ docker compose logs -f openclaw-gateway
## 重启服务
docker compose restart openclaw-gateway

## 使用 SSH 隧道
在您的 本地电脑（Windows/Mac）上执行：
bash
复制

ssh -L 18789:localhost:18789 zgq@10.126.126.2

然后本地浏览器访问：
http://localhost:18789

## 拒绝外部访问和允许LAN
openclaw.json 文件说：
"bind": "loopback" (仅绑定本地回环 127.0.0.1，拒绝外部访问)

```bash
  "plugins": {
    "allow": ["feishu"],
    "entries": {
      "feishu": {
        "enabled": true
      }
    },

```
## 环境
```bash
OPENCLAW_CONFIG_DIR=/home/zgq/.openclaw
OPENCLAW_WORKSPACE_DIR=/home/zgq/.openclaw/workspace
OPENCLAW_GATEWAY_PORT=18789
OPENCLAW_BRIDGE_PORT=18790
OPENCLAW_GATEWAY_BIND=lan
OPENCLAW_GATEWAY_TOKEN=7fd85aa17c771bf75752c2c89b7a7f677c7b07543029118640a1f9160808ee22
OPENCLAW_IMAGE=openclaw:local
OPENCLAW_EXTRA_MOUNTS=
OPENCLAW_HOME_VOLUME=
OPENCLAW_DOCKER_APT_PACKAGES=
```

## 配对设备
你现在的核心需求是完成OpenClaw设备的配对操作，结合之前的环境（网关容器正常运行、需通过容器内命令完成配对），我会给你**完整、可直接执行的设备配对步骤**，确保你能一步步完成操作。

### 完整设备配对操作流程（从宿主机到容器内）
#### 步骤1：进入运行中的网关容器（关键）
在宿主机（docker01）的终端执行以下命令，进入网关容器的交互式终端：
```bash
docker compose exec openclaw-gateway sh
```
执行后命令行提示符会变为 `/home/node $`，表示已成功进入网关容器。

#### 步骤2：查看待配对设备的请求ID
在网关容器内执行命令，列出所有等待配对批准的设备请求（获取核心的`requestId`）：
```bash
node dist/index.js devices list
```
##### 输出解读：
- **有未配对请求**（正常情况）：
  ```
  ┌─────────────────────┬──────────────────────────────┬───────────┬──────────────┐
  │ Device ID           │ Request ID                   │ Status    │ Device Name  │
  ├─────────────────────┼──────────────────────────────┼───────────┼──────────────┤
  │ dev_xxxxxx          │ req_abc123def456             │ PENDING   │ Device-001   │
  └─────────────────────┴──────────────────────────────┴───────────┴──────────────┘
  ```
  记录下`Request ID`列的内容（如`req_abc123def456`），这是下一步批准配对的关键参数。

- **无未配对请求**：
  输出`No pending device pairing requests found`，说明：
  1. 设备未开启配对模式；
  2. 设备与网关不在同一网络，无法访问18789端口；
  3. 设备配对请求已超时（通常5分钟）。
  需先确保设备开启配对模式，再重新执行该命令。

#### 步骤3：批准设备配对（核心操作）
在网关容器内，使用步骤2获取的`requestId`执行批准命令（替换`<requestId>`为实际值）：
```bash
# 替换req_abc123def456为你实际的请求ID
node dist/index.js devices approve req_abc123def456
```
##### 成功提示：
```
Successfully approved device request req_abc123def456
Device dev_xxxxxx paired successfully!
```
此时设备配对完成，可在设备端确认配对状态。

#### 步骤4：验证配对结果（可选）
再次执行`devices list`命令，查看设备状态是否变为`PAIRED`：
```bash
node dist/index.js devices list
```
输出中该设备的`Status`列会显示`PAIRED`，表示配对成功。

#### 步骤5：退出容器（操作完成后）
输入以下命令退出网关容器终端，回到宿主机：
```bash
exit
```

### 常见问题排查
1. **执行`devices list`无结果**：
   - 确认设备已开启「配对模式」（参考设备说明书）；
   - 检查设备与docker01主机的网络连通性（可ping通docker01的IP）；
   - 确认网关容器的18789端口已对外暴露（`docker ps`显示`0.0.0.0:18789->18789/tcp`）。

2. **批准配对提示“request not found”**：
   - 核对`requestId`是否输入正确（区分大小写，无多余空格）；
   - 重新执行`devices list`，确认请求ID未变化/未超时。

### 总结
1. 核心操作顺序：进入网关容器 → 查请求ID → 批准配对；
2. 关键命令：
   - 进入容器：`docker compose exec openclaw-gateway sh`；
   - 查请求ID：`node dist/index.js devices list`；
   - 批准配对：`node dist/index.js devices approve <requestId>`；
3. 配对成功的核心是确保`requestId`正确、设备处于配对模式且网络可达。