---
description: Fournit au système des informations sur un document après la fin de l’opération coller à partir du presse-papiers.
title: DlpNotifyPostPasteFromClipboard, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 8f40b8338164e992bc9102a37d386f9b470e2159cdc7507ca0cf4c4567fb524b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349279"
---
# <a name="dlpnotifypostpastefromclipboard-function"></a>DlpNotifyPostPasteFromClipboard fonction)

Fournit au système des informations sur un document après la fin de l’opération coller à partir du presse-papiers.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DocumentInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document dans lequel le contenu a été copié.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ dans\]
</dt> <dd>

Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération de collage à partir du presse-papiers.

</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |