---
description: 'En savoir plus sur : fonction JetOSSnapshotFreeze'
title: Fonction JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d133f0bc66da7c4f249676dc46ecbf92f2677aa6
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988472"
---
# <a name="jetossnapshotfreeze-function"></a>Fonction JetOSSnapshotFreeze


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetossnapshotfreeze-function"></a>Fonction JetOSSnapshotFreeze

La fonction **JetOSSnapshotFreeze** démarre un instantané. Pendant que l’instantané est en cours, aucune activité d’écriture sur le disque par le moteur ne peut avoir lieu.

**Windows xp :****JetOSSnapshotFreeze** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané.

*pcInstanceInfo*

Nombre d’instances en cours d’exécution dans le moteur qui font partie de la session d’instantané.

*paInstanceInfo*

Tableau de structures, une pour chaque instance en cours d’exécution qui fait partie de la session d’instantané, décrivant l’instance et les bases de données qui en font partie.

*grbit*

Options pour cet appel. Ce paramètre est réservé pour une utilisation ultérieure et la seule valeur valide prise en charge est 0.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Les pointeurs fournis pour les paramètres de sortie ont la valeur NULL, la session d’instantané n’est pas valide ou le paramètre <em>Grbit</em> n’est pas valide.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>La session d’instantané n’est pas dans l’état approprié pour démarrer un blocage (par exemple, un blocage précédent a échoué sur cette session auparavant).</p> | 
| <p>JET_errOSSnapshotNotAllowed</p> | <p>Le moteur n’est pas dans un État dans lequel un instantané peut être exécuté. Une ou plusieurs sauvegardes de streaming sont déjà en cours, ou une ou plusieurs instances passent par des étapes de récupération ou se terminent.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L’identificateur de la session d’instantané n’est pas valide.</p> | 
| <p>JET_errOutOfMemory</p> | <p>La fonction a échoué en raison d’une condition de mémoire insuffisante.</p> | 
| <p>JET_errOutOfThreads</p> | <p>La fonction a échoué en raison de l’échec du démarrage d’un nouveau thread qui n’a pas pu démarrer.</p> | 



Si cette fonction est établie, aucune e/s d’écriture n’est émise pour les fichiers de base de données ou pour les fichiers journaux qui font partie des instances figées. En outre, les informations de l’instance sont correctement remplies et doivent être libérées ultérieurement en appelant [JetFreeBuffer](./jetfreebuffer-function.md) avec le pointeur vers le tableau d’informations d’instance qui a été retourné.

Si cette fonction échoue, le moteur continue de s’exécuter normalement avec les IOs se produisant comme d’habitude. Il n’est pas nécessaire d’appeler [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) si le gel échoue. En outre, les informations de l’instance ne sont pas remplies, il n’est donc pas nécessaire de libérer cette ressource.

#### <a name="remarks"></a>Remarques

Pendant la période de blocage, aucune e/s d’écriture n’est émise pour les bases de données attachées ou les journaux de transactions, même s’il peut y avoir des e/s d’écriture émises dans les bases de données temporaires ou les fichiers de streaming.

L’État dans lequel se trouvent les bases de données et les fichiers journaux pendant le gel (l’État dans lequel les fichiers se trouvent dans une image d’instantané de volume) est tel qu’une récupération normale sera possible si ces fichiers sont restaurés ultérieurement.

Étant donné qu’il n’y a pas d’opérations d’écriture pendant la période de blocage, les appels d’API normaux dans le moteur peuvent être bloqués pour cet intervalle. L’application cliente doit être en mesure de gérer les appels d’API qui peuvent prendre plus de temps que d’habitude si un blocage se produit.

En raison des effets possibles décrits ci-dessus, il existe un délai d’expiration interne après lequel la session d’instantané arrêtera la phase de blocage, même si les API qui effectuent le dégel ou l’abandon n’étaient pas appelées. La valeur du délai d’attente peut être modifiée à l’aide du paramètre système [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) . Notez que l’intervalle de blocage classique est compris entre 10 secondes et le délai d’expiration par défaut est d’environ 60 secondes.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetOSSnapshotFreezeW</strong> (Unicode) et <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
