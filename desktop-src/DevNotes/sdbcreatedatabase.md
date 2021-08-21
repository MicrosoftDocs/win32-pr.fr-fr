---
description: Crée une nouvelle base de données de shims.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6c7ac5d30c9c5a0154d770266410d278c5c3f31a65166515078a5384b1b8b55d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161554"
---
# <a name="sdbcreatedatabase-function"></a>SdbCreateDatabase fonction)

Crée une nouvelle base de données de shims.

## <a name="syntax"></a>Syntaxe


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszPath* \[ dans\]
</dt> <dd>

Chemin d’accès de l’emplacement où la base de données doit être enregistrée. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*ETYPE* \[ dans\]
</dt> <dd>

Type de chemin d’accès. Pour obtenir la liste des valeurs, consultez [**\_ type de chemin d’accès**](path-type.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un descripteur à la base de données du shim ou **null** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




