---
description: Demande d’intersections et de primitives de l’historique des pixels séparément.
MS-HAID: vspixengine.IPixelHistoryRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixelHistoryRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B62A9EBA-4497-4825-A2F1-285A4AD45012
api_name:
- IPixelHistoryRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e789829d85f4cb986de694470a8cebddf3f26675
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317818"
---
# <a name="span-idvspixengineipixelhistoryrequest2spanipixelhistoryrequest2-interface"></a><span data-ttu-id="5a1d0-103"><span id="vspixengine.ipixelhistoryrequest2"></span>Interface IPixelHistoryRequest2</span><span class="sxs-lookup"><span data-stu-id="5a1d0-103"><span id="vspixengine.ipixelhistoryrequest2"></span>IPixelHistoryRequest2 interface</span></span>

<span data-ttu-id="5a1d0-104">Demande d’intersections et de primitives de l’historique des pixels séparément.</span><span class="sxs-lookup"><span data-stu-id="5a1d0-104">Request for pixel history intersections and primitives separately.</span></span>

## <a name="members"></a><span data-ttu-id="5a1d0-105">Membres</span><span class="sxs-lookup"><span data-stu-id="5a1d0-105">Members</span></span>

<span data-ttu-id="5a1d0-106">L’interface **IPixelHistoryRequest2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5a1d0-106">The **IPixelHistoryRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5a1d0-107">**IPixelHistoryRequest2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5a1d0-107">**IPixelHistoryRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="5a1d0-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a1d0-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="5a1d0-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a1d0-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="5a1d0-110">L’interface **IPixelHistoryRequest2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5a1d0-110">The **IPixelHistoryRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="5a1d0-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="5a1d0-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="5a1d0-112">Description</span><span class="sxs-lookup"><span data-stu-id="5a1d0-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="5a1d0-113"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a1d0-113"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestintersections-dword-point2d-dword-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestIntersections</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5a1d0-114">Demande une liste d’événements qui provoquent une modification dans le pixel spécifié, le rendu cible/UAV et le frame.</span><span class="sxs-lookup"><span data-stu-id="5a1d0-114">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="5a1d0-115"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a1d0-115"><a href="/windows/desktop/direct3dtools/ipixelhistoryrequest2-requestprimitives-pixelhistoryintersection-ptr-ipixelhistorycallback2-ptr-dword-dword"><strong>RequestPrimitives</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5a1d0-116">Demande une liste de primitives à partir d’une intersection particulière.</span><span class="sxs-lookup"><span data-stu-id="5a1d0-116">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="5a1d0-117">Pour plus d’informations, consultez la fonction membre RequestIntersections.</span><span class="sxs-lookup"><span data-stu-id="5a1d0-117">For more information, see the RequestIntersections member function.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="5a1d0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a1d0-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5a1d0-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a1d0-119">Header</span></span></p></td><td><span data-ttu-id="5a1d0-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5a1d0-120">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
