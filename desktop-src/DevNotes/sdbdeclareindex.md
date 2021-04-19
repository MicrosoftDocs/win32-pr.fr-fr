---
description: Déclare un nouvel index dans la base de données spécifiée.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516387"
---
# <a name="sdbdeclareindex-function"></a>SdbDeclareIndex fonction)

Déclare un nouvel index dans la base de données spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tWhich* \[ dans\]
</dt> <dd>

Ce paramètre doit être **une \_ \_ liste de types de balises**.

</dd> <dt>

*tKey* \[ dans\]
</dt> <dd>

BALIse qui spécifie le type à utiliser comme clé. Ce paramètre ne peut pas être une **\_ \_ liste de types de balises**.

</dd> <dt>

*dwEntries* \[ dans\]
</dt> <dd>

Nombre d’entrées à allouer dans l’index.

</dd> <dt>

*bUniqueKey* \[ dans\]
</dt> <dd>

Si ce paramètre a la **valeur true**, l’index est un index de clé unique.

</dd> <dt>

*piiIndex* \[ à\]
</dt> <dd>

**IndexID contient** résultant de l’index nouvellement déclaré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="remarks"></a>Notes

Appelez cette fonction avant d’écrire des balises dans le nouvel index.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INDEXID contient**](indexid.md)
</dt> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




