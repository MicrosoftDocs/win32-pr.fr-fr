---
title: Récupération d’un objet IAccessible
description: Microsoft Active Accessibility fournit des fonctions telles que AccessibleObjectFromWindow et AccessibleObjectFromPoint qui permettent aux clients de récupérer des objets accessibles.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309437"
---
# <a name="retrieving-an-iaccessible-object"></a><span data-ttu-id="ee747-103">Récupération d’un objet IAccessible</span><span class="sxs-lookup"><span data-stu-id="ee747-103">Retrieving an IAccessible Object</span></span>

<span data-ttu-id="ee747-104">Microsoft Active Accessibility fournit des fonctions telles que [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) et [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) qui permettent aux clients de récupérer des objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="ee747-104">Microsoft Active Accessibility provides functions such as [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) that allow clients to retrieve accessible objects.</span></span> <span data-ttu-id="ee747-105">Ces fonctions retournent un pointeur d’interface [**IDispatch**](idispatch-interface.md) ou [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) par le biais duquel les clients obtiennent des informations sur l’objet accessible.</span><span class="sxs-lookup"><span data-stu-id="ee747-105">These functions return either an [**IDispatch**](idispatch-interface.md) or [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer through which clients get information about the accessible object.</span></span>

<span data-ttu-id="ee747-106">Lorsqu’un client appelle [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou l’une des autres fonctions \**AccessibleObjectFrom \* \* \* X* qui récupèrent une interface vers un objet, Microsoft Active Accessibility envoie le message de fenêtre [**WM \_ GETOBJECT**](wm-getobject.md) à la procédure de fenêtre applicable au sein de l’application appropriée.</span><span class="sxs-lookup"><span data-stu-id="ee747-106">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other \**AccessibleObjectFrom\*\*\*X* functions that retrieve an interface to an object, Microsoft Active Accessibility sends the [**WM\_GETOBJECT**](wm-getobject.md) window message to the applicable window procedure within the appropriate application.</span></span> <span data-ttu-id="ee747-107">Pour fournir des informations aux clients, les serveurs doivent répondre au message **WM de \_ GETOBJECT** .</span><span class="sxs-lookup"><span data-stu-id="ee747-107">To provide information to clients, servers must respond to the **WM\_GETOBJECT** message.</span></span>

<span data-ttu-id="ee747-108">Pour collecter des informations spécifiques sur un élément d’interface utilisateur, les clients doivent d’abord récupérer une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="ee747-108">To collect specific information about a UI element, clients must first retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="ee747-109">Pour récupérer un objet **IAccessible** d’un élément, les clients peuvent utiliser l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee747-109">To retrieve an element's **IAccessible** object, clients can use one of the following functions:</span></span>

-   [<span data-ttu-id="ee747-110">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="ee747-110">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="ee747-111">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="ee747-111">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="ee747-112">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="ee747-112">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

<span data-ttu-id="ee747-113">**Pour récupérer un pointeur d’interface IAccessible**</span><span class="sxs-lookup"><span data-stu-id="ee747-113">**To retrieve an IAccessible Interface Pointer**</span></span>

1.  <span data-ttu-id="ee747-114">Le client appelle l’une des fonctions \*\*AccessibleObjectFrom \*\* \* \* X.</span><span class="sxs-lookup"><span data-stu-id="ee747-114">Client calls one of the \**AccessibleObjectFrom\*\*\*X* functions.</span></span>
2.  <span data-ttu-id="ee747-115">Oleacc.dll envoie un message WM de la fonction [**\_ GETOBJECT**](wm-getobject.md) au serveur.</span><span class="sxs-lookup"><span data-stu-id="ee747-115">Oleacc.dll sends a [**WM\_GETOBJECT**](wm-getobject.md) message to server.</span></span>
3.  <span data-ttu-id="ee747-116">Le serveur détermine l’élément d’interface utilisateur qui correspond à la demande.</span><span class="sxs-lookup"><span data-stu-id="ee747-116">The server determines which UI element corresponds to the request.</span></span>
4.  <span data-ttu-id="ee747-117">Le serveur retourne la valeur zéro pour demander un proxy Oleacc.dll,</span><span class="sxs-lookup"><span data-stu-id="ee747-117">The server either returns zero to request an Oleacc.dll proxy,</span></span>

    <span data-ttu-id="ee747-118">ou</span><span class="sxs-lookup"><span data-stu-id="ee747-118">Or</span></span>

    <span data-ttu-id="ee747-119">Retourne un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implémentation native).</span><span class="sxs-lookup"><span data-stu-id="ee747-119">Returns an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object (native implementation).</span></span> <span data-ttu-id="ee747-120">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee747-120">To do this, it:</span></span>

    -   <span data-ttu-id="ee747-121">Construit un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="ee747-121">Constructs an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the element.</span></span>
    -   <span data-ttu-id="ee747-122">Appelle [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) pour marshaler le pointeur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee747-122">Calls [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) to marshal the object's pointer.</span></span>
    -   <span data-ttu-id="ee747-123">Retourne la LRESULT à Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="ee747-123">Returns the LRESULT to Oleacc.dll.</span></span>

5.  <span data-ttu-id="ee747-124">Oleacc.dll examine la valeur renvoyée par [**WM \_ GETOBJECT**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="ee747-124">Oleacc.dll examines the return value from [**WM\_GETOBJECT**](wm-getobject.md).</span></span>

    <span data-ttu-id="ee747-125">Si la valeur est égale à zéro, Oleacc.dll construit un objet proxy et le retourne au client.</span><span class="sxs-lookup"><span data-stu-id="ee747-125">If it is zero, Oleacc.dll constructs a proxy object and returns it to the client.</span></span>

    <span data-ttu-id="ee747-126">ou</span><span class="sxs-lookup"><span data-stu-id="ee747-126">Or</span></span>

    <span data-ttu-id="ee747-127">Si la valeur est différente de zéro, Oleacc.dll appelle [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) pour démarshaler le pointeur d’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) natif et le retourne au client.</span><span class="sxs-lookup"><span data-stu-id="ee747-127">If it is nonzero, Oleacc.dll calls [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) to unmarshal the native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object pointer and returns it to the client.</span></span>

 

 




