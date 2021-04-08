---
title: Méthodes ID2D1DeviceContext CreateBitmap
description: Crée une image bitmap qui peut être utilisée comme surface cible, pour la lecture de l’UC ou comme source pour les API DrawBitmap et ID2D1BitmapBrush. En outre, les informations de contexte de couleur peuvent être passées à la bitmap.
ms.assetid: D1896DEE-4464-48D7-8EFB-18E564E1F88D
keywords:
- Méthodes CreateBitmap Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 6086aeef2ee36da9bd3b917ffdae07f3eb6312bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727844"
---
# <a name="id2d1devicecontextcreatebitmap-methods"></a><span data-ttu-id="b90c3-105">ID2D1DeviceContext :: CreateBitmap, méthodes</span><span class="sxs-lookup"><span data-stu-id="b90c3-105">ID2D1DeviceContext::CreateBitmap methods</span></span>

<span data-ttu-id="b90c3-106">Crée une image bitmap qui peut être utilisée comme surface cible, pour la lecture de l’UC ou comme source pour les API [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) et [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="b90c3-106">Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) APIs.</span></span> <span data-ttu-id="b90c3-107">En outre, les informations de contexte de couleur peuvent être passées à la bitmap. [**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="b90c3-107">In addition, color context information can be passed to the bitmap.[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))[**CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span>

### <a name="overload-list"></a><span data-ttu-id="b90c3-108">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="b90c3-108">Overload list</span></span>



| <span data-ttu-id="b90c3-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="b90c3-109">Method</span></span>                                                                                                                                 | <span data-ttu-id="b90c3-110">Description</span><span class="sxs-lookup"><span data-stu-id="b90c3-110">Description</span></span>                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b90c3-111">[**CreateBitmap (D2D1 \_ taille \_ U, void \* , UInt32, d2d1 \_ bitmap \_ PROPERTIES1, ID2D1Bitmap1 \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="b90c3-111">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span>  | <span data-ttu-id="b90c3-112">Crée une image bitmap qui peut être utilisée comme surface cible, pour la lecture de l’UC ou comme source pour les API [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) et [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="b90c3-112">Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the [**DrawBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)) and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) APIs.</span></span> <span data-ttu-id="b90c3-113">En outre, les informations de contexte de couleur peuvent être passées à la bitmap.</span><span class="sxs-lookup"><span data-stu-id="b90c3-113">In addition, color context information can be passed to the bitmap.</span></span><br/> |
| <span data-ttu-id="b90c3-114">[**CreateBitmap (D2D1 \_ taille \_ U, void \* , UInt32, d2d1 \_ bitmap \_ PROPERTIES1 \* , ID2D1Bitmap1 \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="b90c3-114">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1\*, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))</span></span> |                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b90c3-115">[**CreateBitmap (D2D1 \_ size \_ U, void \* , UInt32, D2D1 \_ bitmap \_ PROPERTIES1&, ID2D1Bitmap1 \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="b90c3-115">[**CreateBitmap (D2D1\_SIZE\_U, void\*, UINT32, D2D1\_BITMAP\_PROPERTIES1&, ID2D1Bitmap1\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1))</span></span> |                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="b90c3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b90c3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90c3-117">**ID2D1DeviceContext**</span><span class="sxs-lookup"><span data-stu-id="b90c3-117">**ID2D1DeviceContext**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)
</dt> </dl>

 

