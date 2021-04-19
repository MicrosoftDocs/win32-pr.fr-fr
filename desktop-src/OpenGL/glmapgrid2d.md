---
title: fonction glMapGrid2d (GL. h)
description: Définit un maillage unidimensionnel. | fonction glMapGrid2d (GL. h)
ms.assetid: 5e5887d1-e137-434b-a1f3-b3f10d462823
keywords:
- glMapGrid2d fonction OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6992a904528cf961f27335e7241c50fbd14f058b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531773"
---
# <a name="glmapgrid2d-function"></a>glMapGrid2d fonction)

Définit un maillage unidimensionnel.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glMapGrid2d(
   GLint    un,
   GLdouble u1,
   GLdouble u2,
   GLint    vn,
   GLdouble v1,
   GLdouble v2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*un* 
</dt> <dd>

Nombre de partitions dans l’intervalle de plage de la grille \[ U1, U2 \] . Cette valeur doit être positive.

</dd> <dt>

*U1* 
</dt> <dd>

Valeur utilisée comme mappage de la valeur de domaine de la grille entière i = 0.

</dd> <dt>

*U2* 
</dt> <dd>

Valeur utilisée comme mappage de la valeur de domaine de la grille entière i = non.

</dd> <dt>

*VN* 
</dt> <dd>

Nombre de partitions dans l’intervalle de plage de la grille \[ v1, v2 \] .

</dd> <dt>

*v1* 
</dt> <dd>

Valeur utilisée comme mappage de la valeur de domaine de la grille entière j = 0.

</dd> <dt>

*v2* 
</dt> <dd>

Valeur utilisée comme mappage de la valeur de domaine de la grille entière j = VN.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | Un  ou un *VN* n’était pas positif.<br/>                                                                                      |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Les fonctions **glMapGrid** et [glEvalMesh](glevalmesh-functions.md) sont utilisées en tandem pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées. La fonction glEvalMesh effectue un pas à pas dans le domaine entier d’une grille unidimensionnelle ou à deux dimensions, dont la plage est le domaine des mappages d’évaluation spécifiés par [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md).

Les fonctions [**glMapGrid1**](glmapgrid1d.md) et **glMapGrid2** spécifient les mappages de grille linéaire entre les coordonnées de la grille entière i (ou i et j) et les coordonnées de la carte d’évaluation à virgule flottante u (ou v et v). Pour plus d’informations sur l’évaluation des coordonnées v et v, consultez [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md) .

La fonction [**glMapGrid1**](glmapgrid1d.md) spécifie un mappage linéaire unique, de sorte que la *coordonnée* de grille entière 0 correspond exactement à U1, et que la coordonnée de grille entière n’est pas mappée exactement à *U2*. Toutes les autres coordonnées de grille entières que *je suis* mappées de la façon suivante :

*u = i (U2 U1)/un + U1*

La fonction **glMapGrid2** spécifie deux mappages linéaires de ce type. L’un mappe la coordonnée de grille entière *i = 0* exactement à *U1*, et la coordonnée de grille entière *i =* non exactement à *U2*. L’autre mappe la coordonnée de grille entière *j = 0* exactement à *v1*, et la coordonnée de grille entière *j = VN* exactement à *v2*. Les autres coordonnées de grille entière i et j sont mappées de telle sorte que

*u = i (U2 U1)/un + U1*

*v = j (V2 V1)/VN + v1*

Les mappages spécifiés par [**glMapGrid**](glmapgrid1d.md) sont utilisés de façon identique par [glEvalMesh](glevalmesh-functions.md) et [**glEvalPoint**](glevalpoint.md).

Les fonctions suivantes récupèrent les informations relatives à [**glMapGrid**](glmapgrid1d.md):

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Map1 \_ Grid \_ Domain  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ map2 \_ Grid \_ Domain  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ Map1 d’argument GL  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ map2 d’argument GL  
</dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[glEvalMesh](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





