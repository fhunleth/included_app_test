Run:

```sh
cd test
mix deps.get
mix release
```

You should see this:

```text
==> Release failed, during .boot generation:
        Circular dependencies among applications: [{test,"0.1.0"},{b,"0.1.0"}]
```

To fix, add `b` to the `included_applications`.
