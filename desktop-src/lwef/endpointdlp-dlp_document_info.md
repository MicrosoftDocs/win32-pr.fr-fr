---
description: Spécifie des informations sur un document associé à une opération DLP de point de terminaison.
title: DLP_DOCUMENT_INFO, structure (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 8aa4b6c961b4e80786e9ada480949245b032750499b38f0deead44f97a2d88fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479762"
---
# <a name="dlp_document_info-structure"></a>Structure DLP_DOCUMENT_INFO

Spécifie des informations sur un document associé à une opération DLP de point de terminaison.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a>Membres

<dl> <dt>

*Version* \[ de dans\]
</dt> <dd>

Valeur DWORD spécifiant la version de l’API. Cette valeur doit toujours être **DLP_DOCUMENT_INFO_V_LATEST**. Cette constante est définie dans la liste des fichiers d’en-tête de l’exemple endpointdlp. h dans l’article [protection contre la perte de données](endpointdlp-endpoint-data-loss-prevention.md).

</dd> </dl>

<dl> <dt>

*PersistentFileName* \[ dans\]
</dt> <dd>

LPCWSTR spécifiant le chemin d’accès d’origine du document.

</dd> </dl>

<dl> <dt>

*LocalFileName* \[ dans\]
</dt> <dd>

LPCWSTR spécifiant le chemin d’accès au fichier de sauvegarde réel du document.

</dd> </dl>



## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |

