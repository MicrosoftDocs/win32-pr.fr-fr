---
title: gluNextContour, fonction (Glu. h)
description: La fonction gluNextContour marque le début d’un autre contour.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- gluNextContour fonction OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384251"
---
# <a name="glunextcontour-function"></a>gluNextContour fonction)

\[La fonction **gluNextContour** est obsolète et n’est fournie qu’à des fins de compatibilité descendante. La fonction **gluNextContour** est mappée à [**GluTessEndContour**](glutessendcontour.md) suivie de [**gluTessBeginContour**](glutessbegincontour.md).\]

La fonction **gluNextContour** marque le début d’un autre contour.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tess* 
</dt> <dd>

Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*type* 
</dt> <dd>

Type du contour en cours de définition. Les valeurs suivantes sont valides.



| Valeur                                                                                                                                                                | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <dt>**\_extérieur Glu**</dt> </dl>           | Un contour extérieur définit une frontière extérieure du polygone.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <dt>**GLU \_ intérieur**</dt> </dl>           | Un contour intérieur définit une limite intérieure du polygone (par exemple, un trou).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <dt>**GLU \_ inconnu**</dt> </dl>              | Un contour inconnu est analysé par la bibliothèque pour déterminer s’il se trouve à l’intérieur ou à l’extérieur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <dt>**GLU \_ CCW, Glu \_ CW**</dt> </dl> | Le premier GLU \_ CCW ou Glu \_ CW défini est considéré comme extérieur. Tous les autres contours sont considérés comme extérieurs s’ils sont orientés dans la même direction (dans le sens horaire ou dans le sens inverse des aiguilles d’une montre) que le premier contour et dans l’intérieur s’ils ne le sont pas.<br/> Si un profil est de type GLU \_ CCW ou Glu \_ CW, tous les contours doivent être du même type (si ce n’est pas le cas, tous les contours Glu \_ CCW et Glu \_ CW seront remplacés par Glu \_ inconnu). Notez qu’il n’y a pas de différence réelle entre les \_ types de contour Glu CCW et Glu \_ CW.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez la fonction **gluNextContour** pour décrire les polygones avec plusieurs contournements. Une fois que vous avez décrit le premier profil à travers une série d’appels [**gluTessVertex**](glutessvertex.md) , un appel **gluNextContour** indique que le contour précédent est terminé et que le contour suivant va commencer. Effectuez une autre série d’appels **gluTessVertex** pour décrire le nouveau profil. Répétez ce processus jusqu’à ce que tous les profils aient été décrits.

Le paramètre de *type* définit le type de contour suivant.

Pour définir le type du premier contour, vous pouvez appeler **gluNextContour** avant de décrire le premier contour. Si vous n’appelez pas **gluNextContour** avant le premier contour, le premier contour est marqué Glu \_ extérieur.

## <a name="examples"></a>Exemples

Vous pouvez décrire un quadrilatère avec un trou triangulaire dans celui-ci, comme suit :

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





