---
description: Crée une nouvelle BALIse de liste pour les opérations d’écriture.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: SdbBeginWriteListTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748748"
---
# <a name="sdbbeginwritelisttag-function"></a>SdbBeginWriteListTag fonction)

Crée une nouvelle BALIse de liste pour les opérations d’écriture.

## <a name="syntax"></a>Syntaxe


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tTag* \[ dans\]
</dt> <dd>

BALIse pour la nouvelle entrée. Cette valeur doit être de type **\_ \_ liste de types de balises**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne le [**TagId**](tagid.md) de la nouvelle liste en cas de réussite ou **TagId \_ null** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> <dt>

[**SdbEndWriteListTag**](sdbendwritelisttag.md)
</dt> <dt>

[**Référence**](tag.md)
</dt> <dt>

[Types de BALISes](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




