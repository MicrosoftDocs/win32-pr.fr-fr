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
ms.openlocfilehash: a44fcc9e082878077533edafcd44c9f5a5f26e76bddd3ddb5619fb2842ec0d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745639"
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



 

 




