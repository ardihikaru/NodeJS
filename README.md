# NodeJS
Berbagi seputar NodeJS

# Permasalahan umum (Common problems):

- Penggunaan npm di command line, ketika sedang menggunakan proxy.
   Solusi:
   - Run scripts berikut:
     - npm config set strict-ssl false
     - npm config set registry "http://registry.npmjs.org/"
     - npm config set proxy http://username:password@proxy.namaweb.com:443
     - npm config set https-proxy http://username:password@proxy.namaweb.com:443
   - Source: 
      - https://github.com/npm/npm/issues/9401
      - http://stackoverflow.com/questions/7559648/is-there-a-way-to-make-npm-install-the-command-to-work-behind-proxy
      - https://jjasonclark.com/how-to-setup-node-behind-web-proxy/
   - NB: jika username menggunakan nama domain (e.g. usernameku@namaweb.com), maka ganti symbol @ dengan %40 (e.g. usernameku%40namaweb.com)
   
- Disable proxy (karena sudah di enabled sesuai langkah no.1).
   - Ikuti langkah berikut:
     - npm config rm proxy
     - npm config rm https-proxy
   - Source: 
     - http://stackoverflow.com/questions/21228995/how-to-clear-https-proxy-setting-of-npm
     - http://jonathanblog2000.blogspot.co.id/2013/11/set-and-reset-proxy-for-git-and-npm.html
     - http://luxiyalu.com/how-to-remove-all-npm-proxy-settings/
     
