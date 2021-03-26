---
description: Chaque fois qu’une application crée un contrôleur de domaine et commence immédiatement à appeler les fonctions de sortie ou de dessin GDI, il tire parti de l’espace de la page par défaut à l’espace de l’appareil et de l’espace de l’appareil aux transformations de la zone cliente.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Transformations par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972715"
---
# <a name="default-transformations"></a><span data-ttu-id="57d1a-103">Transformations par défaut</span><span class="sxs-lookup"><span data-stu-id="57d1a-103">Default Transformations</span></span>

<span data-ttu-id="57d1a-104">Chaque fois qu’une application crée un contrôleur de domaine et commence immédiatement à appeler les fonctions de sortie ou de dessin GDI, il tire parti de l’espace de la page par défaut à l’espace de l’appareil et de l’espace de l’appareil aux transformations de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="57d1a-104">Whenever an application creates a DC and immediately begins calling GDI drawing or output functions, it takes advantage of the default page-space to device-space, and device-space to client-area transformations.</span></span> <span data-ttu-id="57d1a-105">Une transformation de l’espace entre les pages ne peut pas se produire tant que l’application n’appelle pas d’abord la fonction [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) pour définir le mode sur GM \_ Advanced, puis appelle la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .</span><span class="sxs-lookup"><span data-stu-id="57d1a-105">A world-to-page space transformation cannot happen until the application first calls the [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) function to set the mode to GM\_ADVANCED and then calls the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function.</span></span>

<span data-ttu-id="57d1a-106">L’utilisation du \_ texte de mm (l’espace de page par défaut pour la transformation de l’espace de l’appareil) entraîne un mappage un-à-un ; autrement dit, un point donné dans l’espace de page est mappé au même point dans l’espace de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="57d1a-106">Use of MM\_TEXT (the default page-space to device-space transformation) results in a one-to-one mapping; that is, a given point in page space maps to the same point in device space.</span></span> <span data-ttu-id="57d1a-107">Comme mentionné précédemment, cette transformation n’est pas spécifiée par une matrice.</span><span class="sxs-lookup"><span data-stu-id="57d1a-107">As previously mentioned, this transformation is not specified by a matrix.</span></span> <span data-ttu-id="57d1a-108">Au lieu de cela, il est obtenu en divisant la largeur de la fenêtre d’affichage par la largeur de la fenêtre et la hauteur de la fenêtre d’affichage par la hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="57d1a-108">Instead, it is obtained by dividing the width of the viewport by the width of the window and the height of the viewport by the height of the window.</span></span> <span data-ttu-id="57d1a-109">Dans le cas par défaut, les dimensions de la fenêtre d’affichage sont de 1 pixel par 1 pixel et les dimensions de la fenêtre sont 1 unité de page par unité de page.</span><span class="sxs-lookup"><span data-stu-id="57d1a-109">In the default case, the viewport dimensions are 1-pixel by 1-pixel and the window dimensions are 1-page unit by 1-page unit.</span></span>

<span data-ttu-id="57d1a-110">La transformation de l’espace périphérique au périphérique physique (zone client, bureau ou imprimante) produit toujours un mappage un-à-un. autrement dit, une unité de l’espace de l’appareil est toujours équivalente à une unité dans la zone cliente, sur le bureau ou sur une page.</span><span class="sxs-lookup"><span data-stu-id="57d1a-110">The device-space to physical-device (client area, desktop, or printer paper) transformation always results in a one-to-one mapping; that is, one unit in device space is always equivalent to one unit in the client area, on the desktop, or on a page.</span></span> <span data-ttu-id="57d1a-111">La traduction est le seul objectif de cette transformation. elle garantit que la sortie apparaît correctement dans la fenêtre d’une application, quel que soit l’endroit où cette fenêtre est déplacée sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="57d1a-111">The sole purpose of this transformation is translation; it ensures that output appears correctly in an application's window no matter where that window is moved on the desktop.</span></span>

<span data-ttu-id="57d1a-112">L’aspect unique du texte de MM \_ est l’orientation de l’axe des y dans l’espace de page.</span><span class="sxs-lookup"><span data-stu-id="57d1a-112">The one unique aspect of MM\_TEXT is the orientation of the y-axis in page space.</span></span> <span data-ttu-id="57d1a-113">Dans \_ le texte de mm, l’axe des y positif s’étend vers le bas et l’axe y négatif s’étend vers le haut.</span><span class="sxs-lookup"><span data-stu-id="57d1a-113">In MM\_TEXT, the positive y-axis extends downward and the negative y-axis extends upward.</span></span>

 

 



