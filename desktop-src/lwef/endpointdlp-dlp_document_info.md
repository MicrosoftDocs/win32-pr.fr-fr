---
description: Spécifie des informations sur un document associé à une opération DLP de point de terminaison.
title: Structure DLP_DOCUMENT_INFO (endpointdlp. h)
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
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495785"
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

