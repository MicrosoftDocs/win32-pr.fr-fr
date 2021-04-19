---
description: Configuration du graphique de filtre DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuration du graphique de filtre DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522404"
---
# <a name="dvd-filter-graph-configuration"></a>Configuration du graphique de filtre DVD

Cette section décrit les différentes configurations de graphique de filtre pour la lecture de DVD dans DirectShow. Ces diagrammes sont fournis principalement à des fins de référence. Le navigateur DVD génère le graphique. ainsi, en général, il n’est pas nécessaire de comprendre les détails de la configuration du graphique. Pour plus d’informations, consultez [génération du graphique de filtre DVD](building-the-dvd-filter-graph.md).

L’illustration suivante montre un graphique de filtre DVD avec un décodeur logiciel.

![graphique de filtre DVD pour Windows XP](images/dvd-graph-xp.png)

Lorsqu’un décodeur matériel est présent, il est généralement connecté directement à la carte vidéo par un port vidéo. Cela permet d’envoyer les bits vidéo décodés directement à la mémoire tampon de trame sur la carte graphique sans passer à la mémoire de l’hôte. Pour gérer cette connexion directe sur les versions antérieures de Windows, DirectShow prend en charge les extensions de port vidéo DirectDraw (VPE) via une interface sur le [filtre de mixage de superposition](overlay-mixer-filter.md).

> [!Note]  
> Le mélangeur de superposition est maintenant déconseillé.

 

Dans Windows XP et versions ultérieures, un décodeur matériel peut se connecter au filtre du [Gestionnaire de port vidéo](video-port-manager.md) .

![graphique DVD pour Windows XP avec un décodeur matériel](images/dvd-hwgraph-xp.png)

Dans tous ces graphiques, le navigateur DVD est le filtre source ; il effectue plusieurs tâches :

-   Lit les données de navigation et de vidéo à partir du disque.
-   Démultiplexe les données vidéo, audio et de sous-image en flux distincts.
-   Pompe les flux dans le graphique pour un traitement ultérieur et un rendu éventuel.
-   Informe votre application d’événements liés aux DVD.

Sur le flux audio, le navigateur DVD se connecte en aval à un décodeur audio, qui se connecte au [filtre de convertisseur DirectSound](directsound-renderer-filter.md), le convertisseur audio par défaut. Dans les flux vidéo et sous-image, les filtres en aval sont le décodeur vidéo tiers et le convertisseur de mixage vidéo (ou le [mélangeur de superposition](overlay-mixer-filter.md)et le [convertisseur vidéo](video-renderer-filter.md) sur les applications de niveau inférieur). Si votre application doit gérer les données de sous-titres de la ligne 21, vous devez ajouter le filtre de la ligne de code de la ligne 21 DirectShow au graphique. Cela implique un appel de méthode unique ; le filtre sera automatiquement connecté.

Votre application communique avec et contrôle le navigateur DVD par le biais des interfaces personnalisées exposées par le navigateur DVD : [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), les méthodes « Set », et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), les méthodes « d’extraction ». Il doit également communiquer avec le gestionnaire de graphique de filtre (par le biais de [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) pour arrêter, démarrer et contrôler le graphique. Vous devrez peut-être également contrôler d’autres filtres individuels, tels que le filtre de mixage de superposition pour basculer entre les affichages plein écran et fenêtre. Pour plus d’informations, consultez [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). La configuration exacte du graphique varie selon le type de décodeur MPEG-2 que vous avez installé, si vous devez gérer les données de sous-titrage de ligne 21 et d’autres facteurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



