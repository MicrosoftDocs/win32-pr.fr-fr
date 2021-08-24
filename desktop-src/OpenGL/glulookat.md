---
title: gluLookAt, fonction (Glu. h)
description: La fonction gluLookAt définit une transformation d’affichage.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- gluLookAt fonction OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b21d0cb2fac6573ab2999eb96b2af8b1ecb670f4e51d1ffd2ad91ba001c9ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675299"
---
# <a name="glulookat-function"></a>gluLookAt fonction)

La fonction **gluLookAt** définit une transformation d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*eyex* 
</dt> <dd>

Position du point oculaire.

</dd> <dt>

*eyey* 
</dt> <dd>

Position du point oculaire.

</dd> <dt>

*eyez* 
</dt> <dd>

Position du point oculaire.

</dd> <dt>

*Center* 
</dt> <dd>

Position du point de référence.

</dd> <dt>

*CenterY* 
</dt> <dd>

Position du point de référence.

</dd> <dt>

*CenterZ* 
</dt> <dd>

Position du point de référence.

</dd> <dt>

*UPX* 
</dt> <dd>

Direction du vecteur up.

</dd> <dt>

*upy* 
</dt> <dd>

Direction du vecteur up.

</dd> <dt>

*upz* 
</dt> <dd>

Direction du vecteur up.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluLookAt** crée une matrice d’affichage dérivée d’un point oculaire, un point de référence indiquant le centre de la scène et un vecteur up. La matrice mappe le point de référence à l’axe z négatif et l’œil au point d’origine, de sorte que lorsque vous utilisez une matrice de projection classique, le centre de la scène est mappé au centre de la fenêtre d’affichage. De même, la direction décrite par le vecteur vers le haut projeté sur le plan d’affichage est mappée sur l’axe des y positif afin qu’il pointe vers le haut dans la fenêtre d’affichage. Le vecteur up ne doit pas être parallèle à la ligne de vue du point de vue du point de référence.

La matrice générée par **gluLookAt** postmultiplies la matrice actuelle.

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

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





