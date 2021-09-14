---
title: gluScaleImage, fonction (Glu. h)
description: La fonction gluScaleImage met à l’échelle une image à une taille arbitraire.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluScaleImage fonction OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416699"
---
# <a name="gluscaleimage-function"></a>gluScaleImage fonction)

La fonction **gluScaleImage** met à l’échelle une image à une taille arbitraire.

## <a name="syntax"></a>Syntaxe


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*format* 
</dt> <dd>

Format des données de pixels. Les valeurs symboliques suivantes sont valides \_ : \_ index de couleur GL, \_ index de stencils GL \_ , \_ \_ composant de profondeur GL, comptabilité GL \_ , vert GL, bleu GL, GL \_ \_ \_ alpha, GL \_ RVB, GL \_ RVBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, luminance du GL \_ et \_ luminance alpha du GL \_ .

</dd> <dt>

*largeur* 
</dt> <dd>

Largeur de l’image source qui est mise à l’échelle.

</dd> <dt>

*hauteur* 
</dt> <dd>

Hauteur de l’image source qui est mise à l’échelle.

</dd> <dt>

*type* 
</dt> <dd>

Type de données pour la *donnée*. Il doit s’agir de l’une des valeurs suivantes : \_ octet non signé GL \_ , \_ octet GL, \_ bitmap GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int ou GL \_ float.

</dd> <dt>

*données* 
</dt> <dd>

Pointeur vers l’image source.

</dd> <dt>

*widthout* 
</dt> <dd>

Largeur de l’image de destination.

</dd> <dt>

*heightout* 
</dt> <dd>

Hauteur de l’image de destination.

</dd> <dt>

*typeout* 
</dt> <dd>

Type de données pour *dataout*. Il doit s’agir de l’une des valeurs suivantes : \_ octet non signé GL \_ , \_ octet GL, \_ bitmap GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int ou GL \_ float.

</dd> <dt>

*dataout* 
</dt> <dd>

Pointeur vers l’image de destination.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction aboutit, la valeur de retour est égale à zéro.

Si la fonction échoue, la valeur de retour est un code d’erreur GLU (consultez [**gluErrorString**](gluerrorstring.md)).

## <a name="remarks"></a>Notes

La fonction **gluScaleImage** met à l’échelle une image de pixel en utilisant les modes de stockage de pixels appropriés pour décompresser les données de l’image source et les données de package dans l’image de destination.

Lors de la réduction d’une image, **gluScaleImage** utilise un filtre de zone pour échantillonner l’image source et créer des pixels pour l’image de destination. Lors de l’agrandissement d’une image, les pixels de l’image source sont interpolés de manière linéaire pour créer l’image de destination.

Pour obtenir une description des valeurs acceptables pour les paramètres *format*, *type* et *typeout* , consultez [**glReadPixels**](glreadpixels.md).

## <a name="requirements"></a>Spécifications



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

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> </dl>

 

 





