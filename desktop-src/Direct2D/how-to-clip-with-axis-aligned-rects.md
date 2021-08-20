---
title: Comment découper avec un rectangle de découpage Axis-Aligned
description: Montre comment découper une zone avec un rectangle de découpage aligné sur l’axe.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f666bac88d93cb8ea0f27bfb9c2d5b14975e0dc8bb67aba4f0e767178f6ebddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569312"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>Comment découper avec un rectangle de découpage Axis-Aligned

Cette rubrique explique comment découper une image avec un rectangle de découpage aligné sur l’axe. Cette approche produit uniquement des clips rectangulaires, car les limites de contenu sont alignées sur l’axe du rectangle. Cette approche est plus efficace que l’utilisation de couches avec les limites du contenu. Pour plus d’informations, consultez[vue d’ensemble des couches](direct2d-layers-overview.md).

**Pour découper avec un rectangle de découpage aligné sur l’axe**

1.  Chargez l’image d’origine à partir d’une ressource. Pour plus d’informations sur le chargement d’une image bitmap, consultez [Comment charger une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md).
2.  Appelez [**ID2D1RenderTarget ::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) pour spécifier un rectangle. Les commandes de rendu sont découpées dans le rectangle.

3.  Paint l’image d’origine.
4.  Appelez [**ID2D1RenderTarget ::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pour supprimer le dernier élément aligné sur l’axe de la cible de rendu.

Par exemple, dans l’illustration suivante, le bitmap d’origine sur la gauche est 200 \* 130 pixels. L’image bitmap de droite est la bitmap d’origine découpée vers le rectangle de découpage aligné sur l’axe. Les dimensions sont (20, 20) à (100, 100).

![illustration d’une image bitmap Goldfish avant et après le découpage de la bitmap](images/cliparegion-axisalignedclip.png)

Pour créer l’image découpée, créez une structure Rectangle comme zone de découpage. Appelez [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) avec la zone de découpage et peignez l’image d’origine. Appelez [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pour supprimer le clip de la cible de rendu. Le code suivant montre comment procéder.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 