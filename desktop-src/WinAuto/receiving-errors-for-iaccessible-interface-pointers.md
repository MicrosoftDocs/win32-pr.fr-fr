---
title: Réception d’erreurs pour les pointeurs d’interface IAccessible
description: Cette rubrique décrit les situations dans lesquelles vous pouvez recevoir une erreur pour un pointeur d’interface IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840430"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a><span data-ttu-id="61e8f-103">Réception d’erreurs pour les pointeurs d’interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="61e8f-103">Receiving Errors for IAccessible Interface Pointers</span></span>

<span data-ttu-id="61e8f-104">Cette rubrique décrit les situations dans lesquelles vous pouvez recevoir une erreur pour un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="61e8f-104">This topic describes situations in which you might receive an error for an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="61e8f-105">Les fonctions **IAccessible** peuvent retourner des erreurs pour les pointeurs d’interface **IAccessible** lorsqu’un utilisateur ferme une application à laquelle l’objet appartient, ou si un utilisateur ignore un contrôle par le biais de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61e8f-105">**IAccessible** functions can return errors for **IAccessible** interface pointers when a user closes an application that the object belongs to, or if a user dismisses a control through the user interface.</span></span>

## <a name="user-closes-an-application"></a><span data-ttu-id="61e8f-106">L’utilisateur ferme une application</span><span class="sxs-lookup"><span data-stu-id="61e8f-106">User Closes an Application</span></span>

<span data-ttu-id="61e8f-107">Si un utilisateur ferme l’application qui contient un objet sur lequel le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pointe, tous les appels futurs à cet objet retournent un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="61e8f-107">If a user closes the application that contains an object to which the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer was pointing, then all future calls to that object will return an error code.</span></span> <span data-ttu-id="61e8f-108">L’erreur, telle que **co \_ E \_ OBJNOTCONNECTED**, indique que l’objet n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="61e8f-108">The error, such as **CO\_E\_OBJNOTCONNECTED**, will indicate that the object does not exist anymore.</span></span> <span data-ttu-id="61e8f-109">Cela s’applique à tous les pointeurs d’interface **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="61e8f-109">This applies to all **IAccessible** interface pointers.</span></span>

## <a name="user-dismisses-a-control"></a><span data-ttu-id="61e8f-110">L’utilisateur ignore un contrôle</span><span class="sxs-lookup"><span data-stu-id="61e8f-110">User Dismisses a Control</span></span>

<span data-ttu-id="61e8f-111">Si un utilisateur ignore un contrôle (par exemple, en appuyant sur un bouton de commande), les clients peuvent toujours appeler des méthodes et des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sur cet objet, car l’objet n’a pas été libéré.</span><span class="sxs-lookup"><span data-stu-id="61e8f-111">If a user dismisses a control (for example, by pressing a push button), clients can still call [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties on this object because the object has not been released.</span></span> <span data-ttu-id="61e8f-112">Toutefois, les appels futurs recevront des messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="61e8f-112">However, future calls will receive error messages.</span></span>

<span data-ttu-id="61e8f-113">Cette situation s’applique aux fonctions et méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="61e8f-113">This situation applies to the following functions and methods:</span></span>

-   [<span data-ttu-id="61e8f-114">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="61e8f-114">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [<span data-ttu-id="61e8f-115">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="61e8f-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="61e8f-116">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="61e8f-116">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="61e8f-117">**IAccessible :: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="61e8f-117">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="61e8f-118">**IAccessible :: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="61e8f-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="61e8f-119">**IAccessible :: \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="61e8f-119">**IAccessible::get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [<span data-ttu-id="61e8f-120">**IAccessible :: \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="61e8f-120">**IAccessible::get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




