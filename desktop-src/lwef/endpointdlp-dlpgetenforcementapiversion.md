---
description: Récupère la version de l’API de protection contre la perte de données (DLP) du point de terminaison sur l’appareil actuel.
title: DlpGetEnforcementApiVersion, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495769"
---
# <a name="dlpgetenforcementapiversion-function"></a>DlpGetEnforcementApiVersion fonction)

Récupère la version de l’API de protection contre la perte de données (DLP) du point de terminaison sur l’appareil actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MajorVersion* \[ dans\]
</dt> <dd>

**Valeur DWORD** spécifiant le numéro de version principale.

</dd> </dl>

<dl> <dt>

*MajorVersion* \[ dans\]
</dt> <dd>

**Valeur DWORD** spécifiant le numéro de version mineure.

</dd> </dl>


## <a name="return-value"></a>Valeur renvoyée

Retourne un HRESULT incluant, sans s’y limiter, les valeurs suivantes.

| HRESULT | Description |
|---------|-------------|
| S_OK | La fonction s’est terminée avec succès |




## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |