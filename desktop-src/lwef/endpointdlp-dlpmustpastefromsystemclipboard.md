---
description: Détermine si l’application doit extraire les données du presse-papiers du système au lieu de les extraire de son cache interne.
title: DlpMustPasteFromSystemClipboard, fonction (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e111cb85c6eada6f84f7bc10eb240e89447a173e741b26b316b232d742f8de48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888579"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>DlpMustPasteFromSystemClipboard fonction)

Détermine si l’application doit extraire les données du presse-papiers du système au lieu de les extraire de son cache interne.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>Valeur de retour

TRUE si l’appel dans le presse-papiers du système d’exploitation est obligatoire ; Sinon, FALSe.

## <a name="remarks"></a>Notes


## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |