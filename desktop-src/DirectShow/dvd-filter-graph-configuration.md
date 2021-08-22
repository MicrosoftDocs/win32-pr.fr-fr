---
description: Configuration de Graph de filtre de DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuration de Graph de filtre de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece69f77ac4a4e6674bbcd12404a10b7f765a514e18cb31963d2ed7f981799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653083"
---
# <a name="dvd-filter-graph-configuration"></a>Configuration de Graph de filtre de DVD

Cette section décrit les différentes configurations de graphique de filtre pour la lecture de DVD dans DirectShow. Ces diagrammes sont fournis principalement à des fins de référence. Le navigateur DVD génère le graphique. ainsi, en général, il n’est pas nécessaire de comprendre les détails de la configuration du graphique. Pour plus d’informations, consultez [génération du filtre de DVD Graph](building-the-dvd-filter-graph.md).

L’illustration suivante montre un graphique de filtre DVD avec un décodeur logiciel.

![graphique de filtre DVD pour Windows XP](images/dvd-graph-xp.png)

Lorsqu’un décodeur matériel est présent, il est généralement connecté directement à la carte vidéo par un port vidéo. Cela permet d’envoyer les bits vidéo décodés directement à la mémoire tampon de trame sur la carte graphique sans passer à la mémoire de l’hôte. pour gérer cette connexion directe sur les versions antérieures de Windows, DirectShow prend en charge les Extensions de Port vidéo (VPE) DirectDraw via une interface sur le [filtre de Mixer de superposition](overlay-mixer-filter.md).

> [!Note]  
> le Mixer de superposition est maintenant déconseillé.

 

dans Windows XP et versions ultérieures, un décodeur matériel peut se connecter au filtre du [gestionnaire de Port vidéo](video-port-manager.md) .

![graphique DVD pour Windows XP avec un décodeur matériel](images/dvd-hwgraph-xp.png)

Dans tous ces graphiques, le navigateur DVD est le filtre source ; il effectue plusieurs tâches :

-   Lit les données de navigation et de vidéo à partir du disque.
-   Démultiplexe les données vidéo, audio et de sous-image en flux distincts.
-   Pompe les flux dans le graphique pour un traitement ultérieur et un rendu éventuel.
-   Informe votre application d’événements liés aux DVD.

Sur le flux audio, le navigateur DVD se connecte en aval à un décodeur audio, qui se connecte au [filtre de convertisseur DirectSound](directsound-renderer-filter.md), le convertisseur audio par défaut. dans les flux vidéo et sous-image, les filtres en aval sont le décodeur vidéo tiers et le convertisseur de mixage vidéo (ou le [Mixer de superposition](overlay-mixer-filter.md)et le [convertisseur vidéo](video-renderer-filter.md) sur les applications de niveau inférieur). si votre application gère les données de sous-titres de la ligne 21, vous devez ajouter le filtre DirectShow ligne 21 décodeur 2 au graphique. Cela implique un appel de méthode unique ; le filtre sera automatiquement connecté.

Votre application communique avec et contrôle le navigateur DVD par le biais des interfaces personnalisées exposées par le navigateur DVD : [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), les méthodes « Set », et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), les méthodes « d’extraction ». Il doit également communiquer avec le gestionnaire de graphique de filtre (par le biais de [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) pour arrêter, démarrer et contrôler le graphique. vous devrez peut-être également contrôler d’autres filtres individuels, tels que la superposition Mixer filtre pour basculer entre l’affichage à l’écran et la fenêtre. Pour plus d’informations, consultez [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). La configuration exacte du graphique varie selon le type de décodeur MPEG-2 que vous avez installé, si vous devez gérer les données de sous-titrage de ligne 21 et d’autres facteurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



