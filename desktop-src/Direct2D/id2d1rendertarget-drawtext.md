---
title: Méthodes ID2D1RenderTarget DrawText
description: Dessine le texte spécifié à l’aide des informations de format fournies par un objet IDWriteTextFormat.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Méthodes DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538088"
---
# <a name="id2d1rendertargetdrawtext-methods"></a><span data-ttu-id="6b02b-104">ID2D1RenderTarget ::D méthodes rawText</span><span class="sxs-lookup"><span data-stu-id="6b02b-104">ID2D1RenderTarget::DrawText methods</span></span>

<span data-ttu-id="6b02b-105">Dessine le texte spécifié à l’aide des informations de format fournies par un objet [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="6b02b-105">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6b02b-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="6b02b-106">Overload list</span></span>



| <span data-ttu-id="6b02b-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="6b02b-107">Method</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="6b02b-108">Description</span><span class="sxs-lookup"><span data-stu-id="6b02b-108">Description</span></span>                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b02b-109">[**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ rect \_ F&, ID2D1Brush \* , d2d1 \_ dessiner \_ \_ des options de texte, \_ méthode de mesure du texte DWRITE \_ \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="6b02b-109">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F&,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>  | <span data-ttu-id="6b02b-110">Dessine le texte spécifié à l’aide des informations de format fournies par un objet [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="6b02b-110">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span><br/>  |
| <span data-ttu-id="6b02b-111">[**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ rect \_ F \* , ID2D1Brush \* , d2d1 \_ dessiner \_ \_ des options de texte, \_ méthode de mesure du texte DWRITE \_ \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="6b02b-111">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F\*,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> | <span data-ttu-id="6b02b-112">Dessine le texte spécifié à l’aide des informations de format fournies par un objet [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="6b02b-112">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="6b02b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6b02b-113">Remarks</span></span>

<span data-ttu-id="6b02b-114">Pour dessiner du texte avec Direct2D, utilisez la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) pour le texte qui a un format unique, ou la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) lorsque vous avez besoin de plusieurs formats, de fonctionnalités OpenType avancées ou d’un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="6b02b-114">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format, or the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method when you need multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="6b02b-115">Ces méthodes utilisent l’API DirectWrite pour fournir un affichage de texte de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="6b02b-115">These methods use the DirectWrite API to provide high-quality text display.</span></span>

<span data-ttu-id="6b02b-116">Cette méthode ne retourne pas de code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="6b02b-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="6b02b-117">Pour déterminer si une opération de dessin (telle que **DrawText**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="6b02b-117">To determine whether a drawing operation (such as **DrawText**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="6b02b-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="6b02b-118">Examples</span></span>

<span data-ttu-id="6b02b-119">Pour obtenir un exemple, consultez [Comment dessiner du texte](how-to--draw-text.md).</span><span class="sxs-lookup"><span data-stu-id="6b02b-119">For an example, see [How to Draw Text](how-to--draw-text.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b02b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b02b-120">Requirements</span></span>



| <span data-ttu-id="6b02b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b02b-121">Requirement</span></span> | <span data-ttu-id="6b02b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b02b-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b02b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6b02b-123">Library</span></span><br/> | <dl> <span data-ttu-id="6b02b-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b02b-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b02b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6b02b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b02b-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b02b-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b02b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b02b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b02b-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="6b02b-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="6b02b-129">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="6b02b-129">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="6b02b-130">Comment dessiner du texte</span><span class="sxs-lookup"><span data-stu-id="6b02b-130">How to Draw Text</span></span>](how-to--draw-text.md)
</dt> <dt>

[<span data-ttu-id="6b02b-131">Présentation de la mise en forme et de la disposition du texte</span><span class="sxs-lookup"><span data-stu-id="6b02b-131">Text Formatting and Layout Overview</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

