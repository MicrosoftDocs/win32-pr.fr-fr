---
title: Méthodes ID2D1RenderTarget CreateBitmap
description: Crée une bitmap Direct2D.
ms.assetid: b45d353f-ae33-4110-b7c8-f14661017e0f
keywords:
- Méthodes CreateBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4576b9111d9180b395527bad8b06ee3f9a8eef2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522813"
---
# <a name="id2d1rendertargetcreatebitmap-methods"></a><span data-ttu-id="7345c-104">ID2D1RenderTarget :: CreateBitmap, méthodes</span><span class="sxs-lookup"><span data-stu-id="7345c-104">ID2D1RenderTarget::CreateBitmap methods</span></span>

<span data-ttu-id="7345c-105">Crée une bitmap Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7345c-105">Creates a Direct2D bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7345c-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="7345c-106">Overload list</span></span>



| <span data-ttu-id="7345c-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="7345c-107">Method</span></span>                                                                                                                                                                                                   | <span data-ttu-id="7345c-108">Description</span><span class="sxs-lookup"><span data-stu-id="7345c-108">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="7345c-109">[**CreateBitmap (D2D1 \_ taille \_ U, d2d1 \_ \_ Propriétés bitmap&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="7345c-109">[**CreateBitmap(D2D1\_SIZE\_U,D2D1\_BITMAP\_PROPERTIES&,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span></span>                                | <span data-ttu-id="7345c-110">Crée une bitmap Direct2D non initialisée.</span><span class="sxs-lookup"><span data-stu-id="7345c-110">Creates an uninitialized Direct2D bitmap.</span></span> <br/>                          |
| <span data-ttu-id="7345c-111">[**CreateBitmap (D2D1 \_ taille \_ U, void \* , UInt32, d2d1 \_ \_ Propriétés bitmap \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="7345c-111">[**CreateBitmap(D2D1\_SIZE\_U,void\*,UINT32,D2D1\_BITMAP\_PROPERTIES\*,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span></span> | <span data-ttu-id="7345c-112">Crée une bitmap Direct2D à partir d’un pointeur vers des données sources en mémoire.</span><span class="sxs-lookup"><span data-stu-id="7345c-112">Creates a Direct2D bitmap from a pointer to in-memory source data.</span></span><br/>  |
| <span data-ttu-id="7345c-113">[**CreateBitmap (D2D1 \_ taille \_ U, void \* , UInt32, D2D1 \_ \_ Propriétés bitmap&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="7345c-113">[**CreateBitmap(D2D1\_SIZE\_U,void\*,UINT32,D2D1\_BITMAP\_PROPERTIES&,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties__id2d1bitmap))</span></span>  | <span data-ttu-id="7345c-114">Crée une bitmap Direct2D à partir d’un pointeur vers des données sources en mémoire.</span><span class="sxs-lookup"><span data-stu-id="7345c-114">Creates a Direct2D bitmap from a pointer to in-memory source data.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="7345c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7345c-115">Requirements</span></span>



| <span data-ttu-id="7345c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7345c-116">Requirement</span></span> | <span data-ttu-id="7345c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7345c-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7345c-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7345c-118">Library</span></span><br/> | <dl> <span data-ttu-id="7345c-119"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7345c-119"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="7345c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7345c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="7345c-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7345c-121"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7345c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7345c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7345c-123">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="7345c-123">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

