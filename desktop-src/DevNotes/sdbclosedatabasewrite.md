---
description: Ferme la base de données spécifiée.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: SdbCloseDatabaseWrite fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0ef1c02731f2875fbdfc910243ed80faa28b6ab029314ea43ef281355a08487a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161580"
---
# <a name="sdbclosedatabasewrite-function"></a>SdbCloseDatabaseWrite fonction)

Ferme la base de données spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ in, out\]
</dt> <dd>

Handle de la base de données de shims.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction appelle [**SdbCloseDatabase**](sdbclosedatabase.md); par conséquent, ces deux fonctions sont équivalentes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
</dt> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbEndWriteListTag**](sdbendwritelisttag.md)
</dt> </dl>

 

 




