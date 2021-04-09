---
title: fonction glEvalPoint1 (GL. h)
description: Les fonctions glEvalPoint1 et glEvalPoint2 génèrent et évaluent un point unique dans une maille. | fonction glEvalPoint1 (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- glEvalPoint1 fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870005"
---
# <a name="glevalpoint1-function"></a>glEvalPoint1 fonction)

Les fonctions [**glEvalPoint1**](glevalpoint.md) et **glEvalPoint2** génèrent et évaluent un point unique dans une maille.

## <a name="syntax"></a>Syntaxe


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*i* 
</dt> <dd>

Valeur entière pour la variable de domaine Grid *i*.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les fonctions [**glMapGrid**](glmapgrid-functions.md) et [**glEvalMesh**](glevalmesh-functions.md) sont utilisées en tandem pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées. Vous pouvez utiliser **glEvalPoint** pour évaluer un seul point de grille dans le même Gridspace parcouru par **glEvalMesh**. L’appel de [**glEvalPoint1**](glevalpoint.md) équivaut à appeler

**glEvalCoord1** (*i* ?*u*  + *u* 1);

where

? *u* = (*u* 2 *u* 1)/*n*

et *n*, *u* 1 et *u* 2 sont les arguments de la fonction **glMapGrid1** la plus récente. La seule exigence numérique absolue est que si *i*  =  *n*, la valeur calculée à partir de (*i* ?*u* + U1) est exactement *u* 2.

Dans le cas à deux dimensions, **glEvalPoint2**, Let

? *u* = (*u* 2 *u* 1)/*n*

? *v* = (*v* 2 *v* 1)/*m*

où *n*, *u* 1, *u* 2, *m*, *v* 1 et *v* 2 sont les arguments de la fonction **glMapGrid2** la plus récente. La fonction **glEvalPoint2** est alors équivalente à l’appel de

**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);

Les seules exigences numériques absolues sont que si *i* = *n*, la valeur est calculée à partir de (*i* ?*u*  +  *u* 1) est exactement U2 et, si *j*  =  *m*, la valeur calculée à partir de (*j* ?*v*  +  *v* 1) est exactement *v* 2.

Les fonctions suivantes récupèrent des informations relatives à [**glEvalPoint1**](glevalpoint.md) et **glEvalPoint2**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Map1 \_ Grid \_ Domain

**glGet** avec argument GL \_ map2 \_ Grid \_ Domain

**glGet** avec des \_ segments de \_ grille \_ Map1 d’argument GL

**glGet** avec des \_ segments de \_ grille \_ map2 d’argument GL

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> </dl>

 

 





