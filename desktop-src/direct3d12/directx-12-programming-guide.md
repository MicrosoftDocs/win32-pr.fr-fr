---
title: Guide de programmation pour Direct3D 12
description: Direct3D 12 fournit une API et une plateforme qui permettent aux applications de tirer parti des capacités graphiques et informatiques des PC équipés d’un ou de plusieurs GPU compatibles Direct3D 12.
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 94afd9125a2e73665e3783419651f34fd72285ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293579"
---
# <a name="direct3d-12-programming-guide"></a>Guide de programmation pour Direct3D 12

Direct3D 12 fournit une API et une plateforme qui permettent aux applications de tirer parti des capacités graphiques et informatiques des PC équipés d’un ou de plusieurs GPU compatibles Direct3D 12.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Qu’est-ce que Direct3D 12?](what-is-directx-12-.md) | DirectX 12 introduit la prochaine version de Direct3D, l’API graphique 3D au cœur de DirectX. Cette version de Direct3D est plus rapide et plus efficace que toute autre version précédente. Direct3D 12 offre des scènes plus riches, des objets plus complexes, des effets plus complexes et une utilisation complète du matériel du GPU moderne.  |
| [Nouveautés de Direct3D 12](new-releases.md) | Décrit la nouvelle documentation la plus significative disponible avec la dernière version du kit de développement logiciel (SDK). |
| [Comprendre Direct3D 12](directx-12-getting-started.md) | pour écrire des jeux et des applications en 3d pour Windows 10 et Windows 10 Mobile, vous devez comprendre les principes fondamentaux de la technologie Direct3D 12 et savoir comment vous préparer à l’utiliser dans vos jeux et vos applications. |
| [Envoi de travail dans Direct3D 12](command-queues-and-command-lists.md) | Pour améliorer l’efficacité de l’UC des applications Direct3D, Direct3D 12 ne prend plus en charge un contexte immédiat associé à un appareil. Au lieu de cela, les applications enregistrent et envoient des *listes de commandes* qui contiennent des appels de gestion des ressources et des dessins. Ces listes de commandes peuvent être envoyées à partir de plusieurs threads vers une ou plusieurs files d’attente de commandes, qui gèrent l’exécution des commandes. Ce changement fondamental augmente l’efficacité monothread en permettant aux applications de précalculer le travail de rendu en vue d’une réutilisation ultérieure et de tirer parti des systèmes multicœurs en répartissant le rendu du travail sur plusieurs threads.  |
| [Liaison de ressource dans Direct3D 12](resource-binding.md) | La liaison est le processus qui consiste à lier des objets de ressource aux nuanceurs du pipeline Graphics.  |
| [Gestion de la mémoire dans Direct3D 12](memory-management.md) | Le passage à D3D12 implique une synchronisation et une gestion appropriées de la résidence en mémoire. La gestion de la résidence en mémoire signifie qu’une plus grande synchronisation doit être effectuée. Cette section traite des stratégies de gestion de la mémoire et de la sous-allocation au sein des tas et des mémoires tampons.  |
| [Systèmes à plusieurs adaptateurs](multi-engine.md) | Décrit la prise en charge dans Direct3D 12 pour les systèmes sur lesquels plusieurs adaptateurs sont installés, couvrant les scénarios dans lesquels votre application cible explicitement plusieurs adaptateurs GPU et les scénarios où les pilotes utilisent implicitement plusieurs adaptateurs GPU pour le compte de votre application. |
| [Synchronisation multi-moteur](user-mode-heap-synchronization.md) | Cette rubrique traite de la synchronisation de l’accès aux multiples moteurs indépendants présents dans la plupart des GPU modernes. |
| [Rendu](rendering.md) | Cette section contient des informations sur les fonctionnalités de rendu nouvelles dans Direct3D 12 (et Direct3D 11,3). |
| [Compteurs, requêtes et mesure de performance](performance-measurement.md) | Les sections suivantes décrivent les fonctionnalités à utiliser dans les tests et l’amélioration des performances, tels que les requêtes, les compteurs, le minutage et la prédicat. |
| [Utilisation de Direct3D 11, Direct3D 10 et Direct2D](direct3d-12-interop.md) | Cette section traite des techniques d’interopérabilité avec les versions antérieures de Direct3D et Direct2D, de l’API Direct3D 11on12 et des instructions de portage de Direct3D 11 vers Direct3D 12. |
| [Exemples fonctionnels](working-samples.md) | Des exemples fonctionnels sont disponibles au téléchargement, qui illustrent l’utilisation d’un certain nombre de fonctionnalités de Direct3D 12. |
| [Guide pas à pas du code D3D12](d3d12-code-walk-throughs.md) | Cette section fournit du code pour les exemples de scénarios. La plupart des procédures pas à pas fournissent des détails sur le codage requis pour être ajouté à un exemple de base, afin d’éviter de répéter le code de base du composant pour chaque scénario. |
| [Débogage et diagnostics avec Direct3D 12](understanding-the-d3d12-debug-layer.md) | Contient des rubriques qui expliquent comment tirer le meilleur parti de la couche de débogage Direct3D 12 avec la validation basée sur GPU (GBV) et comment utiliser les données étendues supprimées des appareils (ordinateur). |

## <a name="related-topics"></a>Rubriques connexes

* [Graphismes Direct3D 12](direct3d-12-graphics.md)
* [Référence de Direct3D 12](direct3d-12-reference.md)
* [Didacticiels vidéo sur DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
