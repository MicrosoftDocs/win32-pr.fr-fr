---
description: 'En savoir plus sur : fonction JetSetSessionContext'
title: JetSetSessionContext fonction)
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61df6b5396a5bffcef4f7e32e9a2c32477d019e0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465286"
---
# <a name="jetsetsessioncontext-function"></a>JetSetSessionContext fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetsetsessioncontext-function"></a>JetSetSessionContext fonction)

La fonction **JetSetSessionContext** associe une session au thread actuel à l’aide du handle de contexte donné. Cette association remplace la spécification de moteur par défaut selon laquelle une transaction pour une session donnée doit se produire entièrement sur le même thread.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*ulContext*

Identificateur unique auquel cette session sera associée.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a produit un résultat inattendu. Cette erreur est retournée par <strong>JetSetSessionContext</strong> dans les conditions suivantes :</p><ul><li><p><em>ulContext</em> a la valeur null</p></li><li><p><em>ulContext</em> est-1</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionContextAlreadySet</p> | <p>La session n’a pas pu être associée au thread actuel, car elle a déjà été associée à un thread.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si cette fonction est établie, la session est associée au thread actuel. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, l’état de la session reste inchangé. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Une session est généralement liée à un thread spécifique pour la durée d’une transaction. Ce comportement est conçu pour aider les applications à détecter et empêcher le partage conceptuel d’une seule session entre plusieurs threads. Parfois, cette vérification simple ne fonctionne pas avec l’architecture de l’application. Par exemple, si l’application héberge des objets côté serveur à l’aide d’un pool de threads et que les transactions s’étendent sur plusieurs appels serveur à un objet donné, cette protection peut entraîner l’échec de certains de ces appels avec JET_errSessionSharingViolation même si le modèle d’utilisation est correct. Cette situation est courante pour les serveurs d’objets COM.

**JetSetSessionContext** et [JetResetSessionContext](./jetresetsessioncontext-function.md) résolvent ce problème en rendant ce partage de session un peu plus flexible. Lorsque l’application commence à effectuer une série d’appels d’API ESE à l’aide d’une session particulière, elle définit tout d’abord le contexte de session sur une valeur donnée. Cette action associe la session au thread appelant. Dans l’exemple donné, ce contexte peut être l’adresse de l’objet qui contient le handle de session JET. Une fois les appels de l’API ESE effectués, l’application réinitialise le contexte de session. Cette action dissocie la session du thread appelant. L’objet et sa session peuvent ensuite être utilisés par un autre thread, même si la session a une transaction active.

Il est important de noter que **JetSetSessionContext** doit être appelé avant l’ouverture d’une transaction sur cette session ou que l’Association ne fonctionnera pas.

**JetSetSessionContext** est thread-safe. Plusieurs threads peuvent tenter de définir un contexte de thread sur la même session en même temps et un seul sera gagnant. Ce fait peut être utilisé par l’application comme un moyen d’allouer une session à partir d’un pool sans stocker l’état externe sur son allocation.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
