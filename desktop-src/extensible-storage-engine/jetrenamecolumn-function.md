---
description: 'En savoir plus sur : fonction JetRenameColumn'
title: JetRenameColumn fonction)
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c60418a0723214b2d2312ebe67a4f47184814e0a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470236"
---
# <a name="jetrenamecolumn-function"></a>JetRenameColumn fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetrenamecolumn-function"></a>JetRenameColumn fonction)

La fonction **JetRenameColumn** peut être utilisée pour modifier le nom d’une colonne existante sur une table.

**Windows xp :****JetRenameColumn** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*szName*

Nom actuel de la colonne qui sera renommée.

*szNameNew*

Nouveau nom de la colonne qui sera renommée.

*grbit*

Ce paramètre doit avoir la valeur 0.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonne spécifiée n’existe pas pour cette table.</p> | 
| <p>JET_errInvalidName</p> | <p>L’un des noms d’objets spécifiés n’est pas valide. Tous les noms d’objets doivent être conformes au même ensemble de règles. Ces règles sont les suivantes :</p><ul><li><p>Les noms d’objets doivent être composés de caractères ASCII.</p></li><li><p>Les noms d’objets doivent comporter au moins un caractère.</p></li><li><p>Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</p></li><li><p>Les noms d’objets ne peuvent pas commencer par un espace. les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</p></li><li><p>Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</p></li><li><p>Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet. Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetRenameColumn</strong> dans les cas suivants :</p><ul><li><p><em>szName</em> a la valeur null.</p></li><li><p><em>szNameNew</em> a la valeur null.</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInTransaction</p> | <p>Cette opération ne peut être effectuée que si la session n’est pas actuellement à l’intérieur d’une transaction.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Une mise à jour ne peut pas être effectuée dans l’étendue d’une transaction en lecture seule. Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 



En cas de réussite, le nom de la colonne spécifiée dans la table associée au curseur est définitivement remplacé par le nouveau nom. Tous les index qui font référence à cette colonne seront également mis à jour.

En cas d’échec, aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

L’opération de changement de nom de colonne est inhabituelle car, contrairement aux autres opérations de schéma, elle n’est pas exécutée en tant que transaction. Lorsqu’une colonne d’une table donnée est renommée dans une session, toute autre session utilisant cette table verra immédiatement la modification, même si elle se trouve dans une transaction qui empêche cette session de voir toute autre modification apportée par la session à effectuer l’opération de changement de nom.

L’ID de colonne d’une colonne n’est pas affecté par l’opération de changement de nom.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetRenameColumnW</strong> (Unicode) et <strong>JetRenameColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
