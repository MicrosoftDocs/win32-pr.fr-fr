---
description: L’interface GDI (Graphics Device Interface) de Microsoft Windows permet aux applications d’utiliser des graphiques et du texte mis en forme à la fois dans l’affichage vidéo et l’imprimante.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: Windows GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5fc6ba9f4eb99786b21daeff2e1c48b9ce09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973051"
---
# <a name="windows-gdi"></a><span data-ttu-id="e6a76-103">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="e6a76-103">Windows GDI</span></span>

## <a name="purpose"></a><span data-ttu-id="e6a76-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="e6a76-104">Purpose</span></span>

<span data-ttu-id="e6a76-105">L’interface GDI (Graphics Device Interface) de Microsoft Windows permet aux applications d’utiliser des graphiques et du texte mis en forme à la fois dans l’affichage vidéo et l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="e6a76-105">The Microsoft Windows graphics device interface (GDI) enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="e6a76-106">Les applications Windows n’accèdent pas directement au matériel graphique.</span><span class="sxs-lookup"><span data-stu-id="e6a76-106">Windows-based applications do not access the graphics hardware directly.</span></span> <span data-ttu-id="e6a76-107">Au lieu de cela, GDI interagit avec les pilotes de périphérique pour le compte des applications.</span><span class="sxs-lookup"><span data-stu-id="e6a76-107">Instead, GDI interacts with device drivers on behalf of applications.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e6a76-108">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="e6a76-108">Where applicable</span></span>

<span data-ttu-id="e6a76-109">GDI peut être utilisé dans toutes les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="e6a76-109">GDI can be used in all Windows-based applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e6a76-110">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="e6a76-110">Developer audience</span></span>

<span data-ttu-id="e6a76-111">Cette API est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="e6a76-111">This API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="e6a76-112">Vous devez vous familiariser avec l' [architecture pilotée](../learnwin32/window-messages.md) par les messages Windows.</span><span class="sxs-lookup"><span data-stu-id="e6a76-112">Familiarity with the Windows [message-driven architecture](../learnwin32/window-messages.md) is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e6a76-113">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="e6a76-113">Run-time requirements</span></span>

<span data-ttu-id="e6a76-114">Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une fonction particulière, consultez la section Configuration requise de la documentation relative à la fonction.</span><span class="sxs-lookup"><span data-stu-id="e6a76-114">For information on which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e6a76-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e6a76-115">In this section</span></span>

-   [<span data-ttu-id="e6a76-116">Images bitmap</span><span class="sxs-lookup"><span data-stu-id="e6a76-116">Bitmaps</span></span>](bitmaps.md)
-   [<span data-ttu-id="e6a76-117">Pinceaux</span><span class="sxs-lookup"><span data-stu-id="e6a76-117">Brushes</span></span>](brushes.md)
-   [<span data-ttu-id="e6a76-118">Portion</span><span class="sxs-lookup"><span data-stu-id="e6a76-118">Clipping</span></span>](clipping.md)
-   [<span data-ttu-id="e6a76-119">Couleurs</span><span class="sxs-lookup"><span data-stu-id="e6a76-119">Colors</span></span>](colors.md)
-   [<span data-ttu-id="e6a76-120">Espaces de coordonnées et transformations</span><span class="sxs-lookup"><span data-stu-id="e6a76-120">Coordinate Spaces and Transformations</span></span>](coordinate-spaces-and-transformations.md)
-   [<span data-ttu-id="e6a76-121">Contextes de périphérique</span><span class="sxs-lookup"><span data-stu-id="e6a76-121">Device Contexts</span></span>](device-contexts.md)
-   [<span data-ttu-id="e6a76-122">Formes remplies</span><span class="sxs-lookup"><span data-stu-id="e6a76-122">Filled Shapes</span></span>](filled-shapes.md)
-   [<span data-ttu-id="e6a76-123">Polices et texte</span><span class="sxs-lookup"><span data-stu-id="e6a76-123">Fonts and Text</span></span>](fonts-and-text.md)
-   [<span data-ttu-id="e6a76-124">Lignes et courbes</span><span class="sxs-lookup"><span data-stu-id="e6a76-124">Lines and Curves</span></span>](lines-and-curves.md)
-   [<span data-ttu-id="e6a76-125">Métafichiers</span><span class="sxs-lookup"><span data-stu-id="e6a76-125">Metafiles</span></span>](metafiles.md)
-   [<span data-ttu-id="e6a76-126">Moniteurs multiples</span><span class="sxs-lookup"><span data-stu-id="e6a76-126">Multiple Display Monitors</span></span>](multiple-display-monitors.md)
-   [<span data-ttu-id="e6a76-127">Peinture et dessin</span><span class="sxs-lookup"><span data-stu-id="e6a76-127">Painting and Drawing</span></span>](painting-and-drawing.md)
-   [<span data-ttu-id="e6a76-128">Chemins d’accès</span><span class="sxs-lookup"><span data-stu-id="e6a76-128">Paths</span></span>](paths.md)
-   [<span data-ttu-id="e6a76-129">Stylets</span><span class="sxs-lookup"><span data-stu-id="e6a76-129">Pens</span></span>](pens.md)
-   <span data-ttu-id="e6a76-130">[Spouleur d’impression et d’impression](/previous-versions//dd162860(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6a76-130">[Printing and Print Spooler](/previous-versions//dd162860(v=vs.85))</span></span>
-   [<span data-ttu-id="e6a76-131">Rectangles</span><span class="sxs-lookup"><span data-stu-id="e6a76-131">Rectangles</span></span>](rectangles.md)
-   [<span data-ttu-id="e6a76-132">Régions</span><span class="sxs-lookup"><span data-stu-id="e6a76-132">Regions</span></span>](regions.md)

## <a name="related-topics"></a><span data-ttu-id="e6a76-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e6a76-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6a76-134">DirectX</span><span class="sxs-lookup"><span data-stu-id="e6a76-134">DirectX</span></span>](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[<span data-ttu-id="e6a76-135">GDI+</span><span class="sxs-lookup"><span data-stu-id="e6a76-135">GDI+</span></span>](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[<span data-ttu-id="e6a76-136">Technologie</span><span class="sxs-lookup"><span data-stu-id="e6a76-136">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="e6a76-137">Acquisition d’image Windows</span><span class="sxs-lookup"><span data-stu-id="e6a76-137">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> </dl>

 

 
