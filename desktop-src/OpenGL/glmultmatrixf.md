---
title: fonction glMultMatrixf (GL. h)
description: La fonction glMultMatrixf multiplie la matrice actuelle par une matrice arbitraire. | fonction glMultMatrixf (GL. h)
ms.assetid: fea5e557-09bd-4c45-89cc-9f3739b577bb
keywords:
- glMultMatrixf fonction OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f981b78dc2d9f152a4a7d1f40c4a2d1f120944b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324883"
---
# <a name="glmultmatrixf-function"></a>glMultMatrixf fonction)

Les fonctions [**glMultMatrixd**](glmultmatrixd.md) et **glMultMatrixf** multiplient la matrice actuelle par une matrice arbitraire.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glMultMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*m* 
</dt> <dd>

Pointeur vers une matrice 4x4 stockée dans la colonne dans l’ordre décroissant de 16 valeurs consécutives.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glMultMatrix** multiplie la matrice actuelle par celle spécifiée dans *m*. Autrement dit, si M est la matrice actuelle et T est la matrice transmise à **glMultMatrix**, m est remplacé par m T.

La matrice actuelle est la matrice de projection, la matrice modelview ou la matrice de texture, déterminée par le mode matrice en cours (voir [**glMatrixMode**](glmatrixmode.md)).

Le paramètre *m* pointe vers une matrice 4x4 de valeurs à virgule flottante simple précision ou à virgule flottante double précision stockées dans l’ordre des colonnes. Autrement dit, la matrice est stockée comme indiqué dans l’image suivante.

![! [Diagramme montrant la matrice 4x4 vers laquelle pointe le paramètre m.]](images/multi01.png)

Les fonctions suivantes récupèrent les informations relatives à **glMultMatrix**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_

**glGet** avec argument GL \_ MODELVIEW \_ Matrix

**glGet** avec argument \_ matrice de projection de la comptabilité \_

matrice de texture **glGet** avec argument GL \_ \_

## <a name="requirements"></a>Spécifications



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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





