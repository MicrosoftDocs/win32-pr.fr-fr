---
description: la méthode OpenView de l’objet Database retourne un objet View qui représente la requête spécifiée par une chaîne de SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Database. OpenView, méthode (certview. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091694"
---
# <a name="databaseopenview-method"></a>Database. OpenView, méthode

la méthode **OpenView** de l’objet [**Database**](database-object.md) retourne un objet [**View**](view-object.md) qui représente la requête spécifiée par une chaîne de SQL.

## <a name="syntax"></a>Syntaxe


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sql* 
</dt> <dd>

obligatoire SQL chaîne de requête.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

pour plus d’informations sur la syntaxe de SQL implémentée dans le programme d’installation, consultez [SQL syntaxe](sql-syntax.md).

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| En-tête<br/>  | <dl> <dt>Certview. h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Base de données**](database-object.md)
</dt> <dt>

[Syntaxe SQL](sql-syntax.md)
</dt> </dl>

 

 




