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
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385199"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
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

 

 




