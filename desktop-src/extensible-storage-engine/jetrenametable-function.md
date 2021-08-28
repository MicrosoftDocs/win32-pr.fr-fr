---
description: 'En savoir plus sur : fonction JetRenameTable'
title: JetRenameTable fonction)
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d91f7af4896e5cb3145321de087a2803aaddd09
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985742"
---
# <a name="jetrenametable-function"></a>JetRenameTable fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetrenametable-function"></a>JetRenameTable fonction)

La fonction **JetRenameTable** peut être utilisée pour modifier le nom d’une table existante.

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*dbid*

Base de données à utiliser pour cet appel.

*szName*

Nom actuel de la table qui sera renommée.

*szNameNew*

Nouveau nom de la table qui sera renommé.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>La base de données spécifiée n’est pas valide.</p><p>cette erreur est renvoyée uniquement dans Windows 2000 lorsqu’une opération de modification de nom de table est tentée sur la base de données temporaire. JET_errInvalidDatabaseId est retourné dans ce cas dans les versions ultérieures.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>L’ID de base de données spécifié n’est pas valide.</p> | 
| <p>JET_errInvalidName</p> | <p>L’un des noms d’objets spécifiés n’est pas valide. Tous les noms d’objets doivent être conformes au même ensemble de règles. Ces règles sont les suivantes :</p><ul><li><p>Les noms d’objets doivent être composés de caractères ASCII.</p></li><li><p>Les noms d’objets doivent comporter au moins un caractère.</p></li><li><p>Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</p></li><li><p>Les noms d’objets ne peuvent pas commencer par un espace.</p></li><li><p>Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</p></li><li><p>Les noms d’objets ne peuvent pas contenir un point d’exclamation ( !), un point (.), un crochet gauche ([) ou un crochet droit (]), une fois validés, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet. Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetRenameTable</strong> dans les cas suivants :</p><ul><li><p><em>szName</em> a la valeur null.</p></li><li><p><em>szNameNew</em> a la valeur null.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errObjectNotFound</p> | <p>La table spécifiée n’existe pas pour cette base de données.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Une mise à jour ne peut pas être effectuée dans l’étendue d’une transaction en lecture seule. Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 



En cas de réussite, le nom de la table spécifiée dans la base de données spécifiée est remplacé définitivement par le nouveau nom.

En cas d’échec, aucune modification de l’état de la base de données ne se produit.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetRenameTableW</strong> (Unicode) et <strong>JetRenameTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
