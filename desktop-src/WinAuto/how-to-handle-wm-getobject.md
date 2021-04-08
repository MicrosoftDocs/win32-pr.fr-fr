---
title: Comment gérer les WM_GETOBJECT
description: Lorsqu’il reçoit un message WM de \_ la fonction GETOBJECT qui contient \_ le client objid, le serveur doit retourner un pointeur vers l’objet qui implémente IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674010"
---
# <a name="how-to-handle-wm_getobject"></a><span data-ttu-id="52df4-103">Comment gérer WM \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="52df4-103">How to Handle WM\_GETOBJECT</span></span>

<span data-ttu-id="52df4-104">Lorsqu’il reçoit un message WM de la fonction [**\_ GETOBJECT**](wm-getobject.md) qui contient le [**\_ client objid**](object-identifiers.md), le serveur doit retourner un pointeur vers l’objet qui implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="52df4-104">When it receives a [**WM\_GETOBJECT**](wm-getobject.md) message that contains [**OBJID\_CLIENT**](object-identifiers.md), the server must return a pointer to the object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="52df4-105">Ce pointeur est un LRESULT obtenu en appelant [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="52df4-105">This pointer is an LRESULT that is obtained by calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span> <span data-ttu-id="52df4-106">Microsoft Active Accessibility, conjointement avec la bibliothèque COM (Component Object Model), effectue le marshaling approprié et passe le pointeur d’interface **IAccessible** du serveur au client.</span><span class="sxs-lookup"><span data-stu-id="52df4-106">Microsoft Active Accessibility, in conjunction with the Component Object Model (COM) library, performs the appropriate marshaling and passes the **IAccessible** interface pointer from the server to the client.</span></span>

<span data-ttu-id="52df4-107">Les serveurs doivent gérer correctement le décompte de références sur l’objet accessible.</span><span class="sxs-lookup"><span data-stu-id="52df4-107">Servers must correctly handle reference counting on the accessible object.</span></span> <span data-ttu-id="52df4-108">N’oubliez pas que lorsque vous créez un objet COM, le nombre de références est 1.</span><span class="sxs-lookup"><span data-stu-id="52df4-108">Remember that when you create a COM object, the reference count is 1.</span></span> <span data-ttu-id="52df4-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrémente ensuite le nombre de références plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="52df4-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) then further increments the reference count several times.</span></span> <span data-ttu-id="52df4-110">Toutes les références créées par **LresultFromObject** sont automatiquement libérées quand l’objet n’est plus nécessaire, mais que le serveur est responsable de la libération de la référence initiale et, à moins qu’elle le fasse, l’objet ne sera jamais détruit.</span><span class="sxs-lookup"><span data-stu-id="52df4-110">All the references created by **LresultFromObject** are automatically released when the object is no longer needed, but the server is responsible for releasing the initial reference, and unless it does so, the object will never be destroyed.</span></span> <span data-ttu-id="52df4-111">Les exemples des sections suivantes montrent comment libérer des références aux objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="52df4-111">The examples in the following sections show how to release references to accessible objects.</span></span>

<span data-ttu-id="52df4-112">En général, les serveurs gèrent [**WM \_ GETOBJECT**](wm-getobject.md) de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="52df4-112">Servers typically handle [**WM\_GETOBJECT**](wm-getobject.md) in one of the following ways:</span></span>

-   [<span data-ttu-id="52df4-113">Créer des objets accessibles</span><span class="sxs-lookup"><span data-stu-id="52df4-113">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="52df4-114">Réutiliser des pointeurs existants vers des objets</span><span class="sxs-lookup"><span data-stu-id="52df4-114">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="52df4-115">Créer des interfaces vers le même objet</span><span class="sxs-lookup"><span data-stu-id="52df4-115">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> <span data-ttu-id="52df4-116">Dans cette section, comme dans le reste de la documentation, lorsqu’un pointeur vers une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est abordé, ce pointeur peut en fait être un pointeur vers un objet proxy qui encapsule l’interface **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="52df4-116">In this section as in the rest of the documentation, when a pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is discussed, this pointer may actually be a pointer to a proxy object that wraps the **IAccessible** interface.</span></span> <span data-ttu-id="52df4-117">Pour plus d’informations sur les objets proxy, consultez [création d’objets proxy](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="52df4-117">For more information about proxy objects, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

 

<span data-ttu-id="52df4-118">Pour obtenir une vue d’ensemble de [**WM \_ GetObject**](wm-getobject.md), consultez fonctionnement de [WM \_ GetObject](how-wm-getobject-works.md).</span><span class="sxs-lookup"><span data-stu-id="52df4-118">For an overview of [**WM\_GETOBJECT**](wm-getobject.md), see [How WM\_GETOBJECT Works](how-wm-getobject-works.md).</span></span>

 

 




