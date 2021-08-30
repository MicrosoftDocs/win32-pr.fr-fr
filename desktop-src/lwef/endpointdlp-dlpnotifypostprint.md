---
description: Fournit au système des informations sur un document une fois l’opération d’impression terminée.
title: DlpNotifyPostPrint, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d471d9de9afaf1017a374b3b4ad9e90b5e966f68012902315b843bac3164de99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778249"
---
# <a name="dlpnotifypostprint-function"></a>DlpNotifyPostPrint fonction)

Fournit au système des informations sur un document une fois l’opération d’impression terminée.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
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

<dl> <dt>

*OpStatus* \[ dans\]
</dt> <dd>

Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération d’impression.

</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |