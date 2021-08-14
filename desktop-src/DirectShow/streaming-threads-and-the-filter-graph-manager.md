---
description: Streaming threads et Filter Graph Manager
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Streaming threads et Filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3501f984880fad22399cbda8710acaf2be1d6c4223e07a4c0f6e4c180d0699cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329769"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Streaming threads et Filter Graph Manager

lorsque le gestionnaire de Graph de filtre arrête le graphique, il attend que tous les threads de diffusion en continu s’arrêtent. Cela a les conséquences suivantes pour les filtres :

-   un filtre ne doit jamais appeler de méthodes sur le gestionnaire de Graph de filtre à partir d’un thread de streaming.

    le gestionnaire de Graph de filtre utilise une section critique pour synchroniser ses propres opérations. Si un thread de streaming tente de conserver cette section critique, il peut provoquer un blocage. Par exemple : Supposons qu’un autre thread arrête le graphique. Ce thread prend le verrou du graphique de filtre et attend que votre filtre cesse de transmettre des données. Si votre filtre attend le verrou, il ne s’arrêtera jamais, provoquant ainsi un blocage.

-   un filtre ne doit jamais **AddRef** ou **QueryInterface** le filtre Graph Manager à partir d’un thread de streaming.

    si le filtre contient un décompte de références sur le gestionnaire de Graph de filtre (par le biais de **AddRef** ou **QueryInterface**), il peut devenir le dernier objet à contenir un décompte de références. lorsque le filtre appelle la **version**, le gestionnaire de Graph de filtre se détruit lui-même. au sein de sa routine de nettoyage, le gestionnaire de Graph de filtre tente d’arrêter le graphique, provoquant l’attente de la fermeture du thread de streaming. Toutefois, il attend dans le thread de diffusion en continu, donc le thread de streaming ne peut pas quitter. Le résultat est un interblocage.

 

 



