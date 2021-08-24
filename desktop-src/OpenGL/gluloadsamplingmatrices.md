---
title: gluLoadSamplingMatrices, fonction (Glu. h)
description: La fonction gluLoadSamplingMatrices charge des matrices d’échantillonnage et de cullinging rationnelles (NURBS) non uniformes.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluLoadSamplingMatrices fonction OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41b2f6b25e0cecf0d13d87760a941d5ea68baa1fdd85495c8a316e862c77aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777529"
---
# <a name="gluloadsamplingmatrices-function"></a>gluLoadSamplingMatrices fonction)

La fonction **gluLoadSamplingMatrices** charge des matrices d’échantillonnage et de Cullinging rationnelles ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniformes.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matrice modelview (à partir d’un appel [**glGetFloatv**](glgetfloatv.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matrice de projection (à partir d’un appel **glGetFloatv** ).

</dd> <dt>

*vue* 
</dt> <dd>

Une fenêtre d’affichage (à partir d’un appel [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **gluLoadSamplingMatrices** utilise *modelMatrix*, *projMatrix* et *Viewport* pour recalculer les matrices d’échantillonnage et de Culling stockées dans *nobj*. La matrice d’échantillonnage détermine la précision avec laquelle une courbe ou surface NURBS doit être fractionnée pour satisfaire la tolérance d’échantillonnage (telle que déterminée par la \_ propriété tolérance d’échantillonnage Glu \_ ). La matrice de Culling est utilisée pour décider si une courbe ou une surface NURBS doit être éliminée avant le rendu (lorsque la \_ propriété Glu Culling est activée).

La fonction **gluLoadSamplingMatrices** est nécessaire uniquement si la propriété de la \_ matrice de chargement automatique Glu \_ \_ est désactivée (voir [**gluNurbsProperty**](glunurbsproperty.md)). Bien qu’il soit pratique de conserver la \_ \_ propriété matrice de chargement automatique Glu \_ activée, cela nécessite un aller-retour au serveur OpenGL pour obtenir les valeurs actuelles de la matrice modelview, de la matrice de projection et de la fenêtre d’affichage.)

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

[**glGetFloatv**](glgetfloatv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





