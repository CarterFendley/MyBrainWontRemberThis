## Add new key to GitHub

Generate key locally (Add password if feeling perticularly paranoid)

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Start ssh-agent (Not 100% sure why we do this)

```
eval "$(ssh-agent -s)"
```

Add newly added key to agent

```
ssh-add ~/.ssh/id_rsa
```

Add new key to github (GitHub > Settings > SSH and GPG keys (sidebar) > Add SSH key)

**Note: Only copy the `.pub` you imbecile**

### Verification 

```
ssh -T git@github.com
```
