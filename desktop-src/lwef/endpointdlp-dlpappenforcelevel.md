---
description: Spécifie le niveau d’application d’une opération de protection contre la perte de données (DLP) de point de terminaison.
title: Énumération DlpAppEnforceLevel (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495770"
---
# <a name="dlpappenforcelevel-enumeration"></a>Énumération DlpAppEnforceLevel

Spécifie le niveau d’application d’une opération de protection contre la perte de données (DLP) de point de terminaison.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a>Constantes

<dl> <dt>

*DlpAppEnforceLevelNone* \[ dans\]
</dt> <dd>

Aucune mise en application par l’application. Le système DLP applique l’opération.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelNotify* \[ dans\]
</dt> <dd>

L’application un utilise les API DLP pour informer le système DLP de l’opération. Le système DLP applique l’opération.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelPrevent* \[ dans\]
</dt> <dd>

Non pris en charge dans la version actuelle.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelFull* \[ dans\]
</dt> <dd>

Non pris en charge dans la version actuelle.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelCount* \[ dans\]
</dt> <dd>

Valeur maximale de l’énumération.

</dd> </dl>



## <a name="remarks"></a>Notes

Les valeurs de cette énumération sont utilisées par la structure [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |

