---
description: Fournit au système des informations sur un document avant le lancement de l’opération de fermeture du document.
title: DlpNotifyCloseDocument, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: f8818e55482420c6b1fd307392138b99d391f4df9b703477ce4c3e950b36f4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962779"
---
# <a name="dlpnotifyclosedocument-function"></a>DlpNotifyCloseDocument fonction)

Fournit au système des informations sur un document avant le lancement de l’opération de fermeture du document.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DocumentInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) contenant des informations sur le document à ouvrir.

</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne void.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |