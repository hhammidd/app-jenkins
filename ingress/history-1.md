 2995* kubectl get nodes -o wide
 2996  clear
 2997  helm search nginx-ingress
 2998* java -jar jenkins.war
 2999  helm install my-release nginx-stable/nginx-ingress
 3000  helm install my-release nginx-stable/nginx-ingress --set controller.image.repository=myregistry.example.com/nginx-plus-ingress --set controller.nginxplus=true
 3001  helm repo add nginx-stable https://helm.nginx.com/stable
 3002  helm repo update
 3003  helm install my-ngnix nginx-stable/nginx-ingress rbac.create=true
 3004  helm install my-ngnix nginx-stable/nginx-ingress --set rbac.create=true
 3005  k get all
 3006  k delete hello-svc
 3007  k delete svc hello-svc
 3008  k get all
 3009* k create -f deploy.yml
 3010* k expose deploy hello-deploy --port 80
 3011* k get svc
 3012* k version --short
 3013* k run ngnix --image ngnix
 3014* k get all
 3015* k get pods
 3016* k get all
 3017* watch k get all
 3018* k run ngnix --image ngnix
 3019* k get pods
 3020* k delete deploy ngnix
 3021* k delete  ngnix
 3022* k delete deploy  ngnix
 3023* k delete svc ngnix
 3024* k get svc
 3025  kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.9.5/manifests/namespace.yaml\n
 3026  kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.9.5/manifests/metallb.yaml\n
 3027  kubectl create secret generic -n metallb-system memberlist --from-literal=secretkey="$(openssl rand -base64 128)"\n
 3028  k get all -n metallb-system
 3029  k get nodes -o wide
 3030  cat <<EOF | kubectl create -f -\napiVersion: v1\nkind: ConfigMap\nmetadata:\n  namespace: metallb-system\n  name: config\ndata:\n  config: |\n    address-pools:\n    - name: default\n      protocol: layer2\n      addresses:\n      - 192.168.65.200-192.168.65.250\nEOF \n \nEOF
 3031  k get nodes -o wide
 3032  cat <<EOF | kubectl create -f -\n\napiVersion: v1\nkind: ConfigMap\nmetadata:\n  namespace: metallb-system\n  name: config\ndata:\n  config: |\n    address-pools:\n    - name: default\n      protocol: layer2\n      addresses:\n      - 92.168.65.200-192.168.65.250\nEOF
 3033  k describe configmap config - n metallb-system
 3034  k describe configmap config -n metallb-system
 3035  k get svc
 3036  k expose deploy hello-deploy --port 80
 3037  k get svc
 3038  k delete svc hello-deploy
 3039  k expose deploy hello-deploy --port 80
 3040  k get svc
 3041* k create -f ingress-resource-1.yaml
 3042* alias k="kubectl"
 3043* k create -f ingress-resource-1.yaml
 3044* cd ingress
 3045* k create -f ingress-resource-1.yaml
 3046* k get ingress
 3047* k get svc
 3048* sudo vi /etc/hosts
 3049* k get ingress
 3050* k delete ingress ingress-resource-1
 3051* k get pods
 3052* k create -f ingress-resource-1.yaml
 3053* k get pods
 3054* k get svc
 3055* k delete ingress ingress-resource-1
 3056* k create -f ingress-resource-1.yaml
 3057* k get svc
 3058* k get ing
 3059* k describe ing ingress-resource-1
 3060* k get svc
 3061* k delete ingress ingress-resource-1
 3062* k get svc
 3063* k delete svc hello-deploy
 3064* k get deploy
 3065* k delete hello-deploy
 3066* k delete deploy hello-deploy
 3067* k create -f deploy.yml
 3068* k get svc
 3069* k create -f ingress-resource-1.yaml
 3070* k delete ingress ingress-resource-1
 3071* k create -f ingress-resource-1.yaml
 3072* k describe in inress-resource-1
 3073* k describe ing inress-resource-1
 3074* k describe ing ingress-resource-1
 3075* kubectl get svc --all-namespaces
 3076* k get svc
 3077* k delete svc hello-deploy
 3078* k create -f svc.yml
 3079* k get svc
 3080* k delete ingress ingress-resource-1
 3081* k create -f ingress-resource-1.yaml
 3082* k delete ingress ingress-resource-1
 3083* k get svc
 3084* k delete svc hello-svc
 3085* k create -f svc.yml
 3086* k get svc
 3087* k create -f ingress-resource-1.yaml
 3088* k get svc
 3089* k describe ing ingress-resource-1
 3090* k delete ingress ingress-resource-1
 3091* k create -f ingress-resource-1.yaml
 3092* k describe ing ingress-resource-1
 3093  docker image ls
 3094  docker rmi b81deaac3dc7
 3095  docker rmi 16591e0ac476
 3096  docker rmi 7467d80712f2
 3097* k delete ingress ingress-resource-1
 3098* k delete svc hello-deploy
 3099* k delete deploy hello-deploy
 3100* k get all
 3101  docker image ls
 3102  docker rmi 16f54e9784c4
 3103  docker rmi 2e80d007317f
 3104  docker image ls
 3105  docker rmi 401a467e4b0d
 3106  docker image ls
 3107* k create
 3108* k create -f ngnix-deploy-main.yaml
 3109* k get all
 3110* k delete deploy ngnix
 3111* k delete pod ngnix
 3112* k get all
 3113* k expose deploy ngnix-deploy-main --port 80
 3114* k expose deploy nginx-deploy-main --port 80
 3115* k get all
 3116* k create -f ingress-resource-1.yaml
 3117* k get ing
 3118* k describe ing infress-resource-1.yaml
 3119* k describe ing ingress-resource-1.yaml
 3120* k describe ing ingress-resource-1
 3121* sudo vi /etc/hosts
 3122* k get all
 3123* kubectl get namespaces
 3124* k get all
 3125* kubectl get pods -n kube-system
 3126* helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
 3127* helm repo update
 3128* helm install my-release ingress-nginx/ingress-nginx
 3129* k get all
 3130* k describe ing ingress-resource-1
 3131* k delete ingress ingress-resource-1
 3132* k create -f ingress-resource-1.yaml
 3133* k get all
 3134* k create -f ingress-resource-1.yaml
 3135* k get all
 3136* k delete pods my-release-ingress-nginx-controller-5fc666bcc5-5sj5l
 3137* k delete svc my-release-ingress-nginx-controller
 3138* k delete svc my-release-ingress-nginx-controller-admission
 3139* k get all
 3140* k delete deploy my-release-ingress-nginx-controller
 3141* k get all
 3142* k create -f ingress-resource-1.yaml
 3143* k get all
 3144* k create -f ingress-resource-1.yaml
 3145* k get all
 3146* k get nodes
 3147* k create -f ingress-resource-1.yaml
 3148* helm list
 3149* helm delete my-release
 3150* k create -f ingress-resource-1.yaml
 3151* k get all
 3152* k describe ing ingress-resource-1
 3153* kubectl logs -n default my-ngnix-nginx-ingress-fddcbbd5c
 3154* k get pods
 3155* kubectl logs -n default my-ngnix-nginx-ingress-fddcbbd5c-47f8z
 3156* k describe ing ingress-resource-1
 3157* k delete ingress ingress-resource-1
 3158* k create -f ingress-resource-1.yaml
 3159* k describe ing ingress-resource-1
 3160* k get all
 3161* k describe ing ingress-resource-1
 3162* k get all
 3163* k version --short
 3164* helm version --short
 3165* helm search ngnx-ingress
 3166* k get all
 3167* k delete ingress ingress-resource-1
 3168* k create -f ingress-resource-1.yaml
 3169* k get all
 3170* k delete ingress ingress-resource-1
 3171* k create -f ingress-resource-1.yaml
 3172* k get pods
 3173* k describe ing ingress-resource-1
 3174* k delete ingress ingress-resource-1
 3175* k create -f ingress-resource-1.yaml
 3176* k describe ing ingress-resource-1
 3177* k delete ingress ngress-resource-1
 3178* k create -f ingress-resource-1.yaml
 3179* k describe ing ingress-resource-1
 3180  kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.42.0/deploy/static/provider/cloud/deploy.yaml\n
 3181  k describe ing ingress-resource-1
 3182* k delete ingress ngress-resource-1
 3183* k create -f ingress-resource-1.yaml
 3184* k get all
 3185* k create -f ingress-resource-1.yaml
 3186* helm list
 3187* k get pods
 3188* k get svc
 3189* k create -f ingress-resource-1.yaml
 3190* k get pods
 3191* k get all
 3192* k get svc
 3193* k get all
 3194* k describe ing ingress-resource-1
 3195* k delete ingress ngress-resource-1
 3196* k delete ingress ingress-resource-1
 3197* k create -f ingress-resource-1.yaml
 3198  kubectl wait --namespace ingress-nginx \\n  --for=condition=ready pod \\n  --selector=app.kubernetes.io/component=controller \\n  --timeout=90s
 3199* k create -f ingress-resource-1.yaml
 3200  kubectl delete -A ValidatingWebhookConfiguration ingress-nginx-admission
 3201* k create -f ingress-resource-1.yaml
 3202* k get all
 3203  kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/mandatory.yaml
 3204* kubectl get nodes
 3205* kubectl get nodes -o wide
 3206* k get all
 3207* k get namespaces
 3208* k delete ingress ingress-resource-1
 3209* k get all
 3210* docker image ls
 3211* k apply -f deploy deploy.yml
 3212* k apply -f  deploy.yml
 3213* k get all
 3214* k expose deploy ngnix-deploy-main --port 80
 3215* k expose deploy nginx-deploy-main --port 80
 3216* k get svc
 3217* k delete ingress ingress-resource-1
 3218* k create -f ingress-resource-1.yaml
 3219* k get ing
 3220* k describe ing ingress-resource-1
 3221* k get svc
 3222* sudo vi /etc/host
 3223* sudo vi /etc/hosts
 3224* kubectl describe svc nginx-deploy-main
 3225* kubectl get ing -o yaml
 3226* kubectl get svc -A
 3227* netstat -a -n -o -b
 3228* $ kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/nginx-0.30.0/deploy/static/mandatory.yaml
 3229* k delete ingress ingress-resource-1
 3230* k create -f ingress-resource-1.yaml
 3231* k get svc
 3232* kubectl get svc -A
 3233* k get namespaces
 3234* kubectl delete ns ingress
 3235* k delete ingress ingress-resource-1
 3236* k create -f ingress-resource-1.yaml
 3237* kubectl expose deployment web --type=ClusterIP --port=8080
 3238* kubectl create deployment web --image=gcr.io/google-samples/hello-app:1.0
 3239* kubectl expose deployment web --type=ClusterIP --port=8080
 3240* kubectl get service web
 3241* k delete ingress ingress-resource-1
 3242* apiVersion: networking.k8s.io/v1beta1
 3243* kind: Ingress
 3244* metadata:
 3245* spec:
 3246* k create -f ingress-resource-1.yaml
 3247* kubectl get ingress
 3248* sudo vi /etc/hosts
 3249* kubectl get pods -n kube-system
 3250* kubectl get pods --all-namespaces | grep -i nginx-controller
 3251* kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/provider/baremetal/deploy.yaml
 3252* kubectl get ingress
 3253* cd ingress
 3254* k delete -f ingress-resource-1.yaml
 3255* kubectl delete -f ingress-resource-1.yaml
 3256* k create -f ingress-resource-1.yaml
 3257* alias k="kubectl"
 3258* k create -f ingress-resource-1.yaml
 3259* kubectl delete -A ValidatingWebhookConfiguration ingress-nginx-admission
 3260* k create -f ingress-resource-1.yaml
 3261* kubectl get pods -n ingress-nginx
 3262* kubectl -n ingress-nginx describe pod nginx-ingress-controller-54b86f8f7b-vndb8
 3263* kubectl get nodes - - show-labels
 3264* kubectl get nodes --show-labels
 3265* kubectl get serviceaccounts
 3266* kubectl get serviceaccounts/build-robot -o yaml
 3267* kubectl get serviceaccounts/my-ngnix-nginx-ingress -o yaml
 3268* kubectl get secrets
 3269* kubectl run nginx --image=nginx --restart=Never
 3270* k get pods
 3271* sudo vi /etc/hosts
 
 curl $(minikube ip)
  1212  k get svc
  1213  ssh -L 8887:10.101.119.40.30:31299 root@94.130.228.242
  1214  k get ing
  1215  k run -it --rm curl --restart=Never --image=nbrown/curl -- 10.101.119.40:80/lazy
  1216  alias k=kubectl
  1217  k run -it --rm curl --restart=Never --image=nbrown/curl -- 10.101.119.40:80/lazy
  1218  k get endpoints hello-deploy
  1219  alias k=kubectl
 
 3272* curl -D- http://203.0.113.3 -H 'Host: hello-world.info'
 3273  kubectl -n ingress-nginx get svc
 3274  k get svc
 3275  kubectl -n ingress-nginx get svc
 3276* curl -D- http://92.168.65.200 -H 'Host: hello-world.info'
 3277* kubectl -n ingress-nginx get pod -o wide
 3278  kubectl get ingress -o wide
 3279* k describe ing ingress-resource-1
 3280* k create -f ingress-resource-1.yaml
 3281* kubectl delete -A ValidatingWebhookConfiguration ingress-nginx-admission
 3282* k delete -f ingress-resource-1.yaml
 3283* k get all
 3284  kubectl get pods -n ingress-nginx -l
 3285  kubectl get pods -n ingress-nginx
 3286  k delete pods ingress-nginx-admission-create-88tzf
 3287  k delete pods ingress-nginx-admission-patch-wm2xh
 3288  k delete pods ingress-nginx-controller-848bfcb64d-twpcz
 3289* k describe ing ingress-resource-1
 3290* k create -f ingress-resource-1.yaml
 3291* k describe ing ingress-resource-1
 3292* kubectl get pods -n ingress-nginx
 3293* k get all
 3294* k describe ing ingress-resource-1
 3295* k describe ing example-ingress
 3296* k delete -f ingress-resource-1.yaml
 3297* k delete -f example-ingress
 3298* k delete -f example-ingress.yaml
 3299* k describe ing example-ingress
 3300* k delete -f ingress-resource-1.yaml
 3301* k create -f ingress-resource-1.yaml
 3302* sudo vi /etc/hosts
 3303* k describe ing example-ingress
 3304* alias k="kubectl"
 3305* k describe ing example-ingress
 3306* k describe ing ingress-resource-1
 3307* k delete -f ingress-resource-1.yaml
 3308* k get pods
 3309  k get nodes
 3310* k version --short
 3311  k get nodes
➜  ~