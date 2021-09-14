---
title: fonction glPointSize (GL. h)
description: La fonction glPointSize spécifie le diamètre des points pixellisés.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- glPointSize fonction OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121358"
---
# <a name="glpointsize-function"></a>glPointSize fonction)

La fonction **glPointSize** spécifie le diamètre des points pixellisés.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*size* 
</dt> <dd>

Diamètre des points pixellisés. La valeur par défaut est 1,0.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *taille* est inférieure ou égale à zéro.<br/>                                                                                     |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glPointSize** spécifie le diamètre pixellisé des points avec et sans alias. L’utilisation d’une taille en points autre que 1,0 a des effets différents, selon que l’anticrénelage des points est activé ou non. L’anticrénelage des points est contrôlé en appelant [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ point \_ Smooth.

Si l’anticrénelage des points est désactivé, la taille réelle est déterminée en arrondissant la taille fournie à l’entier le plus proche. (Si l’arrondi donne la valeur 0, c’est comme si la taille du point était 1.) Si la taille arrondie est impaire, le point central (*x*,*y*) du fragment de pixel qui représente le point est calculé comme

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)

où les indices *w* indiquent les coordonnées des fenêtres. Tous les pixels qui se trouvent dans la grille carrée de la taille arrondie centrée sur (*x*,*y*) composent le fragment. Si la taille est égale à, le point central est

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)

et les centres du fragment pixellisé sont les coordonnées de fenêtre semi-entières dans le carré de la taille arrondie centrée sur (*x*,*y*). Tous les fragments de pixel produits pour pixelliser un point de nonantialiased sont affectés aux mêmes données associées. qui du vertex correspond au point.

Si l’anticrénelage est activé, la pixellisation des points produit un fragment pour chaque carré de pixel qui croise la région située dans le cercle ayant un diamètre égal à la taille du point actuel et centrée aux points (*x*<sub>w</sub> ,*y*<sub>w</sub> ). La valeur de couverture pour chaque fragment correspond à la zone de coordonnées de la fenêtre de l’intersection de la région circulaire avec le carré de pixel correspondant. Cette valeur est enregistrée et utilisée dans l’étape de pixellisation finale. Les données associées à chaque fragment sont les données associées au point en cours de pixellisation.

Toutes les tailles ne sont pas prises en charge lorsque l’anticrénelage des points est activé. Si une taille non prise en charge est demandée, la taille la plus proche prise en charge est utilisée. Seule la taille 1,0 est garantie pour être prise en charge ; d’autres dépendent de l’implémentation. Vous pouvez interroger la plage de tailles prises en charge et la différence de taille entre les tailles prises en charge dans la plage en appelant [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des arguments de granularité de taille de \_ point GL \_ \_ et de \_ \_ granularité de taille de point GL \_ .

La taille en points spécifiée par **glPointSize** est toujours retournée lorsque la \_ taille du point GL \_ est interrogée. Le verrouillage et l’arrondi pour les points avec et sans alias n’ont aucun effet sur la valeur spécifiée.

La taille du point non anticrénelage peut être ancrée à un maximum dépendant de l’implémentation. Même si ce nombre maximal ne peut pas être interrogé, il ne doit pas être inférieur à la valeur maximale pour les points avec anticrénelage, arrondi à la valeur entière la plus proche.

Les fonctions suivantes récupèrent les informations relatives à **glPointSize**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ taille du point GL \_

**glGet** avec argument GL \_ point \_ taille de la \_ plage

**glGet** avec argument de \_ \_ granularité de taille de point GL \_

[**glIsEnabled**](glisenabled.md) avec argument GL \_ point \_ lisse

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





