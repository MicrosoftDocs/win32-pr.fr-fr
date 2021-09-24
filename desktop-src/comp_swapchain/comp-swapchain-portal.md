---
title: Utilise permutation de la composition
description: Cette API est la version publique initiale de l’API utilise permutation de composition
keywords:
- Utilise permutation de la composition
- API utilise permutation de la composition
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: a8c03448333a9bb1b2c6b2b3b1c64b51be9dbada
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523844"
---
# <a name="composition-swapchain"></a>Utilise permutation de la composition

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

## <a name="overview"></a>Vue d’ensemble

Cette API est la version publique initiale de l’API utilise permutation de composition. il permet aux applications utilisant des api de Composition (telles que [**Windows. UI. Composition**](/uwp/api/windows.ui.composition) et [**DirectComposition**](/windows/win32/directcomp/directcomposition-portal)) d’héberger du contenu qui peut être rendu et présenté de façon indépendante. À de nombreux égards, ce type de contenu présenté est similaire à un utilise permutation DXGI. Les deux offrent la possibilité d’effectuer un rendu dans une mémoire tampon, puis de présenter cette mémoire tampon à l’écran. Toutefois, l’API utilise permutation de la composition offre la possibilité de présenter pour cibler une heure spécifique à afficher (le temps *PresentAt* ), tandis que dxgi ne le fait pas, et l’API utilise permutation de composition offre plus de liberté que dxgi autour de l’ordre des mémoires tampons disponibles.

l’objectif de la première version de cette API est de permettre aux infrastructures multimédias, telles que [Windows Media Foundation](/windows/win32/medfound/microsoft-media-foundation-sdk), d’utiliser efficacement une présentation chronométrée.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Guide de programmation utilise permutation de la composition](comp-swapchain.md) | Cette API est un successeur sectaire du utilise permutation DXGI, qui permet aux applications d’afficher et de présenter du contenu à l’écran. |
| [Exemples de code de composition utilise permutation](comp-swapchain-examples.md) | Collection d’exemples de code montrant différents scénarios de utilise permutation de composition. |
| [Glossaire de la composition](comp-swapchain-glossary.md) | Glossaire des termes de la composition utilise permutation. |
