---
description: Fournit au système des informations sur un document avant le lancement d’une opération Enregistrer sous.
title: DlpNotifyPreSaveAsDocument, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 1dbd565ac7a86e381e1e70facf79a2883182260f82c31a2e8a9a3de4f6da8f2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778219"
---
# <a name="dlpnotifypresaveasdocument-function"></a>DlpNotifyPreSaveAsDocument fonction)

Fournit au système des informations sur un document avant le lancement d’une opération Enregistrer sous.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DocumentInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document à enregistrer.

</dd> </dl>

<dl> <dt>

*Destination* \[ dans\]
</dt> <dd>

**LPCWSTR** contenant le chemin d’accès de destination du document à enregistrer.

</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |