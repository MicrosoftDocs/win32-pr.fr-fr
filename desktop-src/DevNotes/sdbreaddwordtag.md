---
Description: Récupère la valeur DWORD pour le TAGID spécifié.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: SdbReadDWORDTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105928"
---
# <a name="sdbreaddwordtag-function"></a>SdbReadDWORDTag fonction)

Récupère la valeur **DWORD** pour le **TagId** spécifié.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
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

*dwDefault* \[ dans\]
</dt> <dd>

Valeur par défaut à retourner en cas d’échec.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne la valeur en cas de réussite ou *dwDefault* en cas d’échec.

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

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




