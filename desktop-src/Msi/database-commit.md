---
description: La méthode Commit de l’objet Database finalise la forme persistante de la base de données.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091734"
---
# <a name="databasecommit-method"></a>Database. Commit, méthode

La méthode **Commit** de l’objet [**Database**](database-object.md) finalise la forme persistante de la base de données. Toutes les données persistantes sont écrites dans la base de données accessible en écriture et aucune colonne ou ligne temporaire n’est écrite. Cette méthode n’a aucun effet sur une base de données ouverte en lecture seule. Cette méthode peut être appelée plusieurs fois pour enregistrer l’état actuel des tables chargées en mémoire. Lorsque la base de données est fermée, toutes les modifications apportées après la dernière **validation** sont annulées. Cette méthode est normalement appelée avant l’arrêt lorsque toutes les modifications de la base de données ont été finalisées.

## <a name="syntax"></a>Syntaxe


```JScript
Database.Commit()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




