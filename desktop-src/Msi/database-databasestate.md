---
description: La propriété DatabaseState de l’objet de base de données est une propriété en lecture seule.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Propriété Database. DatabaseState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537436"
---
# <a name="databasedatabasestate-property"></a>Propriété Database. DatabaseState

La propriété **DatabaseState** de l’objet [**de base de données**](database-object.md) est une propriété en lecture seule.

Cette propriété retourne l’état de persistance de la base de données sous la forme de l’un des paramètres suivants.



| État de la base de données        | Valeur | Description                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| msiDatabaseStateRead  | 0     | La base de données s’ouvre en lecture seule. Les modifications apportées aux données persistantes ne sont pas autorisées et les données temporaires ne sont pas enregistrées. |
| msiDatabaseStateWrite | 1     | La base de données est entièrement opérationnelle pour la lecture et l’écriture.                                                          |



 

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




