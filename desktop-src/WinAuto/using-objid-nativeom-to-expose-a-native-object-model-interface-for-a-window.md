---
title: Utiliser OBJID \_ NATIVEOM pour exposer une interface native pour une fenêtre
description: Cette technique permet aux clients d’obtenir un objet personnalisé pour une fenêtre. Les serveurs peuvent l’utiliser pour exposer un pointeur vers un objet de document personnalisé pour une fenêtre.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104381104"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a><span data-ttu-id="d1a71-104">Utiliser OBJID \_ NATIVEOM pour exposer une interface native pour une fenêtre</span><span class="sxs-lookup"><span data-stu-id="d1a71-104">Use OBJID\_NATIVEOM to expose a native interface for a window</span></span>

<span data-ttu-id="d1a71-105">Cette technique permet aux clients d’obtenir un objet personnalisé pour une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d1a71-105">This technique allows clients to get a custom object for a window.</span></span> <span data-ttu-id="d1a71-106">Les serveurs peuvent l’utiliser pour exposer un pointeur vers un objet de document personnalisé pour une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d1a71-106">Servers can use this to expose a pointer to a custom document object for a window.</span></span>

<span data-ttu-id="d1a71-107">**Pour exposer une interface de modèle objet natif pour une fenêtre (serveurs)**</span><span class="sxs-lookup"><span data-stu-id="d1a71-107">**To expose a native object model interface for a window (servers)**</span></span>

1.  <span data-ttu-id="d1a71-108">Gérez le message [**WM \_ GETOBJECT**](wm-getobject.md) dans la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d1a71-108">Handle the [**WM\_GETOBJECT**](wm-getobject.md) message in the window procedure.</span></span> <span data-ttu-id="d1a71-109">Lorsque la valeur *lParam* est [**objID \_ NATIVEOM**](object-identifiers.md), retourne un pointeur d’interface vers l’objet personnalisé à l’aide de [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="d1a71-109">When the *lParam* value is [**OBJID\_NATIVEOM**](object-identifiers.md), return an interface pointer to the custom object using [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span>
2.  <span data-ttu-id="d1a71-110">Libérez votre pointeur d’interface après l’appel de [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d1a71-110">Release your interface pointer after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), if appropriate.</span></span> <span data-ttu-id="d1a71-111">Pour plus d’informations, consultez **LresultFromObject**.</span><span class="sxs-lookup"><span data-stu-id="d1a71-111">For more information, see **LresultFromObject**.</span></span>

<span data-ttu-id="d1a71-112">Les clients peuvent obtenir un pointeur vers cet objet personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d1a71-112">Clients can obtain a pointer to this custom object.</span></span>

<span data-ttu-id="d1a71-113">**Pour obtenir un pointeur pour un objet personnalisé pour une fenêtre (clients)**</span><span class="sxs-lookup"><span data-stu-id="d1a71-113">**To obtain a pointer for a custom object for a window (clients)**</span></span>

-   <span data-ttu-id="d1a71-114">Appelez [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) et transmettez [**objID \_ NATIVEOM**](object-identifiers.md) en tant que second paramètre.</span><span class="sxs-lookup"><span data-stu-id="d1a71-114">Call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and pass [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

<span data-ttu-id="d1a71-115">Notez les points suivants pour cette technique :</span><span class="sxs-lookup"><span data-stu-id="d1a71-115">Note the following issues for this technique:</span></span>

-   <span data-ttu-id="d1a71-116">Cette technique est similaire au retour d’un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , à l’exception de l’ID d’objet utilisé et du fait que [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) retourne un objet personnalisé au lieu de **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="d1a71-116">This technique is similar to returning an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer except for the object ID used and the fact that [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) returns a custom object instead of **IAccessible**.</span></span>
-   <span data-ttu-id="d1a71-117">Les développeurs de serveurs peuvent avoir besoin de publier des informations qui permettent aux clients d’identifier le **HWND** de manière unique afin qu’il puisse le trouver avant d’appeler [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) sur son handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d1a71-117">Server developers may need to publish information that allows clients to uniquely identify the **HWND** so that they can find it before calling [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) on its window handle.</span></span>
-   <span data-ttu-id="d1a71-118">N’implémentez pas l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sur l’objet personnalisé qui est retourné.</span><span class="sxs-lookup"><span data-stu-id="d1a71-118">Do not implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the custom object that is returned.</span></span> <span data-ttu-id="d1a71-119">Dans ce cas, OLEACC le traite comme un **IAccessible** standard et peut empêcher l’utilisation des interfaces personnalisées.</span><span class="sxs-lookup"><span data-stu-id="d1a71-119">If you do, OLEACC will treat it is as a standard **IAccessible** and may prevent the custom interfaces from being used.</span></span>
-   <span data-ttu-id="d1a71-120">Pour pouvoir être utilisé dans plusieurs processus, les interfaces sur l’objet retourné peuvent avoir besoin d’être inscrites auprès du modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="d1a71-120">In order to be used across processes, the interfaces on the returned object may need to be registered with Component Object Model (COM).</span></span>

<span data-ttu-id="d1a71-121">Cette technique est prise en charge par plusieurs composants de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d1a71-121">This technique is supported by several Microsoft Office components.</span></span> <span data-ttu-id="d1a71-122">Pour plus d’informations, consultez [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="d1a71-122">For more information, see [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

 

 




