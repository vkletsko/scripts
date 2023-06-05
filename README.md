# scripts
## Usage
add prefix "kubectl-" to the script name and place it in your PATH
```
kubectl-<scriptname>
```

To use a plugin, make the plugin executable:
```
sudo chmod +x ./kubectl-kubeplugin
```
and place it anywhere in your PATH:
```
sudo mv ./kubectl-kubeplugin /usr/local/bin
```

You may now invoke your plugin as a kubectl command:
``` 
kubectl kubeplugin
```

All args and flags are passed as-is to the executable:
```
kubectl kubeplugin top <resource_type> <podname> <namespace>
```

example
```
kubectl kubeplugin top pod nginx-8f458dc5b-czt8p default
```

example for logs
```
kubectl kubeplugin logs pod nginx-8f458dc5b-czt8p default
```

# check that kubectl recognizes your plugin
```
kubectl plugin list
```