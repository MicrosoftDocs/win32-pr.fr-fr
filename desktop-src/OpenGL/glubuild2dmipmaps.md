---
title: gluBuild2DMipmaps, fonction (Glu. h)
description: La fonction gluBuild2DMipmaps crée des des mipmaps 2D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- gluBuild2DMipmaps fonction OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27dcf3d0e95b0b52d5b7f4c4ce0e5692f3fc856b81d9c1d82c9661a70e2f818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489649"
---
# <a name="glubuild2dmipmaps-function"></a>gluBuild2DMipmaps fonction)

La fonction **gluBuild2DMipmaps** crée des des mipmaps 2D.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture cible. Doit être une \_ texture GL \_ 2D.

</dd> <dt>

*components* 
</dt> <dd>

Nombre de composants de couleur dans la texture. Doit être 1, 2, 3 ou 4.

</dd> <dt>

*width* 
</dt> <dd>

Largeur de l’image de texture.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur de l’image de texture.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Il doit s’agir de l’un des éléments suivants : GL \_ Color \_ index, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ alpha, GL \_ RGB, GL \_ RVBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminance ou GL \_ luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Type de données pour les *données*. Il doit s’agir de l’une des valeurs suivantes : \_ octet non signé GL \_ , \_ octet GL, \_ bitmap GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int ou GL \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Pointeur vers les données de l’image en mémoire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluBuild2DMipmaps** obtient l’image d’entrée et génère toutes les images mipmap (à l’aide de [**gluScaleImage**](gluscaleimage.md)), de sorte que l’image d’entrée peut être utilisée comme image de texture mipmapped. Pour charger chacune des images, appelez [**glTexImage2D**](glteximage2d.md). Si les dimensions de l’image d’entrée ne sont pas des puissances de deux, l’image est mise à l’échelle afin que la largeur et la hauteur soient des puissances de deux avant la génération des des mipmaps.

Une valeur de retour de zéro indique une réussite. Dans le cas contraire, un code d’erreur GLU est retourné (voir [**gluErrorString**](gluerrorstring.md)).

Pour obtenir une description des valeurs acceptables pour le paramètre *format* , consultez **glTexImage2D**. Pour obtenir une description des valeurs acceptables pour le *type*, consultez [**glDrawPixels**](gldrawpixels.md).

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





