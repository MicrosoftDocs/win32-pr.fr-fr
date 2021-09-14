---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Décrit les composants rouge, vert, bleu et alpha d’une couleur. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113477"
---
# <a name="d2d1_color_f"></a>D2D1 \_ couleur \_ F

Décrit les composants rouge, vert, bleu et alpha d’une couleur.


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a>Notes

**D2d1 \_ La couleur \_ f** est un typedef pour la [**couleur D2D ( \_ \_ f**](d2d-color-f.md)), qui est lui-même un typedef pour [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md). Pour plus d’informations sur les membres fournis par **d2d1 \_ Color \_ F**, consultez [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).

La classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) fournit un ensemble de couleurs prédéfinies et de fonctions d’assistance pour définir des couleurs. Pour plus d’informations, consultez la référence [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

## <a name="examples"></a>Exemples

L’exemple suivant utilise la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) pour spécifier une couleur prédéfinie (noire) lors de la création d’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



L’exemple suivant utilise la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) pour spécifier une couleur à l’aide des valeurs rouge, vert, bleu et alpha.


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2DBaseTypes. h (inclure D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

