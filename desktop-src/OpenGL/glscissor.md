---
title: fonction glScissor (GL. h)
description: La fonction glScissor définit la zone de ciseaux.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glScissor fonction OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fafefaaaa3315679af2900808f581324040512816dd2211a0250375c36f824dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777819"
---
# <a name="glscissor-function"></a>glScissor fonction)

La fonction **glScissor** définit la zone de ciseaux.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* 
</dt> <dd>

Coordonnée x (axe vertical) du coin inférieur gauche de la zone de ciseaux.

</dd> <dt>

*y* 
</dt> <dd>

Coordonnée y (axe horizontal) du coin inférieur gauche de la zone de ciseaux. Ensemble, x et y spécifient l’angle inférieur gauche de la zone de ciseaux. À l’origine (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Largeur de la zone de ciseaux.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur de la zone de ciseaux. Lorsqu’un contexte OpenGL est attaché pour la *première fois* à une fenêtre, la *largeur* et la *hauteur* sont définies sur les dimensions de cette fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | La *largeur* ou la *hauteur* était négative.<br/>                                                                                   |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glScissor** définit un rectangle, appelé zone de ciseaux, dans les coordonnées de la fenêtre. Les deux premiers paramètres, *x* et *y*, spécifient l’angle inférieur gauche de la zone. Les paramètres de *largeur* et de *hauteur* spécifient la largeur et la hauteur de la zone.

Le test de ciseaux est activé et désactivé à l’aide de [**glEnable**](glenable.md) et de **GLDISABLE** avec argument GL \_ ciseaux \_ test. Pendant que le test de ciseaux est activé, seuls les pixels qui se trouvent dans la zone de ciseaux peuvent être modifiés en dessinant des commandes. Les coordonnées de fenêtre ont des valeurs entières aux angles partagés de trame pixels. par conséquent, **glScissor**(0, 0, 1, 1) autorise uniquement la modification du pixel inférieur gauche de la fenêtre, tandis que **glScissor**(0, 0, 0, 0) interdit la modification de tous les pixels de la fenêtre.

Lorsque le test de ciseaux est désactivé, c’est comme si la zone de la ciseaux inclue la fenêtre entière.

Les fonctions suivantes récupèrent les informations relatives à **glScissor**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ ciseaux \_ zone

[**glIsEnabled**](glisenabled.md) avec argument GL \_ de \_ test de ciseaux

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
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





