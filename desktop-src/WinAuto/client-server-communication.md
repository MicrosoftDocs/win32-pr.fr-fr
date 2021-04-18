---
title: Communication client/serveur
description: Le mécanisme WinEvents permet aux serveurs de communiquer facilement avec les clients Microsoft Active Accessibility.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "106509235"
---
# <a name="clientserver-communication"></a><span data-ttu-id="e2d30-103">Communication client/serveur</span><span class="sxs-lookup"><span data-stu-id="e2d30-103">Client/Server Communication</span></span>

<span data-ttu-id="e2d30-104">Le mécanisme [winEvents](winevents-overview.md) permet aux serveurs de communiquer facilement avec les clients Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="e2d30-104">The [WinEvents](winevents-overview.md) mechanism provides a way for servers to communicate easily with Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="e2d30-105">Les clients recueillent souvent des informations en réagissant à WinEvents (par exemple, après le focus), mais ils sont libres de demander des informations à un serveur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="e2d30-105">Clients often collect information by reacting to WinEvents (for example, following focus), but they are free to request information from a server at any time.</span></span>

<span data-ttu-id="e2d30-106">Pour demander des informations pour un objet accessible qui génère un WinEvent, un client doit traiter l’événement et établir une connexion avec l’objet accessible approprié.</span><span class="sxs-lookup"><span data-stu-id="e2d30-106">To request information for an accessible object that generates a WinEvent, a client must process the event and establish a connection with the relevant accessible object.</span></span> <span data-ttu-id="e2d30-107">Pour ce faire, le client effectue les six étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2d30-107">To do this, the client performs the following six steps:</span></span>

-   <span data-ttu-id="e2d30-108">Un serveur appelle [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) pour générer une notification WinEvent pour chaque modification apportée à ses éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2d30-108">A server calls [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to generate a WinEvent notification for each change to its user interface elements.</span></span>
-   <span data-ttu-id="e2d30-109">Le code de gestion WinEvent dans l’utilisateur détermine si des applications clientes ont inscrit une [*fonction de hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent à l’aide de [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) et appelle la fonction de rappel inscrite.</span><span class="sxs-lookup"><span data-stu-id="e2d30-109">The WinEvent management code in USER determines if any client applications have registered a WinEvent [*hook function*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) using [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and calls the registered callback function.</span></span>
-   <span data-ttu-id="e2d30-110">Dans sa fonction de rappel, le client demande l’accès à l’objet qui a généré l’événement en appelant [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) ou d’autres fonctions de récupération d’objet accessibles.</span><span class="sxs-lookup"><span data-stu-id="e2d30-110">In its callback function, the client requests access to the object that generated the event by calling [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) or other accessible object retrieval functions.</span></span> <span data-ttu-id="e2d30-111">Pour plus d’informations, consultez [récupération d’un objet IAccessible](retrieving-an-iaccessible-object.md).</span><span class="sxs-lookup"><span data-stu-id="e2d30-111">For more information, see [Retrieving an IAccessible Object](retrieving-an-iaccessible-object.md).</span></span>
-   <span data-ttu-id="e2d30-112">Cette API Microsoft Active Accessibility envoie à l’application serveur [**un \_ message WM**](wm-getobject.md) pour récupérer l’objet accessible.</span><span class="sxs-lookup"><span data-stu-id="e2d30-112">This Microsoft Active Accessibility API sends the server application a [**WM\_GETOBJECT**](wm-getobject.md) message to retrieve the accessible object.</span></span>
-   <span data-ttu-id="e2d30-113">En réponse à la fonction « [**WM \_ GETOBJECT**](wm-getobject.md)», l’application serveur retourne la valeur zéro ou retourne une valeur qui agit comme une référence unique à l’objet qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-113">In response to [**WM\_GETOBJECT**](wm-getobject.md), the server application either returns zero or returns a value that acts as a one-time reference to the object that generated the event.</span></span>
-   <span data-ttu-id="e2d30-114">Si le serveur retourne la valeur zéro, Microsoft Active Accessibility crée un objet proxy et lui donne son adresse au client.</span><span class="sxs-lookup"><span data-stu-id="e2d30-114">If the server returns zero, Microsoft Active Accessibility creates a proxy object and gives its address to the client.</span></span> <span data-ttu-id="e2d30-115">Dans le cas contraire, Microsoft Active Accessibility utilise cette référence pour récupérer l’adresse d’une interface d’objet telle que [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou [**IDispatch**](idispatch-interface.md)et donne cette adresse au client.</span><span class="sxs-lookup"><span data-stu-id="e2d30-115">Otherwise, Microsoft Active Accessibility uses this reference to retrieve the address of an object interface such as [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or [**IDispatch**](idispatch-interface.md), and gives that address to the client.</span></span>

<span data-ttu-id="e2d30-116">Une fois que le client dispose d’une adresse d’interface, il peut appeler les propriétés et méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet accessible pour récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="e2d30-116">Once the client has an interface address, it can call the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of the accessible object to retrieve information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e2d30-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e2d30-117">In this section</span></span>

-   [<span data-ttu-id="e2d30-118">WinEvents et Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="e2d30-118">WinEvents and Active Accessibility</span></span>](winevents-overview.md)
-   [<span data-ttu-id="e2d30-119">Fonctionnement de la fonction GETOBJECT de WM \_</span><span class="sxs-lookup"><span data-stu-id="e2d30-119">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
-   [<span data-ttu-id="e2d30-120">Récupération d’un objet IAccessible</span><span class="sxs-lookup"><span data-stu-id="e2d30-120">Retrieving an IAccessible Object</span></span>](retrieving-an-iaccessible-object.md)

 

 




