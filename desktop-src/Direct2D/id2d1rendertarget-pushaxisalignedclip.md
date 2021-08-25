---
title: Méthodes ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1. h)
description: Spécifie un rectangle dans lequel toutes les opérations de dessin suivantes sont découpées.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Méthodes PushAxisAlignedClip Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3ce76db0608ccd79ecd8ea1be716f8cbdf4313f95bfdda9cfac7b63474e3f412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873989"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>ID2D1RenderTarget ::P méthodes ushAxisAlignedClip

Spécifie un rectangle dans lequel toutes les opérations de dessin suivantes sont découpées.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                         | Description                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**PushAxisAlignedClip (D2D1 \_ rect \_ F&, \_ mode antialias d2d1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Spécifie un rectangle dans lequel toutes les opérations de dessin suivantes sont découpées. <br/> |
| [**PushAxisAlignedClip (D2D1 \_ rect \_ F \* , \_ mode anticrénelage d2d1 \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Spécifie un rectangle dans lequel toutes les opérations de dessin suivantes sont découpées. <br/> |



## <a name="remarks"></a>Remarques

Une paire [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) et [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) peut se produire autour ou dans un [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), mais ne peut pas se chevaucher. Par exemple, la séquence de **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** est valide, mais la séquence de **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** n’est pas valide.

Cette méthode ne retourne pas de code d’erreur en cas d’échec. Pour déterminer si une opération de dessin (telle que **PushAxisAlignedClip**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez la section [How to clip with a Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1 \_ 1. h (inclure D2d1. h)</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
