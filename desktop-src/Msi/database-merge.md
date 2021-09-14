---
description: La méthode Merge de l’objet Database fusionne la base de données de référence avec la base de données de base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091702"
---
# <a name="databasemerge-method"></a>Database. Merge, méthode

La méthode **Merge** de l’objet [**Database**](database-object.md) fusionne la base de données de référence avec la base de données de base.

## <a name="syntax"></a>Syntaxe


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*reference* 
</dt> <dd>

Objet [**de base de données**](database-object.md) requis à fusionner dans la base de données.

</dd> <dt>

*errorTable* 
</dt> <dd>

Nom facultatif d’une table qui contient les noms des tables contenant les conflits de fusion, le nombre de lignes en conflit dans la table et une référence à la table avec le conflit de fusion.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) et la méthode **Merge** de l’objet [**Database**](database-object.md) ne peuvent pas être utilisées pour fusionner un module inclus dans un package d’installation. ils ne doivent pas être utilisés pour fusionner des [Modules de fusion](merge-modules.md) dans un package de Windows Installer. Pour inclure un module de fusion dans un package d’installation, les auteurs des packages d’installation doivent suivre les instructions décrites dans la rubrique [application de modules de fusion](applying-merge-modules.md) .

La méthode **Merge** ne copie pas les [fichiers CAB](cabinet-files.md) incorporés ni les [transformations incorporées](embedded-transforms.md) de la base de données de référence dans la base de données cible. Les flux de données incorporés qui sont répertoriés dans la table [binaire](binary-table.md) ou [icône](icon-table.md) sont copiés de la base de données de référence vers la base de données cible. Les stockages incorporés dans la base de données de référence ne sont pas copiés dans la base de données cible.

Si aucune table n’est fournie, le message d’erreur général indique le nombre de tables contenant des conflits de fusion. Une table peut être transmise, mais toutes les autres colonnes doivent avoir la valeur null, car l’opération de mise à jour de la [table d’erreurs](error-table.md) échoue si une colonne n’accepte pas la valeur null. Une table nouvellement créée peut également être transmise, car la méthode **Merge** crée automatiquement les colonnes qu’elle utilise si des conflits de fusion sont détectés. Deux colonnes sont utilisées pour présenter les conflits de fusion. La première colonne est le nom de la table et la colonne de clé primaire. La deuxième colonne est le nombre de lignes de cette table qui ont des échecs de fusion.

Si des tables portant le même nom dans les deux bases de données ne correspondent pas au nombre de clés primaires, aux types de colonnes, au nombre de colonnes ou aux noms de colonnes, la méthode de **fusion** échoue et publie un message d’erreur indiquant ce qui s’est produit.

Pour que la table d’erreurs reste, le gestionnaire d’erreurs doit valider la base de données à laquelle la table d’erreurs appartient. Toutefois, cette validation doit être effectuée après l’utilisation de la troisième colonne pour obtenir les références aux tables où des conflits de fusion se sont produits.

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




