---
title: fonction glEvalCoord2fv (GL. h)
description: La fonction glEvalCoord2fv évalue les mappages à deux dimensions activés.
ms.assetid: fff786b4-a9e1-4f3e-a62e-36e89bc9c35d
keywords:
- glEvalCoord2fv fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de18441f1b62bbd4084476dabec1cf14bd096c62ba1b26f35985208f19200b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888359"
---
# <a name="glevalcoord2fv-function"></a>glEvalCoord2fv fonction)

La fonction **glEvalCoord2fv** évalue les mappages à deux dimensions activés.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glEvalCoord2fv(
   const GLfloat *u
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*u* 
</dt> <dd>

Pointeur vers un tableau contenant la coordonnée de domaine *u*.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fonction **glEvalCoord2fv** évalue les mappages à deux dimensions activés à l’aide de deux valeurs de domaine, *u* et *v*. Définissez Maps avec [**glMap1**](glmap1.md). Activez ou désactivez-les avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md).

Lorsque l’une des fonctions **glEvalCoord** est émise, tous les mappages actuellement activés de la dimension indiquée sont évalués. Ensuite, pour chaque mappage activé, c’est comme si la fonction OpenGL correspondante avait été émise avec la valeur calculée. Autrement dit, si l’index \_ Map1 GL \_ ou l' \_ index map2 GL \_ est activé, une fonction [**glIndex**](glindex-functions.md) est simulée. Si GL \_ Map1 \_ Color \_ 4 ou GL \_ map2 \_ Color \_ 4 est activé, une fonction **glcolor** est simulée. Si GL \_ Map1 \_ normal ou GL \_ map2 \_ normal est activé, un vecteur normal est produit, et si l’un des \_ Map1 de \_ texture GL \_ Coord \_ 1, GL \_ Map1 texture Coord \_ \_ \_ 2, GL \_ Map1 texture Coord \_ \_ \_ 3, GL \_ Map1 \_ texture \_ Coord 4, GL map2 texture Coord \_ \_ \_ \_ \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 et GL \_ map2 \_ texture \_ Coord \_ 4 est activé, une fonction [**glTexCoord**](gltexcoord-functions.md) appropriée est simulée.

OpenGL utilise des valeurs évaluées au lieu des valeurs actuelles pour les évaluations qui sont activées, et les valeurs actuelles dans le cas contraire, pour les coordonnées de couleur, d’index de couleur, normales et de texture. Toutefois, les valeurs évaluées ne mettent pas à jour les valeurs actuelles. Ainsi, si les fonctions [**glVertex**](glvertex-functions.md) sont intercalées avec les fonctions **glEvalCoord** , les coordonnées de couleur, normale et de texture associées aux fonctions **glVertex** ne sont pas affectées par les valeurs générées par les fonctions **GlEvalCoord** , mais uniquement par les fonctions [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)et [**glTexCoord**](gltexcoord-functions.md) les plus récentes.

Si la génération automatique normale est activée, **glEvalCoord2fv** appelle [**glEnable**](glenable.md) avec l’argument GL \_ auto \_ normal pour générer des normales de surface analytiques, quel que soit le contenu ou l’activation de la \_ \_ carte normale GL map2. Let

![Équation représentant une valeur de produit croisé pour une carte m.](images/evlcrd01.png)

Le **n** normal généré est

![Équation qui indique la n normale générée pour la carte.](images/evlcrd02.png)

Les fonctions suivantes récupèrent les informations relatives à la fonction **glEvalCoord2fv** :

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 3

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 4

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ index

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ couleur \_ 4

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ normal

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 1

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 2

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ repère \_ 3

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ texture \_ Coord \_ 4

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 3

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ vertex \_ 4

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ index

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ couleur \_ 4

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ normal

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 1

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 2

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ repère \_ 3

[**glIsEnabled**](glisenabled.md) avec argument GL \_ map2 \_ texture \_ Coord \_ 4

[**glIsEnabled**](glisenabled.md) avec l’argument GL \_ auto \_ normal

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





