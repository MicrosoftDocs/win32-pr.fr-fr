---
title: fonction glPixelMapfv (GL. h)
description: La fonction glPixelMapfv définit les mappages de transfert de pixels.
ms.assetid: 13403243-1ec4-4b1d-a9da-9a6693b6f9b8
keywords:
- glPixelMapfv fonction OpenGL
topic_type:
- apiref
api_name:
- glPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e447e471f1a37f4d0c8c6bd8fb3ce548bb5657e49afafa01e785b0870ebdd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938354"
---
# <a name="glpixelmapfv-function"></a>glPixelMapfv fonction)

La fonction **glPixelMapfv** définit les mappages de transfert de pixels.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPixelMapfv(
         GLenum  map,
         GLsizei mapsize,
   const GLfloat *values
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*map* 
</dt> <dd>

Nom de mappage symbolique. Les dix cartes sont les suivantes.



| Valeur                                                                                                                                                                               | Signification                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**\_ \_ carte de pixels \_ GL \_ i \_**</dt> </dl> | Cartes index de couleurs pour les index de couleurs.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**\_ \_ cartes de pixels \_ GL \_ sur \_ s**</dt> </dl> | Cartes les index stencil aux index de stencil.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**\_ \_ carte de pixels GL \_ I \_ à \_ R**</dt> </dl> | Cartes les index de couleurs aux composants red.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**\_ \_ carte de pixels GL \_ I \_ à \_ G**</dt> </dl> | Cartes les index de couleurs aux composants verts.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**\_ \_ carte de pixels GL \_ I \_ à \_ B**</dt> </dl> | Cartes les index de couleurs aux composants bleus.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**\_ \_ carte de pixels GL \_ I \_ à \_ A**</dt> </dl> | Cartes les index de couleurs aux composants alpha.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**\_ \_ carte de pixels GL \_ r \_ vers \_ r**</dt> </dl> | Cartes les composants red aux composants red.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**\_ \_ carte de pixels GL \_ g \_ à \_ g**</dt> </dl> | Cartes les composants verts aux composants verts.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**\_ \_ carte de pixels GL \_ b \_ à \_ b**</dt> </dl> | Cartes les composants bleus aux composants bleus.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**\_mappage de pixel GL \_ \_ a \_ à \_ un**</dt> </dl> | Cartes composants alpha aux composants alpha.<br/> |



 

</dd> <dt>

*mapper* 
</dt> <dd>

Taille de la carte en cours de définition.

</dd> <dt>

*valeurs* 
</dt> <dd>

Tableau de valeurs de la valeur de *Mapping* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mappage* n’est pas une valeur acceptée.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la valeur de la taille de *mappage* était négative ou supérieure à celle de la \_ table de mappage de pixels GL \_ \_ . <br/>                                                                                                                                                   |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *Map* était la \_ \_ carte de pixels GL \_ i \_ à \_ i \_ , \_ les cartes de pixels GL \_ s \_ à \_ s, les \_ mappages de pixel GL \_ \_ i \_ à \_ R, \_ les cartes de pixel GL \_ \_ i \_ à \_ G, \_ \_ la carte de pixels GL \_ i \_ à \_ B, ou \_ \_ la carte de pixels GL \_ i \_ à \_ a, et la *correspondance* n’était pas une puissance de deux. <br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md). <br/>                                                                                     |



## <a name="remarks"></a>Remarques

La fonction **glPixelMap** définit les tables de traduction, ou *Maps*, utilisées [**par glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)et [**glTexSubImage2D**](gltexsubimage2d.md). L’utilisation de ces mappages est décrite entièrement dans la rubrique [**glPixelTransfer**](glpixeltransfer.md) , et en partie dans les rubriques relatives aux commandes de pixels et d’images de texture. Seule la spécification des mappages est décrite dans cette rubrique.

Le paramètre *Map* est un nom de mappage symbolique, indiquant l’un des dix mappages à définir. Le paramètre *Mapping* spécifie le nombre d’entrées dans le mappage, et les *valeurs* sont un pointeur vers un tableau de valeurs de mappage *de mappage.*

Les entrées d’un mappage peuvent être spécifiées sous la forme de nombres à virgule flottante simple précision, d’entiers courts non signés ou d’entiers longs non signés. Cartes qui stockent les valeurs de composant de couleur (toutes les cartes de \_ pixels gl \_ \_ i \_ à \_ i et les \_ \_ cartes de pixels gl \_ \_ en \_ s) conservent leurs valeurs dans un format à virgule flottante, avec la mantisse et les tailles d’exposant non spécifiées. Les valeurs à virgule flottante spécifiées par [**glPixelMapfv**](glpixelmap.md) sont converties directement au format à virgule flottante interne de ces mappages, puis ancrées à la plage \[ 0, 1 \] . Les valeurs entières non signées spécifiées par **glPixelMapusv** et **glPixelMapuiv** sont converties de manière linéaire de telle sorte que le plus grand entier pouvant être représenté est mappé à 1,0, et zéro est mappé à 0,0.

Cartes qui stockent des index, \_ une carte de pixels gl \_ \_ i \_ à \_ i et \_ \_ une carte de pixels gl \_ s \_ à \_ s, conservent leurs valeurs dans un format à virgule fixe, avec un nombre non spécifié de bits à droite du point binaire. Les valeurs à virgule flottante spécifiées par [**glPixelMapfv**](glpixelmap.md) sont converties directement au format à virgule fixe interne de ces mappages. Les valeurs entières non signées spécifiées par **glPixelMapusv** et **glPixelMapuiv** spécifient des valeurs entières, avec des zéros à droite du point binaire.

Le tableau suivant indique les tailles et les valeurs initiales de chaque mappage. les Cartes indexés par les index de couleur ou de stencil doivent avoir la valeur *mapping* = 2 ^ *n* pour un nombre *n* ou les résultats ne sont pas définis. La taille maximale autorisée pour chaque mappage dépend de l’implémentation et peut être déterminée en appelant **glGet** à l’aide de la \_ table de correspondance de pixels max. de l’argument GL \_ \_ \_ . La valeur maximale unique s’applique à tous les mappages et est au moins égale à 32.



| Mappage                      | Index de recherche  | Valeur de recherche  | Taille initiale | Valeur initiale |
|--------------------------|---------------|---------------|--------------|---------------|
| \_ \_ carte de pixels \_ GL \_ i \_ | index des couleurs   | index des couleurs   | 1            | 0.0           |
| \_ \_ cartes de pixels \_ GL \_ sur \_ s | index de stencil | index de stencil | 1            | 0.0           |
| \_ \_ carte de pixels GL \_ I \_ à \_ R | index des couleurs   | R             | 1            | 0.0           |
| \_ \_ carte de pixels GL \_ I \_ à \_ G | index des couleurs   | G             | 1            | 0.0           |
| \_ \_ carte de pixels GL \_ I \_ à \_ B | index des couleurs   | B             | 1            | 0.0           |
| \_ \_ carte de pixels GL \_ I \_ à \_ A | index des couleurs   | A             | 1            | 0.0           |
| \_ \_ carte de pixels GL \_ r \_ vers \_ r | R             | R             | 1            | 0.0           |
| \_ \_ carte de pixels GL \_ g \_ à \_ g | G             | G             | 1            | 0.0           |
| \_ \_ carte de pixels GL \_ b \_ à \_ b | B             | B             | 1            | 0.0           |
| \_mappage de pixel GL \_ \_ a \_ à \_ un | A             | A             | 1            | 0.0           |



 

Les fonctions suivantes récupèrent les informations relatives à **glPixelMap**:

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

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





