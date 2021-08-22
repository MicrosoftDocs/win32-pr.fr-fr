---
description: Fournit au système des informations d’État après la fin d’une opération de presse-papiers.
title: DlpNotifyPostStashClipboard, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 97366a356b960fb8bea87bf552bf98576363663a6ca21de290d4035414fcb904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751658"
---
# <a name="dlpnotifypoststashclipboard-function"></a>DlpNotifyPostStashClipboard fonction)

Fournit au système des informations d’État après la fin d’une opération de presse-papiers.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Paramètres


<dl> <dt>

*OpStatus* \[ dans\]
</dt> <dd>

Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération de dissimulation du presse-papiers.

</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |