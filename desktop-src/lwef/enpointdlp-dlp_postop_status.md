---
description: Spécifie les informations d’État relatives à une opération DLP de point de terminaison.
title: Structure DLP_POSTOP_STATUS (endpointdlp. h)
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
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495440"
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
