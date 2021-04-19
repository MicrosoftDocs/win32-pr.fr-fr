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
# <a name="id2d1rendertargetdrawtext-methods"></a>ID2D1RenderTarget ::D méthodes rawText

Dessine le texte spécifié à l’aide des informations de format fournies par un objet [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                                                                               | Description                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ rect \_ F&, ID2D1Brush \* , d2d1 \_ dessiner \_ \_ des options de texte, \_ méthode de mesure du texte DWRITE \_ \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | Dessine le texte spécifié à l’aide des informations de format fournies par un objet [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .<br/>  |
| [**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ rect \_ F \* , ID2D1Brush \* , d2d1 \_ dessiner \_ \_ des options de texte, \_ méthode de mesure du texte DWRITE \_ \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | Dessine le texte spécifié à l’aide des informations de format fournies par un objet [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) . <br/> |



## <a name="remarks"></a>Notes

Pour dessiner du texte avec Direct2D, utilisez la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) pour le texte qui a un format unique, ou la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) lorsque vous avez besoin de plusieurs formats, de fonctionnalités OpenType avancées ou d’un test de positionnement. Ces méthodes utilisent l’API DirectWrite pour fournir un affichage de texte de haute qualité.

Cette méthode ne retourne pas de code d’erreur en cas d’échec. Pour déterminer si une opération de dessin (telle que **DrawText**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [Comment dessiner du texte](how-to--draw-text.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[Comment dessiner du texte](how-to--draw-text.md)
</dt> <dt>

[Présentation de la mise en forme et de la disposition du texte](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

