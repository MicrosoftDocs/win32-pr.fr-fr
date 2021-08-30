---
description: 'En savoir plus sur : fonction JetStopService'
title: Fonction JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314750e8a01ea58e2d29ee7c2bd9ca29564f107c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986522"
---
# <a name="jetstopservice-function"></a>Fonction JetStopService


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetstopservice-function"></a>Fonction JetStopService

La fonction **JetStopService** prépare une instance pour l’arrêt.

**JetStopService** est l’appel hérité lorsqu’une seule instance est autorisée. Dans ce cas, la seule instance active est celle qui est préparée pour l’arrêt.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Il n’est pas évident de déterminer l’instance à préparer pour l’arrêt lors de l’utilisation de <strong>JetStopService</strong> avec plusieurs modes d’instance.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 



Si cette fonction est réussie, elle se prépare à un arrêt ultérieur. Les étapes à suivre pour préparer un arrêt sont les suivantes :

  - Arrêtez la défragmentation en ligne si elle est en cours d’exécution.

  - Démarrez un nettoyage de la Banque des versions.

  - Réduisez la profondeur du point de contrôle en commençant à vider les pages incorrectes dans le gestionnaire de tampons.

  - Empêcher les appels ultérieurs à la plupart des fonctions pour cette instance.

Si cette fonction échoue, aucune des étapes de préparation d’un arrêt de l’instance n’est effectuée, donc aucune modification de l’état de l’instance ne se produit.

#### <a name="remarks"></a>Remarques

Cette fonction réduit le travail que l’instance doit effectuer une fois qu’elle est terminée, mais ne met pas fin à l’instance. Par conséquent, cette fonction est simplement une optimisation et n’est pas obligatoire pour l’utilisation. notez que la quantité de travail effectuée en préparation était moindre dans Windows 2000 et Windows XP. Une fois la fonction réussie, l’appel de fonctions qui ne sont plus autorisées retourne JET_errClientRequestToStopJetService. Les fonctions qui sont toujours autorisées après cet appel sont les suivantes : [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).

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
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
