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
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515879"
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



 

 




