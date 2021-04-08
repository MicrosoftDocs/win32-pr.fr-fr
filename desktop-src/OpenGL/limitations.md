---
title: Limites
description: Limites
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL sur Windows, limitations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672682"
---
# <a name="limitations"></a><span data-ttu-id="4ffa3-104">Limites</span><span class="sxs-lookup"><span data-stu-id="4ffa3-104">Limitations</span></span>

<span data-ttu-id="4ffa3-105">L’implémentation générique présente les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ffa3-105">The generic implementation has the following limitations:</span></span>

-   <span data-ttu-id="4ffa3-106">Impression.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-106">Printing.</span></span>

    <span data-ttu-id="4ffa3-107">Vous pouvez imprimer une image OpenGL directement sur une imprimante en utilisant uniquement des fichiers.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-107">You can print an OpenGL image directly to a printer using metafiles only.</span></span> <span data-ttu-id="4ffa3-108">Pour plus d’informations, consultez [impression d’une image OpenGL](printing-an-opengl-image.md).</span><span class="sxs-lookup"><span data-stu-id="4ffa3-108">For more information, see [Printing an OpenGL Image](printing-an-opengl-image.md).</span></span>

-   <span data-ttu-id="4ffa3-109">Les graphiques OpenGL et GDI ne peuvent pas être mélangés dans une fenêtre à double mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-109">OpenGL and GDI graphics cannot be mixed in a double-buffered window.</span></span>

    <span data-ttu-id="4ffa3-110">Une application peut directement dessiner des graphiques OpenGL et des graphiques GDI dans une fenêtre à une seule mise en mémoire tampon, mais pas dans une fenêtre à deux mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-110">An application can directly draw both OpenGL graphics and GDI graphics into a single-buffered window, but not into a double-buffered window.</span></span>

-   <span data-ttu-id="4ffa3-111">Il n’y a pas de palettes de couleurs matérielles par fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-111">There are no per-window hardware color palettes.</span></span>

    <span data-ttu-id="4ffa3-112">Windows dispose d’une palette de couleurs matérielles système unique, qui s’applique à l’ensemble de l’écran.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-112">Windows has a single system hardware color palette, which applies to the whole screen.</span></span> <span data-ttu-id="4ffa3-113">Une fenêtre OpenGL ne peut pas avoir sa propre palette matérielle, mais elle peut avoir sa propre palette logique.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-113">An OpenGL window cannot have its own hardware palette, but can have its own logical palette.</span></span> <span data-ttu-id="4ffa3-114">Pour ce faire, il doit devenir une application prenant en charge la palette.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-114">To do so, it must become a palette-aware application.</span></span> <span data-ttu-id="4ffa3-115">Pour plus d’informations, consultez [modes de couleurs OpenGL et gestion de la palette Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="4ffa3-115">For more information, see [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

-   <span data-ttu-id="4ffa3-116">Il n’existe aucune prise en charge directe pour le presse-papiers, l’échange dynamique de données (DDE) ou OLE.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-116">There is no direct support for the Clipboard, dynamic data exchange (DDE), or OLE.</span></span>

    <span data-ttu-id="4ffa3-117">Une fenêtre avec des graphiques OpenGL ne prend pas directement en charge ces fonctionnalités Windows.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-117">A window with OpenGL graphics does not directly support these Windows capabilities.</span></span> <span data-ttu-id="4ffa3-118">Toutefois, il existe des solutions de contournement pour l’utilisation du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-118">There are workarounds, however, for using the Clipboard.</span></span> <span data-ttu-id="4ffa3-119">Pour plus d’informations, consultez [copie d’une image OpenGL dans le presse-papiers](copying-an-opengl-image-to-the-clipboard.md).</span><span class="sxs-lookup"><span data-stu-id="4ffa3-119">For more information, see [Copying an OpenGL Image to the Clipboard](copying-an-opengl-image-to-the-clipboard.md).</span></span>

-   <span data-ttu-id="4ffa3-120">La bibliothèque de classes ininventor 2,0 C++ n’est pas incluse.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-120">The Inventor 2.0 C++ class library is not included.</span></span>

    <span data-ttu-id="4ffa3-121">La bibliothèque de classes d’inventaire, basée sur OpenGL, fournit des constructions de niveau supérieur pour la programmation de graphiques 3D.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-121">The Inventor class library, built on top of OpenGL, provides higher-level constructs for programming 3-D graphics.</span></span> <span data-ttu-id="4ffa3-122">Elle n’est pas incluse dans la version actuelle de l’implémentation de OpenGL pour Windows par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-122">It is not included in the current version of Microsoft's implementation of OpenGL for Windows.</span></span>

-   <span data-ttu-id="4ffa3-123">Il n’existe aucune prise en charge des fonctionnalités de format de pixel suivantes : les images stéréoscopiques, les bitplanes alpha et les tampons auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="4ffa3-123">There is no support for the following pixel format features: stereoscopic images, alpha bitplanes, and auxiliary buffers.</span></span>

    <span data-ttu-id="4ffa3-124">Toutefois, il existe une prise en charge de plusieurs mémoires tampons auxiliaires, notamment : tampon stencil, tampon d’accumulation, mémoire tampon d’arrière-plan (double mise en mémoire tampon), mémoire tampon plan Underlay et mémoire tampon de plan de profondeur (axe z).</span><span class="sxs-lookup"><span data-stu-id="4ffa3-124">There is, however, support for several ancillary buffers including: stencil buffer, accumulation buffer, back buffer (double buffering), overlay and underlay plane buffer, and depth (z-axis) buffer.</span></span>

 

 




