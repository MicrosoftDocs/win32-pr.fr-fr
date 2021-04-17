---
title: fonction glScaled (GL. h)
description: Les fonctions glScaled et glScalef multiplient la matrice actuelle par une matrice de mise à l’échelle générale. | fonction glScaled (GL. h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- glScaled fonction OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2655924f5716e142832882441066d4772d0e63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104570331"
---
# <a name="glscaled-function"></a>glScaled fonction)

Les fonctions **glScaled** et [**glScalef**](glscalef.md) multiplient la matrice actuelle par une matrice de mise à l’échelle générale.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* 
</dt> <dd>

Facteurs d’échelle le long de l’axe *x* .

</dd> <dt>

*y* 
</dt> <dd>

Facteurs d’échelle le long de l’axe *y* .

</dd> <dt>

*z* 
</dt> <dd>

Facteurs d’échelle le long de l’axe *z* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glScaled** produit une mise à l’échelle générale le long des axes *x*, *y* et *z* . Les trois arguments indiquent les facteurs d’échelle souhaités le long de chacun des trois axes. La matrice résultante est

![Diagramme montrant la matrice des facteurs d’échelle le long des axes x, y et z.](images/scale01.png)

La matrice actuelle (voir [**glMatrixMode**](glmatrixmode.md)) est multipliée par cette matrice de mise à l’échelle, le produit remplaçant la matrice actuelle. Autrement dit, si M est la matrice active et S est la matrice d’échelle, M est remplacé par M S.

Si le mode matriciel est GL \_ MODELVIEW ou GL \_ projection, tous les objets dessinés après l’appel de **glScaled** sont mis à l’échelle. Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer le système de coordonnées non mis à l’échelle.

Si des facteurs de mise à l’échelle autres que 1,0 sont appliqués à la matrice modelview et que l’éclairage est activé, la normalisation automatique des normales doit probablement également être activée ([**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize).

Les fonctions suivantes récupèrent les informations relatives à **glScaled**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ MODELVIEW \_ Matrix

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ matrice de projection de la comptabilité \_

matrice de texture [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ \_

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotated**](glrotated.md)
</dt> <dt>

[**glRotatef**](glrotatef.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





