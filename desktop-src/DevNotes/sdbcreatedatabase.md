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
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950612"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




