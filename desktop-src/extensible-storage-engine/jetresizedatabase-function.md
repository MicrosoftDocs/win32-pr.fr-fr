---
description: 'En savoir plus sur : fonction JetResizeDatabase'
title: JetResizeDatabase fonction)
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f12fc06b915f5462c9209416cf54436ef3d7239b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985682"
---
# <a name="jetresizedatabase-function"></a>JetResizeDatabase fonction)


_**S’applique à :** Windows | Windows Serveurs_

La fonction **JetResizeDatabase** étend ou réduit la taille d’une base de données qui est actuellement ouverte.

la fonction **JetResizeDatabase** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*dbid*

Base de données qui sera étendue.

*CPG*

Taille demandée de la base de données, en pages.

*pcpgActual*

Pointeur vers un nombre qui reçoit la taille de la base de données, en pages, après l’appel d’API. Si l’appel d’API échoue, le contenu du paramètre *pcpgActual* n’est pas défini.

*grbit*

Groupe de bits qui spécifie zéro, une ou plusieurs des valeurs énumérées dans le tableau suivant.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitResizeDatabaseOnlyGrow</p> | <p>Développez uniquement la base de données. Si l’appel Resize réduit la base de données, ne faites rien.</p> | 



### <a name="return-value"></a>Valeur retournée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. pour plus d’informations sur les erreurs ESE (extensible Stockage engine) possibles, consultez [erreurs du moteur de Stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errDiskFull</p> | <p>L’espace libre est insuffisant sur le volume pour effectuer l’opération d’augmentation.</p> | 
| <p>JET_errDiskIO</p> | <p>Une erreur liée à un fichier a été retournée par la fonction <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> . Pour plus d’informations sur les autres erreurs liées aux fichiers qui peuvent être retournées, consultez <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p> | 



#### <a name="remarks"></a>Remarques

Si la fonction **JetResizeDatabase** est appelée avant l’insertion de grandes quantités de données, le fichier de base de données sera augmenté en une seule opération. Cela permet de réduire la probabilité que le fichier de base de données soit fragmenté au niveau du système de fichiers et de réduire également le nombre de fois où le fichier de base de données doit être augmenté. La croissance du fichier de base de données peut être plus rapide que la croissance à plusieurs reprises.

Pour définir la taille d’une base de données qui n’est pas ouverte, consultez [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

La taille du fichier peut ne pas correspondre au nombre de pages retournées dans le paramètre *pcpgReal* . Deux pages réservées supplémentaires peuvent ne pas être comptées dans le paramètre *pcpgReal* .

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Requiert Windows 8.</p> | 
| <p><strong>Serveur</strong></p> | <p>Requiert Windows Server 2012.</p> | 
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
