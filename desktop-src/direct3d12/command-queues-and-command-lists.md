---
title: Envoi de travail dans Direct3D 12
description: Pour améliorer l’efficacité de l’UC des applications Direct3D, Direct3D 12 ne prend plus en charge un contexte immédiat associé à un appareil.
ms.assetid: BE2F46EA-D4A9-47F7-A2D1-6A486DD4DC1A
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: aa852fc82280b14b0270a7c4a4c40cfe441803b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521764"
---
# <a name="work-submission-in-direct3d-12"></a>Envoi de travail dans Direct3D 12

Pour améliorer l’efficacité de l’UC des applications Direct3D, à compter de la version 12, Direct3D ne prend plus en charge un contexte immédiat associé à un appareil. Au lieu de cela, votre application enregistre, puis soumet les *listes de commandes*, qui contiennent des appels de gestion des ressources et des dessins. Vous pouvez envoyer ces listes de commandes à partir de plusieurs threads vers une ou plusieurs files d’attente de commandes, qui gèrent l’exécution des commandes. Ce changement fondamental augmente l’efficacité monothread en permettant à votre application de précalculer le travail de rendu en vue d’une réutilisation ultérieure et de tirer parti des systèmes multicœurs en répartissant le rendu du travail sur plusieurs threads.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Philosophie de conception des files d’attente de commandes et des listes de commandes](design-philosophy-of-command-queues-and-command-lists.md) | Les objectifs de la réutilisation du travail de rendu et de la mise à l’échelle multithread requièrent des modifications fondamentales à la façon dont les applications Direct3D soumettent le rendu du travail au GPU. |
| [Création et enregistrement de listes de commandes et de bundles](recording-command-lists-and-bundles.md) | Cette rubrique décrit l’enregistrement des listes de commandes et des offres groupées dans les applications Direct3D 12. Les listes de commandes et les offres groupées permettent aux applications d’enregistrer des appels de dessin ou de modification d’État pour une exécution ultérieure sur l’unité de traitement graphique (GPU). |
| [Exécution et synchronisation de listes de commandes](executing-and-synchronizing-command-lists.md) | Dans Microsoft Direct3D 12, le mode immédiat des versions précédentes n’est plus présent. Au lieu de cela, les applications créent des listes de commandes et des offres groupées, puis enregistrent des jeux de commandes GPU. Les files d’attente de commandes sont utilisées pour envoyer des listes de commandes à exécuter. Ce modèle permet aux développeurs de mieux contrôler l’utilisation efficace du GPU et du processeur. |
| [Gestion de l’état des pipelines graphiques dans Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md) | Cette rubrique décrit comment l’état du pipeline graphique est défini dans Direct3D 12. |
| [Utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md) | Pour réduire l’utilisation globale du processeur et activer le traitement multithread et le prétraitement des pilotes, Direct3D 12 déplace la responsabilité de la gestion de l’État par ressource du pilote Graphics vers l’application. |
| [Pipelines et nuanceurs avec Direct3D 12](pipelines-and-shaders-with-directx-12.md) | Le pipeline programmable Direct3D 12 augmente considérablement les performances de rendu par rapport aux interfaces de programmation graphique de génération précédente. |
| [Ombrage à taux variable (VRS)](vrs.md) | L’ombrage à taux variable &mdash; ou l’ombrage de pixels grossistes &mdash; est un mécanisme qui vous permet d’allouer les performances de rendu/la puissance à des vitesses qui varient d’un rendu à l’autre. |
| [Passes de rendu](direct3d-12-render-passes.md) | La fonctionnalité de passes de rendu permet à votre convertisseur d’améliorer l’efficacité du GPU en réduisant le trafic de mémoire vers/à partir de la mémoire hors puce. pour ce faire, il permet à votre application d’identifier plus facilement les exigences de classement de rendu des ressources et les dépendances de données. |

## <a name="related-topics"></a>Rubriques connexes

* [Guide de programmation Direct3D 12](directx-12-programming-guide.md)
