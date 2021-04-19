---
description: Indique au système les modes de mise en conformité souhaités pour un ensemble d’opérations de protection contre la perte de données (DLP) de point de terminaison.
title: DlpInitializeEnforcementMode, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495523"
---
# <a name="dlpinitializeenforcementmode-function"></a>DlpInitializeEnforcementMode fonction)

Indique au système les modes de mise en conformité souhaités pour un ensemble d’opérations de protection contre la perte de données (DLP) de point de terminaison.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nombre* \[ dans\]
</dt> <dd>

**Valeur DWORD** spécifiant le nombre d’opérations incluses dans le tableau *OperationEnforcement* .

</dd> </dl>

<dl> <dt>

*OperationEnforcement* \[ dans\]
</dt> <dd>

Tableau de structures [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) qui spécifient le niveau d’application pour une opération DLP de point de terminaison.

</dd> </dl>


## <a name="return-value"></a>Valeur renvoyée

Retourne un HRESULT incluant, sans s’y limiter, les valeurs suivantes.

| HRESULT | Description |
|---------|-------------|
| S_OK | La fonction s’est terminée avec succès |
| E_INVALIDARG | Un ou plusieurs des paramètres de fonction ne sont pas valides. |
| E_OUTOFMEMORY | L’allocation de mémoire pour l’opération a échoué. |



## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |