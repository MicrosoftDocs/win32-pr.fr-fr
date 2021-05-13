---
description: Libère le descripteur associé à la liste des derniers fichiers utilisés (MRU) et écrit les données mises en cache dans le registre.
title: FreeMRUList fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840620"
---
# <a name="freemrulist-function"></a>FreeMRUList fonction)

Libère le descripteur associé à la liste des derniers fichiers utilisés (MRU) et écrit les données mises en cache dans le registre.

## <a name="syntax"></a>Syntaxe


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMRU* \[ dans\]
</dt> <dd>

Type : **handle**

Handle de la liste MRU à libérer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **int**

Retourne une valeur non négative en cas de réussite,-1 dans le cas contraire.

## <a name="remarks"></a>Notes

Si la liste MRU a été créée à l’aide de l’indicateur **\_ CACHEWRITE MRU** , l’appel de **FreeMRUList** entraîne l’écriture des modifications qui n’ont pas encore été écrites dans la version de la liste MRU stockée dans le registre.

Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque. Elle doit être extraite de comctl32.dll par l’ordinal 152.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 




