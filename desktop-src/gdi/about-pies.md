---
description: Un secteur est une région délimitée par l’intersection d’une courbe ellipse et deux radiales. L’illustration suivante montre un graphique à secteurs dessiné à l’aide de la fonction Pie.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: À propos des secteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034234"
---
# <a name="about-pies"></a><span data-ttu-id="5e904-104">À propos des secteurs</span><span class="sxs-lookup"><span data-stu-id="5e904-104">About Pies</span></span>

<span data-ttu-id="5e904-105">Un *secteur* est une région délimitée par l’intersection d’une courbe ellipse et deux radiales.</span><span class="sxs-lookup"><span data-stu-id="5e904-105">A *pie* is a region bounded by the intersection of an ellipse curve and two radials.</span></span> <span data-ttu-id="5e904-106">L’illustration suivante montre un graphique à secteurs dessiné à l’aide de la fonction [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .</span><span class="sxs-lookup"><span data-stu-id="5e904-106">The following illustration shows a pie drawn by using the [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) function.</span></span>

![Illustration montrant une ellipse avec un graphique en secteurs ombré](images/csfsh-03.png)

<span data-ttu-id="5e904-108">Lors de l’appel de [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), une application fournit les coordonnées des angles supérieur gauche et inférieur droit du rectangle englobant de l’ellipse, ainsi que les coordonnées de deux points définissant deux radiales.</span><span class="sxs-lookup"><span data-stu-id="5e904-108">When calling [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span>

<span data-ttu-id="5e904-109">Lorsque le système dessine la partie courbée du graphique, il utilise la direction d’arc actuelle pour le contexte de périphérique donné.</span><span class="sxs-lookup"><span data-stu-id="5e904-109">When the system draws the curved part of the pie, it uses the current arc direction for the given device context.</span></span> <span data-ttu-id="5e904-110">La direction de l’arc par défaut est dans le sens inverse des aiguilles.</span><span class="sxs-lookup"><span data-stu-id="5e904-110">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="5e904-111">Une application peut réinitialiser la direction de l’arc en appelant la fonction [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="5e904-111">An application can reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
