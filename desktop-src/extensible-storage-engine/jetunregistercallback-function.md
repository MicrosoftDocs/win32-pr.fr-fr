---
description: 'En savoir plus sur : fonction JetUnregisterCallback'
title: JetUnregisterCallback fonction)
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cb60d8b0d06ff6af9d950c53d8bdf8f4eedb774
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466244"
---
# <a name="jetunregistercallback-function"></a>JetUnregisterCallback fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetunregistercallback-function"></a>JetUnregisterCallback fonction)

La fonction **JetUnregisterCallback** permet à l’application de configurer le moteur de base de données pour arrêter l’émission de notifications à l’application, comme demandé précédemment via [JetRegisterCallback](./jetregistercallback-function.md).

**Windows xp :****JetUnregisterCallback** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*cbtyp*

Masque de masque composé des raisons de rappel pour lesquelles l’application ne souhaite plus recevoir de notifications.

Pour créer ce masque de masque, il suffit ou ensemble des raisons de rappel valides de l’énumération [JET_CBTYP](./jet-cbtyp.md) .

*hCallbackId*

Handle du rappel inscrit qui a été retourné par [JetRegisterCallback](./jetregistercallback-function.md).

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si cette fonction réussit, le rappel spécifié sera désinscrit pour les raisons de rappel données avec la table associée au curseur donné. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, le rappel spécifié n’est pas annulé. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Le masque de masque donné doit correspondre exactement au masque de données spécifié lors de l’inscription du rappel. Le moteur de base de données ne prend pas actuellement en charge la suppression d’un sous-ensemble de ces notifications et ne renvoie pas d’erreur lorsque cette tentative est effectuée.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetStopService](./jetstopservice-function.md)
