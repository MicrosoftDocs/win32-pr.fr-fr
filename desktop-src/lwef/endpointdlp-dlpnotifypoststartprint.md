---
description: Fournit au système des informations sur un document après le démarrage d’une opération d’impression.
title: DlpNotifyPostStartPrint, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 23caba53e754c54bfd717274b5f889ad224a2dc80fbe54fb97f70125c0c74f23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976579"
---
# <a name="dlpnotifypoststartprint-function"></a>DlpNotifyPostStartPrint fonction)

Fournit au système des informations sur un document après le démarrage d’une opération d’impression.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*DocumentInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document associé à l’opération d’impression.

</dd> </dl>

<dl> <dt>

*PrintInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) contenant des informations sur l’opération d’impression.

</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |