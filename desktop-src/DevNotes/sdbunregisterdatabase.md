---
description: Annule l’inscription de la base de données spécifiée, ce qui la rend n’est plus disponible.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2ea0cfeedbf74bea02af60b8c01d04b9e0e02f527ba35c0478da801253687b8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815309"
---
# <a name="sdbunregisterdatabase-function"></a>SdbUnregisterDatabase fonction)

Annule l’inscription de la base de données spécifiée, ce qui la rend n’est plus disponible.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguidDB* \[ dans\]
</dt> <dd>

GUID de la base de données. Ce paramètre ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




