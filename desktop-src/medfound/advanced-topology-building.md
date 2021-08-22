---
description: Génération de topologie avancée
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Génération de topologie avancée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7f2bba412a698d688bc9d88e9935ed0988cc909931634633a0d75b88c2fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664869"
---
# <a name="advanced-topology-building"></a>Génération de topologie avancée

Cette section décrit quelques techniques avancées pour la création de topologies. Vous pouvez utiliser ces techniques si vous souhaitez davantage de contrôle sur les topologies que vous envoyez à la session multimédia.

Étant donné que ces techniques sont destinées à des scénarios qui dépassent la fonctionnalité fournie par le chargeur de topologie standard, un grand nombre des détails dépendent des exigences spécifiques de votre application. Par conséquent, cette section est organisée de façon faible autour des tâches subordonnées plus petites, plutôt que des scénarios complets de bout en bout.

L’application de lecture classique suit les étapes suivantes :

1.  L’application génère une topologie partielle et la met en file d’attente dans la session multimédia.
2.  La session multimédia appelle le chargeur de topologie pour résoudre la topologie.

Si vous souhaitez aller au-delà des fonctionnalités du chargeur de topologie, il existe trois approches générales :

-   Créez une topologie complète. Lorsque vous vous connectez à la topologie de la session multimédia, appelez [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) avec l' \_ \_ indicateur nosolution MFSESSION SetTopology. Cet indicateur empêche la session multimédia d’essayer de résoudre la topologie.

-   Appelez directement le chargeur de topologie pour résoudre la topologie. Vous pouvez ensuite modifier la topologie complète avant de la mettre en file d’attente dans la session multimédia.

-   Implémentez un chargeur de topologie personnalisé. Avec cette approche, vous mettrez en file d’attente une topologie partielle, mais la session multimédia appelle votre chargeur personnalisé au lieu de l’implémentation de Media Foundation standard. L’un des avantages de cette approche est que vous pouvez effectuer une génération de topologie personnalisée dans l’environnement protégé. (Dans ce cas, toutefois, le chargeur de topologie doit être un composant approuvé. Pour plus d’informations, consultez [chemin d’accès au média protégé](protected-media-path.md).)

Cette section contient les rubriques suivantes :



| Rubrique                                                                          | Description                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Chargeurs de topologie personnalisés](custom-topology-loaders.md)                         | Comment fournir une implémentation personnalisée de [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) pour la session multimédia.          |
| [Liaison de nœuds de sortie à des récepteurs multimédias](binding-output-nodes-to-media-sinks.md) | Comment préparer les nœuds de sortie dans une topologie si vous utilisez le chargeur de topologie en dehors de la session multimédia. |
| [Ajout d’un décodeur à une topologie](adding-a-decoder-to-a-topology.md)           | Comment sélectionner manuellement un décodeur et l’ajouter à une topologie.                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Topologies](topologies.md)
</dt> </dl>

 

 



