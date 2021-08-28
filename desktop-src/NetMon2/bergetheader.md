---
description: La fonction BERGetHeader décode un en-tête Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: BERGetHeader, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d6dfd50856202e78177d2ad259b16638f466d9bca236a691c65802ce2758c948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012305"
---
# <a name="bergetheader-function"></a>BERGetHeader fonction)

La fonction **BERGetHeader** décode un en-tête Choice.

## <a name="syntax"></a>Syntaxe


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Pointeur désignant l’en-tête Choice.

</dd> <dt>

*pTag* 
</dt> <dd>

Pointeur désignant la balise retournée.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Pointeur vers la longueur d’en-tête retournée.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Pointeur vers la longueur des données retournées.

</dd> <dt>

*ppNext* 
</dt> <dd>

Pointeur vers le contenu d’en-tête.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (autrement dit, un en-tête de choix BER valide est trouvé), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




