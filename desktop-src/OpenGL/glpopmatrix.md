---
title: fonction glPopMatrix (GL. h)
description: Les fonctions glPushMatrix et glPopMatrix poussent et dépilent la pile de matrice actuelle. | fonction glPopMatrix (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- glPopMatrix fonction OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096609"
---
# <a name="glpopmatrix-function"></a>glPopMatrix fonction)

Les fonctions [**glPushMatrix**](glpushmatrix.md) et **glPopMatrix** poussent et dépilent la pile de matrice actuelle.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

La transmission d’une pile de matrices complète ou la dépilement d’une pile de matrice contenant une seule matrice ne constitue pas une erreur. Dans les deux cas, l’indicateur d’erreur est défini et aucune autre modification n’est apportée à l’État OpenGL.

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DÉPASSEMENT de capacité de la \_ pile GL \_**</dt> </dl>   | La fonction a été appelée alors que la pile de matrice actuelle ne contenait qu’une seule matrice.<br/>                                     |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Il existe une pile de matrices pour chaque mode de matrice. En \_ mode MODELVIEW GL, la profondeur de la pile est au moins égale à 32. Dans les deux autres modes, \_ la projection GL et \_ la texture GL, la profondeur est au moins égale à 2. La matrice actuelle dans n’importe quel mode est la matrice située en haut de la pile pour ce mode.

La fonction [**glPushMatrix**](glpushmatrix.md) pousse la pile de la matrice active d’une unité, en dupliquant la matrice actuelle. Autrement dit, après un appel **glPushMatrix** , la matrice située en haut de la pile est identique à celle qui se trouve au-dessous. La fonction **glPopMatrix** dépile la pile de matrice actuelle, en remplaçant la matrice actuelle par celle qui est située au-dessous de celle-ci sur la pile. Initialement, chacune des piles contient une matrice, une matrice d’identité.

Les fonctions suivantes récupèrent les informations relatives à [**glPushMatrix**](glpushmatrix.md) et **glPopMatrix**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_

**glGet** avec argument GL \_ MODELVIEW \_ Matrix

**glGet** avec argument \_ matrice de projection de la comptabilité \_

matrice de texture **glGet** avec argument GL \_ \_

**glGet** avec argument GL MODELVIEW de la profondeur de la \_ \_ pile \_

**glGet** avec la profondeur de la pile de projection de l’argument GL \_ \_ \_

**glGet** avec la profondeur de la pile de texture de l’argument GL \_ \_ \_

**glGet** avec argument GL \_ Max \_ MODELVIEW \_ \_ profondeur de la pile

**glGet** avec l’argument de profondeur de la \_ pile de projection Max GL \_ \_ \_

**glGet** avec argument de la profondeur de la \_ \_ pile texture Max \_ . GL \_

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





