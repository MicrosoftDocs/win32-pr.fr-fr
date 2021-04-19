---
title: fonction glLineWidth (GL. h)
description: La fonction glLineWidth spécifie la largeur des lignes pixellisées.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- glLineWidth fonction OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518127"
---
# <a name="gllinewidth-function"></a>glLineWidth fonction)

La fonction **glLineWidth** spécifie la largeur des lignes pixellisées.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*width* 
</dt> <dd>

Largeur des lignes pixellisées. La valeur par défaut est 1,0.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *largeur* était inférieure ou égale à zéro.<br/>                                                                                    |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glLineWidth** spécifie la largeur pixellisée des lignes avec et sans alias. L’utilisation d’une largeur de ligne autre que 1,0 a des effets différents, selon que l’anticrénelage de ligne est activé ou non. L’anticrénelage de ligne est contrôlé en appelant [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ line \_ Smooth.

Si l’anticrénelage de ligne est désactivé, la largeur réelle est déterminée en arrondissant la largeur fournie à l’entier le plus proche. (Si l’arrondi donne la valeur 0,0, c’est comme si la largeur de ligne était 1,0) Si \| ? x \|  =  \| ? y \| , les pixels *i* sont remplis dans chaque colonne pixellisée, où *i* est la valeur arrondie de *Width*. Dans le cas *contraire, les* pixels sont remplis sur chaque ligne pixellisée.

Si l’anticrénelage est activé, la pixellisation de ligne produit un fragment pour chaque carré de pixel qui croise la région située dans le rectangle dont la largeur est égale à la largeur de la ligne active, la longueur est égale à la longueur réelle de la ligne et est centrée sur le segment de ligne mathématique. La valeur de couverture pour chaque fragment correspond à la zone de coordonnées de la fenêtre de l’intersection de la zone rectangulaire avec le carré de pixels correspondant. Cette valeur est enregistrée et utilisée dans l’étape de pixellisation finale.

Toutes les largeurs ne peuvent pas être prises en charge lorsque l’anticrénelage de ligne est activé. Si une largeur non prise en charge est demandée, la largeur la plus proche prise en charge est utilisée. Seule la largeur 1,0 est garantie pour être prise en charge ; d’autres dépendent de l’implémentation. Vous pouvez interroger la plage des largeurs prises en charge et la différence de taille entre les largeurs prises en charge au sein de la plage en appelant **glGet** avec les arguments \_ plage de largeur de ligne GL \_ \_ et largeur de \_ ligne GL \_ \_ .

La largeur de ligne spécifiée par **glLineWidth** est toujours retournée lorsque la \_ largeur de ligne GL \_ est interrogée. Le verrouillage et l’arrondi pour les lignes avec et sans alias n’ont aucun effet sur la valeur spécifiée.

La largeur de ligne non anticrénelage peut être ancrée à un maximum dépendant de l’implémentation. Même si ce nombre maximal ne peut pas être interrogé, il ne doit pas être inférieur à la valeur maximale pour les lignes avec un alias, arrondi à la valeur entière la plus proche.

Les fonctions suivantes récupèrent les informations relatives à **glLineWidth**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ largeur de ligne du GL \_

**glGet** avec l’argument \_ \_ plage de largeur de ligne GL \_

**glGet** avec la \_ \_ granularité de la largeur de ligne de l’argument GL \_

[**glIsEnabled**](glisenabled.md) avec argument GL \_ ligne \_ Smooth

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





