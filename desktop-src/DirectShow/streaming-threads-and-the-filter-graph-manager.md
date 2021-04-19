---
description: Streaming threads et le gestionnaire de graphique de filtre
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Streaming threads et le gestionnaire de graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520625"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Streaming threads et le gestionnaire de graphique de filtre

Lorsque le gestionnaire de graphes de filtres arrête le graphique, il attend que tous les threads de diffusion en continu s’arrêtent. Cela a les conséquences suivantes pour les filtres :

-   Un filtre ne doit jamais appeler de méthodes sur le gestionnaire de graphique de filtre à partir d’un thread de streaming.

    Le gestionnaire de graphique de filtre utilise une section critique pour synchroniser ses propres opérations. Si un thread de streaming tente de conserver cette section critique, il peut provoquer un blocage. Par exemple : Supposons qu’un autre thread arrête le graphique. Ce thread prend le verrou du graphique de filtre et attend que votre filtre cesse de transmettre des données. Si votre filtre attend le verrou, il ne s’arrêtera jamais, provoquant ainsi un blocage.

-   Un filtre ne doit jamais **AddRef** ou **QueryInterface** du gestionnaire de graphique de filtre à partir d’un thread de streaming.

    Si le filtre contient un décompte de références sur le gestionnaire de graphes de filtre (par le biais de **AddRef** ou **QueryInterface**), il peut devenir le dernier objet à contenir un décompte de références. Lorsque le filtre appelle **Release**, le gestionnaire de graphique de filtre détruit lui-même. Au sein de sa routine de nettoyage, le gestionnaire de graphes de filtre tente d’arrêter le graphique, provoquant l’attente de la fermeture du thread de streaming. Toutefois, il attend dans le thread de diffusion en continu, donc le thread de streaming ne peut pas quitter. Le résultat est un interblocage.

 

 



