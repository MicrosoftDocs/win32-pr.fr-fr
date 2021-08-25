---
description: Fournit au système des informations sur un document après l’exécution d’une opération glisser-déplacer.
title: DlpNotifyPostDragDrop, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 3d20f9356007973b580d136aef1a74b8206026bf62fe14c5db46eb2cc0cbf1f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062109"
---
# <a name="dlpnotifypostdragdrop-function"></a>DlpNotifyPostDragDrop fonction)

Fournit au système des informations sur un document après l’exécution d’une opération glisser-déplacer.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DocumentInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document associé à l’opération glisser-déplacer.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ dans\]
</dt> <dd>

Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur le glisser-déplacer.

</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |