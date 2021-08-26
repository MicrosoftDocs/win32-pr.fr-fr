---
description: La propriété TablePersistent de l’objet de base de données retourne l’état de persistance de la table en tant que l’un des paramètres suivants.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Propriété Database. TablePersistent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f5eaf32996adef39976ba9fbaf88834c339e27dbe13c4e7fbcd1928ac1973b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129639"
---
# <a name="databasetablepersistent-property"></a>Propriété Database. TablePersistent

La propriété **TablePersistent** de l’objet [**de base de données**](database-object.md) retourne l’état de persistance de la table en tant que l’un des paramètres suivants.



| État de la table               | Valeur | Description                    |
|---------------------------|-------|--------------------------------|
| msiEvaluateConditionFalse | 0     | La table est temporaire.            |
| msiEvaluateConditionTrue  | 1     | La table est persistante.           |
| msiEvaluateConditionNone  | 2     | La table n’est pas dans la base de données.  |
| msiEvaluateConditionError | 3     | Nom de table non valide ou manquant. |



 

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




