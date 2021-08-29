---
title: fonction glGetPolygonStipple (GL. h)
description: La fonction glGetPolygonStipple retourne le modèle Polygon stipple.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- glGetPolygonStipple fonction OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 566a2e112b4e9d64487292adafbd4fda016f3a4ceb695a473d958a374c0add8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144192"
---
# <a name="glgetpolygonstipple-function"></a>glGetPolygonStipple fonction)

La fonction **glGetPolygonStipple** retourne le modèle Polygon stipple.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mask* 
</dt> <dd>

Retourne le modèle stipple.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glGetPolygonStipple** retourne un modèle de stipple de polygone 32 x 32 via le paramètre *Mask* . Le modèle est compressé en mémoire comme si [**glReadPixels**](glreadpixels.md) avec la *hauteur* et la *largeur* de 32, le *type* de \_ bitmap GL et le *format* de \_ l’index de couleur GL \_ ont été appelés, et le modèle stipple était stocké dans une mémoire tampon d’index de couleurs 32 x 32 interne. Contrairement à **glReadPixels**, toutefois, les opérations de transfert de pixels (décalage, décalage et carte de pixels) ne sont pas appliquées à l’image stipple retournée.

Si une erreur est générée, aucune modification n’est apportée au contenu du *masque*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





