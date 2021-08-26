---
description: Applications DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Applications DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d601fdbf94ef2a2d9a70d1f28f68854200b58f9fb44d23c3738994f3001e3a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102959"
---
# <a name="dvd-applications"></a>Applications DVD

DirectShow fournit un composant appelé filtre de la source du [navigateur dvd](dvd-navigator-filter.md) , qui simplifie les tâches de navigation sur les dvd en C++. Le navigateur DVD offre toutes les fonctionnalités que vous trouvez sur un lecteur de DVD autonome complet, ainsi que des fonctionnalités supplémentaires spécifiques à la lecture de DVD sur des ordinateurs personnels. Grâce au navigateur DVD, les développeurs de scripts et C++ peuvent créer des applications DVD complètes sans faire référence à la spécification DVD. Le navigateur DVD, en coordination avec les filtres de décodeur, gère également la gestion régionale et la protection des droits d’auteur (CSS et protection de copie analogique), en isolant les développeurs d’applications de ces détails.

Le filtre de navigateur DVD fonctionne sur l’intégralité d’un volume DVD-Video, qui se compose des fichiers du répertoire de la vidéo \_ TS. contrairement à la plupart des DirectShow filtres source qui fonctionnent avec des fichiers ou flux individuels, le navigateur DVD utilise la structure DVD-Video des titres, des chapitres et des codes de temps. les développeurs souhaitant lire des fichiers mpeg-2 individuels dans DirectShow doivent utiliser le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) au lieu du filtre de navigateur DVD. pour plus d’informations, consultez [prise en charge de MPEG-2 dans DirectShow](mpeg-2-support-in-directshow.md) .

> [!Note]  
> Pour lire des DVD, l’utilisateur doit disposer d’un décodeur MPEG-2.

 

Cette section contient les rubriques suivantes :

-   [Fonctionnalités de prise en charge des DVD dans DirectShow](dvd-support-features-in-directshow.md)
-   [Notions de base sur les DVD](dvd-basics.md)
-   [Génération du filtre de DVD Graph](building-the-dvd-filter-graph.md)
-   [Obtention des pointeurs d’interface DVD](obtaining-the-dvd-interface-pointers.md)
-   [Commandes de DVD](dvd-commands.md)
-   [Identification des opérations DVD valides](identifying-valid-dvd-operations.md)
-   [Synchronisation des commandes de DVD](synchronizing-dvd-commands.md)
-   [Flow de données dans le navigateur DVD](data-flow-in-the-dvd-navigator.md)
-   [Gestion des notifications d’événements DVD](handling-dvd-event-notifications.md)
-   [Utilisation des menus de DVD](working-with-dvd-menus.md)
-   [Flux audio et sous-image](audio-and-subpicture-streams.md)
-   [Application des niveaux de gestion parentale](enforcing-parental-management-levels.md)
-   [Enregistrement et restauration d’objets DvdState](saving-and-restoring-dvdstate-objects.md)
-   [Utilisation des chaînes de texte de DVD](working-with-dvd-text-strings.md)
-   [Lecture de l’audio karaoké Flux](playing-karaoke-audio-streams.md)
-   [Gestion des éjections de disque](handling-disc-ejections.md)
-   [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Configuration de Graph de filtre de DVD](dvd-filter-graph-configuration.md)
-   [Raccourcis vers les pages de référence des DVD C++](shortcuts-to-c-dvd-reference-pages.md)

Pour obtenir des références sur le développement d’un décodeur de DVD/MPEG2, consultez [développement d’un décodeur de DVD dans DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DirectShow](using-directshow.md)
</dt> </dl>

 

 



