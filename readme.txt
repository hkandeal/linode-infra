{
  search(keyword: "java" page: 20) {
    totalItems
    items {
      id
      volumeInfo {
        title
        authors
        description
        imageLinks {
          smallThumbnail
          thumbnail
        }
      }
    }
  }
}

https://www.googleapis.com/books/v1/volumes?q=java&key=AIzaSyBfRCTvba9HdzeD4gUURMbEKRwNFdz7c7I&maxResults=40&startIndex=10
https://bozo.hossam.io/bookinfo/q/graphql-ui/
https://bozo.hossam.io/bookinfo/graphql/schema.graphql


firebase config
const firebaseConfig = {
  apiKey: "AIzaSyCTRftAWpS4ByqSz_brMO3ipFldlR7_mcY",
  authDomain: "bozo-book-library-1e53b.firebaseapp.com",
  projectId: "bozo-book-library-1e53b",
  storageBucket: "bozo-book-library-1e53b.appspot.com",
  messagingSenderId: "37170209713",
  appId: "1:37170209713:web:5252edb99e96f684be5390",
  measurementId: "G-9VNTFGBH15"
};

https://console.firebase.google.com/project/bozo-book-library-1e53b/overview



https://medium.com/@abvijaykumar/chapter-2-secure-secrets-with-hashicorp-vault-eafb6c6d9471 
https://devopscube.com/vault-agent-injector-tutorial/


argocd pwd:COu0ryoc1lH0BkI2
vault kv put bozobooks/reactjs-firebase-config apiKey="AIzaSyCTRftAWpS4ByqSz_brMO3ipFldlR7_mcY" messagingSenderId="37170209713" appId="1:37170209713:web:5252edb99e96f684be5390" measurementId="G-9VNTFGBH15" 



initlization output
{
  "unseal_keys_b64": [
    "9zcTv1gUtcR/qq/PkMe1uSBH9zgTcUMxoKn76nNUqYg="
  ],
  "unseal_keys_hex": [
    "f73713bf5814b5c47faaafcf90c7b5b92047f73813714331a0a9fbea7354a988"
  ],
  "unseal_shares": 1,
  "unseal_threshold": 1,
  "recovery_keys_b64": [],
  "recovery_keys_hex": [],
  "recovery_keys_shares": 0,
  "recovery_keys_threshold": 0,
  "root_token": "hvs.gGSJgN7sUYW06lvspvYy6O0t"
}




Unseal Key 1: CHEQ6Y2S4+QUCXSUWRUBFbRR1zMJitPltY7aGGCE8X1o
Unseal Key 2: G2KE9U9K4oSepf06Js/uSr7T1dULe/L9kTA534SiB+k7
Unseal Key 3: 66KBeiuYCCLw7x/Q9PuATnxRExOmj+dkCYYhJYG8110b
Unseal Key 4: bpIRN6MK/UYKLlPDn5bRUhifwy7+j2tCnIl1mqunPage
Unseal Key 5: L5L0BdCK/z9FaMyogCe5eOicjOfRymnUXA3NZL3U3DaO

Initial Root Token: hvs.4lwAklGjvjoxkMu95ydusgWF



vault write auth/kubernetes/config kubernetes_host="https://$KUBERNETES_PORT_443_TCP_ADDR:443"

vault kv put bozobooks/reactjs-firebase-config apiKey="AIzaSyCTRftAWpS4ByqSz_brMO3ipFldlR7_mcY" appId="1:37170209713:web:5252edb99e96f684be5390" measurementId= "G-9VNTFGBH15" messagingSenderId="37170209713"


vault operator unseal CHEQ6Y2S4+QUCXSUWRUBFbRR1zMJitPltY7aGGCE8X1o
vault operator unseal G2KE9U9K4oSepf06Js/uSr7T1dULe/L9kTA534SiB+k7
vault operator unseal 66KBeiuYCCLw7x/Q9PuATnxRExOmj+dkCYYhJYG8110b




