---
title: fonction glClipPlane (GL. h)
description: La fonction glClipPlane spécifie un plan par rapport auquel toute la géométrie est découpée.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glClipPlane fonction OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb55edd88b8c8dcd6b4481e60dfc05a012bb79f4f484fde8987e9ed23239d837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618039"
---
# <a name="glclipplane-function"></a>glClipPlane fonction)

La fonction **glClipPlane** spécifie un plan par rapport auquel toute la géométrie est découpée.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*plane (avion)* 
</dt> <dd>

Plan de découpage positionné. Les noms symboliques de la forme \_ plan du clip GL \_ *i*, où *i* est un nombre entier compris entre 0 et \_ le nombre maximal \_ de clips de la comptabilité \_ -1, sont acceptés.

</dd> <dt>

*Sommaire* 
</dt> <dd>

Adresse d’un tableau de quatre valeurs à virgule flottante double précision. Ces valeurs sont interprétées comme une équation plan.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *plan* n’est pas une valeur acceptée.<br/>                                                                                         |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La géométrie est toujours découpée par rapport aux limites d’un frustum à six plans en *x*, *y* et *z*. La fonction **glClipPlane** permet de spécifier des plans supplémentaires, pas nécessairement perpendiculairement à l’axe des *x*, à l’axe *y* ou à l’axe *z*, par rapport auquel toutes les géométries sont découpées. Vous pouvez spécifier jusqu’à un \_ nombre maximal de \_ plans de captures de l’élément GL \_ , où le \_ nombre maximal \_ \_ de plans de clip GL est d’au moins six dans toutes les implémentations. Étant donné que la zone de découpage obtenue est l’intersection des demi-espaces définis, elle est toujours convexe.

La fonction **glClipPlane** spécifie un demi-espace à l’aide d’une équation de plan à quatre composants. Quand vous appelez **glClipPlane**,*Equation* est transformé par l’inverse de la matrice modelview et stocké dans les coordonnées oculaire obtenues. Les modifications ultérieures apportées à la matrice modelview n’ont aucun effet sur les composants d’équation plan stocké. Si le produit scalaire des coordonnées oculaires d’un vertex avec les composants de l’équation du plan stocké est positif ou zéro, le vertex est en rapport avec ce plan de découpage. Sinon, elle est en sortie.

Utilisez les fonctions [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) pour activer et désactiver les plans de découpage. Appelez les plans de découpage avec l’argument GL \_ clip \_ plan *i*, où *i* est le numéro de plan.

Par défaut, tous les plans de découpage sont définis en tant que (0, 0, 0, 0) dans les coordonnées oculaires et sont désactivés.

C’est toujours le cas dans le cadre du \_ plan de clip GL \_ *i* = GL \_ clip \_ PLANE0 + *i*.

Les fonctions suivantes récupèrent les informations relatives à **glClipPlane**:

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled**](glisenabled.md) avec argument GL \_ clip \_ plan *i*

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





