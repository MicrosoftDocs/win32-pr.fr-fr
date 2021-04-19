---
description: Spécifie des informations sur un document associé à une opération d’impression DLP de point de terminaison.
title: Structure DLP_PRINT_INFO (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495778"
---
# <a name="dlp_print_info-structure"></a>Structure DLP_PRINT_INFO

Spécifie des informations sur un document associé à une opération d’impression DLP de point de terminaison.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a>Membres

<dl> <dt>

*Version* \[ de dans\]
</dt> <dd>

Valeur DWORD spécifiant la version de l’API. Cette valeur doit toujours être **DLP_PRINT_INFO_V_LATEST**. Cette constante est définie dans la liste des fichiers d’en-tête de l’exemple endpointdlp. h dans l’article [protection contre la perte de données](endpointdlp-endpoint-data-loss-prevention.md).

</dd> </dl>

<dl> <dt>

*Nom_imprimante* \[ dans\]
</dt> <dd>

LPCWSTR identifiant l’imprimante de destination.

</dd> </dl>

<dl> <dt>

*JobName* \[ dans\]
</dt> <dd>

LPCWSTR spécifiant le nom du travail d’impression.

</dd> </dl>

<dl> <dt>

*OutputFileName* \[ dans\]
</dt> <dd>

LPCWSTR spécifiant le chemin d’accès au fichier de sortie, lors de l’impression dans un fichier.

</dd> </dl>



## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |

