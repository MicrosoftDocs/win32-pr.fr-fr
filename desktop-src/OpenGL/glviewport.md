---
title: fonction glViewport (GL. h)
description: La fonction glViewport définit la fenêtre d’affichage.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- glViewport fonction OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416677"
---
# <a name="glviewport-function"></a>glViewport fonction)

La fonction **glViewport** définit la fenêtre d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glViewport(
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

Angle inférieur gauche du rectangle de la fenêtre d’affichage, en pixels. La valeur par défaut est (0,0).

</dd> <dt>

*y* 
</dt> <dd>

Angle inférieur gauche du rectangle de la fenêtre d’affichage, en pixels. La valeur par défaut est (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Largeur de la fenêtre d'affichage. Lorsqu’un contexte OpenGL est attaché pour la première fois à une fenêtre, la *largeur* et la *hauteur* sont définies sur les dimensions de cette fenêtre.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur de la fenêtre d'affichage. Lorsqu’un contexte OpenGL est attaché pour la première fois à une fenêtre, la *largeur* et la *hauteur* sont définies sur les dimensions de cette fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | La *largeur* ou la *hauteur* était négative.<br/>                                                                                   |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glViewport** spécifie la transformation affine de *x* et *y* à partir des coordonnées de l’appareil normalisées en coordonnées de la fenêtre. Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) sont des coordonnées de périphérique normalisées. Les coordonnées de la fenêtre (*x*<sub>w</sub> , *y*<sub>w</sub> ) sont ensuite calculées comme suit :

![Équation qui indique le calcul des coordonnées de la fenêtre.](images/view01.png)

La largeur et la hauteur de la fenêtre d’affichage sont ancrées silencieusement à une plage qui dépend de l’implémentation. Cette plage est interrogée en appelant **glGet** avec l’argument GL \_ Max \_ VIEWPORT \_ DIMS.

Les fonctions suivantes récupèrent les informations relatives à **glViewport**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL \_ VIEWPORT

**glGet** avec l’argument GL \_ Max \_ VIEWPORT \_ DIMS

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

[**glDepthRange**](gldepthrange.md)
</dt> </dl>

 

 





