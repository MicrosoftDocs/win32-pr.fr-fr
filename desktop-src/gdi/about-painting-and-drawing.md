---
description: Presque toutes les applications utilisent l’écran pour afficher les données qu’elles manipulent.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: À propos de la peinture et du dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991153"
---
# <a name="about-painting-and-drawing"></a><span data-ttu-id="de553-103">À propos de la peinture et du dessin</span><span class="sxs-lookup"><span data-stu-id="de553-103">About Painting and Drawing</span></span>

<span data-ttu-id="de553-104">Presque toutes les applications utilisent l’écran pour afficher les données qu’elles manipulent.</span><span class="sxs-lookup"><span data-stu-id="de553-104">Nearly all applications use the screen to display the data they manipulate.</span></span> <span data-ttu-id="de553-105">Une application peint des images, dessine des figures et écrit du texte afin que l’utilisateur puisse afficher les données à mesure qu’elles sont créées, modifiées et imprimées.</span><span class="sxs-lookup"><span data-stu-id="de553-105">An application paints images, draws figures, and writes text so that the user can view data as it is created, edited, and printed.</span></span> <span data-ttu-id="de553-106">Microsoft Windows offre une prise en charge enrichie de la peinture et du dessin, mais, en raison de la nature des systèmes d’exploitation multitâche, les applications doivent coopérer les unes avec les autres lors de l’accès à l’écran.</span><span class="sxs-lookup"><span data-stu-id="de553-106">Microsoft Windows provides rich support for painting and drawing, but, because of the nature of multitasking operating systems, applications must cooperate with one another when accessing the screen.</span></span>

<span data-ttu-id="de553-107">Pour que toutes les applications fonctionnent correctement et de manière coopérative, le système gère l’ensemble de la sortie à l’écran.</span><span class="sxs-lookup"><span data-stu-id="de553-107">To keep all applications functioning smoothly and cooperatively, the system manages all output to the screen.</span></span> <span data-ttu-id="de553-108">Les applications utilisent Windows comme périphérique de sortie principal plutôt que l’écran lui-même.</span><span class="sxs-lookup"><span data-stu-id="de553-108">Applications use windows as their primary output device rather than the screen itself.</span></span> <span data-ttu-id="de553-109">Le système fournit des contextes de périphérique d’affichage qui correspondent de manière unique aux fenêtres.</span><span class="sxs-lookup"><span data-stu-id="de553-109">The system supplies display device contexts that uniquely correspond to the windows.</span></span> <span data-ttu-id="de553-110">Les applications utilisent des contextes de périphérique d’affichage pour diriger leur sortie vers les fenêtres spécifiées.</span><span class="sxs-lookup"><span data-stu-id="de553-110">Applications use display device contexts to direct their output to the specified windows.</span></span> <span data-ttu-id="de553-111">Le fait de dessiner dans une fenêtre (en dirigeant la sortie) empêche une application d’interférer avec la sortie d’autres applications et permet aux applications de coexister les unes avec les autres tout en tirant pleinement parti des fonctionnalités graphiques du système.</span><span class="sxs-lookup"><span data-stu-id="de553-111">Drawing in a window (directing output to it) prevents an application from interfering with the output of other applications and allows applications to coexist with one another while still taking full advantage of the graphics capabilities of the system.</span></span>

-   [<span data-ttu-id="de553-112">Quand dessiner dans une fenêtre</span><span class="sxs-lookup"><span data-stu-id="de553-112">When to Draw in a Window</span></span>](when-to-draw-in-a-window.md)
-   [<span data-ttu-id="de553-113">Message de \_ peinture WM</span><span class="sxs-lookup"><span data-stu-id="de553-113">The WM\_PAINT Message</span></span>](the-wm-paint-message.md)
-   [<span data-ttu-id="de553-114">Dessin sans le \_ message WM Paint</span><span class="sxs-lookup"><span data-stu-id="de553-114">Drawing Without the WM\_PAINT Message</span></span>](drawing-without-the-wm-paint-message.md)
-   [<span data-ttu-id="de553-115">Système de coordonnées de fenêtre</span><span class="sxs-lookup"><span data-stu-id="de553-115">Window Coordinate System</span></span>](window-coordinate-system.md)
-   [<span data-ttu-id="de553-116">Régions de fenêtre</span><span class="sxs-lookup"><span data-stu-id="de553-116">Window Regions</span></span>](window-regions.md)
-   [<span data-ttu-id="de553-117">Arrière-plan de fenêtre</span><span class="sxs-lookup"><span data-stu-id="de553-117">Window Background</span></span>](window-background.md)
-   [<span data-ttu-id="de553-118">Fenêtres réduites</span><span class="sxs-lookup"><span data-stu-id="de553-118">Minimized Windows</span></span>](minimized-windows.md)
-   [<span data-ttu-id="de553-119">Fenêtres redimensionnées</span><span class="sxs-lookup"><span data-stu-id="de553-119">Resized Windows</span></span>](resized-windows.md)
-   [<span data-ttu-id="de553-120">Zone non cliente</span><span class="sxs-lookup"><span data-stu-id="de553-120">Nonclient Area</span></span>](nonclient-area.md)
-   [<span data-ttu-id="de553-121">Zone de mise à jour de la fenêtre enfant</span><span class="sxs-lookup"><span data-stu-id="de553-121">Child Window Update Region</span></span>](child-window-update-region.md)
-   [<span data-ttu-id="de553-122">Périphériques d’affichage</span><span class="sxs-lookup"><span data-stu-id="de553-122">Display Devices</span></span>](display-devices.md)
-   [<span data-ttu-id="de553-123">Verrou de mise à jour de fenêtre</span><span class="sxs-lookup"><span data-stu-id="de553-123">Window Update Lock</span></span>](window-update-lock.md)
-   [<span data-ttu-id="de553-124">Rectangle englobant cumulé</span><span class="sxs-lookup"><span data-stu-id="de553-124">Accumulated Bounding Rectangle</span></span>](accumulated-bounding-rectangle.md)

 

 



