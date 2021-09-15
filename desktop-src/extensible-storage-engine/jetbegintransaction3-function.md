---
description: 'En savoir plus sur : fonction JetBeginTransaction3'
title: Fonction JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca07ad3957efadfb86ac5df9b1994d5c4525c7a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523800"
---
# <a name="jetbegintransaction3-function"></a>Fonction JetBeginTransaction3


_**S’applique à :** Windows | Windows Serveurs_

La fonction **JetBeginTransaction3** oblige une session à entrer dans une transaction et à créer un nouveau point d’enregistrement. Cette fonction peut être appelée plusieurs fois dans une seule session pour créer des points d’enregistrement supplémentaires. Ces points d’enregistrement peuvent être utilisés pour conserver ou abandonner les modifications apportées à la base de données de manière sélective.

la fonction **JetBeginTransaction3** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*trxid*

Identificateur facultatif fourni par l’utilisateur pour identifier la transaction.

*grbit*

Groupe de bits qui spécifie zéro, une ou plusieurs des valeurs d’option d’appel énumérées dans le tableau suivant.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitTransactionReadOnly</p> | <p>La transaction ne modifie pas la base de données. Si une mise à jour est tentée, cette opération échoue avec JET_errTransReadOnly code de réponse. Cette option est ignorée sauf si elle est demandée lorsque la session donnée n’est pas déjà dans une transaction. cette option est disponible dans les versions du système d’exploitation Windows à partir de Windows XP.</p> | 



### <a name="return-value"></a>Valeur de retour

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. pour plus d’informations sur les erreurs ESE (extensible Stockage engine) possibles, consultez [erreurs du moteur de Stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>ce code de retour est retourné par les versions de Windows à partir de Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est retournée par les versions de Windows à partir de Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Une nouvelle transaction ne peut pas être démarrée, car la session est déjà à la profondeur de point d’enregistrement maximale autorisée par le moteur de base de données.</p> | 



En cas de réussite, la session fournie se trouve à l’intérieur d’une transaction. Si la session était précédemment à l’intérieur d’une transaction, un nouveau point d’enregistrement sera créé.

En cas d’échec, l’état transactionnel de la session reste inchangé. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Notes

Pour plus d’informations sur le fonctionnement des transactions, consultez [JetBeginTransaction](./jetbegintransaction-function.md).

#### <a name="requirements"></a>Spécifications


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
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
