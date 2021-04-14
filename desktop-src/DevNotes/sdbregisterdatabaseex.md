---
description: Inscrit la base de données spécifiée.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523343"
---
# <a name="sdbregisterdatabaseex-function"></a>SdbRegisterDatabaseEx fonction)

Inscrit la base de données spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszDatabasePath* \[ dans\]
</dt> <dd>

Chemin d’accès de la base de données. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*dwDatabaseType* \[ dans\]
</dt> <dd>

Type de base de données. Pour obtenir la liste des valeurs, consultez [types de bases de données de shims](shim-database-types.md) .

</dd> <dt>

*pTimeStamp* \[ dans, facultatif\]
</dt> <dd>

Horodatage de la base de données. Si ce paramètre a la **valeur null**, l’heure système est utilisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="remarks"></a>Notes

Une base de données doit être inscrite pour que vous puissiez utiliser d’autres fonctions SDB.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




