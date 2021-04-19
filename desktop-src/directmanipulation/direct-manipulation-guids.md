---
description: Les GUID de classe de manipulation directe suivants sont définis dans DirectManipulation. idl.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUID de manipulation directe
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 57dfa5701d7f01a9738206e7a2e3d669f6cf6a4a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544546"
---
# <a name="direct-manipulation-guids"></a>GUID de manipulation directe

Les GUID de classe de [manipulation directe](direct-manipulation-portal.md) suivants sont définis dans DirectManipulation. idl.

- [ID de classe principale](#master-class-ids)
- [Classe de contenu secondaire-ID](#secondary-content-class-ids)
- [ID de classe d’objets de comportement](#behavior-objects-class-ids)
- [Rubriques connexes](#related-topics)

## <a name="master-class-ids"></a>ID de classe principale

| GUID                                     | Description                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | Classe DirectManipulationManager. Cet objet permet d’accéder à toutes les fonctionnalités de [manipulation directe](direct-manipulation-portal.md) et aux API disponibles pour l’application.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | Classe DCompManipulationCompositor. Il s’agit d’une implémentation du [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) qui encapsule DirectComposition. Grâce à cet objet compository, DirectManipulation peut appliquer la sortie en définissant les transformations directement sur l’arborescence DComp. |

## <a name="secondary-content-class-ids"></a>Classe de contenu secondaire-ID

| GUID                                  | Description                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ VerticalIndicatorContent**   | Indicateur de panoramique vertical. Élément visuel qui affiche la position actuelle dans le contenu qui s’étend hors écran verticalement.     |
| **CLSID \_ HorizontalIndicatorContent** | Indicateur de panoramique horizontal. Élément visuel qui affiche la position actuelle dans le contenu qui s’étend horizontalement hors écran. |
| **CLSID \_ VirtualViewportContent**     | Fenêtre d’affichage virtuelle. Une fenêtre d’affichage virtuelle peut être utilisée pour respecter les éléments de position fixes des Viewports avec la configuration du zoom.          |

## <a name="behavior-objects-class-ids"></a>ID de classe d’objets de comportement

| GUID                                     | Description                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ DragDropConfigurationBehavior** | Faites glisser & comportement de déplacement. Permet de sélectionner et de faire glisser des éléments.                                                                                       |
| **CLSID \_ AutoScrollBehavior**            | Comportement du défilement automatique. Permet au contenu de faire défiler automatiquement l’approche de la limite d’un axe donné.                                           |
| **CLSID \_ DeferContactService**           | Contactez le comportement de report. Durée d’attente (en millliseconds) avant l’appel de [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). |

## <a name="related-topics"></a>Rubriques connexes

[Manipulation directe](direct-manipulation-portal.md), [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**AddConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration), [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
