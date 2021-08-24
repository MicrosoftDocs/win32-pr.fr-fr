---
description: Fournit au système des informations sur un document avant le lancement d’une opération coller à partir du presse-papiers.
title: DlpNotifyPrePasteFromClipboard, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b490f4f5a258805c785822d815d9e341feb8bbd494e428eb7bf1be6da843d775
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778179"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a>DlpNotifyPrePasteFromClipboard fonction)

Fournit au système des informations sur un document avant le lancement d’une opération coller à partir du presse-papiers.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DocumentInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document dans lequel le contenu est collé.

</dd> </dl>




## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |