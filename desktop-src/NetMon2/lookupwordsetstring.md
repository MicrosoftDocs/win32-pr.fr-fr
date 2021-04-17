---
description: La fonction LookupWordSetString retourne la chaîne correspondant à la valeur demandée d’un jeu étiqueté.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: LookupWordSetString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526763"
---
# <a name="lookupwordsetstring-function"></a>LookupWordSetString fonction)

La fonction **LookupWordSetString** retourne la chaîne correspondant à la valeur demandée d’un jeu étiqueté.

## <a name="syntax"></a>Syntaxe


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpSet* 
</dt> <dd>

Jeu étiqueté à partir duquel vous extrayez l’étiquette de la valeur.

</dd> <dt>

*Valeur* 
</dt> <dd>

Valeur d’un jeu étiqueté.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une chaîne qui correspond à la valeur demandée.

Si la fonction échoue, la valeur spécifiée n’est pas dans l’ensemble, la valeur de retour est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




