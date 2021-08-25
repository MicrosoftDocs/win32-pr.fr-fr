---
title: Méthode IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread
description: Cette API déterminera si le jeton du contexte actuel a accès à la classe d’interface de périphérique spécifiée. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- Méthode DeviceInterfaceClassAccessCheckWithCallingThread API Broker d’accès du périphérique
- Méthode DeviceInterfaceClassAccessCheckWithCallingThread API Broker d’accès du périphérique, interface IDeviceAccessPolicyCheck
- API Broker d’accès du périphérique de l’interface IDeviceAccessPolicyCheck, méthode DeviceInterfaceClassAccessCheckWithCallingThread
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f279972c3b716f111fa37fc2dd01ef9184b2f804f07106f6b971358daf290c44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635349"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>IDeviceAccessPolicyCheck ::D méthode eviceInterfaceClassAccessCheckWithCallingThread

> [!Important]  
> Ces interfaces ne sont pas prises en charge et ne doivent pas être utilisées. Utilisez plutôt les API dans la [référence de programmation C++ de l’API d’accès à l’appareil](device-access-api-c---programming-reference.md) .

Cette API déterminera si le jeton du contexte actuel a accès à la classe d’interface de périphérique spécifiée. IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszDeviceInterfaceClassGuid* \[ dans\]
</dt> <dd>

GUID de la classe d’interface de l’appareil pour lequel l’accès doit être vérifié.

</dd> <dt>

*dwClientThreadId* \[ dans\]
</dt> <dd>

ID de thread client où toute interface utilisateur associée doit être affichée si nécessaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est réussie, elle retourne S_OK. Sinon, elle retourne un code d’erreur HRESULT.
