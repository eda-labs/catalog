# EDA Labs catalog
This catalog contains community created apps for Nokia Event-Driven Automation (EDA).

For the catalog with Nokia supported apps visit [https://docs.eda.dev](https://docs.eda.dev/26.4/apps/) for more info.

## Adding the catalog
Register the EDA Labs catalog with the EDA Store in your EDA instance by applying a Catalog CR with `edactl apply -f`:

```
apiVersion: appstore.eda.nokia.com/v1
kind: Catalog
metadata:
  name: eda-labs-catalog
  namespace: eda-system
spec:
  remoteType: git
  remoteURL: https://github.com/eda-labs/catalog.git
  skipTLSVerify: false
  title: EDA Labs Catalog
```

> [!NOTE]
> If you deployed EDA through the [Playground](https://docs.eda.dev/25.8/getting-started/try-eda/), the ghcr.io registry (used by EDA Labs) is already registered with the EDA Store, so only the Catalog CR needs to be applied.
