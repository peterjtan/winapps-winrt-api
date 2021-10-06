---
-api-id: M:Microsoft.Windows.ApplicationModel.WindowsAppRuntime.DeploymentManager.Initialize
-api-type: winrt method
---

# Microsoft.Windows.ApplicationModel.WindowsAppRuntime.DeploymentManager.Initialize

<!--
public static Microsoft.Windows.ApplicationModel.WindowsAppRuntime.DeploymentResult Initialize ();
-->


## -description

Checks the status of the Windows App SDK runtime referenced by the current package and attempts to register any missing packages that can be registered.

## -returns

An object that provides deployment status and error information for the Windows App SDK runtime referenced by the current package.

## -remarks

If an error occurs during a package install, the [ExtendedError](deploymentresult_extendederror.md) property of the return value will contain the first error that was encountered.

If multiple packages are required for install, this method will attempt to install all required packages. If an error occurs during one of the subsequent package installations, packages that were successfully installed earlier will not be rolled back.

## -see-also

[Deployment guide for packaged apps](/windows/apps/windows-app-sdk/deploy-packaged-apps)

## -examples

