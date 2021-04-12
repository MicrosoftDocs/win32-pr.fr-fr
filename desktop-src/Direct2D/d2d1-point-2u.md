---
title: D2D1_POINT_2U (D2DBaseTypes. h)
description: Représente une paire de coordonnées x et y dans l’espace à deux dimensions. | D2D1_POINT_2U (D2DBaseTypes. h)
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211488"
---
# <a name="d2d1_point_2u"></a><span data-ttu-id="af029-105">\_Point d2d1 \_ 2U</span><span class="sxs-lookup"><span data-stu-id="af029-105">D2D1\_POINT\_2U</span></span>

<span data-ttu-id="af029-106">Représente une paire de coordonnées x et y dans l’espace à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="af029-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a><span data-ttu-id="af029-107">Notes</span><span class="sxs-lookup"><span data-stu-id="af029-107">Remarks</span></span>

<span data-ttu-id="af029-108">Les points dans Direct2D sont représentés par les structures [**d2d1 \_ point \_ 2F**](d2d1-point-2f.md) ou **d2d1 \_ point \_ 2U** .</span><span class="sxs-lookup"><span data-stu-id="af029-108">Points in Direct2D are represented by the [**D2D1\_POINT\_2F**](d2d1-point-2f.md) or **D2D1\_POINT\_2U** structures.</span></span> <span data-ttu-id="af029-109">Tous deux contiennent une paire de coordonnées x et y dans l’espace à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="af029-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="af029-110">La **structure \_ d2d1 point \_ 2F** stocke les coordonnées en tant que valeurs **float** , et la structure de **point d2d1 \_ \_ 2U** les stocke en tant que valeurs **UInt32** .</span><span class="sxs-lookup"><span data-stu-id="af029-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="af029-111">**D2d1 \_ POINT \_ 2U** est un nouveau nom pour le type déjà défini au format [**D2D \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span><span class="sxs-lookup"><span data-stu-id="af029-111">**D2D1\_POINT\_2U** is a new name for the already defined type [**D2D\_POINT\_2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span></span>

## <a name="requirements"></a><span data-ttu-id="af029-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af029-112">Requirements</span></span>



| <span data-ttu-id="af029-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af029-113">Requirement</span></span> | <span data-ttu-id="af029-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="af029-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af029-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af029-115">Minimum supported client</span></span><br/> | <span data-ttu-id="af029-116">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="af029-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="af029-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af029-117">Minimum supported server</span></span><br/> | <span data-ttu-id="af029-118">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="af029-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="af029-119">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af029-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="af029-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="af029-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="af029-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="af029-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="af029-122"><dt>D2DBaseTypes. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af029-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="af029-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af029-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af029-124">**\_Point D2D \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="af029-124">**D2D\_POINT\_2U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[<span data-ttu-id="af029-125">**\_Point D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="af029-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





