---
description: Les textures traditionnelles sont considérées comme des textures à un seul élément.
ms.assetid: 8fe8da80-0879-413a-a7db-617d2f558b28
title: Textures à plusieurs éléments (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a69c04c54f4be73b71a1ac5f2ead123bb51d649ad5e75369411b6bf0906517c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563539"
---
# <a name="multiple-element-textures-direct3d-9"></a>Textures à plusieurs éléments (Direct3D 9)

Les textures traditionnelles sont considérées comme des textures à un seul élément. Les textures à plusieurs éléments permettent aux applications d’écrire simultanément sur plusieurs éléments d’une texture à partir du nuanceur de pixels. Le résultat de la prochaine passe de rendu est qu’une application peut utiliser un ou plusieurs des éléments comme une texture à un seul élément, c’est-à-dire en tant qu’entrées dans le nuanceur de pixels. Ces éléments supplémentaires peuvent être considérés comme un magasin temporaire pour les résultats intermédiaires qui seront utilisés ultérieurement par l’application.

La première génération de matériel qui expose cette fonctionnalité présente les restrictions suivantes :

-   Toutes les surfaces de texture à plusieurs éléments sont automatiquement allouées. Cette limitation est traitée en traitant cela comme un nouveau type de format de surface avec plusieurs canaux RVBA entrelacés.
-   Tous les éléments de la texture à éléments multiples peuvent avoir la même profondeur de bit. Cette limitation est exprimée par le nom des nouveaux formats de surface.
-   Une texture à plusieurs éléments ne peut pas être la primaire/affichable. En d’autres termes, il doit être hors écran uniquement. Cette limitation est exprimée par l’énumération de format de surface.
-   Aucun tramage, test alpha, buée, fusion, Raster-op ou masquage n’est autorisé. Aucun traitement de nuanceur de pixel postérieur n’est effectué, à l’exception du test z-test et du stencil.
-   La texture ne peut pas être un mipmap. La création de la chaîne MIP échoue.
-   Le même élément ne peut pas être défini comme une texture en même temps qu’il s’agit d’une cible de rendu. Toutefois, différents éléments de la même surface de texture à élément multiple peuvent être simultanément des textures et des cibles de rendu.
-   Aucun anticrénelage n’est pris en charge.
-   Les surfaces de texture à plusieurs éléments, lorsqu’elles sont utilisées comme texture, ne peuvent pas être filtrées. Cette limitation peut être vérifiée à l’aide de [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).
-   Les surfaces de texture à plusieurs éléments ne peuvent pas être verrouillées.
-   Plusieurs surfaces de texture à élément multiple peuvent être utilisées simultanément en affectant chacune à différentes étapes, tout comme avec les textures normales.
-   Les surfaces de texture à plusieurs éléments prennent en charge la conversion de la valeur gamma de 2,2 à 1,0 conversion en une opération de lecture, tout comme avec d’autres formats de texture.
-   Certaines implémentations n’appliquent pas le masque d’écriture de sortie (D3DRS \_ COLORWRITEENABLE). Ceux qui peuvent avoir des masques d’écriture de couleur indépendants. Cela est exprimé à l’aide d’un nouveau bit de fonctionnalité. Le nombre de masques d’écriture de couleur indépendants disponibles sera égal au nombre maximal d’éléments dont l’appareil est autorisé.
-   [**Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) efface tous les éléments de la texture à plusieurs éléments qui est définie en tant que cible de rendu.

L’utilisation de textures à plusieurs éléments suit les étapes suivantes :

1.  Les applications découvrent la prise en charge de cette fonctionnalité en vérifiant la disponibilité des formats de texture à plusieurs éléments.
2.  L’application crée ces surfaces en appelant [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture).
3.  L’application définit la surface en tant que cible de rendu à l’aide de l’appel [**SetRenderTarget**](/windows/desktop/api) . Le nuanceur de pixels fournit une sortie aux surfaces à l’aide de l’instruction [MOV-PS](../direct3dhlsl/mov---ps.md) .
4.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) est appelé pour définir une surface de texture à plusieurs éléments à une étape particulière. Comme pour les autres textures, la même surface peut être définie à plusieurs étapes à la fois.
5.  [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) est appelé pour définir D3DSAMP \_ ELEMENTINDEX sur le numéro d’élément approprié dans la texture à plusieurs éléments à partir de laquelle l’échantillonneur échantillonne. La valeur par défaut de cet État est 0, ce qui signifie que les textures qui ne sont pas à plusieurs éléments fonctionneront. L’affectation d’un nombre inapproprié à cet État entraîne un comportement indéfini : si la texture à plusieurs éléments est composée uniquement de deux éléments larges, alors que l’échantillonneur est invité à échantillonner à partir du quatrième élément, par exemple.

## <a name="api-support"></a>Prise en charge des API

Voici un résumé des éléments d’API qui prennent en charge les textures à plusieurs éléments :

-   Le format de surface d' [D3DFMT \_ MULTI2 \_ ARGB8](d3dformat.md) exprime la nature entrelacée du format.
-   L' \_ État de l’échantillonneur D3DSAMP ELEMENTINDEX indique l’index d’élément à utiliser.
-   Les États de rendu suivants prennent en charge les textures à plusieurs éléments :

    -   D3DRS \_ COLORWRITEENABLE1
    -   D3DRS \_ COLORWRITEENABLE2
    -   D3DRS \_ COLORWRITEENABLE3

    D3DRS \_ COLORWRITEENABLE s’applique à la cible de rendu (ou à l’élément) zéro.

-   L’indicateur [D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS](d3dpmisccaps.md) indique que l’appareil prend en charge des masques d’écriture indépendants pour plusieurs textures d’élément ou plusieurs cibles de rendu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de pixels](pixel-pipeline.md)
</dt> </dl>

 

 
