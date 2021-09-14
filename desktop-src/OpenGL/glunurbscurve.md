---
title: gluNurbsCurve, fonction (Glu. h)
description: La fonction gluNurbsCurve définit la forme d’une courbe B-spline rationnelle non uniforme (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- gluNurbsCurve fonction OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194400"
---
# <a name="glunurbscurve-function"></a>gluNurbsCurve fonction)

La fonction **gluNurbsCurve** définit la forme d’une courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*nknots* 
</dt> <dd>

Nombre de nœuds dans le *nœud*. Le paramètre *nknots* est égal au nombre de points de contrôle plus l’ordre.

</dd> <dt>

*noeud* 
</dt> <dd>

Tableau de valeurs de nœud nondecreasing *nknots* .

</dd> <dt>

*progrès* 
</dt> <dd>

Offset (sous la forme d’un nombre de valeurs à virgule flottante simple précision) entre des points de contrôle de courbe successifs.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Pointeur vers un tableau de points de contrôle. Les coordonnées doivent être conformes au *type*.

</dd> <dt>

*order* 
</dt> <dd>

Ordre de la courbe NURBS. Le paramètre *Order* est égal à degree + 1 ; par conséquent, une courbe cubique a un ordre de 4.

</dd> <dt>

*type* 
</dt> <dd>

Type de la courbe. Si cette courbe est définie au sein d’une paire [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) , le type peut être n’importe lequel des types d’évaluateurs unidimensionnels valides (tels que GL \_ Map1 \_ vertex \_ 3 ou GL \_ Map1 \_ Color \_ 4). Entre une paire [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , les seuls types valides sont Glu \_ Map1 \_ Trim \_ 2 et Glu \_ Map1 \_ Trim \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Quand **gluNurbsCurve** apparaît entre une  / paire de **gluEndCurve** gluBeginCurve, il décrit une courbe à restituer. Vous associez les coordonnées de position, de texture et de couleur en les présentant comme un **gluNurbsCurve** distinct entre une paire **gluBeginCurve** / **gluEndCurve** . N’effectuez pas plus d’un appel à **gluNurbsCurve** pour les données de couleur, de position et de texture dans une paire de / **gluEndCurve** gluBeginCurve unique. Effectuez un seul appel pour décrire la position de la courbe (un *type* de Map1 de comptabilité GL de \_ \_ vertex \_ 3 ou de Map1 de type GL \_ \_ \_ 4).

Quand **gluNurbsCurve** apparaît entre une [](glubegintrim.md) / paire de [**gluEndTrim**](gluendtrim.md) gluBeginTrim, il décrit une courbe de rognage sur une surface NURBS. Si le *type* est Glu \_ Map1 \_ Trim \_ 2, il décrit une courbe dans l’espace de paramètres à deux dimensions (*u* et *v*). S’il s’agit \_ de Glu Map1 \_ Trim \_ 3, il décrit une courbe dans un espace de paramètre homogène à deux dimensions (*u*, *v* et *w*). Pour plus d’informations sur les courbes de suppression, consultez **gluBeginTrim**.

## <a name="examples"></a>Exemples

Les fonctions suivantes affichent une courbe NURBS texturée avec des normales :

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
```

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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndCurve**](gluendcurve.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





