---
description: Associe une action de protection contre la perte de données (DLP) au niveau de l’application.
title: DLP_APP_OP_ENLIGHTENED_LEVEL, structure (endpointdlp.h)
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
ms.openlocfilehash: e47fa7705701701af2fc0832c5ea27cfdc7d1e67948ec095f3c24837a93de18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610479"
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





## <a name="remarks"></a>Remarques

Transmettez un tableau de ces structures dans [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) pour définir le mode de mise en application pour un ensemble d’opérations DLP de point de terminaison.

## <a name="requirements"></a>Configuration requise



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |

