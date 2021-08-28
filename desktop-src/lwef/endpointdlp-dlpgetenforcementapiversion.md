---
description: Récupère la version de l’API de protection contre la perte de données (DLP) du point de terminaison sur l’appareil actuel.
title: DlpGetEnforcementApiVersion, fonction (endpointdlp.h)
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
ms.openlocfilehash: d126b720f1b6a0912598671c75240fb7f2a351098fc1fb00a748d873d1481905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725799"
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


## <a name="return-value"></a>Valeur retournée

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