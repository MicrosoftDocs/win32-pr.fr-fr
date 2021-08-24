---
description: Fournit au système des informations sur un fichier de document avant le lancement d’une opération d’ouverture.
title: DlpNotifyPreOpenDocumentFile, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: f2be797d0f4045f17e753031247797406f332afa2fcc47b3ca83973527d99216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778229"
---
# <a name="dlpnotifypreopendocumentfile-function"></a>DlpNotifyPreOpenDocumentFile fonction)

Fournit au système des informations sur un fichier de document avant le lancement d’une opération d’ouverture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
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