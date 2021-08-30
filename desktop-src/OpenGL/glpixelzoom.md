---
title: fonction glPixelZoom (GL. h)
description: La fonction glPixelZoom spécifie les facteurs de zoom de pixel.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- glPixelZoom fonction OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e991b6431a4f1c1752f60f20c46d93e10803d4b2821da5d39162c2eebedfda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081472"
---
# <a name="glpixelzoom-function"></a>glPixelZoom fonction)

La fonction **glPixelZoom** spécifie les facteurs de zoom de pixel.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*xfactor* 
</dt> <dd>

Facteur de zoom *x* pour les opérations d’écriture de pixels.

</dd> <dt>

*yfactor* 
</dt> <dd>

Facteur de zoom *y* pour les opérations d’écriture de pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glPixelZoom** spécifie des valeurs pour les facteurs de zoom *x* et *y* . Pendant l’exécution de [**glDrawPixels**](gldrawpixels.md) ou [**glCopyPixels**](glcopypixels.md), si (*x*<sub>r</sub> ,*y*<sub>r</sub> ) est la position raster actuelle, et qu’un élément donné se trouve dans la *n* *ième ligne et la* énième colonne du rectangle de pixels, alors les pixels dont les centres se trouvent dans le rectangle avec des angles à

![Équation représentant les emplacements où les pixels sont candidats au remplacement.](images/pix05.png)

sont des candidats au remplacement. Tout pixel dont le Centre se trouve sur le bord inférieur ou gauche de cette zone rectangulaire est également modifié.

Les facteurs de zoom de pixel ne sont pas limités aux valeurs positives. Les facteurs de zoom négatifs reflètent l’image résultante sur la position de la trame actuelle.

Les fonctions suivantes récupèrent les informations relatives à **glPixelZoom**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Zoom \_ X

**glGet** avec argument GL \_ Zoom \_ Y

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





