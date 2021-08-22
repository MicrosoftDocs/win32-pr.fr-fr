---
description: Le diagramme suivant montre le chemin emprunté par les coordonnées de texture de la source, jusqu’au traitement, et au rastériseur.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Traitement des coordonnées de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5a002e7171f97ab60c0af3cd5e8228cb8222ba70b8e718f2d93c28cebf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044221"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Traitement des coordonnées de texture (Direct3D 9)

Le diagramme suivant montre le chemin emprunté par les coordonnées de texture de la source, jusqu’au traitement, et au rastériseur.

![diagramme du chemin d’accès des coordonnées de texture d’une source au rastériseur](images/tex-processing.png)

Il existe deux sources à partir desquelles le système peut dessiner des coordonnées de texture. Pour une étape de texture donnée, vous pouvez utiliser des coordonnées de texture incluses dans le format de vertex (D3DFVF \_ TEX1 à D3DFVF \_ TEX8), ou vous pouvez utiliser des coordonnées de texture générées automatiquement par Direct3D. Pour plus d’informations sur ce dernier cas, consultez [coordonnées de texture générées automatiquement (Direct3D 9)](automatically-generated-texture-coordinates.md). Si l' \_ État de l’étape de texture D3DTSS TEXTURETRANSFORMFLAGS pour l’étape de texture actuelle est défini sur D3DTTFF \_ Disable (paramètre par défaut), les coordonnées d’entrée ne sont pas transformées. Si D3DTSS \_ TEXTURETRANSFORMFLAGS> est défini sur une autre valeur, la matrice de transformation pour cette étape est appliquée aux coordonnées d’entrée.

Le type énuméré [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) définit des valeurs valides pour l' \_ État de l’étape de texture TEXTURETRANSFORMFLAGS D3DTSS. À l’exception de l' \_ indicateur D3DTTFF Disable, qui ignore la transformation de coordonnée de texture, les valeurs définies dans cette énumération configurent le nombre de coordonnées de sortie que le système passe au rastériseur. Les \_ indicateurs D3DTTFF COUNT1 through D3DTTFF \_ COUNT4 indiquent au système de passer un, deux, trois ou quatre éléments des coordonnées de sortie au rastériseur.

L' \_ indicateur D3DTTFF projeté est spécial : il indique au système que les coordonnées de texture sont destinées à une texture projetée. Combinez l' \_ indicateur D3DTTFF projeté avec un autre membre de [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) pour indiquer au rastériseur de diviser tous les éléments par le dernier élément avant que la pixellisation n’ait lieu. Par exemple, lorsque vous utilisez explicitement des coordonnées de texture à trois éléments, ou lorsque la transformation génère une coordonnée de texture à trois éléments, vous pouvez combiner les \_ indicateurs D3DTTFF COUNT3 et D3DTTFF \_ projeté pour que le rastériseur divise les deux premiers éléments par le dernier, produisant des coordonnées de texture 2D requises pour traiter une texture 2D.

> [!Note]  
> À l’exception des cartes d’environnement cubique et des textures de volume, les rastériseurs ne peuvent pas traiter les textures en utilisant des coordonnées de texture avec plus de deux éléments. Si vous spécifiez plus d’éléments que ce qui peut être utilisé pour traiter la texture actuelle pour cette étape, les éléments superflus sont ignorés. Cela s’applique également lors de l’utilisation de coordonnées de texture 2D pour une texture 1D.

 

Des informations supplémentaires sont contenues dans les rubriques suivantes.

-   [Coordonnées de texture générées automatiquement (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Transformations de coordonnées de texture (Direct3D 9)](texture-coordinate-transformations.md)
-   [Effets spéciaux (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Coordonnées de texture](texture-coordinates.md)
</dt> </dl>

 

 
