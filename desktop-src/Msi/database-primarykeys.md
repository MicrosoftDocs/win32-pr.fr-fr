---
description: La propriété PrimaryKeys de l’objet de base de données retourne un objet record contenant le nom de la table dans le champ 0 et les noms de colonnes (qui composent les clés primaires) dans les champs suivants qui correspondent à leurs numéros de colonne.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Propriété Database. PrimaryKeys
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 50cbc29aa87f2dcaf9d347b1439b3914ba50a7a585d5c37c25823b10c8e5ca36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119382919"
---
# <a name="databaseprimarykeys-property"></a>Propriété Database. PrimaryKeys

La propriété **PrimaryKeys** de l’objet [**de base de données**](database-object.md) retourne un objet [**Record**](record-object.md) contenant le nom de la table dans le champ 0 et les noms de colonnes (qui composent les clés primaires) dans les champs suivants qui correspondent à leurs numéros de colonne. Le nombre de champs de l’enregistrement est le nombre de colonnes clés primaires.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a>Valeur de la propriété

Nom obligatoire d’une table existante. Une erreur est générée si la table n’existe pas.

## <a name="remarks"></a>Remarques

La propriété **PrimaryKeys** ne peut pas être utilisée avec la table [ \_ tables](-tables-table.md) ou la [ \_ Table Columns](-columns-table.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




