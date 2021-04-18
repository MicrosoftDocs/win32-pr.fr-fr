---
title: Vue d’ensemble de l’API Windows Automation
description: Microsoft Windows propose deux spécifications d’API pour l’accessibilité de l’interface utilisateur et l’automatisation des tests logiciels Microsoft Active Accessibility et Microsoft UI Automation.
ms.assetid: 73acc580-9573-40ea-8727-b0e7292b2a4c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac67c5311d0d936e45235c527ebb15c238ba808
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315659"
---
# <a name="windows-accessibility-api-overview"></a><span data-ttu-id="3b8de-103">Vue d’ensemble de l’API d’accessibilité Windows</span><span class="sxs-lookup"><span data-stu-id="3b8de-103">Windows Accessibility API overview</span></span>

<span data-ttu-id="3b8de-104">Cette section fournit des vues d’ensemble de haut niveau et une référence d’API détaillée pour l’API Microsoft Windows Automation 3,0, qui inclut l’implémentation Windows de la [spécification Microsoft UI Automation](./uiauto-specandcommunitypromise.md)et Microsoft Active Accessibility (fonctionnalité héritée introduite dans Windows 95 en tant que complément de plateforme).</span><span class="sxs-lookup"><span data-stu-id="3b8de-104">This section provides high-level overviews and detailed API reference for both the Microsoft Windows Automation API 3.0, which includes the Windows implementation of the Microsoft [UI Automation Specification](./uiauto-specandcommunitypromise.md), and Microsoft Active Accessibility (legacy feature introduced in Windows 95 as a platform add-in).</span></span>

<span data-ttu-id="3b8de-105">Nous décrivons les similitudes et les différences entre Microsoft Active Accessibility et UI Automation, les composants et les fonctionnalités qui permettent aux deux technologies de travailler ensemble, et fournissent des instructions pour le choix de la technologie à implémenter pour votre scénario spécifique.</span><span class="sxs-lookup"><span data-stu-id="3b8de-105">We describe the similarities and differences between Microsoft Active Accessibility and UI Automation, the components and features that enable the two technologies to work together, and provide guidelines for choosing which technology to implement for your specific scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b8de-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b8de-106">Related topics</span></span>

[<span data-ttu-id="3b8de-107">Promesse de la communauté UI Automation</span><span class="sxs-lookup"><span data-stu-id="3b8de-107">UI Automation Community Promise</span></span>](./uiauto-specandcommunitypromise.md)