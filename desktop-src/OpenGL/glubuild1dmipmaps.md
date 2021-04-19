---
title: gluBuild1DMipmaps, fonction (Glu. h)
description: La fonction gluBuild1DMipmaps crée des des mipmaps 1D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- gluBuild1DMipmaps fonction OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510129"
---
# <a name="glubuild1dmipmaps-function"></a>gluBuild1DMipmaps fonction)

La fonction **gluBuild1DMipmaps** crée des des mipmaps 1D.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture cible. Doit être une \_ texture GL \_ 1D.

</dd> <dt>

*components* 
</dt> <dd>

Nombre de composants de couleur dans la texture. Doit être 1, 2, 3 ou 4.

</dd> <dt>

*width* 
</dt> <dd>

Largeur de l’image de texture.

</dd> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Les valeurs suivantes sont valides : GL \_ Color \_ index, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ alpha, GL \_ RGB, GL \_ RVBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminance ou GL \_ luminance \_ alpha.

</dd> <dt>

*type* 
</dt> <dd>

Type de données pour les *données*. Les valeurs suivantes sont valides : \_ octet non signé GL \_ , \_ octet GL, bitmap GL \_ , GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int ou GL \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Pointeur vers les données de l’image en mémoire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluBuild1DMipmaps** obtient l’image d’entrée et génère toutes les images mipmap (à l’aide de [**gluScaleImage**](gluscaleimage.md)) afin que l’image d’entrée puisse être utilisée comme image de texture mipmapped. La fonction [**glTexImage1D**](glteximage1d.md) est ensuite appelée pour charger chacune des images. Si la largeur de l’image d’entrée n’est pas une puissance de deux, l’image est mise à l’échelle à la puissance de deux la plus proche pour que les des mipmaps soient générés.

Une valeur de retour de zéro indique une réussite. Dans le cas contraire, un code d’erreur GLU est retourné (voir [**gluErrorString**](gluerrorstring.md)).

Pour obtenir une description des valeurs acceptables pour le paramètre *format* , consultez **glTexImage1D**. Pour obtenir une description des valeurs acceptables pour le paramètre de *type* , consultez [**glDrawPixels**](gldrawpixels.md).

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





