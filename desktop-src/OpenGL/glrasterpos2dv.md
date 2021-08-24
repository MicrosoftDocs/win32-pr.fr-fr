---
title: fonction glRasterPos2dv (GL. h)
description: Spécifie la position raster pour les opérations de pixel. | fonction glRasterPos2dv (GL. h)
ms.assetid: de927101-616e-4879-a4eb-3a4e3ae31732
keywords:
- glRasterPos2dv fonction OpenGL
topic_type:
- apiref
api_name:
- glRasterPos2dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bca99f2e187314ffe6fbf7506b0efae9cdc14593283bf37f34af4e8f4c615d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492549"
---
# <a name="glrasterpos2dv-function"></a>glRasterPos2dv fonction)

Spécifie la position raster pour les opérations de pixel.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glRasterPos2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*v* 
</dt> <dd>

Pointeur vers un tableau de deux éléments, en spécifiant les coordonnées x et y pour la position du raster en cours.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

OpenGL gère une position 3D dans les coordonnées de la fenêtre. Cette position, appelée position raster, est conservée avec la précision des sous-pixels. Il est utilisé pour positionner les opérations d’écriture de pixel et de bitmap. Consultez [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)et [**glCopyPixels**](glcopypixels.md).

La position actuelle du raster est constituée de trois coordonnées de fenêtre (*x, y, z*), d’une valeur *w* de la coordonnée d’un élément, d’une distance de coordonnée oculaire, d’un bit valide, de données de couleur et de coordonnées de texture associées. La coordonnée *w* est une coordonnée de clip, car *w* n’est pas projeté aux coordonnées de la fenêtre. La fonction [glRasterPos4](glrasterpos-functions.md) spécifie les coordonnées d’objet *x, y, z* et *w* explicitement. La fonction glRasterPos3 spécifie les coordonnées d’objet *x, y* et *z* explicitement, tandis que *w* est implicitement défini sur un. La fonction glRasterPos2 utilise les valeurs d’argument pour *x* et *y* tout en définissant *z* et *w* de manière implicite sur zéro et un.

Les coordonnées d’objet présentées par [glRasterPos](glrasterpos-functions.md) sont traitées comme celles d’une commande [glVertex](glvertex-functions.md) . Elles sont transformées par les matrices de projection et de modelview actuelles et transmises à l’étape de découpage. Si le vertex n’est pas sélectionné, il est projeté et mis à l’échelle sur les coordonnées de la fenêtre, qui devient la nouvelle position de la trame actuelle, et l’indicateur de la position de la \_ trame active du GL \_ \_ \_ est défini. Si le vertex est sélectionné, le bit valide est effacé et la position raster actuelle ainsi que les coordonnées de couleur et de texture associées ne sont pas définies.

La position actuelle du raster comprend également des données de couleur et des coordonnées de texture associées. Si l’éclairage est activé, la \_ \_ couleur de tramage actuelle de la comptabilité GL \_ , en mode RVBA, ou l' \_ index raster actuel du GL \_ \_ , en mode d’index des couleurs, est définie sur la couleur produite par le calcul de l’éclairage (voir [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)et [**glShadeModel**](glshademodel.md)). Si l’éclairage est désactivé, la couleur actuelle (en mode RVBA, la couleur actuelle de la comptabilité de la variable d’état \_ \_ ) ou l’index de couleurs (en mode d’index des couleurs, l’index de la valeur de la comptabilité générale de \_ la variable d’état \_ ) est utilisé pour mettre à jour la couleur raster actuelle.

De même, \_ les \_ \_ \_ coordonnées de la texture raster actuelle du GL sont mises à jour en fonction de la mesure de \_ texture actuelle du GL \_ \_ , en fonction de la matrice de texture et des fonctions de génération de texture (voir [glTexGen](gltexgen-functions.md)). Enfin, la distance entre l’origine du système de coordonnées oculaire et le sommet, telle qu’elle est transformée par la matrice modelview, remplace la distance de la \_ trame actuelle du GL \_ \_ .

Au départ, la position du raster actuel est (0, 0, 0, 1), la distance de trame actuelle est 0, le bit valide est défini, la couleur RVBA associée est (1, 1, 1, 1), l’index de couleur associé est 1 et les coordonnées de texture associées sont (0, 0, 0, 1). En mode RVBA, \_ \_ l’index de tramage actuel de GL \_ est toujours 1 ; dans le mode d’index de couleurs, la couleur RVBA raster actuelle conserve toujours sa valeur initiale.

> [!Note]  
> La position Raster est modifiée à la fois par [glRasterPos](glrasterpos-functions.md) et par [**glBitmap**](glbitmap.md).

 

> [!Note]  
> Lorsque les coordonnées de la position raster ne sont pas valides, les commandes de dessin basées sur la position raster sont ignorées (c’est-à-dire qu’elles n’entraînent pas de modifications de l’État OpenGL).

 

Les fonctions suivantes récupèrent les informations relatives à [glRasterPos](glrasterpos-functions.md):

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ position \_ valide  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ distance  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ couleur  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Current \_ Raster \_ index  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture de TRAMe actuelle du \_ GL \_  
</dl>

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[glLight](gllight-functions.md)
</dt> <dt>

[glLightModel](gllightmodel-functions.md)
</dt> <dt>

[**glShadeModel**](glshademodel.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





