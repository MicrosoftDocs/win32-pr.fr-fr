---
description: La méthode GenerateTransform de l’objet Database crée une transformation qui, lorsqu’elle est appliquée à la base de données Object, produit la base de données de référence. La transformation est stockée dans l’objet de stockage.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Database. GenerateTransform, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091706"
---
# <a name="databasegeneratetransform-method"></a>Database. GenerateTransform, méthode

La méthode **GenerateTransform** de l’objet [**Database**](database-object.md) crée une [*transformation*](t-gly.md) qui, lorsqu’elle est appliquée à la base de données Object, produit la base de données de référence. La transformation est stockée dans l’objet de stockage.

Si la transformation doit être appliquée au cours d’une installation, vous devez utiliser la méthode [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) pour renseigner le flux d’informations de synthèse.

## <a name="syntax"></a>Syntaxe


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*reference* 
</dt> <dd>

Base de données requise qui n’inclut pas les modifications.

</dd> <dt>

*storage* 
</dt> <dd>

Nom du fichier de transformation généré. Cette étape est facultative.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Une transformation peut ajouter des colonnes clés non primaires à la fin d’une table. Impossible de créer une transformation qui ajoute des colonnes clés primaires à une table. Impossible de créer une transformation qui modifie l’ordre, les noms ou les définitions des colonnes.

Cette méthode retourne une valeur booléenne. Elle retourne la valeur TRUE si une transformation est générée. Elle retourne la valeur FALSe si aucune transformation n’est générée, car il n’existe aucune différence entre les deux bases de données. Si la méthode échoue, elle génère une erreur.

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Base de données**](database-object.md)
</dt> <dt>

[Transformations de base de données](database-transforms.md)
</dt> </dl>

 

 




