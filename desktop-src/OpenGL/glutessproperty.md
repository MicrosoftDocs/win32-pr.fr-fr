---
title: gluTessProperty, fonction (Glu. h)
description: La fonction gluTessProperty définit la propriété d’un objet pavage.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- gluTessProperty fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011456"
---
# <a name="glutessproperty-function"></a>gluTessProperty fonction)

La fonction **gluTessProperty** définit la propriété d’un objet pavage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tess* 
</dt> <dd>

Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*et* 
</dt> <dd>

Valeur de propriété à définir. Les valeurs suivantes sont valides : \_ \_ règle d’enroulement Tess Glu \_ , limite de Glu \_ Tess \_ \_ uniquement et \_ tolérance Glu Tess \_ .



| Valeur                                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**\_règle d' \_ enroulement \_ Tess Glu**</dt> </dl>    | Détermine les parties du polygone qui se trouvent à l’intérieur. Le paramètre de valeur peut être défini sur l’une des valeurs suivantes : GLU Tess enroulement \_ \_ \_ impair, Glu \_ Tess \_ Winding non \_ nul, Glu \_ Tess \_ bobinage \_ positif, Glu \_ Tess \_ enroulement \_ négatif ou Glu \_ Tess \_ \_ ABS \_ GEQ \_ . <br/> Pour comprendre le fonctionnement de la règle d’enroulement, envisagez d’abord que les profils d’entrée partitionnent le plan en régions. La règle d’enroulement détermine laquelle de ces régions se trouve à l’intérieur du polygone.<br/> Pour un seul contour C, le nombre d’enroulements d’un point x est tout simplement le nombre de tours que nous avons défini autour de x, car nous nous déplacerons une fois autour de C (où le sens inverse est positif). Lorsqu’il existe plusieurs conversions, les nombres enroulements individuels sont additionnés. Cette procédure associe une valeur entière signée à chaque point x dans le plan. Notez que le nombre d’enroulements est le même pour tous les points d’une même région.<br/> La règle d’enroulement classe une région comme « à l’intérieur » si son numéro d’enroulement appartient à la catégorie choisie (valeur impaire, différente de zéro, positive, négative ou absolue d’au moins deux). Le du paveur GLU précédent (antérieur à GLU 1,2) utilisait la règle « étrange ». La règle « différente de zéro » (GLU \_ Tess \_ Winding \_ non Zero) est une autre méthode courante pour définir l’intérieur. Les trois autres règles (GLU \_ Tess \_ enroulement \_ positif, Glu \_ Tess \_ enroulement \_ négatif, Glu \_ Tess \_ \_ ABS \_ GEQ \_ Two) sont utiles pour les opérations Polygon CSG lèvent.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**\_limite Glu \_ Tess \_ uniquement**</dt> </dl> | Spécifie une valeur booléenne (définissez la valeur sur GL \_ true ou GL \_ false). Lorsque vous définissez la valeur sur GL \_ true, un ensemble de contours fermés séparant l’intérieur et l’extérieur du polygone est retourné à la place d’un pavage. Les contournements extérieurs sont orientés vers le sens inverse de la normale. les contournements intérieurs sont orientés dans le sens des aiguilles d’une montre. Les \_ \_ rappels de données Begin et Glu Glu Tess Begin et \_ \_ \_ utilisent le \_ type \_ de boucle de ligne GL pour chaque contour.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**\_tolérance Tess \_ Glu**</dt> </dl>              | Spécifie une tolérance pour la fusion des fonctionnalités afin de réduire la taille de la sortie. Par exemple, deux sommets très proches les uns des autres peuvent être remplacés par un seul vertex. La tolérance est multipliée par la plus grande amplitude de coordonnée de n’importe quel vertex d’entrée ; Cela spécifie la distance maximale qu’une fonctionnalité peut déplacer à la suite d’une opération de fusion unique. Si une fonctionnalité unique participe à plusieurs opérations de fusion, la distance totale déplacée peut être supérieure. <br/> La fusion de fonctionnalités est entièrement facultative ; la tolérance n’est qu’une indication. L’implémentation est libre de fusionner dans certains cas et non dans d’autres, ou de ne jamais fusionner des fonctionnalités. La tolérance par défaut est zéro.<br/> L’implémentation actuelle fusionne les sommets uniquement s’ils coïncident exactement, quelle que soit la tolérance actuelle. Un vertex est épissé dans une arête uniquement si l’implémentation ne peut pas distinguer le côté du bord sur lequel se trouve le vertex. Deux bords sont fusionnés uniquement lorsque les deux points de terminaison sont identiques.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

Valeur de la propriété indiquée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluTessProperty** contrôle les propriétés stockées dans un objet pavage. Ces propriétés affectent la manière dont les polygones sont interprétés et rendus.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**gluGetTessProperty**](glugettessproperty.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> </dl>

 

 





