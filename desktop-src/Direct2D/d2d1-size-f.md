---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Stocke une paire ordonnée de nombres à virgule flottante, en général la largeur et la hauteur d’un rectangle.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464742"
---
# <a name="d2d1_size_f"></a><span data-ttu-id="2d9c2-104">D2D1 \_ taille \_ F</span><span class="sxs-lookup"><span data-stu-id="2d9c2-104">D2D1\_SIZE\_F</span></span>

<span data-ttu-id="2d9c2-105">Stocke une paire ordonnée de nombres à virgule flottante, en général la largeur et la hauteur d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="2d9c2-105">Stores an ordered pair of floats, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a><span data-ttu-id="2d9c2-106">Notes</span><span class="sxs-lookup"><span data-stu-id="2d9c2-106">Remarks</span></span>

<span data-ttu-id="2d9c2-107">Comme les points, les tailles sont un autre concept graphique important.</span><span class="sxs-lookup"><span data-stu-id="2d9c2-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="2d9c2-108">Dans Direct2D, les tailles sont représentées par les structures **d2d1 \_ size \_ F** ou [**d2d1 \_ size \_ U**](d2d1-size-u.md) .</span><span class="sxs-lookup"><span data-stu-id="2d9c2-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_F** or [**D2D1\_SIZE\_U**](d2d1-size-u.md) structures.</span></span> <span data-ttu-id="2d9c2-109">Tous deux contiennent une paire ordonnée de nombres, en général la largeur et la hauteur d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="2d9c2-109">Both contain an ordered pair of numbers, typically the width and height of a rectangle.</span></span> <span data-ttu-id="2d9c2-110">La **structure d2d1 \_ size \_ F** contient une paire ordonnée de valeurs **float** et la structure **d2d1 \_ size \_ U** contient une paire ordonnée de valeurs **UInt32** .</span><span class="sxs-lookup"><span data-stu-id="2d9c2-110">The **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values, and the **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values.</span></span>

<span data-ttu-id="2d9c2-111">**D2d1 \_ La taille \_ f** est un nouveau nom pour un type déjà défini ( **\_ taille D2D \_**).</span><span class="sxs-lookup"><span data-stu-id="2d9c2-111">**D2D1\_SIZE\_F** is a new name for an already defined type **D2D\_SIZE\_F**.</span></span> <span data-ttu-id="2d9c2-112">Pour obtenir la liste des champs fournis par **d2d1 \_ size \_ f**, consultez **D2D \_ size \_ f**.</span><span class="sxs-lookup"><span data-stu-id="2d9c2-112">For a list of the fields provided by **D2D1\_SIZE\_F**, see **D2D\_SIZE\_F**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d9c2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d9c2-113">Requirements</span></span>



| <span data-ttu-id="2d9c2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d9c2-114">Requirement</span></span> | <span data-ttu-id="2d9c2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d9c2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d9c2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d9c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2d9c2-117">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2d9c2-117">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2d9c2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d9c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2d9c2-119">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2d9c2-119">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2d9c2-120">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d9c2-120">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2d9c2-121">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="2d9c2-121">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="2d9c2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d9c2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d9c2-123"><dt>D2DBaseTypes. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d9c2-123"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2d9c2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d9c2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9c2-125">**\_Taille ( \_ F) D2D**</span><span class="sxs-lookup"><span data-stu-id="2d9c2-125">**D2D\_SIZE\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[<span data-ttu-id="2d9c2-126">**Taille de D2D1 \_ \_ U**</span><span class="sxs-lookup"><span data-stu-id="2d9c2-126">**D2D1\_SIZE\_U**</span></span>](d2d1-size-u.md)
</dt> <dt>

[<span data-ttu-id="2d9c2-127">**D2D1 \_ point \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="2d9c2-127">**D2D1\_POINT\_2F**</span></span>](d2d1-point-2f.md)
</dt> </dl>

 

