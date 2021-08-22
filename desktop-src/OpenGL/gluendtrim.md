---
title: gluEndTrim, fonction (Glu. h)
description: Les fonctions gluBeginTrim et gluEndTrim délimitent une définition de boucle de découpage NURBS B-spline (NURBS) non uniforme. | gluEndTrim, fonction (Glu. h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- gluEndTrim fonction OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e47f1ef8a1dcbeef4bc2d582699556a87d39a786b36c01a6de930fcfbd9a6b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612945"
---
# <a name="gluendtrim-function"></a>gluEndTrim fonction)

Les fonctions [**gluBeginTrim**](glubegintrim.md) et **gluEndTrim** délimitent une définition de boucle de découpage [NURBS](using-nurbs-curves-and-surfaces.md)B-spline (NURBS) non uniforme.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez [**gluBeginTrim**](glubegintrim.md) pour marquer le début d’une boucle de suppression et **gluEndTrim** pour marquer la fin d’une boucle de suppression. Une boucle de rognage est un ensemble de segments de courbe orientés (formant une courbe fermée) qui définissent les limites d’une surface NURBS. Vous incluez ces boucles de suppression dans la définition d’une surface NURBS, entre les appels à [**gluBeginSurface**](glubeginsurface.md) et [**gluEndSurface**](gluendsurface.md).

La définition d’une surface NURBS peut contenir de nombreuses boucles de découpage. Par exemple, si vous écrivez une définition pour une surface NURBS qui ressemble à un rectangle avec un trou perforé, la définition contient deux boucles de découpage. Une boucle définit le bord extérieur du rectangle ; l’autre définit le trou perforé. Les définitions de chacune de ces boucles de suppression sont placées entre parenthèses par une paire [**gluBeginTrim**](glubegintrim.md)  /  **gluEndTrim** .

La définition d’une boucle de rognage fermée unique peut se composer de plusieurs segments de courbe, chacun décrit comme une série de segments de ligne formant une courbe linéaire (consultez [**gluPwlCurve**](glupwlcurve.md)), comme une courbe NURBS unique (voir [**gluNurbsCurve**](glunurbscurve.md)) ou comme une combinaison des deux dans n’importe quel ordre. Les seuls appels de bibliothèque qui peuvent apparaître dans une définition de boucle de suppression (entre les appels à [**gluBeginTrim**](glubegintrim.md) et **GluEndTrim**) sont **gluPwlCurve** et **gluNurbsCurve**.

La zone affichée de la surface NURBS correspond à la région dans le domaine située à gauche de la courbe de rognage à mesure que le paramètre Curve augmente. Par conséquent, la région conservée de la surface NURBS est à l’intérieur d’une boucle de suppression dans le sens inverse des aiguilles d’une montre. Pour le rectangle mentionné précédemment, la boucle de rognage pour le bord extérieur du rectangle s’exécute dans le sens inverse des aiguilles d’une montre, tandis que la boucle de rognage pour le trou perforé s’exécute dans le sens des aiguilles d’une montre.

Si vous utilisez plusieurs courbes pour définir une seule boucle de rognage, les segments de courbe doivent former une boucle fermée (autrement dit, le point de terminaison de chaque courbe doit être le point de départ de la courbe suivante et le point de terminaison de la courbe finale doit être le point de départ de la première courbe). Si les points de terminaison de la courbe sont suffisamment proches les uns des autres, mais ne coïncident pas exactement, ils sont forcés de correspondre. Si les points de terminaison ne sont pas suffisamment proches, une erreur se produit (consultez [*gluNurbsCallback*](glunurbs.md)).

Si une définition de boucle de rognage contient plusieurs courbes, la direction des courbes doit être cohérente (c’est-à-dire que l’intérieur doit être à gauche de toutes les courbes). Vous pouvez utiliser des boucles de découpage imbriquées tant que les orientations de courbe alternent correctement. Les courbes de rognage ne peuvent pas se croiser et ne peuvent pas se croiser les unes avec les autres (ou un résultat d’erreur).

Si aucune information de rognage n’est donnée pour une surface NURBS, la surface entière est dessinée.

## <a name="examples"></a>Exemples

Ce fragment de code définit une boucle de rognage qui se compose d’une courbe linéaire par morceaux et de deux courbes NURBS :

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





