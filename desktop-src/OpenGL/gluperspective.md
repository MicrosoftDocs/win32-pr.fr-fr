---
title: gluPerspective, fonction (Glu. h)
description: La fonction gluPerspective définit une matrice de projection de perspective.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- gluPerspective fonction OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973040fc9d9f23e6cfba5e30ceea89a1c13cfbaab0071cc7905080cfcdf60f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061587"
---
# <a name="gluperspective-function"></a>gluPerspective fonction)

La fonction **gluPerspective** définit une matrice de projection de perspective.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fovy* 
</dt> <dd>

Champ d’angle de vue, en degrés, dans l’axe y.

</dd> <dt>

*aspect* 
</dt> <dd>

Proportions qui détermine le champ de vue sur l’axe x. Les proportions sont le rapport entre *x* (largeur) et *y* (hauteur).

</dd> <dt>

*zNear* 
</dt> <dd>

Distance entre la visionneuse et le plan de découpage proche (toujours positive).

</dd> <dt>

*zFar* 
</dt> <dd>

Distance entre la visionneuse et le plan de découpage Far (toujours positive).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluPerspective** spécifie un frustum d’affichage dans le système de coordonnées universel. En général, les proportions dans **gluPerspective** doivent correspondre aux proportions de la fenêtre d’affichage associée. Par exemple, l' *aspect* = 2,0 signifie que l’angle de vue de la visionneuse est deux fois plus large dans *x* que dans *y*. Si la fenêtre d’affichage est deux fois plus larges que sa hauteur, elle affiche l’image sans distorsion.

La matrice générée par **gluPerspective** est multipliée par la matrice actuelle, tout comme si [**glMultMatrix**](glmultmatrix.md) était appelé avec la matrice générée. Pour charger la matrice de perspective sur la pile de matrice actuelle, faites précéder l’appel à **gluPerspective** d’un appel à [**glLoadIdentity**](glloadidentity.md).

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**gluOrtho2D**](gluortho2d.md)
</dt> </dl>

 

 





