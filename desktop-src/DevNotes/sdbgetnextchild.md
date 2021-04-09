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
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861049"
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

## <a name="remarks"></a>Notes

Avant d’appeler cette fonction, appelez la fonction [**SdbGetFirstChild**](sdbgetfirstchild.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




