---
description: Spécifie le niveau d’application d’une opération de protection contre la perte de données (DLP) de point de terminaison.
title: DlpAppEnforceLevel, énumération (endpointdlp.h)
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
ms.openlocfilehash: 99bd06a41c88ff0b5a02b9b329877c015aea7dfb3fdbc58fea3c2e305829faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349349"
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



## <a name="remarks"></a>Remarques

Les valeurs de cette énumération sont utilisées par la structure [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .


## <a name="requirements"></a>Configuration requise



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |

