---
title: Choix du modèle de thread
description: Choix du modèle de thread
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363311"
---
# <a name="choosing-the-threading-model"></a>Choix du modèle de thread

Le choix du modèle de thread pour un objet dépend de la fonction de l’objet. Un objet qui effectue des e/s étendues peut prendre en charge le thread libre pour fournir une réponse maximale aux clients en autorisant les appels d’interface pendant la latence d’e/s. En revanche, un objet qui interagit avec l’utilisateur peut prendre en charge le thread cloisonné pour synchroniser les appels COM entrants avec ses opérations de fenêtre.

Il est plus facile de prendre en charge le thread cloisonné dans des Apartments à thread unique, car COM assure la synchronisation par appel. La prise en charge des threads libres est plus difficile, car l’objet doit implémenter la synchronisation. Toutefois, la réponse aux clients peut être meilleure car la synchronisation peut être implémentée pour des sections de code plus petites.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux interfaces à travers les Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Apartments (cloisonnés) multithread](multithreaded-apartments.md)
</dt> <dt>

[Problèmes liés aux threads du serveur in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Communication monothread et multithread](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments (cloisonnés) à thread unique](single-threaded-apartments.md)
</dt> </dl>

 

 




