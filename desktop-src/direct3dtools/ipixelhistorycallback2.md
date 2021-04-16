---
description: Rappel pour retourner les intersections de l’historique des pixels (dessiner le niveau d’appel) et les primitives (niveau de triangle) dans deux résultats différents.
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixelHistoryCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 473f3540ad9c6a16659a6e43c3aa31eef706ec59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521559"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span data-ttu-id="17f08-103"><span id="vspixengine.ipixelhistorycallback2"></span>Interface IPixelHistoryCallback2</span><span class="sxs-lookup"><span data-stu-id="17f08-103"><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2 interface</span></span>

<span data-ttu-id="17f08-104">Rappel pour retourner les intersections de l’historique des pixels (dessiner le niveau d’appel) et les primitives (niveau de triangle) dans deux résultats différents.</span><span class="sxs-lookup"><span data-stu-id="17f08-104">Callback to return pixel history intersections (draw call level) and primitives (triangle level) in two different results.</span></span>

## <a name="members"></a><span data-ttu-id="17f08-105">Membres</span><span class="sxs-lookup"><span data-stu-id="17f08-105">Members</span></span>

<span data-ttu-id="17f08-106">L’interface **IPixelHistoryCallback2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="17f08-106">The **IPixelHistoryCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="17f08-107">**IPixelHistoryCallback2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="17f08-107">**IPixelHistoryCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="17f08-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17f08-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="17f08-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="17f08-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="17f08-110">L’interface **IPixelHistoryCallback2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="17f08-110">The **IPixelHistoryCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="17f08-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="17f08-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="17f08-112">Description</span><span class="sxs-lookup"><span data-stu-id="17f08-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="17f08-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="17f08-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17f08-114">Rappel qui avertit l’hôte des informations d’intersection de l’historique des pixels retournées par la requête dans.</span><span class="sxs-lookup"><span data-stu-id="17f08-114">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="17f08-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="17f08-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="17f08-116">Rappel qui avertit l’hôte des informations d’opération primitives de l’historique des pixels retournées par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="17f08-116">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="17f08-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17f08-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="17f08-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="17f08-118">Header</span></span></p></td><td><span data-ttu-id="17f08-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="17f08-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
