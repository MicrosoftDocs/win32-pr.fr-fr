---
Description: Récupère la valeur QWORD pour le TAGID spécifié.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: SdbReadQWORDTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4280c21983fa86312229930b7496625c594f0caac384f0dc6d130f673ce68509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815279"
---
# <a name="sdbreadqwordtag-function"></a>SdbReadQWORDTag fonction)

Récupère la valeur **QWord** pour le **TagId** spécifié.

## <a name="syntax"></a>Syntaxe


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tiWhich* \[ dans\]
</dt> <dd>

**TagId** qui correspond aux données à récupérer.

</dd> <dt>

*qwDefault* \[ dans\]
</dt> <dd>

Valeur par défaut à retourner en cas d’échec.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne la valeur en cas de réussite ou *qwDefault* en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




