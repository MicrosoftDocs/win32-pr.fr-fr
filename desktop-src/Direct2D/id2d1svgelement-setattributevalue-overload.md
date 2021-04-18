---
title: Méthodes ID2D1SvgElement SetAttributeValue (D2d1svg. h)
description: Définit un attribut de cet élément.
ms.assetid: 33403a07-28d1-4138-ea7f-04f3ac42a8f7
keywords:
- Méthodes SetAttributeValue Direct2D
topic_type:
- apiref
api_location:
- d2d1svg.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c49f224d364523653e13fb7b6cc141e8e8c6eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533357"
---
# <a name="id2d1svgelementsetattributevalue-methods"></a>ID2D1SvgElement :: SetAttributeValue, méthodes

Définit un attribut de cet élément.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                      | Description                                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAttributeValue (PCWSTR, FLOAT)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_float))                                             | Définit un attribut de cet élément à l’aide d’un float.<br/>                                                                                                 |
| [**SetAttributeValue (PCWSTR, D2D1 de \_ couleur \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_color_f_))                                  | Définit un attribut de cet élément en tant que couleur.<br/>                                                                                                    |
| [**SetAttributeValue (PCWSTR, \_ mode de remplissage d2d1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_fill_mode))                                  | Définit un attribut de cet élément en tant que mode de remplissage. Cette méthode peut être utilisée pour définir la valeur des propriétés « Fill-Rule » ou « clip-Rule ».<br/>         |
| [**SetAttributeValue (PCWSTR, \_ affichage SVG d2d1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_display))                                | Obtient un attribut de cet élément sous la forme d’une valeur d’affichage. Cette méthode peut être utilisée pour obtenir la valeur de la propriété d’affichage.<br/>                          |
| [**SetAttributeValue (PCWSTR, \_ mode Extend d2d1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_extend_mode))                               | Définit un attribut de cet élément en tant que valeur du mode d’extension. Cette méthode peut être utilisée pour définir la valeur d’un attribut spreadMethod.<br/>                 |
| [**SetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Overflow)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_overflow))                               | Définit un attribut de cet élément en tant que valeur de dépassement de capacité. Cette méthode peut être utilisée pour définir la valeur de la propriété overflow.<br/>                       |
| [**SetAttributeValue (PCWSTR, D2D1 \_ - \_ Cap ligne SVG \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_cap))                             | Définit un attribut de cet élément en tant que valeur d’extrémité de ligne. Cette méthode peut être utilisée pour définir la valeur de la propriété Stroke-LineCap.<br/>                  |
| [**SetAttributeValue (PCWSTR, D2D1 \_ \_ & de longueur SVG)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_length_))                              | Définit un attribut de cet élément comme une valeur de longueur.<br/>                                                                                             |
| [**SetAttributeValue (PCWSTR, D2D1 \_ \_ ligne SVG \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_join))                             | Définit un attribut de cet élément en tant que valeur de jointure de ligne. Cette méthode peut être utilisée pour définir la valeur de la propriété Stroke-LineJoin.<br/>                |
| [**SetAttributeValue (PCWSTR, \_ type d' \_ unité SVG d2d1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_unit_type))                            | Définit un attribut de cet élément en tant que valeur de type d’unité. Cette méthode peut être utilisée pour définir la valeur d’un attribut gradientUnits ou clipPathUnits.<br/>  |
| [**SetAttributeValue (PCWSTR, ID2D1SvgAttribute \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_id2d1svgattribute))                              | Définit un attribut de cet élément à l’aide d’une interface.<br/>                                                                                            |
| [**SetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Visibility)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_visibility))                            | Définit un attribut de cet élément en tant que valeur de visibilité. Cette méthode peut être utilisée pour définir la valeur de la propriété Visibility.<br/>                    |
| [**SetAttributeValue (PCWSTR, D2D1 \_ Matrix \_ matrice \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_matrix_3x2_f_))                           | Définit un attribut de cet élément en tant que valeur de matrice. Cette méthode peut être utilisée pour définir la valeur d’un attribut Transform ou gradientTransform.<br/>     |
| [**SetAttributeValue (PCWSTR, D2D1 SVG conserver les proportions \_ \_ \_ \_ &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_preserve_aspect_ratio_))             | Définit un attribut de cet élément en tant que valeur conserver le proportions. Cette méthode peut être utilisée pour définir la valeur d’un attribut preserveAspectRatio.<br/> |
| [**SetAttributeValue (type de chaîne d’attribut svg PCWSTR, D2D1 \_ \_ \_ \_ , PCWSTR)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_string_type_pcwstr))          | Définit un attribut de cet élément à l’aide d’une chaîne. <br/>                                                                                               |
| [**SetAttributeValue (PCWSTR, D2D1 \_ SVG \_ attribut \_ \_ type Pod, void \* , UInt32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_pod_type_constvoid_uint32)) | Définit un attribut de cet élément à l’aide d’un type POD.<br/>                                                                                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D2d1svg. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

�

�
