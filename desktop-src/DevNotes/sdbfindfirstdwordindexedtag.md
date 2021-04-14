---
description: Recherche le premier enregistrement DWORD de l’index spécifié qui répond aux critères spécifiés.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522815"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>SdbFindFirstDWORDIndexedTag fonction)

Recherche le premier enregistrement **DWORD** de l’index spécifié qui répond aux critères spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
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

Type de l'index. Pour obtenir la liste des valeurs, consultez [**tag**](tag.md) .

</dd> <dt>

*tKey* \[ dans\]
</dt> <dd>

Type de clé.

</dd> <dt>

*dwName* \[ dans\]
</dt> <dd>

Nom des données à trouver. Cette valeur est convertie en clé.

</dd> <dt>

*pFindInfo* \[ à\]
</dt> <dd>

Structure [**d' \_ informations de recherche**](find-info.md) qui reçoit l’enregistrement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**TagId** de la première correspondance ou **balise \_ null** si aucune correspondance n’est trouvée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




