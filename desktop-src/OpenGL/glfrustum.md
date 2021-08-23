---
title: fonction glFrustum (GL. h)
description: La fonction glFrustum multiplie la matrice actuelle par une matrice de perspective.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- glFrustum fonction OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1ca2375206165576405c96528d0590596f4d4d870121f0a30884c8e448ca93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625251"
---
# <a name="glfrustum-function"></a>glFrustum fonction)

La fonction **glFrustum** multiplie la matrice actuelle par une matrice de perspective.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*gauche* 
</dt> <dd>

Coordonnée du plan de découpage vertical gauche.

</dd> <dt>

*Oui* 
</dt> <dd>

Coordonnée du plan de découpage vertical à droite.

</dd> <dt>

*ballon* 
</dt> <dd>

Coordonnée du plan de découpage inférieur horizontal.

</dd> <dt>

*top* 
</dt> <dd>

Coordonnée du plan de découpage inférieur horizontal.

</dd> <dt>

*zNear* 
</dt> <dd>

Les distances par le plan de découpage près de profondeur. Doit être positif.

</dd> <dt>

*zFar* 
</dt> <dd>

Distances avec les plans de découpage de profondeur lointaine. Doit être positif.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *zNear* ou *zFar* n’était pas postitive.<br/>                                                                                       |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glFrustum** décrit une matrice de perspective qui produit une projection de perspective. Les paramètres (*gauche*, *bas*, *zNear*) et (*Right*, *Top*, *zNear*) spécifient les points sur le plan de découpage proche qui sont mappés aux angles inférieur gauche et supérieur droit de la fenêtre, respectivement, en supposant que l’œil se trouve à (0, 0,0). Le paramètre *zFar* spécifie l’emplacement du plan de découpage Far. *ZNear* et *zFar* doivent être positifs. La matrice correspondante est présentée dans l’image suivante.

![Diagramme montrant la matrice de perspective qui produit une projection de perspective.](images/frust01.png)![Équations présentant la fonction glFrustum qui décrit une matrice de perspective.](images/frust02.png)

La fonction **glFrustum** multiplie la matrice actuelle par cette matrice, avec le résultat qui remplace la matrice actuelle. Autrement dit, si M est la matrice actuelle et que F est la matrice de perspective frustum, **glFrustum** remplace M par m F.

Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer la pile de matrice actuelle.

La précision de la mémoire tampon de profondeur est affectée par les valeurs spécifiées pour *zNear* et *zFar*. Plus le rapport entre *zFar* et *zNear* est élevé, moins le tampon de profondeur est en effet à distinguer les surfaces proches les unes des autres. Si

![Équation qui indique le rapport entre le haut et le bas.](images/frust03.png)

le *Journal* 2 (*r*) bits de précision du tampon de profondeur est perdu. Étant donné que *r* approche l’infini comme *zNear* approche de zéro, vous ne devez jamais définir *zNear* à zéro.

Les fonctions suivantes récupèrent des informations sur **glFrustum**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_

**glGet** avec argument GL \_ MODELVIEW \_ Matrix

**glGet** avec argument \_ matrice de projection de la comptabilité \_

matrice de texture **glGet** avec argument GL \_ \_

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





