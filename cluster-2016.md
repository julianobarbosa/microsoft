# Microsoft Cluster 2015

## Get Cluster Level
```console
Get-Cluster | Select ClusterFunctionalLevel
```

## Update Cluster Level
```console
Update-ClusterFunctionalLevel
```

## Get Cluster Log
```console
Get-ClusterLog -UseLocalTime
```

## Metric’s can be manually configured as well
### Cluster automatically assigned mode (default)
```console
(Get-ClusterNetwork “Cluster Network 1").AutoMetric = $true
```
### Manually set
```console
(Get-ClusterNetwork “Cluster Network 2").Metric = 40000
```

## Modifyin Heartbeats During Create Cluster
```console
HKLM\SYSTEM\CurrentControlSet\Services\ClusSvc\Parameters
- SetHeartbeatThresholdOnClusterCreate
- DWORD - 10
```

# SMB
```console
Get-SmbServerConfiguration
```

# Reference
https://docs.microsoft.com/en-us/windows-server/failover-clustering/failover-clustering-overview
