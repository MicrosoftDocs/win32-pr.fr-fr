---
title: Considérations relatives à la conception des objets proxy
description: La conception d’objets proxy et accessibles dépend de la conception des éléments de l’interface utilisateur du serveur. Quelle que soit la conception, un élément d’interface utilisateur doit notifier son objet proxy avant qu’il ne soit détruit afin que l’objet proxy gère les appels des clients de manière appropriée.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028798"
---
# <a name="design-considerations-for-proxy-objects"></a><span data-ttu-id="4c62e-104">Considérations relatives à la conception des objets proxy</span><span class="sxs-lookup"><span data-stu-id="4c62e-104">Design Considerations for Proxy Objects</span></span>

<span data-ttu-id="4c62e-105">La conception d’objets proxy et accessibles dépend de la conception des éléments de l’interface utilisateur du serveur.</span><span class="sxs-lookup"><span data-stu-id="4c62e-105">Proxy and accessible object design depends on the design of the server UI elements.</span></span> <span data-ttu-id="4c62e-106">Quelle que soit la conception, un élément d’interface utilisateur doit notifier son objet proxy avant qu’il ne soit détruit afin que l’objet proxy gère les appels des clients de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="4c62e-106">Regardless of the design, a UI element must notify its proxy object right before it is destroyed so that the proxy object handles calls from clients appropriately.</span></span>

<span data-ttu-id="4c62e-107">La liste suivante décrit deux possibilités de conception :</span><span class="sxs-lookup"><span data-stu-id="4c62e-107">The following list describes two design possibilities:</span></span>

-   <span data-ttu-id="4c62e-108">Placez le code qui implémente l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dans le même module que le code qui implémente l’élément d’interface utilisateur si le code de l’interface utilisateur est facilement extensible.</span><span class="sxs-lookup"><span data-stu-id="4c62e-108">Place the code that implements the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface in the same module as the code that implements the user interface element if the user interface code is easily extensible.</span></span> <span data-ttu-id="4c62e-109">Dans ce cas, le proxy est « léger » dans le sens où il n’est qu’à surveiller la durée de vie de l’objet accessible, transférer les appels à l’objet accessible et retourner les résultats.</span><span class="sxs-lookup"><span data-stu-id="4c62e-109">In this case, the proxy is "lightweight" in the sense that all it does is monitor the life span of the accessible object, forward calls to the accessible object, and return the results.</span></span>
-   <span data-ttu-id="4c62e-110">Placez le code qui implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dans le même module que le code qui implémente l’objet proxy.</span><span class="sxs-lookup"><span data-stu-id="4c62e-110">Place the code that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in the same module as the code that implements the proxy object.</span></span> <span data-ttu-id="4c62e-111">Dans ce cas, l’objet accessible utilise des fonctions internes pour obtenir des informations sur l’élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c62e-111">In this case, the accessible object uses internal functions to obtain information about the UI element.</span></span>

## <a name="trackbar-controls"></a><span data-ttu-id="4c62e-112">Contrôles TrackBar</span><span class="sxs-lookup"><span data-stu-id="4c62e-112">Trackbar Controls</span></span>

<span data-ttu-id="4c62e-113">Lors de l’implémentation de contrôles TrackBar, utilisez le type de ligne de commande TrackBar **\_ inversé** pour fournir des informations plus explicites.</span><span class="sxs-lookup"><span data-stu-id="4c62e-113">When implementing trackbar controls, use the trackbar style **TBS\_REVERSED** to provide more meaningful information.</span></span> <span data-ttu-id="4c62e-114">Ce style inverse l’échelle utilisée par [**IAccessible :: \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="4c62e-114">This style reverses the scale used by [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="4c62e-115">Pour les trackbarss verticaux sans ce style, [**IAccessible :: obtenir \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) retourne la valeur zéro (0) lorsque le curseur de la barre de défilement se trouve en haut du contrôle ; les valeurs augmentent à mesure que vous faites glisser le curseur vers le bas.</span><span class="sxs-lookup"><span data-stu-id="4c62e-115">For vertical trackbars without this style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns zero (0) when the trackbar thumb is at the top of the control; the values increase as you slide the thumb toward the bottom.</span></span> <span data-ttu-id="4c62e-116">Avec le **style \_ inversé tbs** , **IAccessible :: obten \_ accValue** retourne 100 (100) quand le curseur de la barre de défilement se trouve en haut ; les nombres diminuent lorsque vous déplacez le curseur de la barre de défilement vers le bas.</span><span class="sxs-lookup"><span data-stu-id="4c62e-116">With the **TBS\_REVERSED** style, **IAccessible::get\_accValue** returns one hundred (100) when the trackbar thumb is at the top; the numbers decrease as you move the trackbar thumb toward the bottom.</span></span>

<span data-ttu-id="4c62e-117">Pour les trackbars horizontaux sans ce style, la valeur zéro (0) est retournée lorsque le curseur de la barre de défilement se trouve à l’extrémité gauche du contrôle ; les valeurs augmentent à mesure que vous déplacez le curseur de la barre de défilement vers la droite.</span><span class="sxs-lookup"><span data-stu-id="4c62e-117">For horizontal trackbars without this style, zero (0) is returned when the trackbar thumb is at the left end of the control; the values increase as you move the trackbar thumb to the right.</span></span> <span data-ttu-id="4c62e-118">Avec le **style \_ inversé tbs** , [**IAccessible :: obten \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) retourne 100 (100) quand le curseur de la barre de défilement se trouve à gauche ; les valeurs diminuent lorsque vous déplacez le curseur de la barre de défilement vers la droite.</span><span class="sxs-lookup"><span data-stu-id="4c62e-118">With the **TBS\_REVERSED** style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns one hundred (100) when the trackbar thumb is at the left; the values decrease as you move the trackbar thumb to the right.</span></span>

 

 




