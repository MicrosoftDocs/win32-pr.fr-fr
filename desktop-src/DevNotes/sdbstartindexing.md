---
description: Active la création et la modification d’index pour la base de données spécifiée.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: SdbStartIndexing fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3643936511755642cf9997709faa69d7bb3e902e5cf3e9dd2b0f56bda681b381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815269"
---
# <a name="sdbstartindexing-function"></a>SdbStartIndexing fonction)

Active la création et la modification d’index pour la base de données spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*iiWhich* \[ dans\]
</dt> <dd>

Identificateur d’index.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




