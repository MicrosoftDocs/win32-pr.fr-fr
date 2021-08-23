---
title: fonction glTranslatef (GL. h)
description: La fonction glTranslatef multiplie la matrice actuelle par une matrice de translation.
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- glTranslatef fonction OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12975095aa78d143aaaf096e8b0141f37d45a56286e7d607a9253e59e27ba5bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489842"
---
# <a name="gltranslatef-function"></a>glTranslatef fonction)

La fonction [**glTranslatef**](gltranslate.md) multiplie la matrice actuelle par une matrice de translation.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* 
</dt> <dd>

Coordonnée *x* d’un vecteur de translation.

</dd> <dt>

*y* 
</dt> <dd>

Coordonnée *y* d’un vecteur de translation.

</dd> <dt>

*Lettre* 
</dt> <dd>

Coordonnée *z* d’un vecteur de translation.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **glTranslatef** produit la traduction spécifiée par (*x*, *y*, *z*). Le vecteur de translation est utilisé pour calculer une matrice de traduction 4x4 :

![Diagramme montrant la matrice de translation 4x4 spécifiée par x, y, z.](images/trans01.png)

La matrice actuelle (voir [**glMatrixMode**](glmatrixmode.md)) est multipliée par cette matrice de translation, le produit remplaçant la matrice actuelle. Autrement dit, si M est la matrice active et que T est la matrice de translation, M est remplacé par M T.

Si le mode matriciel est GL \_ MODELVIEW ou GL \_ projection, tous les objets dessinés après l’appel de **glTranslatef** sont traduits. Utilisez [**glPushMatrix**](glpushmatrix.md) et **glPopMatrix** pour enregistrer et restaurer le système de coordonnées non traduit.

Les fonctions suivantes récupèrent les informations relatives à [**glTranslated**](gltranslate.md) et **glTranslatef**:

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> </dl>

 

 





