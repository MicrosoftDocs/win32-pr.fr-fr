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
ms.openlocfilehash: 40f54dfc109ec2f7f4807d57052b9c4e1f99d5b629e8028be2931d9b42081f43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161570"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




