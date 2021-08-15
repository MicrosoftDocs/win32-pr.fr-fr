---
title: gluPickMatrix, fonction (Glu. h)
description: La fonction gluPickMatrix définit une région de prélèvement.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- gluPickMatrix fonction OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 394e10c460b406e510b1423f299b4a8724492f5a5b180212ff121f4ad593041e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061577"
---
# <a name="glupickmatrix-function"></a>gluPickMatrix fonction)

La fonction **gluPickMatrix** définit une région de prélèvement.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* 
</dt> <dd>

Coordonnée x de la fenêtre d’une région de prélèvement.

</dd> <dt>

*y* 
</dt> <dd>

Coordonnée de la fenêtre y d’une région de prélèvement.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur de la région de prélèvement en coordonnées de fenêtre.

</dd> <dt>

*width* 
</dt> <dd>

Largeur de la région de prélèvement en coordonnées de la fenêtre.

</dd> <dt>

*vue* 
</dt> <dd>

La fenêtre d’affichage actuelle (à partir d’un appel [**glGetIntegerv**](glgetintegerv.md) ).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluPickMatrix** crée une matrice de projection que vous pouvez utiliser pour restreindre le dessin à une petite zone de la fenêtre d’affichage.

1.  Utilisez **gluPickMatrix** pour restreindre le dessin à une petite zone autour du curseur.
2.  Entrez le mode de sélection (avec [**glRenderMode**](glrendermode.md)), puis rerendez la scène.

    Toutes les primitives qui auraient été dessinées près du curseur sont identifiées et stockées dans la mémoire tampon de sélection.

La matrice créée par **gluPickMatrix** est multipliée par la matrice actuelle comme si [**glMultMatrix**](glmultmatrix.md) était appelé avec la matrice générée.

1.  Appelez [**glLoadIdentity**](glloadidentity.md) pour charger une matrice d’identité dans la pile de la matrice de perspective.
2.  Appelez **gluPickMatrix**.
3.  Appelez une fonction (telle que [**gluPerspective**](gluperspective.md)) pour multiplier la matrice de perspective par la matrice Pick.

Quand vous utilisez **gluPickMatrix** pour choisir une courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)), veillez à désactiver la propriété NURBS Glu la \_ matrice de \_ chargement automatique \_ . Si \_ \_ \_ la matrice de chargement automatique Glu n’est pas désactivée, toute surface NURBS rendue est sous-divisée différemment avec la matrice Pick de la manière dont elle a été subdivisée sans la matrice Pick.

## <a name="examples"></a>Exemples

Lors du rendu d’une scène, procédez comme suit :


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



le code suivant sélectionne une partie de la fenêtre d’affichage :


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glGetIntegerv**](glgetintegerv.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





