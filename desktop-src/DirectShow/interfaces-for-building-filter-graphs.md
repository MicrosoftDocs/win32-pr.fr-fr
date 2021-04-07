---
description: Interfaces pour la création de graphiques de filtre
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Interfaces pour la création de graphiques de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746012"
---
# <a name="interfaces-for-building-filter-graphs"></a>Interfaces pour la création de graphiques de filtre

Les applications utilisent ces interfaces pour générer différents types de graphiques de filtre.



| Interface                                                  | Description                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [**IAMFilterGraphCallback**](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | Recevoir des notifications de rappel si un code confidentiel ne peut pas être rendu. |
| [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | Fournit un mécanisme de rappel lors de la génération du graphique.        |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | Créer des graphiques de filtre pour la capture vidéo.                      |
| [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | Énumérer les périphériques système, tels que les périphériques de capture.          |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | Générez des graphiques de filtre pour la navigation et la lecture des DVD.        |
| [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | Énumérez les filtres dans le graphique.                         |
| [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | Ajoutez, supprimez ou connectez des filtres.                            |
| [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | Énumérer les filtres inscrits sur le système de l’utilisateur.      |
| [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | Générez des graphiques de filtre pour la lecture de fichiers ou pour des utilisations personnalisées.   |
| [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | Reconfigurez dynamiquement un graphique de filtre.                     |
| [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | Déterminez le moment où le graphique change.                           |



 

 

 



