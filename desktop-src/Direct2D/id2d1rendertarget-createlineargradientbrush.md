---
title: Méthodes ID2D1RenderTarget CreateLinearGradientBrush (D2d1. h)
description: Crée un objet ID2D1LinearGradientBrush pour peindre des zones avec un dégradé linéaire.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Méthodes CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523936"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>ID2D1RenderTarget :: CreateLinearGradientBrush, méthodes

Crée un objet [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pour peindre des zones avec un dégradé linéaire.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                       | Description                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLinearGradientBrush ( \_ Propriétés de pinceau de dégradé linéaire D2D1 \_ \_ \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | Crée un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) qui contient les points de dégradé spécifiés, n’a aucune transformation et a une opacité de base de 1,0. <br/> |
| [**CreateLinearGradientBrush ( \_ Propriétés de pinceau de dégradé linéaire D2D1 \_ \_ \_&, \_ Propriétés de pinceau d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | Crée un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) qui contient les points de dégradé spécifiés et a la transformation et l’opacité de base spécifiées. <br/> |
| [**CreateLinearGradientBrush ( \_ Propriétés de pinceau de dégradé linéaire d2d1 \_ \_ \_ \* , propriétés de \_ pinceau d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | Crée un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) qui contient les points de dégradé spécifiés et a la transformation et l’opacité de base spécifiées. <br/> |



## <a name="examples"></a>Exemples

Pour obtenir un exemple qui montre comment créer une collection de points de dégradé et l’utiliser pour définir un dégradé linéaire, consultez [comment créer un pinceau de dégradé linéaire](how-to-create-a-linear-gradient-brush.md).

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

[**CreateGradientStopCollection**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[Comment créer un pinceau de dégradé linéaire](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Vue d’ensemble des pinceaux](direct2d-brushes-overview.md)
</dt> </dl>

�

�
