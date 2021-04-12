---
title: fonction glPolygonStipple (GL. h)
description: La fonction glPolygonStipple définit le modèle Polygon stippling.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glPolygonStipple fonction OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465654"
---
# <a name="glpolygonstipple-function"></a>glPolygonStipple fonction)

La fonction **glPolygonStipple** définit le modèle Polygon stippling.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mask* 
</dt> <dd>

Pointeur vers un modèle stipple 32x32 qui sera décompressé de la mémoire de la même façon que [**glDrawPixels**](gldrawpixels.md) décompresse les pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glPolygonStipple** définit le modèle Polygon stippling. Polygon stippling, comme Line stippling (voir [**glLineStipple**](gllinestipple.md)), masque certains fragments produits par pixellisation, en créant un modèle. Stippling est indépendant de l’anticrénelage de polygones.

Le paramètre *Mask* est un pointeur vers un modèle 32 x 32 stipple qui est stocké en mémoire comme les données de pixels fournies à **glDrawPixels** avec une *hauteur* et une *largeur* égales à 32, un *format* de pixel de l’index de couleur GL \_ et le \_ *type* de données de la \_ bitmap GL. Autrement dit, le modèle stipple est représenté sous la forme d’un tableau 32x32 d’index de couleurs 1 bits, compacté en octets non signés. Les paramètres de la fonction [**glPixelStore**](glpixelstore-functions.md) , tels que \_ décompresser les \_ \_ octets d’échange et \_ décompresser les \_ LSB au format GL \_ , affectent tout d’abord l’assemblage des bits dans un modèle stipple. Toutefois, les opérations de transfert de pixels (Maj, décalage et mappage de pixels) ne sont pas appliquées à l’image stipple.

Polygon stippling est activé et désactivé avec [**glEnable**](glenable.md) et **glDisable**, à l’aide de l’argument GL \_ Polygon \_ STIPPLE. Si cette option est activée, un fragment de polygone pixellisé avec les coordonnées de fenêtre *x*<sub>w</sub> et *y*<sub>w</sub> est envoyé à l’étape suivante d’OpenGL si et seulement si le bit (*x*<sub>w</sub> mod 32) de la ligne (*y*<sub>w</sub> mod 32) TH est un. Lorsque Polygon stippling est désactivé, c’est comme si le modèle stipple était tous des éléments.

Les fonctions suivantes récupèrent les informations relatives à **glPolygonStipple**:

[**glGetPolygonStipple**](glgetpolygonstipple.md)

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Polygon \_ STIPPLE

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





