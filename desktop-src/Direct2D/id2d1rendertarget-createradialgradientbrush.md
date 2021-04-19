---
title: Méthodes ID2D1RenderTarget CreateRadialGradientBrush (D2d1. h)
description: Crée un objet ID2D1RadialGradientBrush qui peut être utilisé pour peindre des zones avec un dégradé radial.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Méthodes CreateRadialGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530447"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a>ID2D1RenderTarget :: CreateRadialGradientBrush, méthodes

Crée un objet [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui peut être utilisé pour peindre des zones avec un dégradé radial.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                       | Description                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRadialGradientBrush ( \_ Propriétés du pinceau de dégradé radial D2D1 \_ \_ \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))                            | Crée un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui contient les points de dégradé spécifiés, n’a aucune transformation et a une opacité de base de 1,0. <br/> |
| [**CreateRadialGradientBrush ( \_ Propriétés de pinceau de dégradé radial D2D1 \_ \_ \_&, \_ Propriétés de pinceau d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))   | Crée un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui contient les points de dégradé spécifiés et a la transformation et l’opacité de base spécifiées. <br/> |
| [**CreateRadialGradientBrush ( \_ Propriétés de pinceau de dégradé radial d2d1 \_ \_ \_ \* , propriétés de \_ pinceau d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) | Crée un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) qui contient les points de dégradé spécifiés et a la transformation et l’opacité de base spécifiées. <br/> |



## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [comment créer un pinceau de dégradé radial](how-to-create-a-radial-gradient-brush.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Comment créer un pinceau de dégradé radial](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Vue d’ensemble des pinceaux](direct2d-brushes-overview.md)
</dt> </dl>

�

�
