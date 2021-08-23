---
description: Spécifie les informations d’État relatives à une opération DLP de point de terminaison.
title: DLP_POSTOP_STATUS, structure (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 6b8922bee5fb93ee4412833418a63c19dd311c8809cf64132a0f28fbe91d11bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610229"
---
# <a name="dlp_postop_status-structure"></a>Structure DLP_POSTOP_STATUS

Spécifie les informations d’État relatives à une opération DLP de point de terminaison.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a>Membres

<dl> <dt>

*Version* \[ de dans\]
</dt> <dd>

Valeur DWORD spécifiant la version de l’API. Cette valeur doit toujours être **DLP_POSTOP_STATUS_V_LATEST**. Cette constante est définie dans la liste des fichiers d’en-tête de l’exemple endpointdlp. h dans l’article [protection contre la perte de données](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*OperationSuccess* \[ dans\]
</dt> <dd>

Valeur BOOLÉENNE indiquant si l’opération d’ouverture a réussi.

</dd> </dl>





## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
