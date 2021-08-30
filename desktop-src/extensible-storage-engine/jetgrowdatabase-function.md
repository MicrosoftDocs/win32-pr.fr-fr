---
description: 'En savoir plus sur : fonction JetGrowDatabase'
title: JetGrowDatabase fonction)
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4928bbf4b057192a846b627a6bdc821244726333
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984572"
---
# <a name="jetgrowdatabase-function"></a>JetGrowDatabase fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgrowdatabase-function"></a>JetGrowDatabase fonction)

La fonction **JetGrowDatabase** étend la taille d’une base de données qui est actuellement ouverte.

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*dbid*

Base de données qui sera étendue.

*CPG*

Taille souhaitée de la base de données, en pages.

*pcpgReal*

Pointeur vers un nombre qui reçoit la taille de la base de données, en pages, après l’appel d’API. Si l’appel d’API échoue, le contenu de *pcpgReal* n’est pas défini.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errDiskFull</p> | <p>L’espace libre est insuffisant sur le volume pour effectuer l’opération d’augmentation.</p> | 
| <p>JET_errDiskIO</p> | <p>Une erreur liée à un fichier a été retournée par <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>. Pour plus d’informations sur les autres erreurs liées aux fichiers qui peuvent être retournées, consultez <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p> | 



#### <a name="remarks"></a>Remarques

Si **JetGrowDatabase** est appelé avant d’insérer de grandes quantités de données, le fichier de base de données sera augmenté en une seule opération. Cela permet de réduire la probabilité que le fichier de base de données soit fragmenté au niveau du système de fichiers et de réduire également le nombre de fois où le fichier de base de données doit être augmenté. La croissance du fichier de base de données peut être plus rapide que la croissance à plusieurs reprises.

Seule la croissance du fichier est actuellement prise en charge. Pour réduire un fichier, utilisez la fonctionnalité de défragmentation du programme utilitaire **esentutl.exe** .

Pour définir la taille d’une base de données qui n’est pas ouverte, consultez [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

La taille du fichier peut ne pas correspondre au nombre de pages retournées dans *pcpgReal*. Il existe deux pages réservées supplémentaires qui peuvent ne pas être comptées dans *pcpgReal*.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
