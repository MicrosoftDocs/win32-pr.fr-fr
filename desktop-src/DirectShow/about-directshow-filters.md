---
description: À propos des filtres DirectShow
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: À propos des filtres DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104571204"
---
# <a name="about-directshow-filters"></a>À propos des filtres DirectShow

DirectShow utilise une architecture modulaire, où chaque étape de traitement est effectuée par un objet COM appelé filtre. DirectShow fournit un ensemble de filtres standard pour les applications à utiliser, et les développeurs peuvent écrire leurs propres filtres personnalisés qui étendent les fonctionnalités de DirectShow. Pour illustrer ce point, Voici les étapes nécessaires pour lire un fichier vidéo AVI, ainsi que les filtres qui effectuent chaque étape :

-   Lit les données brutes du fichier sous la forme d’un flux d’octets (filtre de source de fichier).
-   Examinez les en-têtes AVI, puis analysez le flux d’octets dans des images vidéo et des échantillons audio distincts (filtre de séparateur AVI).
-   Décodez les images vidéo (différents filtres de décodeur, selon le format de compression).
-   Dessinez les images vidéo (filtre de convertisseur vidéo).
-   Envoyez les exemples audio à la carte son (filtre de périphérique DirectSound par défaut).

Ces filtres sont présentés dans le diagramme suivant.

![graphique de filtre pour lire un fichier AVI avec une vidéo compressée](images/avi-filter-graph.png)

Comme le montre le diagramme, chaque filtre est connecté à un ou plusieurs autres filtres. Les points de connexion sont également des objets COM, appelés *codes PIN*. Les filtres utilisent des broches pour déplacer les données d’un filtre à l’autre. Les flèches dans le diagramme indiquent la direction dans laquelle les données transitent. Dans DirectShow, un ensemble de filtres est appelé un *graphique de filtre*.

Les filtres ont trois États possibles : en cours d’exécution, arrêté et suspendu. Lorsqu’un filtre est en cours d’exécution, il traite les données multimédias. Lorsqu’il est arrêté, il arrête le traitement des données. L’état suspendu est utilisé pour signaler des données avant de s’exécuter ; la section [Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md) décrit ce concept plus en détail. À de rares exceptions près, les modifications d’État sont coordonnées dans tout le graphique de filtre ; tous les filtres du graphique basculent entre les États. Ainsi, l’ensemble du graphique de filtre est également dit en cours d’exécution, arrêté ou suspendu.

Les filtres peuvent être regroupés en plusieurs grandes catégories :

-   Un filtre *source* introduit des données dans le graphique. Les données peuvent provenir d’un fichier, d’un réseau, d’un appareil photo ou de tout autre emplacement. Chaque filtre source gère un type de source de données différent.
-   Un filtre de *transformation* prend un flux d’entrée, traite les données et crée un flux de sortie. Les encodeurs et les décodeurs sont des exemples de filtres de transformation.
-   Les filtres de *convertisseur* se trouvent à la fin de la chaîne. Ils reçoivent des données et les présentent à l’utilisateur. Par exemple, un convertisseur vidéo dessine des images vidéo sur l’écran. un convertisseur audio envoie des données audio à la carte son. et un filtre d’écriture de fichier écrit des données dans un fichier.
-   Un filtre *Splitter* fractionne un flux d’entrée en deux sorties ou plus, en analysant généralement le flux d’entrée en cours de route. Par exemple, le séparateur AVI analyse un flux d’octets dans des flux vidéo et audio distincts.
-   Un filtre *MUX* prend plusieurs entrées et les combine en un seul flux. Par exemple, le multiplexeur de multiplexage (AVI) effectue l’opération inverse du séparateur AVI. Elle prend des flux audio et vidéo et produit un flux d’octets au format AVI.

Les différences entre ces catégories ne sont pas absolues. Par exemple, le filtre de lecteur ASF agit à la fois comme un filtre source et un filtre de séparateur.

Tous les filtres DirectShow exposent l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) , et tous les codes confidentiels exposent l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) . DirectShow définit également de nombreuses autres interfaces qui prennent en charge des fonctionnalités plus spécifiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du gestionnaire de graphique de filtre](about-the-filter-graph-manager.md)
</dt> <dt>

[Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



