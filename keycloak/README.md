# keycloak 

`kustomize build overlays/dev | kubectl apply -f -`

`oc get keycloak/defaultkeycloak -o jsonpath='{.status.ready}'`

`oc get keycloakrealms/default -o jsonpath='{.status.ready}'`

`oc get keycloak default-keycloak --output="jsonpath={.status.credentialSecret}"`

`oc get secret credential-default-keycloak -o go-template='{{range $k,$v := .data}}{{printf "%s: " $k}}{{if not $v}}{{$v}}{{else}}{{$v | base64decode}}{{end}}{{"\n"}}{{end}}'`