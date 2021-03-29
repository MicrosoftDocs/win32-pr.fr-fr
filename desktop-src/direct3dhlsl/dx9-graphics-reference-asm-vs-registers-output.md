---
title: Registres de sortie
description: Registres de sortie
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990600"
---
# <a name="output-registers"></a>Registres de sortie

-   Registre des couleurs des vertex
-   Registre de brouillard
-   Registre de position \_
-   Registre de la taille du point \_ \_
-   \_Registre de coordonnées de texture \_

Les noms de registres sont précédés d’une lettre o minuscule, indiquant que les registres de sortie sont en écriture seule.

## <a name="vertex-color-register---od0-od1"></a>Registre des couleurs des vertex-oD0, oD1

oD0 est le registre de couleur diffuse. oD1 est le registre de couleurs spéculaire. La valeur oD0 est interpolée et écrite dans le registre de couleur d’entrée 0 (v0) du nuanceur de pixels. La valeur oD1 est interpolée et écrite dans le registre des couleurs d’entrée 1 (v1) du nuanceur de pixels. Pour plus d’informations sur les registres de couleurs du nuanceur de pixels, consultez registres.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre des couleurs des vertex  | x    | x    | x     | x    |      |       |



 

## <a name="fog-register---ofog"></a>Registre de brouillard-oFog

La valeur de brouillard de sortie est inscrite. La valeur est le facteur de brouillard à interpoler, puis est routé vers la table de brouillard. Seul le composant x scalaire du brouillard est utilisé. Les valeurs sont ancrées entre zéro et un avant de passer au rastériseur.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre de brouillard           | x    | x    | x     | x    |      |       |



 

## <a name="position-register---opos"></a>Registre de position-oPos

La position de sortie est inscrite. La valeur correspond à la position dans l’espace de découpage homogène. Cette valeur doit être écrite par le nuanceur de sommets.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre de position      | x    | x    | x     | x    |      |       |



 

## <a name="point-size-register---opts"></a>Registre de la taille du point-oPts

Registres de taille de point de sortie. Seul le composant x scalaire de la taille en points est utilisé.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre de la taille du point    | x    | x    | x     | x    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a>Registre des coordonnées de texture-oT0 à oT7

Les coordonnées de la texture de sortie s’inscrivent. Plus précisément, il s’agit d’un tableau de registres de données de sortie qui sont itérés et utilisés comme coordonnées de texture par les étapes d’échantillonnage de texture qui acheminent les données vers le nuanceur de pixels.



| Versions de nuanceur vertex      | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|-----------------------------|------|------|-------|------|------|-------|
| Registre de coordonnées de texture | x    | x    | x     | x    |      |       |



 

Lors de l’écriture dans un registre de coordonnées de texture, il est recommandé de passer uniquement les valeurs à virgule flottante en tant que dimension de la carte de texture correspondante. Contrôler les valeurs passées avec un modificateur. Par exemple, utilisez. XY pour une carte de texture 2D.

Lorsque la projection de texture est activée pour une étape de texture, les quatre valeurs à virgule flottante doivent être écrites dans le registre de texture correspondant.

L’un des \* indicateurs de transformation de texture D3DTTFF doit être égal à zéro lorsque le pipeline programmable est utilisé.

### <a name="texture-coordinate-range"></a>Plage de coordonnées de texture

Les données de vertex d’objet fournissent des coordonnées de texture d’entrée. Les objets qui n’utilisent pas les textures en mosaïque ont généralement des coordonnées de texture dans la plage \[ 0, 1 \] . Les objets qui utilisent des textures en mosaïque, telles que le terrain, ont généralement des coordonnées de texture allant de \[ - ?, + ? \] où ? Il peut s’agir d’un grand nombre à virgule flottante.

L’interpolation de coordonnée de texture est effectuée sur les données de vertex pour la pixellisation. Pendant la pixellisation, les coordonnées de texture sont interpolées entre les vertex d’objet, modifiées par l’habillage de texture et mises à l’échelle par la taille de la texture (en tenant également compte du mode d’adresse de texture) pour produire un index d’entiers. L’index est ensuite utilisé pour effectuer une recherche de texture. MaxTextureRepeat peut être utilisé pour déterminer le nombre de fois qu’une texture peut être affichée en mosaïque.

Si les coordonnées de texture sont lues directement dans un nuanceur de pixels (à l’aide de texcoord ou texcrd), la plage de coordonnées de texture dépend de l’instruction et de la version du nuanceur de pixels.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




