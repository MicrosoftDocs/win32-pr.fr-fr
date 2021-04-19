---
description: Fournit au système des informations sur un document après le démarrage d’une opération d’impression.
title: DlpNotifyPostStartPrint, fonction (endpointdlp. h)
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
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495476"
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


## <a name="return-value"></a>Valeur renvoyée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |