---
title: Mode de conservation et mode immédiat
description: Les API Graphics peuvent être divisées en API en mode mémorisé et en API en mode immédiat.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104565825"
---
# <a name="retained-mode-versus-immediate-mode"></a><span data-ttu-id="defa5-103">Mode de conservation et mode immédiat</span><span class="sxs-lookup"><span data-stu-id="defa5-103">Retained Mode Versus Immediate Mode</span></span>

<span data-ttu-id="defa5-104">Les API Graphics peuvent être divisées en API *en mode mémorisé* et *en API en mode immédiat* .</span><span class="sxs-lookup"><span data-stu-id="defa5-104">Graphics APIs can be divided into *retained-mode* APIs and *immediate-mode* APIs.</span></span> <span data-ttu-id="defa5-105">Direct2D est une API en mode immédiat.</span><span class="sxs-lookup"><span data-stu-id="defa5-105">Direct2D is an immediate-mode API.</span></span> <span data-ttu-id="defa5-106">Windows Presentation Foundation (WPF) est un exemple d’API en mode conservé.</span><span class="sxs-lookup"><span data-stu-id="defa5-106">Windows Presentation Foundation (WPF) is an example of a retained-mode API.</span></span>

<span data-ttu-id="defa5-107">Une API en mode mémorisé est déclarative.</span><span class="sxs-lookup"><span data-stu-id="defa5-107">A retained-mode API is declarative.</span></span> <span data-ttu-id="defa5-108">L’application construit une scène à partir de primitives graphiques, telles que des formes et des lignes.</span><span class="sxs-lookup"><span data-stu-id="defa5-108">The application constructs a scene from graphics primitives, such as shapes and lines.</span></span> <span data-ttu-id="defa5-109">La bibliothèque Graphics stocke un modèle de la scène en mémoire.</span><span class="sxs-lookup"><span data-stu-id="defa5-109">The graphics library stores a model of the scene in memory.</span></span> <span data-ttu-id="defa5-110">Pour dessiner un frame, la bibliothèque de graphiques transforme la scène en un ensemble de commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="defa5-110">To draw a frame, the graphics library transforms the scene into a set of drawing commands.</span></span> <span data-ttu-id="defa5-111">Entre les frames, la bibliothèque Graphics conserve la scène en mémoire.</span><span class="sxs-lookup"><span data-stu-id="defa5-111">Between frames, the graphics library keeps the scene in memory.</span></span> <span data-ttu-id="defa5-112">Pour modifier ce qui est affiché, l’application émet une commande pour mettre à jour la scène, par exemple pour ajouter ou supprimer une forme.</span><span class="sxs-lookup"><span data-stu-id="defa5-112">To change what is rendered, the application issues a command to update the scene—for example, to add or remove a shape.</span></span> <span data-ttu-id="defa5-113">La bibliothèque est alors chargée de redessiner la scène.</span><span class="sxs-lookup"><span data-stu-id="defa5-113">The library is then responsible for redrawing the scene.</span></span>

![diagramme qui affiche des graphiques en mode mémorisé.](images/graphics06.png)

<span data-ttu-id="defa5-115">Une API en mode immédiat est procédurale.</span><span class="sxs-lookup"><span data-stu-id="defa5-115">An immediate-mode API is procedural.</span></span> <span data-ttu-id="defa5-116">Chaque fois qu’un nouveau frame est dessiné, l’application émet directement les commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="defa5-116">Each time a new frame is drawn, the application directly issues the drawing commands.</span></span> <span data-ttu-id="defa5-117">La bibliothèque Graphics ne stocke pas de modèle de scène entre les frames.</span><span class="sxs-lookup"><span data-stu-id="defa5-117">The graphics library does not store a scene model between frames.</span></span> <span data-ttu-id="defa5-118">Au lieu de cela, l’application effectue le suivi de la scène.</span><span class="sxs-lookup"><span data-stu-id="defa5-118">Instead, the application keeps track of the scene.</span></span>

![diagramme qui affiche des graphiques en mode immédiat.](images/graphics07.png)

<span data-ttu-id="defa5-120">Les API en mode mémorisé peuvent être plus simples à utiliser, car l’API effectue davantage de tâches pour vous, telles que l’initialisation, la maintenance de l’État et le nettoyage.</span><span class="sxs-lookup"><span data-stu-id="defa5-120">Retained-mode APIs can be simpler to use, because the API does more of the work for you, such as initialization, state maintenance, and cleanup.</span></span> <span data-ttu-id="defa5-121">En revanche, ils sont souvent moins flexibles, car l’API impose son propre modèle de scène.</span><span class="sxs-lookup"><span data-stu-id="defa5-121">On the other hand, they are often less flexible, because the API imposes its own scene model.</span></span> <span data-ttu-id="defa5-122">En outre, une API en mode mémorisé peut avoir des exigences de mémoire plus élevées, car elle doit fournir un modèle de scène à usage général.</span><span class="sxs-lookup"><span data-stu-id="defa5-122">Also, a retained-mode API can have higher memory requirements, because it needs to provide a general-purpose scene model.</span></span> <span data-ttu-id="defa5-123">Avec une API en mode immédiat, vous pouvez implémenter des optimisations ciblées.</span><span class="sxs-lookup"><span data-stu-id="defa5-123">With an immediate-mode API, you can implement targeted optimizations.</span></span>

## <a name="next"></a><span data-ttu-id="defa5-124">Suivant</span><span class="sxs-lookup"><span data-stu-id="defa5-124">Next</span></span>

[<span data-ttu-id="defa5-125">Votre premier programme Direct2D</span><span class="sxs-lookup"><span data-stu-id="defa5-125">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)

 

 




