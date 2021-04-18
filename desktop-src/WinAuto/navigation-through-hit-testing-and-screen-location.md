---
title: Navigation via le test de positionnement et l’emplacement à l’écran
description: Pour localiser les enfants d’un objet ou pour déterminer la taille d’un objet, les clients peuvent atteindre des points de test sur l’écran.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509192"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a><span data-ttu-id="aeda0-103">Navigation via le test de positionnement et l’emplacement à l’écran</span><span class="sxs-lookup"><span data-stu-id="aeda0-103">Navigation Through Hit Testing and Screen Location</span></span>

<span data-ttu-id="aeda0-104">Pour localiser les enfants d’un objet ou pour déterminer la taille d’un objet, les clients peuvent atteindre des points de test sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="aeda0-104">To locate an object's children or to determine an object's size, clients can hit test points on the screen.</span></span> <span data-ttu-id="aeda0-105">Deux méthodes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="aeda0-105">Two methods are available:</span></span>

-   [<span data-ttu-id="aeda0-106">**IAccessible :: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="aeda0-106">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="aeda0-107">**IAccessible :: accLocation**</span><span class="sxs-lookup"><span data-stu-id="aeda0-107">**IAccessible::accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a><span data-ttu-id="aeda0-108">Utilisation de IAccessible :: accHitTest</span><span class="sxs-lookup"><span data-stu-id="aeda0-108">Using IAccessible::accHitTest</span></span>

<span data-ttu-id="aeda0-109">Pour déterminer si un point se trouve dans un objet, au sein de son enfant, ou si aucun des clients n’appelle la méthode [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) de l’objet parent, en passant les coordonnées d’écran du point à tester.</span><span class="sxs-lookup"><span data-stu-id="aeda0-109">To identify whether a point is within an object, within its child, or neither, clients call the [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) method of the parent object, passing the screen coordinates of the point to be hit tested.</span></span> <span data-ttu-id="aeda0-110">La liste suivante décrit certains scénarios types :</span><span class="sxs-lookup"><span data-stu-id="aeda0-110">The following list describes some typical scenarios:</span></span>

-   <span data-ttu-id="aeda0-111">Si les enfants de l’objet se chevauchent à un point spécifié, [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) récupère l’enfant le plus élevé qui semble occuper l’espace.</span><span class="sxs-lookup"><span data-stu-id="aeda0-111">If the object's children overlap at a specified point, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) retrieves the topmost child that visually appears to occupy the space.</span></span>
-   <span data-ttu-id="aeda0-112">Si une fenêtre couvre un enfant, ou si l’enfant est coupé par le parent, le test de positionnement sur le point couvert récupère l’enfant même s’il n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="aeda0-112">If a window covers a child, or if the child is clipped by the parent, hit testing the covered point retrieves the child even though it is not visible.</span></span>
-   <span data-ttu-id="aeda0-113">Si l’enfant trouvé au point spécifié est un objet accessible, par opposition à un élément enfant, la méthode retourne l’interface [**IDispatch**](idispatch-interface.md) de l’enfant.</span><span class="sxs-lookup"><span data-stu-id="aeda0-113">If the child found at the specified point is an accessible object, as opposed to a child element, the method returns the child's [**IDispatch**](idispatch-interface.md) interface.</span></span>

## <a name="using-iaccessibleacclocation"></a><span data-ttu-id="aeda0-114">Utilisation de IAccessible :: accLocation</span><span class="sxs-lookup"><span data-stu-id="aeda0-114">Using IAccessible::accLocation</span></span>

<span data-ttu-id="aeda0-115">Pour récupérer l’emplacement à l’écran d’un objet ou de l’un des enfants de l’objet, les clients appellent [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span><span class="sxs-lookup"><span data-stu-id="aeda0-115">To get the screen location of an object or one of the object's children, clients call [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span></span> <span data-ttu-id="aeda0-116">Cette méthode retourne les coordonnées du rectangle englobant de l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="aeda0-116">This method returns the coordinates of the specified object's bounding rectangle.</span></span> <span data-ttu-id="aeda0-117">Si l’objet n’est pas mis en forme comme un rectangle, la méthode retourne les coordonnées du plus petit rectangle qui englobe la totalité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aeda0-117">If the object is not shaped like a rectangle, the method returns the coordinates of the smallest rectangle that encompasses the entire object.</span></span>

<span data-ttu-id="aeda0-118">L’illustration suivante montre la relation entre la région d’un objet non rectangulaire et son rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="aeda0-118">The following illustration shows the relationship between a non-rectangular object's region and its bounding rectangle.</span></span>

![Illustration montrant la région d’un objet non rectangulaire (un cercle) et son rectangle englobant.](images/region.gif)

> [!Note]  
> <span data-ttu-id="aeda0-120">[**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) est plus précis que [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , car il permet aux clients de déterminer l’emplacement des objets sur une base pixel par pixel plutôt qu’avec des rectangles englobants.</span><span class="sxs-lookup"><span data-stu-id="aeda0-120">[**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) is more precise than [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because it enables clients to determine the location of objects on a pixel-by-pixel basis rather than with bounding rectangles.</span></span> <span data-ttu-id="aeda0-121">Cette précision est utile, par exemple, lorsqu’une application collecte des informations en effectuant le suivi de l’emplacement du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="aeda0-121">This precision is useful, for example, when an application is gathering information by tracking the location of the mouse pointer.</span></span>

 

 

 




