---
description: Avant de peindre, le système doit préparer le périphérique d’affichage pour les opérations de dessin.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Périphériques d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972702"
---
# <a name="display-devices"></a><span data-ttu-id="e8c3f-103">Périphériques d’affichage</span><span class="sxs-lookup"><span data-stu-id="e8c3f-103">Display Devices</span></span>

<span data-ttu-id="e8c3f-104">Avant de peindre, le système doit préparer le périphérique d’affichage pour les opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-104">Before painting, the system must prepare the display device for drawing operations.</span></span> <span data-ttu-id="e8c3f-105">Un contexte de périphérique d’affichage définit un ensemble d’objets graphiques et leurs attributs associés, ainsi que les modes graphiques qui affectent la sortie.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-105">A display device context defines a set of graphic objects and their associated attributes, and the graphic modes that affect output.</span></span> <span data-ttu-id="e8c3f-106">Le système prépare chaque contexte de périphérique d’affichage pour la sortie dans une fenêtre, en définissant les objets de dessin, les couleurs et les modes de la fenêtre au lieu du périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-106">The system prepares each display device context for output to a window, setting the drawing objects, colors, and modes for the window instead of the display device.</span></span> <span data-ttu-id="e8c3f-107">Lorsque l’application fournit le contexte de périphérique d’affichage par le biais d’appels aux fonctions GDI, GDI utilise les informations dans le contexte pour générer la sortie dans la fenêtre spécifiée sans aucune intrusion sur les autres fenêtres ou autres parties de l’écran.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-107">When the application supplies the display device context through calls to GDI functions, GDI uses the information in the context to generate output in the specified window without intruding on other windows or other parts of the screen.</span></span>

<span data-ttu-id="e8c3f-108">Le système fournit cinq types de contextes de périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-108">The system provides five kinds of display device contexts.</span></span>



| <span data-ttu-id="e8c3f-109">Type</span><span class="sxs-lookup"><span data-stu-id="e8c3f-109">Type</span></span>                                           | <span data-ttu-id="e8c3f-110">Signification</span><span class="sxs-lookup"><span data-stu-id="e8c3f-110">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8c3f-111">classiques</span><span class="sxs-lookup"><span data-stu-id="e8c3f-111">common</span></span>](common-display-device-contexts.md)   | <span data-ttu-id="e8c3f-112">Autorise le dessin dans la zone cliente d’une fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-112">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="e8c3f-113">class</span><span class="sxs-lookup"><span data-stu-id="e8c3f-113">class</span></span>](class-display-device-contexts.md)     | <span data-ttu-id="e8c3f-114">Autorise le dessin dans la zone cliente d’une fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-114">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="e8c3f-115">parent</span><span class="sxs-lookup"><span data-stu-id="e8c3f-115">parent</span></span>](parent-display-device-contexts.md)   | <span data-ttu-id="e8c3f-116">Autorise le dessin n’importe où dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-116">Permits drawing anywhere in the window.</span></span> <span data-ttu-id="e8c3f-117">Bien que le contexte de périphérique parent autorise également le dessin dans la fenêtre parente, il n’est pas destiné à être utilisé de cette façon.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-117">Although the parent device context also permits drawing in the parent window, it is not intended to be used in this way.</span></span> |
| [<span data-ttu-id="e8c3f-118">priv</span><span class="sxs-lookup"><span data-stu-id="e8c3f-118">private</span></span>](private-display-device-contexts.md) | <span data-ttu-id="e8c3f-119">Autorise le dessin dans la zone cliente d’une fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-119">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="e8c3f-120">window</span><span class="sxs-lookup"><span data-stu-id="e8c3f-120">window</span></span>](window-display-device-contexts.md)   | <span data-ttu-id="e8c3f-121">Autorise le dessin n’importe où dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-121">Permits drawing anywhere in the window.</span></span>                                                                                                                          |



 

<span data-ttu-id="e8c3f-122">Le système fournit un contexte de périphérique commun, de classe, parent ou privé à une fenêtre en fonction du type de contexte de périphérique d’affichage spécifié dans le style de classe de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-122">The system supplies a common, class, parent, or private device context to a window based on the type of display device context specified in that window's class style.</span></span> <span data-ttu-id="e8c3f-123">Le système fournit un contexte de périphérique Windows uniquement lorsque l’application en demande explicitement une, par exemple, en appelant la fonction [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) .</span><span class="sxs-lookup"><span data-stu-id="e8c3f-123">The system supplies a window device context only when the application explicitly requests one for example, by calling the [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function.</span></span> <span data-ttu-id="e8c3f-124">Dans tous les cas, une application peut utiliser la fonction [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) pour déterminer la fenêtre qu’un DC d’affichage représente actuellement.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-124">In all cases, an application can use the [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) function to determine which window a display DC currently represents.</span></span>

<span data-ttu-id="e8c3f-125">Cette section fournit des informations sur les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8c3f-125">This section provides information on the following topics.</span></span>

-   [<span data-ttu-id="e8c3f-126">Afficher le cache du contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="e8c3f-126">Display Device Context Cache</span></span>](display-device-context-cache.md)
-   [<span data-ttu-id="e8c3f-127">Afficher les paramètres par défaut du contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="e8c3f-127">Display Device Context Defaults</span></span>](display-device-context-defaults.md)
-   [<span data-ttu-id="e8c3f-128">Contextes de périphérique d’affichage courants</span><span class="sxs-lookup"><span data-stu-id="e8c3f-128">Common Display Device Contexts</span></span>](common-display-device-contexts.md)
-   [<span data-ttu-id="e8c3f-129">Contextes de périphérique d’affichage privé</span><span class="sxs-lookup"><span data-stu-id="e8c3f-129">Private Display Device Contexts</span></span>](private-display-device-contexts.md)
-   [<span data-ttu-id="e8c3f-130">Contextes de périphérique d’affichage parent</span><span class="sxs-lookup"><span data-stu-id="e8c3f-130">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)
-   [<span data-ttu-id="e8c3f-131">Affichage de la classe contextes de périphérique</span><span class="sxs-lookup"><span data-stu-id="e8c3f-131">Class Display Device Contexts</span></span>](class-display-device-contexts.md)
-   [<span data-ttu-id="e8c3f-132">Fenêtre Affichage des contextes de périphérique</span><span class="sxs-lookup"><span data-stu-id="e8c3f-132">Window Display Device Contexts</span></span>](window-display-device-contexts.md)
-   [<span data-ttu-id="e8c3f-133">Contextes de périphérique d’affichage parent</span><span class="sxs-lookup"><span data-stu-id="e8c3f-133">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)

 

 



