---
description: 'En savoir plus sur : fonction JetGetThreadStats'
title: JetGetThreadStats fonction)
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b47cd9de933efdc5a73aba32a212432a9e37a12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915884"
---
# <a name="jetgetthreadstats-function"></a>JetGetThreadStats fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetthreadstats-function"></a>JetGetThreadStats fonction)

La fonction **JetGetThreadStats** récupère les informations de performance du moteur de base de données pour le thread actuel. Plusieurs appels peuvent être utilisés pour collecter des statistiques qui reflètent l’activité du moteur de base de données sur ce thread entre ces appels.

**Windows vista :****JetGetThreadStats** est introduit dans Windows vista.  

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Paramètres

*pvResult*

Mémoire tampon de sortie qui reçoit les données de statistiques de thread. La mémoire tampon contient une structure [JET_THREADSTATS](./jet-threadstats-structure.md) après un appel réussi.

*cbMax*

Taille maximale, en octets, de la mémoire tampon de sortie.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>L’opération a échoué, car la mémoire tampon de sortie fournie était trop petite pour contenir les données demandées. La fonction <strong>JetGetThreadStats</strong> renvoie cette erreur lorsque la mémoire tampon de sortie est trop petite pour contenir la version la plus petite de la structure <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> prise en charge par le moteur de base de données.</p> | 



En cas de réussite, la mémoire tampon de sortie contient une structure [JET_THREADSTATS](./jet-threadstats-structure.md) qui contient les statistiques du moteur de base de données pour le thread actuel.

En cas d’échec, l’état de la mémoire tampon de sortie n’est pas défini.

#### <a name="remarks"></a>Notes

Les informations fournies par deux appels consécutifs de cette API sont destinées à calculer le coût des autres opérations du moteur de base de données sur le thread actuel. En règle générale, cette opération s’effectue en acceptant une valeur avant et après la lecture des statistiques et en soustrayant le nombre d’opérations après le comptage avant d’obtenir le nombre net d’opérations effectuées.

Par exemple, une application peut appeler **JetGetThreadStats** une fois pour obtenir une lecture initiale des statistiques du thread actuel. Elle peut ensuite appeler la fonction [JetMove](./jetmove-function.md) avec le paramètre *cRow* défini sur JET_MoveNext pour passer à l’entrée d’index suivante sur un index. Il peut ensuite appeler **JetGetThreadStats** à nouveau pour recevoir une autre lecture des statistiques du thread. Il peut ensuite soustraire le compteur cPageReferenced de la deuxième lecture du premier. Le résultat est le nombre de pages de base de données référencées par le moteur de base de données pour effectuer l’opération [JetMove](./jetmove-function.md) .

Les statistiques de chaque thread sont accumulées pendant la durée de vie de ce thread. Les statistiques sont réinitialisées si la DLL du moteur de base de données est déchargée du processus hôte.

La structure [JET_THREADSTATS](./jet-threadstats-structure.md) sera probablement développée à l’avenir pour contenir plus de statistiques. De nouvelles statistiques seront ajoutées à la fin de la structure et peuvent être récupérées avec une taille de mémoire tampon de sortie accrue. La présence de statistiques supplémentaires peut être déduite par une valeur cbStruct plus grande.

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)
