---
description: 'En savoir plus sur : fonction JetStopServiceInstance'
title: JetStopServiceInstance fonction)
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55f9a8c6e91a70e447f03bc19bcd191d01ba0e08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525885"
---
# <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance fonction)

La fonction **JetStopServiceInstance** prépare une instance pour l’arrêt.

**Windows xp :****JetStopServiceInstance** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance en cours d’exécution à utiliser pour l’appel d’API.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Le paramètre d’instance spécifié a une valeur non valide (pas une instance en cours d’exécution).</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 



Si cette fonction est réussie, elle se prépare à un arrêt ultérieur. Les étapes à suivre pour préparer un arrêt sont les suivantes :

  - Arrêtez la défragmentation en ligne si elle est en cours d’exécution.

  - Démarrez un nettoyage de la Banque des versions.

  - Réduisez la profondeur du point de contrôle en commençant à vider les pages incorrectes dans le gestionnaire de tampons.

  - Empêcher les appels ultérieurs à la plupart des fonctions pour cette instance.

Si cette fonction échoue, aucune des étapes de préparation d’un arrêt de l’instance n’est effectuée, donc aucune modification de l’état de l’instance ne se produit.

#### <a name="remarks"></a>Notes

Cette fonction permet de réduire le travail que l’instance doit effectuer une fois terminé, mais ne met pas fin à l’instance. Par conséquent, cette fonction est simplement une optimisation et n’est pas obligatoire pour l’utilisation. notez que la quantité de travail effectuée en préparation était moindre dans Windows 2000 et Windows XP. Une fois la fonction réussie, l’appel de fonctions qui ne sont plus autorisées retourne JET_errClientRequestToStopJetService. Les fonctions qui sont toujours autorisées après cet appel sont les suivantes : [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
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
