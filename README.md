# Get all applications
- argocd app list
- kubectl get applications -n argocd
- kubectl describe application <application-name>

# Get all projects
- kubectl get appprojects -n argocd
- kubectl describe appproject <project-name> -n argocd
- k get appproject project-with-role -n argocd -o yaml

# Create argocd project token
- argocd proj role create-token project-with-role ci-role
- eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJhcmdvY2QiLCJzdWIiOiJwcm9qOnByb2plY3Qtd2l0aC1yb2xlOmNpLXJvbGUiLCJuYmYiOjE2NjY5Mzc0NTcsImlhdCI6MTY2NjkzNzQ1NywianRpIjoiYzg2YjE3ODktOTRlOC00OGM3LWFlZTgtNDUxNjQ4MTNiYTY1In0.X_e8v0uYWNpx8FCX2PbjKd-yb2rtjMh9FN1VeYx-Umg

# Delete argocd projects
- argocd app list
- argocd app delete <app-name> --auth-token <token>

# K8S Scaling command
- kubectl scale deployment.apps/guestbook-ui --replicas=10 -n auto-selfheal-demo
