# popup-infra: a sample MongoDB deployment

This is a collection of Ansible roles & playbooks that will create a sharded cluster **with no authentication or encryption** on
DigitalOcean.
Because of the lack of security, the (9) servers it brings up will be bound only to localhost and the private IP address
assigned by DigitalOcean.
To use it, you need to create a digital_ocean.ini file containing an `api_token` value that has read and write access to the API.
(I recommend that you *don't* check the digital_ocean.ini file into source control.)

```
[digital_ocean]
api_token = YOUR-TOKEN-HERE
```

This set of roles & playbooks was created for Ansible learning purposes only, not to provide a template for a production system.
If you want sharded MongoDB, but don't want to learn the nitty-gritty of administering it, I'd suggest you look into a hosted
solution like [Atlas][atlas] or [mLab][mlab].

[atlas]: https://www.mongodb.com/cloud/atlas
[mlab]: https://mlab.com/