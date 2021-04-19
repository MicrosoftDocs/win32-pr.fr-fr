---
title: D2D1_POINT_2F (D2DBaseTypes. h)
description: Représente une paire de coordonnées x et y dans l’espace à deux dimensions. | D2D1_POINT_2F (D2DBaseTypes. h)
ms.assetid: b317ae75-d738-4e1a-bcd1-adf3e95b197e
keywords:
- D2D1_POINT_2F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f93bf4a0d1a1b3f988f1c6d168388e9910080dcb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535775"
---
# <a name="d2d1_point_2f"></a><span data-ttu-id="0a77b-105">D2D1 \_ point \_ 2F</span><span class="sxs-lookup"><span data-stu-id="0a77b-105">D2D1\_POINT\_2F</span></span>

<span data-ttu-id="0a77b-106">Représente une paire de coordonnées x et y dans l’espace à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="0a77b-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2F D2D1_POINT_2F;
```



## <a name="remarks"></a><span data-ttu-id="0a77b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0a77b-107">Remarks</span></span>

<span data-ttu-id="0a77b-108">Les points dans Direct2D sont représentés par les structures **d2d1 \_ point \_ 2F** ou [**d2d1 \_ point \_ 2U**](d2d1-point-2u.md) .</span><span class="sxs-lookup"><span data-stu-id="0a77b-108">Points in Direct2D are represented by the **D2D1\_POINT\_2F** or [**D2D1\_POINT\_2U**](d2d1-point-2u.md) structures.</span></span> <span data-ttu-id="0a77b-109">Tous deux contiennent une paire de coordonnées x et y dans l’espace à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="0a77b-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="0a77b-110">La **structure \_ d2d1 point \_ 2F** stocke les coordonnées en tant que valeurs **float** , et la structure de **point d2d1 \_ \_ 2U** les stocke en tant que valeurs **UInt32** .</span><span class="sxs-lookup"><span data-stu-id="0a77b-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="0a77b-111">**D2d1 \_ Le POINT \_ 2F** est un nouveau nom pour le type déjà défini du [**\_ point D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span><span class="sxs-lookup"><span data-stu-id="0a77b-111">**D2D1\_POINT\_2F** is a new name for the already defined type [**D2D\_POINT\_2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a77b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a77b-112">Requirements</span></span>



| <span data-ttu-id="0a77b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a77b-113">Requirement</span></span> | <span data-ttu-id="0a77b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a77b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a77b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a77b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0a77b-116">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0a77b-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="0a77b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a77b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0a77b-118">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0a77b-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="0a77b-119">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a77b-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="0a77b-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="0a77b-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="0a77b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a77b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a77b-122"><dt>D2DBaseTypes. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a77b-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0a77b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a77b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a77b-124">**\_Point d2d1 \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="0a77b-124">**D2D1\_POINT\_2U**</span></span>](/windows/desktop/Direct2D/d2d1-point-2u)
</dt> <dt>

[<span data-ttu-id="0a77b-125">**\_Point D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="0a77b-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

