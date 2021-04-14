---
title: Contrôles sans fenêtre
description: Contrôles sans fenêtre
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380410"
---
# <a name="windowless-controls"></a><span data-ttu-id="b5361-103">Contrôles sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="b5361-103">Windowless Controls</span></span>

<span data-ttu-id="b5361-104">La spécification des contrôles ActiveX 96 contient une définition pour les contrôles sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b5361-104">The ActiveX Controls 96 specification includes a definition for windowless controls.</span></span> <span data-ttu-id="b5361-105">Ces contrôles ne fonctionnent pas dans leur propre fenêtre et requièrent qu’un conteneur offre une fenêtre partagée dans laquelle le contrôle peut être dessiné, consultez le kit de développement logiciel (SDK) ActiveX.</span><span class="sxs-lookup"><span data-stu-id="b5361-105">Such controls do not operate in their own window and require a container to offer a shared window into which the control may draw, see the ActiveX SDK.</span></span> <span data-ttu-id="b5361-106">Les contrôles sans fenêtre sont conçus pour être compatibles avec les conteneurs de contrôle plus anciens en créant leur propre fenêtre dans cette situation, les conteneurs de contrôle sans fenêtre doivent héberger les contrôles de fenêtre de manière traditionnelle sans problème.</span><span class="sxs-lookup"><span data-stu-id="b5361-106">Windowless controls are designed to be compatible with older control containers by creating their own window in that situation, windowless control containers should host windowed controls in the traditional way with no problem.</span></span> <span data-ttu-id="b5361-107">Il peut toutefois être utile pour un conteneur de distinguer les contrôles qui peuvent fonctionner en mode sans fenêtre, donc une catégorie de composant appropriée est définie.</span><span class="sxs-lookup"><span data-stu-id="b5361-107">It may however be useful for a container to distinguish those controls that can operate in a windowless mode, so an appropriate component category is defined.</span></span>

<span data-ttu-id="b5361-108">CATID-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject</span><span class="sxs-lookup"><span data-stu-id="b5361-108">CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID\_WindowlessObject</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5361-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5361-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5361-110">Catégories de composant</span><span class="sxs-lookup"><span data-stu-id="b5361-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




