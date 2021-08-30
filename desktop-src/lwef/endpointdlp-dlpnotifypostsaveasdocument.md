---
description: Fournit au système des informations sur un document après la fin de l’opération Enregistrer sous.
title: DlpNotifyPostSaveAsDocument, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ebdf21bd4d4d212c66ae54c4439e30b9efbf91b9c7ffeb1d3edef0b6e8efdc3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962749"
---
# <a name="dlpnotifypostsaveasdocument-function"></a>DlpNotifyPostSaveAsDocument fonction)

Fournit au système des informations sur un document après la fin de l’opération Enregistrer sous.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*DocumentInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document qui a été enregistré.

</dd> </dl>

<dl> <dt>

*Destination* \[ dans\]
</dt> <dd>

**LPCWSTR** contenant le chemin d’accès de destination du document qui a été enregistré.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ dans\]
</dt> <dd>

Pointeur vers une structure [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) contenant des informations d’État sur l’opération Enregistrer sous.

</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |