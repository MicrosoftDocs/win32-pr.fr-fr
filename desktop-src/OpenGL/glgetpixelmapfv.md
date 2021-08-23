---
title: fonction glGetPixelMapfv (GL. h)
description: Les fonctions glGetPixelMapfv, glGetPixelMapuiv et glGetPixelMapusv retournent la carte de pixels spécifiée. | fonction glGetPixelMapfv (GL. h)
ms.assetid: b09f4799-8e36-4d4f-90d8-4a8ed3d15718
keywords:
- glGetPixelMapfv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacb74cb4cc08b283b500306d3a3456807cea8b0416a3ddb4fac85bfaa6ed5a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554259"
---
# <a name="glgetpixelmapfv-function"></a>glGetPixelMapfv fonction)

Les fonctions **glGetPixelMapfv**, [**glGetPixelMapuiv**](glgetpixelmapuiv.md)et [**glGetPixelMapusv**](glgetpixelmapusv.md) retournent la carte de pixels spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetPixelMapfv(
   GLenum  map,
   GLfloat *values
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*map* 
</dt> <dd>

Nom de la carte de pixels à retourner. Les valeurs acceptées sont \_ les \_ cartes \_ de pixels GL i \_ à \_ i, les \_ \_ cartes de pixels GL \_ s \_ à \_ s, GL \_ pixel \_ Map \_ i \_ à \_ R, GL \_ pixel \_ Map \_ i \_ à \_ g, GL \_ Pixel Map \_ i à b, GL Pixel Map i à a, GL Pixel Map \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ R \_ to R, GL pixel \_ \_ \_ mapper \_ G \_ à \_ g, GL \_ Pixel Map \_ \_ b \_ to \_ b et GL \_ pixel \_ Map \_ A \_ sur \_ A.

</dd> <dt>

*valeurs* 
</dt> <dd>

Retourne le contenu de la carte de pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mappage* n’est pas une valeur acceptée.<br/>                                                                                           |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Consultez [**glPixelMap**](glpixelmap.md) pour obtenir une description des valeurs acceptables pour le paramètre *Map* . La fonction **glGetPixelMap** retourne dans les *valeurs* le contenu de la carte de pixels spécifiée dans *Map*. Utilisez des mappages de pixels pendant l’exécution de [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)et [**glTexImage2D**](glteximage2d.md) pour mapper les index de couleurs, les index de stencil, les composants de couleur et les composants de profondeur à d’autres valeurs.

Les valeurs entières non signées, si elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne fixe ou à virgule flottante, de sorte que 1,0 correspond à la plus grande valeur entière représentable, et 0,0 correspond à zéro. Les valeurs entières non signées de retour ne sont pas définies si la valeur de mappage n’est pas comprise entre \[ 0 et 1 \] .

Pour déterminer la taille requise pour *Map*, appelez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec la constante symbolique appropriée.

Si une erreur est générée, aucune modification n’est apportée au contenu des *valeurs*.

Les fonctions suivantes récupèrent les informations relatives à **glGetPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec arguments GL \_ pixel \_ Map \_ i \_ à \_ i \_ Size

**glGet** avec argument GL de \_ correspondance des pixels \_ \_ \_ en \_ s \_

**glGet** avec argument GL de \_ mappage de pixel \_ \_ I \_ à \_ R \_ taille

**glGet** avec argument GL de \_ cartes de pixels \_ \_ I \_ à \_ G \_ taille

**glGet** avec argument GL \_ pixel \_ Map \_ I \_ à \_ B \_ Size

**glGet** avec argument GL \_ pixel \_ Map \_ I \_ en \_ \_ taille

**glGet** avec argument GL de \_ mappage de pixel \_ \_ r \_ à \_ \_ taille r

**glGet** avec argument GL de \_ mappage de pixel \_ \_ g \_ à \_ g \_ taille

**glGet** avec argument GL \_ pixel \_ carte \_ b \_ à \_ b \_ taille

**glGet** avec argument GL \_ pixel \_ mapper \_ a \_ à \_ une \_ taille

**glGet** avec argument table de la \_ carte de pixels max. GL \_ \_ \_

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
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





