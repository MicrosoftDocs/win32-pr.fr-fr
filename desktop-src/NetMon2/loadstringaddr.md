---
description: La fonction LoadStringAddr transforme une chaîne (par exemple &\# 0034 ; 157.54.32.45&\# 0034 ;) et crée une adresse DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: LoadStringAddr, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5c706d47c6923de0c01f346430e8050eb94484782cf030186e1ef865f220cc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037139"
---
# <a name="loadstringaddr-function"></a>LoadStringAddr fonction)

La fonction **LoadStringAddr** transforme une chaîne (telle que « 157.54.32.45 ») et crée une adresse **DWORD** .

## <a name="syntax"></a>Syntaxe


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAddress* 
</dt> <dd>

Pointeur vers une **valeur DWORD**.

</dd> <dt>

*str* 
</dt> <dd>

Pointeur désignant une chaîne de caractères avec la représentation x. x de l’adresse IP (par exemple, 127.0.0.1).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction a réussi (le nom de l’adresse a été trouvé); la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




