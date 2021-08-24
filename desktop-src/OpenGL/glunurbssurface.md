---
title: gluNurbsSurface, fonction (Glu. h)
description: La fonction gluNurbsSurface définit la forme d’une surface de courbe B-spline rationnelle non uniforme (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- gluNurbsSurface fonction OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50f56232ac891cbdfba18195741d875ecc5436112772ed4fa665903374e96602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554189"
---
# <a name="glunurbssurface-function"></a>gluNurbsSurface fonction)

La fonction **gluNurbsSurface** définit la forme d’une surface de courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*nombre de sknot \_* 
</dt> <dd>

Nombre de nœuds dans la direction du paramétrique *u* .

</dd> <dt>

*sknot* 
</dt> <dd>

Tableau de valeurs de nœud nondecreasing *sknot \_ Count* dans la direction paramétrique *u* .

</dd> <dt>

*nombre de tknot \_* 
</dt> <dd>

Nombre de nœuds dans la direction paramétrique *v* .

</dd> <dt>

*tknot* 
</dt> <dd>

Tableau de valeurs de nœud nondecreasing *tknot \_ Count* dans la direction paramétrique *v* .

</dd> <dt>

*s \_ Stride* 
</dt> <dd>

Décalage (sous la forme d’un nombre de valeurs de point precisionfloating unique) entre des points de contrôle successifs dans la direction du paramétrique *u* dans *ctlarray*.

</dd> <dt>

*t \_ Stride* 
</dt> <dd>

Décalage (en valeurs uniques de point precisionfloating) entre des points de contrôle successifs dans la direction paramétrique *v* dans *ctlarray*.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Tableau contenant des points de contrôle pour la surface NURBS. Les décalages entre les points de contrôle successifs dans les directions paramétriques *u* et *v* sont fournis par *s \_ Stride* et *t \_ Stride*.

</dd> <dt>

*sorder* 
</dt> <dd>

Ordre de la surface de la courbe NURBS dans la direction paramétrique *u* . L’ordre est supérieur à un degré. par conséquent, une surface qui est cubique en *u* a un ordre *u* de 4.

</dd> <dt>

*torder* 
</dt> <dd>

Ordre de la surface de la courbe NURBS dans la direction paramétrique *v* . L’ordre est supérieur à un degré. par conséquent, une surface cubique en *v* a un ordre *v* de 4.

</dd> <dt>

*type* 
</dt> <dd>

Type de l’aire. Le paramètre de *type* peut être n’importe lequel des types d’évaluateurs à deux dimensions valides (tels que GL \_ map2 \_ vertex \_ 3 ou GL \_ map2 \_ Color \_ 4).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez **gluNurbsSurface** dans une définition de surface NURBS pour décrire la forme d’une surface NURBS (avant tout rognage). Pour marquer le début d’une définition de surface NURBS, utilisez la fonction [**gluBeginSurface**](glubeginsurface.md) . Pour marquer la fin d’une définition de surface NURBS, utilisez la fonction [**gluEndSurface**](gluendsurface.md) . Appelez **gluNurbsSurface** dans une définition de surface NURBS uniquement.

Vous associez les coordonnées de position, de texture et de couleur à une surface en les présentant comme un **gluNurbsSurface** distinct entre une paire de  / **gluEndSurface** gluBeginSurface. Au sein d’une paire **gluBeginSurface** / **gluEndSurface** unique, vous ne pouvez effectuer qu’un seul appel à **gluNurbsSurface** pour les données de couleur, de position et de texture. Effectuez un seul appel pour décrire la position de l’aire (un *type* de map2 de comptabilité GL \_ \_ \_ , vertex 3 ou map2 du GL de \_ \_ vertex \_ 4).

Vous pouvez supprimer une surface NURBS en utilisant les fonctions [**gluNurbsCurve**](glunurbscurve.md) et [**gluPwlCurve**](glupwlcurve.md) entre les appels à [**gluBeginTrim**](glubegintrim.md) et [**gluEndTrim**](gluendtrim.md).

Un **gluNurbsSurface** avec des nœuds de *\_ nombre de sknot* dans les nœuds direction *u* et *\_ nombre de tknot* dans la direction *v* avec les commandes *sorder* et *torder* doit avoir les points de contrôle (*sknot \_ Count*  - *sorder*) multipied par (*tknot \_ Count*  - *torder*).

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

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





