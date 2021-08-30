---
description: 'En savoir plus sur : fonction JetBeginTransaction'
title: Fonction JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c03991d9efe73d20e5984217a2c205adc087e170
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987672"
---
# <a name="jetbegintransaction-function"></a>Fonction JetBeginTransaction


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetbegintransaction-function"></a>Fonction JetBeginTransaction

La fonction **JetBeginTransaction** oblige une session à entrer dans une transaction et à créer un nouveau point d’enregistrement. Cette fonction peut être appelée plusieurs fois sur une seule session pour provoquer la création de points d’enregistrement supplémentaires. Ces points d’enregistrement peuvent être utilisés pour conserver ou ignorer de manière sélective les modifications apportées à l’état de la base de données.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Une nouvelle transaction ne peut pas être démarrée, car la session est déjà à la profondeur de point d’enregistrement maximale autorisée par le moteur de base de données.</p> | 



En cas de réussite, la session fournie se trouve à l’intérieur d’une transaction. Si la session était précédemment à l’intérieur d’une transaction, un nouveau point d’enregistrement sera créé.

En cas d’échec, l’état transactionnel de la session reste inchangé. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Le moteur de base de données fournit un modèle d’isolation d’instantané pour ses transactions. Cela signifie que, lorsqu’une session entre pour la première fois dans un état transactionnel, la session voit l’intégralité de la base de données figée à l’heure au début de la transaction. Une session n’a pas besoin de lire le verrou de données, car elle peut toujours accéder à la version appropriée de ces données. Cela signifie qu’une session qui met à jour des données ne bloquera jamais une autre session pour la lecture de ces données.

Une autre implication de l’utilisation de l’isolement d’instantané est le modèle de verrouillage utilisé pour les mises à jour. Le moteur de base de données récompense un verrou d’écriture sur un élément de données donné dans la première session qui le demande. Ce verrou d’écriture est libéré lorsque la transaction est validée ou abandonnée complètement, de sorte que la session n’est plus dans une transaction. Lorsqu’une session maintient un verrou en écriture, toute autre session qui demande le même verrou d’écriture n’est pas bloquée tant que le verrou d’écriture n’est pas disponible. Au lieu de cela, cette deuxième session échouera immédiatement avec JET_errWriteConflict. Pour résoudre ce conflit, la deuxième session doit abandonner (ou valider) entièrement sa transaction, attendre une courte période de temps pour que la première session valide ou abandonne sa transaction, puis recommencer.

Pour la prise en charge de l’isolation d’instantané, le moteur de base de données stocke toutes les versions de toutes les données modifiées dans la mémoire depuis le premier démarrage de la transaction active la plus ancienne dans une session. Cela a des implications importantes pour votre application. Tout comportement qui provoque la génération d’un grand nombre de versions en mémoire peut provoquer l’épuisement de la taille maximale de la Banque de versions (voir [JET_paramMaxVerPages](./resource-parameters.md) dans [paramètres système](./extensible-storage-engine-system-parameters.md) pour plus d’informations). Ce comportement comprend, sans s’y limiter, les mises à jour très volumineuses dans une transaction unique et les transactions à long terme. Par conséquent, il est très important de configurer correctement la taille de la Banque des versions pour le chargement transactionnel attendu de l’application. Il est également important de veiller à limiter le nombre de mises à jour effectuées dans une transaction unique. En outre, il est important de rendre les transactions aussi courtes que possible dans des scénarios de charge élevée.

Il est fortement recommandé que l’application soit toujours dans le contexte d’une transaction lors de l’appel d’API ESE qui récupèrent ou mettent à jour des données. Si ce n’est pas le cas, le moteur de base de données encapsule automatiquement chaque appel d’API ESE de ce type dans une transaction au nom de l’application. Le coût de ces transactions très courtes peut s’ajouter rapidement dans certains cas.

Le comportement par défaut du moteur est de limiter l’utilisation d’une session au même thread à partir du moment où le premier appel à **JetBeginTransaction** est effectué jusqu’au moment où l’appel correspondant à [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) est effectué. Ce comportement peut être modifié pour supprimer cette restriction en définissant un contexte de session personnalisé à l’aide de [JetSetSessionContext](./jetsetsessioncontext-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).

Le moteur de base de données prend également en charge les modifications de schéma transactionnel. Par exemple, il est possible de commencer une nouvelle transaction, de créer une table, d’ajouter quelques colonnes, de créer un ou deux index, puis d’abandonner la transaction. Les éléments de schéma qui viennent d’être ajoutés seront supprimés de la base de données. Il est également possible de mélanger des modifications de schéma et des mises à jour de base de données ordinaires dans la même transaction.

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
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
