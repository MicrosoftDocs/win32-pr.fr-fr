---
description: Une corde est une région délimitée par l’intersection d’une ellipse et un segment de ligne appelé sécante. L’illustration suivante montre une corde dessinée à l’aide de la fonction corde.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: À propos des cordes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527705"
---
# <a name="about-chords"></a><span data-ttu-id="0e8f1-104">À propos des cordes</span><span class="sxs-lookup"><span data-stu-id="0e8f1-104">About Chords</span></span>

<span data-ttu-id="0e8f1-105">Une *corde* est une région délimitée par l’intersection d’une ellipse et un segment de ligne appelé *sécante*.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-105">A *chord* is a region bounded by the intersection of an ellipse and a line segment called a *secant*.</span></span> <span data-ttu-id="0e8f1-106">L’illustration suivante montre une corde dessinée à l’aide de la fonction [**corde**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .</span><span class="sxs-lookup"><span data-stu-id="0e8f1-106">The following illustration shows a chord drawn by using the [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) function.</span></span>

![illustration d’un Elipse, montrant deux radials, une sécante et une corde](images/csfsh-02.png)

<span data-ttu-id="0e8f1-108">Lors de l’appel de [**corde**](/windows/win32/api/wingdi/nf-wingdi-chord), une application fournit les coordonnées des angles supérieur gauche et inférieur droit du rectangle englobant de l’ellipse, ainsi que les coordonnées de deux points définissant deux radiales.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-108">When calling [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span> <span data-ttu-id="0e8f1-109">Un radial est une ligne dessinée du centre du rectangle englobant d’une ellipse à un point sur l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-109">A radial is a line drawn from the center of an ellipse's bounding rectangle to a point on the ellipse.</span></span>

<span data-ttu-id="0e8f1-110">Lorsque le système dessine la partie courbée du cordon, il le fait en utilisant la direction d’arc actuelle pour le contexte de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-110">When the system draws the curved part of the chord, it does so by using the current arc direction for the specified device context.</span></span> <span data-ttu-id="0e8f1-111">La direction de l’arc par défaut est dans le sens inverse des aiguilles.</span><span class="sxs-lookup"><span data-stu-id="0e8f1-111">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="0e8f1-112">Vous pouvez demander à votre application de réinitialiser la direction de l’arc en appelant la fonction [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="0e8f1-112">You can have your application reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
