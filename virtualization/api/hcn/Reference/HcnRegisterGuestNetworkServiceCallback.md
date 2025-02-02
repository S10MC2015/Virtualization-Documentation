---
title: HcnRegisterGuestNetworkServiceCallback
description: HcnRegisterGuestNetworkServiceCallback
author: Keith-Mange
ms.author: kemange
ms.topic: reference
ms.prod: virtualization
ms.technology: virtualization
ms.date: 10/31/2021
api_name:
- HcnRegisterGuestNetworkServiceCallback
api_location:
- computenetwork.dll
api_type:
- DllExport
topic_type:
- apiref
---
# HcnRegisterGuestNetworkServiceCallback

## Description

Registers a callback function to receive GuestNetworkService notifications.

## Syntax

```cpp
HRESULT
WINAPI
HcnRegisterGuestNetworkServiceCallback(
    _In_ HCN_GUESTNETWORKSERVICE GuestNetworkService,
    _In_ HCN_NOTIFICATION_CALLBACK Callback,
    _In_ void* Context,
    _Outptr_ HCN_CALLBACK* CallbackHandle
    );
```

## Parameters

`GuestNetworkService`

The [HCN_GUESTNETWORKSERVICE](./HCN_GUESTNETWORKSERVICE.md) for the callback.

`Callback`

The [HCN_NOTIFICATION_CALLBACK](./HCN_NOTIFICATION_CALLBACK.md) for the callback.

`Context`

Context that is provided on the callbacks.

`CallbackHandle`

Receives a [HCN_CALLBACK](./HCN_CALLBACK.md). It is the responsibility of the caller to release the handle using [HcnUnregisterGuestNetworkServiceCallback](./HcnUnregisterGuestNetworkServiceCallback.md) once it is no longer in use.

## Return Values

The function returns [HRESULT](./HCNHResult.md).

## Requirements

|Parameter|Description|
|---|---|
| **Minimum supported client** | Windows 10, version 1809 |
| **Minimum supported server** | Windows Server 2019 |
| **Target Platform** | Windows |
| **Header** | ComputeNetwork.h |
| **Library** | ComputeNetwork.lib |
| **Dll** | ComputeNetwork.dll |

