---
description: Fournit au système des informations sur un document après l’exécution d’une opération copier dans le presse-papiers.
title: DlpNotifyPostCopyToClipboard, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b4b1a375d68819fc36f82a530a7fe7a8abe881c0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495508"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a>DlpNotifyPostCopyToClipboard fonction)

Fournit au système des informations sur un document après l’exécution d’une opération copier dans le presse-papiers.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DocumentInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document à partir duquel le contenu a été copié.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ dans\]
</dt> <dd>

Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération copier dans le presse-papiers.

</dd> </dl>


## <a name="return-value"></a>Valeur renvoyée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |