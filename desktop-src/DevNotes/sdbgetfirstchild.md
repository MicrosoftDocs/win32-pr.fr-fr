---
description: Recherche une BALIse enfant dans le parent spécifié et retourne le TAGID du premier enfant.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: SdbGetFirstChild fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58e63b3c1c8b3e56c9610ec795c1706fe58990e4611c36886ee4a3061d0816fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075973"
---
# <a name="sdbgetfirstchild-function"></a>SdbGetFirstChild fonction)

Recherche une BALIse enfant dans le parent spécifié et retourne le **TagId** du premier enfant.

## <a name="syntax"></a>Syntaxe


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tiParent* \[ dans\]
</dt> <dd>

**TagId** du début de la recherche. Ce paramètre peut être **TagId \_ racine** ou **\_ \_ liste de types de balises**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le **TagId** du premier enfant ou **TagId \_ null** n’est pas un enfant trouvé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetNextChild**](sdbgetnextchild.md)
</dt> </dl>

 

 




