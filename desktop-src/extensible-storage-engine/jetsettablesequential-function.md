---
description: 'En savoir plus sur : fonction JetSetTableSequential'
title: JetSetTableSequential fonction)
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9286cc9ffc07f9b03bf6cfa84add8ba5b031fe97
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983312"
---
# <a name="jetsettablesequential-function"></a>JetSetTableSequential fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetsettablesequential-function"></a>JetSetTableSequential fonction)

La fonction **JetSetTableSequential** avertit le moteur de base de données que l’application analyse l’intégralité de l’index actuel qui contient un curseur donné. Par conséquent, les méthodes utilisées pour accéder aux données d’index seront paramétrées pour rendre ce scénario aussi rapide que possible.

**Windows xp :****JetSetTableSequential** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*grbit*

Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitPrereadForward</p> | <p>Cette option est utilisée pour indexer vers l’avant.</p><p><strong>Windows 7 :</strong><strong>JET_bitPrereadForward</strong> est introduite dans Windows 7.  </p> | 
| <p>JET_bitPrereadBackward</p> | <p>Cette option est utilisée pour indexer dans le sens inverse.</p><p><strong>Windows 7 :</strong><strong>JET_bitPrereadBackward</strong> est introduite dans Windows 7.  </p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été suspendue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si cette fonction fonctionne, l’index actuel du curseur est optimisé pour une analyse séquentielle de la totalité de l’index. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, aucune modification de la configuration du curseur ne se produit. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Si l’application doit analyser efficacement un sous-ensemble connu d’un index, une optimisation similaire est également effectuée chaque fois qu’une plage d’index est établie à l’aide de [JetSetIndexRange](./jetsetindexrange-function.md). cette optimisation est disponible uniquement sur Windows XP et les versions ultérieures.

Si l’application doit analyser efficacement un sous-ensemble inconnu d’un index, aucune action ne doit être effectuée. Le moteur peut détecter automatiquement le comportement de l’analyse et récupérer les données à l’avance. Toutefois, ce comportement n’est pas aussi agressif.

Cette optimisation rendra l’analyse efficace de l’index principal et fera en sorte que l’analyse des données d’entrée d’index dans un index secondaire soit efficace. Il n’effectue pas l’analyse d’un index secondaire pendant la récupération des données d’enregistrement. Cela est dû au fait que le moteur n’effectue pas de lecture anticipée sur les données de l’enregistrement.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
