# Troubleshooting Log

## Issue 001: Unknown Device in Windows Device Manager

### Problem

During the initial hardware inspection, Windows 7 Device Manager displayed an unknown device with a yellow warning symbol.

### Investigation

Opened Device Manager and navigated to:

`Unknown Device → Properties → Details → Hardware Ids`

The following hardware identifiers were reported:

```text
ACPI\AWY0001
*AWY0001
```

### Findings

The identifiers correspond to an Away Mode System device, associated with legacy power-management functionality.

The device was not recognized correctly by the existing Windows installation.

### Resolution

No driver was installed because the computer is being repurposed as a Linux server.

The device is not expected to affect basic Linux server operation.

### Status

Identified. No further Windows troubleshooting required.

---

## Issue 002: Hard Drive Health Verification

### Objective

Determine whether the existing Western Digital 320 GB hard drive reports a predicted failure before reusing it for Linux.

### Diagnostic Command

Executed in an elevated Windows Command Prompt:

```cmd
wmic diskdrive get model,status
```

### Result

```text
Model                                 Status
WDC WD3200AAKS-75SBA SCSI Disk Device OK
```

### Findings

Windows reported an OK status for the installed hard drive.

This is only a basic health indicator and does not rule out bad sectors or other developing drive problems.

### Next Steps

Perform a detailed S.M.A.R.T. assessment using a compatible diagnostic tool.

### Status

Initial check completed. Detailed assessment pending.