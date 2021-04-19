---
title: fonction glLoadMatrixd (GL. h)
description: La fonction glLoadMatrixd remplace la matrice actuelle par une matrice arbitraire. | fonction glLoadMatrixd (GL. h)
ms.assetid: 66c499f7-3f55-4de2-b67b-5b775b5854e0
keywords:
- glLoadMatrixd fonction OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4715da159dff60024adb3c7331cbf03c7c3759ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522294"
---
# <a name="glloadmatrixd-function"></a>glLoadMatrixd fonction)

Les fonctions **glLoadMatrixd** et [**glLoadMatrixf**](glloadmatrixf.md) remplacent la matrice actuelle par une matrice arbitraire.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glLoadMatrixd(
   const GLdouble *m
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

La fonction **glLoadMatrix** remplace la matrice actuelle par celle spécifiée dans *m*. La matrice actuelle est la matrice de projection, la matrice modelview ou la matrice de texture, déterminée par le mode matrice en cours (voir [**glMatrixMode**](glmatrixmode.md)).

Le paramètre *m* pointe vers une matrice 4x4 de valeurs à virgule flottante simple précision ou à virgule flottante double précision stockées dans l’ordre des colonnes. Autrement dit, la matrice est stockée comme indiqué dans l’image suivante.

![Diagramme montrant la matrice 4x4 vers laquelle pointe le paramètre m.](images/load02.png)

Les fonctions suivantes récupèrent les informations relatives à **glLoadMatrix**:

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





