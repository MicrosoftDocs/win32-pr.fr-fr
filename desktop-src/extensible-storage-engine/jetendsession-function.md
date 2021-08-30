---
description: 'En savoir plus sur : fonction JetEndSession'
title: JetEndSession fonction)
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f6e620a801f0ee7f2dc6f9c6f2dfe90e9f766e5e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983462"
---
# <a name="jetendsession-function"></a>JetEndSession fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetendsession-function"></a>JetEndSession fonction)

La fonction **JetEndSession** met fin à la session et nettoie et libère toutes les ressources associées à la session spécifiée.

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à terminer. Les ressources associées sont libérées à la fin de la session.

*grbit*

Réservé. Ce paramètre peut contenir l’indicateur JET_bitForceSessionClosed, mais cet indicateur est réservé et sa définition n’a aucun effet.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a produit un résultat inattendu.</p> | 
| <p>JET_errInvalidSesid</p> | <p>La session n’était pas une session JET valide.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué car la mémoire n’a pas pu être allouée.</p> | 
| <p>JET_errSessionInUse</p> | <p>Cela signifie que la session était en cours d’utilisation sur un autre thread ou que la session n’a pas été définie ou réinitialisée correctement.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errOutOfBuffers</p> | <p>Erreur système qui indique qu’il n’y a plus de tampons.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, le descripteur de session est fermé et non disponible, et toutes les ressources associées à cette session sont nettoyées.

En cas d’échec, plusieurs autres erreurs peuvent se produire dans le cadre de la fermeture de la table de tri, de la fermeture du curseur et de la restauration de la transaction. Ces erreurs sont relativement peu probables, et très peu probables si vos sessions ne sont pas entièrement utilisées lorsque **JetEndSession** est appelé. Ces erreurs sont retournées si une partie de la session n’a pas pu être nettoyée correctement.

#### <a name="remarks"></a>Remarques

Cette API restaure toutes les transactions ouvertes (non validées au niveau 0). De même, tous les curseurs associés à cette session et les tables de tri qui ont été créées ou ouvertes sont nettoyés.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
