---
description: Associe une action de protection contre la perte de données (DLP) au niveau de l’application.
title: Structure DLP_APP_OP_ENLIGHTENED_LEVEL (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495786"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>Structure DLP_APP_OP_ENLIGHTENED_LEVEL

Associe une action de protection contre la perte de données (DLP) au niveau de l’application.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>Membres

<dl> <dt>

*Opération* \[ dans\]
</dt> <dd>

Valeur de l’énumération [DlpActionType](endpointdlp-dlpactiontype.md) qui spécifie le type d’action DLP de point de terminaison.

</dd> </dl>

<dl> <dt>

*AppEnforcementLevel* \[ dans\]
</dt> <dd>

Valeur de [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) qui spécifie le niveau de mise en application pour le type d’action DLP de point de terminaison associé.

</dd> </dl>





## <a name="remarks"></a>Notes

Transmettez un tableau de ces structures dans [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) pour définir le mode de mise en application pour un ensemble d’opérations DLP de point de terminaison.

## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |

