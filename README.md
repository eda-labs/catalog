# EDA Labs catalog

This catalog contains community-created apps for Nokia Event-Driven Automation (EDA).

For the catalog with Nokia-supported apps visit [https://docs.eda.dev](https://docs.eda.dev/26.4/apps/) for more info.

## Adding the catalog

Register the EDA Labs catalog with the EDA Store in your EDA instance by applying a Catalog CR with `edactl apply -f` or by creating this resource in the EDA UI (System Administration -> Catalogs):

```yaml
apiVersion: appstore.eda.nokia.com/v1
kind: Catalog
metadata:
  name: eda-labs-catalog
  namespace: eda-system
spec:
  remoteType: git
  remoteURL: https://github.com/eda-labs/catalog
  skipTLSVerify: false
  title: EDA Labs Catalog
```
