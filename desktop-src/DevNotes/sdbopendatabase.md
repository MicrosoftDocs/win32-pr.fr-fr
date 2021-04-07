---
description: Ouvre la base de données de shims spécifiée.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747853"
---
# <a name="sdbopendatabase-function"></a>SdbOpenDatabase fonction)

Ouvre la base de données de shims spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszPath* \[ dans\]
</dt> <dd>

Chemin d’accès de la base de données. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*ETYPE* \[ dans\]
</dt> <dd>

Type de chemin d’accès. Pour obtenir la liste des valeurs, consultez [**\_ type de chemin d’accès**](path-type.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un descripteur à la base de données de shims.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 




