---
title: fonction glRotated (GL. h)
description: La fonction glRotated multiplie la matrice actuelle par une matrice de rotation.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- glRotated fonction OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32216eab9a7c7613f082470360d3f938bbdeaf8ae38cd875d84cd0338dfa78c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491769"
---
# <a name="glrotated-function"></a>glRotated fonction)

La fonction **glRotated** multiplie la matrice actuelle par une matrice de rotation.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*angle* 
</dt> <dd>

Angle de rotation, en degrés.

</dd> <dt>

*x* 
</dt> <dd>

Coordonnée *x* d’un vecteur.

</dd> <dt>

*y* 
</dt> <dd>

Coordonnée *y* d’un vecteur.

</dd> <dt>

*Lettre* 
</dt> <dd>

Coordonnée *z* d’un vecteur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glRotated** calcule une matrice qui effectue une rotation dans le sens inverse des degrés d' *angle* sur le vecteur à partir de l’origine jusqu’au point (*x*, *y*, *z*).

La matrice actuelle (voir [**glMatrixMode**](glmatrixmode.md)) est multipliée par cette matrice de rotation, le produit remplaçant la matrice actuelle. Autrement dit, si M est la matrice actuelle et que R est la matrice de translation, M est remplacé par M R.

Si le mode matriciel est GL \_ MODELVIEW ou GL \_ projection, tous les objets dessinés après l’appel de **glRotated** sont pivotés. Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer le système de coordonnées non pivoté.

Les fonctions suivantes récupèrent les informations relatives à **glRotated**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Render \_ mode

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

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





