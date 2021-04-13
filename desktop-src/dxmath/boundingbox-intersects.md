---
description: Teste BoundingBox pour l’intersection avec un autre objet.
ms.assetid: df3d3df9-aa74-413d-808c-f7b276d11279
title: BoundingBox. croisements, méthodes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9039d99640ae3989d0b20e9d48f681edabb021f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528114"
---
# <a name="boundingboxintersects-methods"></a><span data-ttu-id="f63b9-103">BoundingBox. croisements, méthodes</span><span class="sxs-lookup"><span data-stu-id="f63b9-103">BoundingBox.Intersects methods</span></span>

<span data-ttu-id="f63b9-104">Teste BoundingBox pour l’intersection avec un autre objet.</span><span class="sxs-lookup"><span data-stu-id="f63b9-104">Tests the BoundingBox for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f63b9-105">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="f63b9-105">Overload list</span></span>



| <span data-ttu-id="f63b9-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="f63b9-106">Method</span></span>                                                                                   | <span data-ttu-id="f63b9-107">Description</span><span class="sxs-lookup"><span data-stu-id="f63b9-107">Description</span></span>                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f63b9-108">[**BoundingBox :: intersections (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="f63b9-108">[**BoundingBox::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span></span>                   | <span data-ttu-id="f63b9-109">Testez BoundingBox pour l’intersection avec un plan.</span><span class="sxs-lookup"><span data-stu-id="f63b9-109">Test the BoundingBox for intersection with a plane.</span></span><br/>                                                                     |
| <span data-ttu-id="f63b9-110">[**BoundingBox :: croisements (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="f63b9-110">[**BoundingBox::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="f63b9-111">Teste BoundingBox pour l’intersection avec un autre BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="f63b9-111">Tests the BoundingBox for intersection with another BoundingBox.</span></span><br/>                                                        |
| <span data-ttu-id="f63b9-112">[**BoundingBox :: croisements (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f63b9-112">[**BoundingBox::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span></span>      | <span data-ttu-id="f63b9-113">Teste BoundingBox pour l’intersection avec un BoundingSphere.</span><span class="sxs-lookup"><span data-stu-id="f63b9-113">Tests the BoundingBox for intersection with a BoundingSphere.</span></span><br/>                                                           |
| <span data-ttu-id="f63b9-114">[**BoundingBox :: croisements (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="f63b9-114">[**BoundingBox::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="f63b9-115">Testez [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) pour l’intersection avec un [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span><span class="sxs-lookup"><span data-stu-id="f63b9-115">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="f63b9-116">[**BoundingBox :: intersections (XMVECTOR, XMVECTOR, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="f63b9-116">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="f63b9-117">Testez BoundingBox pour l’intersection avec un rayon.</span><span class="sxs-lookup"><span data-stu-id="f63b9-117">Test the BoundingBox for intersection with a ray.</span></span><br/>                                                                       |
| <span data-ttu-id="f63b9-118">[**BoundingBox :: intersections (XMVECTOR, XMVECTOR, XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="f63b9-118">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="f63b9-119">Testez BoundingBox pour l’intersection avec un triangle.</span><span class="sxs-lookup"><span data-stu-id="f63b9-119">Test the BoundingBox for intersection with a triangle.</span></span><br/>                                                                  |
| <span data-ttu-id="f63b9-120">[**BoundingBox :: croisements (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="f63b9-120">[**BoundingBox::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="f63b9-121">Testez [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) pour l’intersection avec un [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span><span class="sxs-lookup"><span data-stu-id="f63b9-121">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f63b9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f63b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63b9-123">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f63b9-123">Methods</span></span>](boundingbox-methods.md)
</dt> <dt>

<span data-ttu-id="f63b9-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f63b9-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f63b9-125">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="f63b9-125">**BoundingBox**</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
