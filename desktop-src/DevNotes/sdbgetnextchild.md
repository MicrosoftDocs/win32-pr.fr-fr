---
description: Recherche la BALIse enfant suivante dans le parent spécifié et retourne le TAGID de l’enfant suivant.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 210e0aab8cb5e43bfc649e8abb72cf565c4d4f892f651708286f7a3f87d11ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045309"
---
# <a name="sdbgetnextchild-function"></a>SdbGetNextChild fonction)

Recherche la BALIse enfant suivante dans le parent spécifié et retourne le **TagId** de l’enfant suivant.

## <a name="syntax"></a>Syntaxe


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
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

</dd> <dt>

*tiPrev* \[ dans\]
</dt> <dd>

**TagId** de l’enfant précédent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**TagId** de l’enfant ou **TagId \_ null** si aucun enfant n’est trouvé.

## <a name="remarks"></a>Remarques

Avant d’appeler cette fonction, appelez la fonction [**SdbGetFirstChild**](sdbgetfirstchild.md) .

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

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




