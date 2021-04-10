---
title: Méthodes ID2D1SvgElement GetAttributeValue
description: Obtient un attribut de cet élément.
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- Méthodes GetAttributeValue Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 85e31a8efb1e39d47ab3959fc5ecc175336ab7b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031498"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>ID2D1SvgElement :: GetAttributeValue, méthodes

Obtient un attribut de cet élément.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                     | Description                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue (PCWSTR, FLOAT \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Obtient un attribut de cet élément en tant que valeur float.<br/>                                                                                                    |
| [**GetAttributeValue (PCWSTR, D2D1 \_ couleur \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Obtient un attribut de cet élément en tant que couleur.<br/>                                                                                                    |
| [**GetAttributeValue (PCWSTR, REFIID, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Obtient un attribut de cet élément sous la forme d’un type d’interface. <br/>                                                                                         |
| [**GetAttributeValue (PCWSTR, \_ mode de remplissage d2d1 \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Obtient un attribut de cet élément en tant que mode de remplissage. Cette méthode peut être utilisée pour récupérer la valeur des propriétés Fill-Rule ou clip-Rule.<br/>             |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Obtient un attribut de cet élément sous forme de peinture. Cette méthode peut être utilisée pour récupérer la valeur des propriétés de remplissage ou de trait.<br/>                         |
| [**GetAttributeValue (PCWSTR, D2D1 \_ - \_ longueur SVG \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Obtient un attribut de cet élément sous la forme d’une valeur de longueur.<br/>                                                                                             |
| [**GetAttributeValue (PCWSTR, \_ affichage SVG \_ d2d1 \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Obtient un attribut de cet élément sous la forme d’une valeur d’affichage. Cette méthode peut être utilisée pour obtenir la valeur de la propriété d’affichage.<br/>                          |
| [**GetAttributeValue (PCWSTR, \_ mode Extend \_ d2d1 \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Obtient un attribut de cet élément sous la forme d’une valeur de mode extension. Cette méthode peut être utilisée pour obtenir la valeur d’un attribut spreadMethod.<br/>                  |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Overflow \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Obtient un attribut de cet élément sous la forme d’une valeur de dépassement de capacité. Cette méthode peut être utilisée pour récupérer la valeur de la propriété overflow.<br/>                       |
| [**GetAttributeValue (PCWSTR, D2D1 \_ - \_ Cap ligne SVG \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Obtient un attribut de cet élément sous la forme d’une valeur d’extrémité de ligne. Cette méthode peut être utilisée pour récupérer la valeur de la propriété Stroke-LineCap.<br/>                  |
| [**GetAttributeValue (PCWSTR, D2D1 \_ Matrix \_ matrice \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Obtient un attribut de cet élément sous la forme d’une valeur de matrice. Cette méthode peut être utilisée pour obtenir la valeur d’un attribut Transform ou gradientTransform.<br/>     |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Obtient un attribut de cet élément en tant que données de chemin d’accès. Cette méthode peut être utilisée pour obtenir la valeur de l’attribut d sur un élément Path.<br/>                   |
| [**GetAttributeValue (PCWSTR, D2D1 \_ \_ ligne SVG \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Obtient un attribut de cet élément sous la forme d’une valeur de jointure de ligne. Cette méthode peut être utilisée pour récupérer la valeur de la propriété Stroke-LineJoin.<br/>                |
| [**GetAttributeValue (PCWSTR, \_ type d' \_ unité SVG d2d1 \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Obtient un attribut de cet élément en tant que valeur de type d’unité. Cette méthode peut être utilisée pour obtenir la valeur d’un attribut gradientUnits ou clipPathUnits.<br/>  |
| [**GetAttributeValue (PCWSTR, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Obtient un attribut de cet élément.<br/>                                                                                                               |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Visibility \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Obtient un attribut de cet élément sous la forme d’une valeur de visibilité. Cette méthode peut être utilisée pour récupérer la valeur de la propriété Visibility.<br/>                    |
| [**GetAttributeValue (PCWSTR, ID2D1SvgStrokeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Obtient un attribut de cet élément sous la forme d’un tableau de traits de soulignement. Cette méthode peut être utilisée pour récupérer la valeur de la propriété Stroke-dashArray.<br/>             |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Obtient un attribut de cet élément en tant que points. Cette méthode peut être utilisée pour obtenir la valeur de l’attribut points sur un polygone ou un élément Polyline.<br/>  |
| [**GetAttributeValue (PCWSTR, D2D1 SVG conserver les proportions \_ \_ \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Obtient un attribut de cet élément sous la forme d’une valeur conserver le proportions. Cette méthode peut être utilisée pour obtenir la valeur d’un attribut preserveAspectRatio.<br/> |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ attribut \_ \_ type Pod, void \* , UInt32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Obtient un attribut de cet élément en tant que type POD.<br/>                                                                                                 |
| [**GetAttributeValue (PCWSTR, \_ type de chaîne d’attribut svg d2d1 \_ \_ \_ , PWSTR, UInt32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Obtient un attribut de cet élément sous la forme d’une chaîne. <br/>                                                                                                  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

