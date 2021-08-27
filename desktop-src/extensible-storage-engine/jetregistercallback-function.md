---
description: 'En savoir plus sur : fonction JetRegisterCallback'
title: Fonction JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ef90466b736facf5bd9fefee31c0449964d003b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985802"
---
# <a name="jetregistercallback-function"></a>Fonction JetRegisterCallback


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetregistercallback-function"></a>Fonction JetRegisterCallback

La fonction **JetRegisterCallback** permet à l’application de configurer le moteur de base de données pour émettre des notifications à l’application pour des événements spécifiques. Ces notifications sont associées à une table spécifique et restent effectives uniquement jusqu’à ce que l’instance contenant la table soit arrêtée à l’aide de [JetTerm](./jetterm-function.md).

**Windows xp : JetRegisterCallback** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*cbtyp*

Masque de bits composé des raisons de rappel pour lesquelles l’application souhaite recevoir des notifications.

Pour créer ce masque de bits, tout simplement ou ensemble des raisons de rappel valides à partir de l’énumération [JET_CBTYP](./jet-cbtyp.md) .

*pCallback*

Pointeur de fonction vers la fonction de rappel pour l’application.

*pvContext*

Spécifie un pointeur de contexte qui sera attribué à la fonction de rappel pour l’application.

*phCallbackId*

Retourne un handle qui peut être utilisé ultérieurement pour annuler l’inscription de la fonction de rappel donnée à l’aide de [JetUnregisterCallback](./jetunregistercallback-function.md).

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cette erreur est retournée par <strong>JetRegisterCallback</strong> quand :</p><ul><li><p><em>cbtyp</em> est égal à zéro,</p></li><li><p><em>pCallback</em> a la valeur null.</p></li><li><p><em>phCallbackId</em> a la valeur null.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, le rappel spécifié sera inscrit pour les raisons de rappel données avec la table associée au curseur donné. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, le rappel n’est pas inscrit. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Cette méthode permet à l’application d’associer des rappels volatiles à une table dans une base de données. Si l’application souhaite associer les rappels rendus persistants à une table dans la base de données, elle doit passer le rappel à [JET_TABLECREATE](./jet-tablecreate-structure.md) à l’aide de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetTerm](./jetterm-function.md)  
[JetUnregisterCallback](./jetunregistercallback-function.md)
