---
description: La méthode Execute de l’objet View utilise le jeton de point d’interrogation pour représenter les paramètres dans une instruction SQL. Pour plus d’informations, consultez syntaxe SQL. Les valeurs de ces paramètres sont transmises en tant que champs correspondants d’un enregistrement de paramètre.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: Méthode de View.Exe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525141"
---
# <a name="viewexecute-method"></a>Méthode de View.Exe

La méthode **Execute** de l’objet [**View**](view-object.md) utilise le jeton de point d’interrogation pour représenter les paramètres dans une instruction SQL. Pour plus d’informations, consultez [syntaxe SQL](sql-syntax.md). Les valeurs de ces paramètres sont transmises en tant que champs correspondants d’un enregistrement de paramètre.

## <a name="syntax"></a>Syntaxe


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*enregistrement* 
</dt> <dd>

Objets d' [**enregistrement**](record-object.md) facultatifs qui contiennent les valeurs qui remplacent les jetons de paramètre ( ?) dans la requête SQL.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode doit être appelée avant tout appel à la méthode [**Fetch**](view-fetch.md) .

Si la requête SQL spécifie des valeurs avec des marqueurs de paramètres ( ?), un enregistrement qui contient toutes les valeurs de remplacement doit être dans le même ordre et le même type de données que les marqueurs de paramètres. Lorsque cette méthode est utilisée avec les requêtes INSERT et UPDATE, les jetons de point d’interrogation doivent précéder toutes les valeurs non paramétrées.

Par exemple, ces requêtes sont valides :

MISE à jour {table-List} définie {Column} = ? , {Column} = {constant}

INSÉRER dans {table} ({Column-List}) valeurs ( ?, {constant-List})

Toutefois, ces requêtes ne sont pas valides :

UPDATE {table-List} SET {Column} = {constante}, {Column} = ?

INSÉRER dans {table} ({Column-List}) valeurs ({constant-List}, ? )

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




