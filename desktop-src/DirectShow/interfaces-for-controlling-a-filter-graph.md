---
description: Interfaces pour le contrôle d’un filtre Graph
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Interfaces pour le contrôle d’un filtre Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8170b8d2da80272a5620abe163f938e53105cc5b471593a3799d4c36069fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154090"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a>Interfaces pour le contrôle d’un filtre Graph

Ces interfaces fournissent des méthodes pour le contrôle d’un graphique de filtre.



| Interface                                  | Description                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | Ajustez l’horloge du graphique.                                                                                   |
| [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | Synchroniser des flux en direct dans un graphique de filtre.                                                               |
| [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | Chaînes de contrôle des filtres.                                                                                |
| [**Appel**](/windows/desktop/api/Control/nn-control-imediacontrol)     | Exécutez, suspendez et arrêtez le graphique de filtre. (Fournit également des méthodes compatibles Automation pour la génération de graphiques.) |
| [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)     | Répondre aux événements dans le graphique.                                                                           |
| [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | Recherchez dans un fichier.                                                                                       |
| [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)     | Met en file d’attente les commandes à exécuter ultérieurement.                                                                    |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | Effectuer un pas à pas détaillé dans un flux vidéo.                                                                        |



 

 

 



