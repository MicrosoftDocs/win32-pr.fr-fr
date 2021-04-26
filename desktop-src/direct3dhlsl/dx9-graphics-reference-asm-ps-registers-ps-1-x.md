---
title: Registres de ps_1_1__ps_1_2__ps_1_3__ps_1_4
description: Les nuanceurs de pixels dépendent des registres pour obtenir des données de vertex, pour produire des données de pixels, pour conserver des résultats temporaires pendant les calculs et pour identifier les étapes d’échantillonnage de texture.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- Inscrit-ps_1_1 pour ps_1_4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 291f78b8bf74a20dfecf4a74ed65173a895bcc1b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998636"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>registres PS 1 \_ \_ 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ 3 PS 1 \_ \_ \_ \_ 4

Les nuanceurs de pixels dépendent des registres pour obtenir des données de vertex, pour produire des données de pixels, pour conserver des résultats temporaires pendant les calculs et pour identifier les étapes d’échantillonnage de texture. Il existe plusieurs types de registres, chacun avec une fonctionnalité unique. Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 1 \_ X.

Les registres stockent les données pour une utilisation par le nuanceur de pixels. Les registres sont décrits en détail dans les sections suivantes.

-   Les types de registres décrivent les quatre types de registres disponibles et leurs objectifs.
-   Lire le port Limit détaille les restrictions liées à l’utilisation de plusieurs registres dans une instruction unique.
-   Lecture seule lecture écriture décrit les registres qui peuvent être utilisés pour la lecture, l’écriture ou les deux.
-   Plage détaille la plage des données du composant.

## <a name="register-types"></a>Types de registres



|      |                    | Versions |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nom | Type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registre de constante  | 8        | 8    | 8    | 8            |
| r\#  | Registre temporaire | 2        | 2    | 2    | 6            |
| t\#  | Registre de texture   | 4        | 4    | 4    | 6            |
| v\#  | Registre des couleurs     | 2        | 2    | 2    | 2 à la phase 2 |



 

-   Les registres de constantes contiennent des données constantes. Les données peuvent être chargées dans un registre de constante à l’aide de [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) ou elles peuvent être définies à l’aide de [def-PS](def---ps.md). Les registres de constantes ne sont pas utilisables par les instructions d’adresse de texture. La seule exception est l’instruction [texm3x3spec-PS](texm3x3spec---ps.md) , qui utilise un registre de constante pour fournir un vecteur de rayon oculaire.
-   Les registres temporaires sont utilisés pour stocker les résultats intermédiaires. R0 sert également de sortie de nuanceur de pixels. La valeur en R0 à la fin du nuanceur est la couleur de pixel du nuanceur.

    La validation du nuanceur échouera [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) sur tout nuanceur qui tente de lire à partir d’un registre temporaire qui n’a pas été écrit par une instruction précédente. [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) échoue de la même manière, en supposant que la validation est activée (n’utilisez pas D3DXSHADER \_ SKIPVALIDATION).

-   Registres de texture

    Pour le nuanceur de pixels version 1 \_ 1 à 1 \_ 3, les registres de texture contiennent des données de texture ou des coordonnées de texture. Les données de texture sont chargées dans un registre de texture lorsqu’une texture est échantillonnée. L’échantillonnage de texture utilise des coordonnées de texture pour rechercher, ou échantillonner, une valeur de couleur aux coordonnées spécifiées (u, v, w, q) tout en tenant compte des attributs d’état de la phase de texture. Les données de coordonnée de texture sont interpolées à partir des données de coordonnée de texture de vertex et sont associées à une étape de texture spécifique. Il existe une association un-à-un par défaut entre le numéro de l’étape de texture et l’ordre de déclaration des coordonnées de texture. Par défaut, le premier jeu de coordonnées de texture défini dans le format vertex est associé à l’étape de texture 0.

    Pour ces versions de nuanceur de pixels, les registres de texture se comportent comme des registres temporaires lorsqu’ils sont utilisés par des instructions arithmétiques.

    Pour le nuanceur de pixels version 1 \_ 4, les registres de texture (t \# ) contiennent des données de coordonnée de texture en lecture seule. Cela signifie que le jeu de coordonnées de texture et le numéro de l’étape de texture sont indépendants les uns des autres. Le numéro de l’étape de texture (à partir duquel échantillonner une texture) est déterminé par le numéro de registre de destination (R0 à R5). Pour l’instruction texld, le jeu de coordonnées de texture est déterminé par le registre source (T0 à T5), de sorte que le jeu de coordonnées de texture peut être mappé à n’importe quelle étape de texture. En outre, le registre source (en spécifiant des coordonnées de texture) pour texld peut également être un registre temporaire (r \# ), auquel cas le contenu du registre temporaire est utilisé comme coordonnées de texture.

-   Les registres de couleurs contiennent des valeurs de couleur par pixel. Les valeurs sont obtenues par itération par pixel des valeurs chromatiques diffuses et spéculaires dans les données de vertex. Pour les nuanceurs de pixels version 1 \_ 4, les registres de couleur sont uniquement disponibles pendant la deuxième phase.

    Si le mode d’ombrage est défini sur D3DSHADE \_ Flat, l’itération des deux couleurs de vertex (diffuse et spéculaire) est désactivée. Quel que soit le mode de nuance, le brouillard est toujours itéré par le pipeline si le brouillard de pixel est activé. Gardez à l’esprit que le brouillard est appliqué plus tard dans le pipeline que le PixelShader.

    Il est courant de charger le registre v0 avec les données de couleur diffuse de vertex. Il est également courant de charger le registre v1 avec les données de couleur spéculaire du vertex.

    Les valeurs de données de couleur d’entrée sont ancrées (saturées) à la plage de 0 à 1, car il s’agit de la plage d’entrée valide pour les registres de couleurs dans le nuanceur de pixels.

    Les nuanceurs de pixels ont un accès en lecture seule aux registres de couleur. Le contenu de ces registres est une itération des valeurs, mais l’itération peut être effectuée avec une précision nettement inférieure à celle des coordonnées de texture.

## <a name="read-port-limit"></a>Limite de lecture du port

La limite de lecture du port spécifie le nombre de registres différents de chaque type de Registre qui peuvent être utilisés comme Registre source dans une instruction unique.



|      |                    | Versions |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nom | Type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registre de constante  | 2        | 2    | 2    | 2            |
| r\#  | Registre temporaire | 2        | 2    | 2    | 3            |
| t\#  | Registre de texture   | 2        | 3    | 3    | 1            |
| v\#  | Registre des couleurs     | 2        | 2    | 2    | 2 à la phase 2 |



 

Par exemple, les registres de couleurs pour presque toutes les versions ont une limite de deux ports de lecture. Cela signifie qu’une instruction unique peut utiliser un maximum de deux registres de couleurs différents (v0 et v1 par exemple) en tant que registres sources. Cet exemple montre que deux registres de couleur sont utilisés dans la même instruction :


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Lecture seule, lecture/écriture

Les types de registres sont identifiés en fonction de la capacité en lecture seule (RO) ou de la fonctionnalité de lecture/écriture (RW) dans le tableau suivant. Les registres en lecture seule ne peuvent être utilisés qu’en tant que registres sources dans une instruction. ils ne peuvent jamais être utilisés comme registre de destination.



|      |                    | Versions |      |      |                    |
|------|--------------------|----------|------|------|--------------------|
| Nom | Type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Registre de constante  | RO       | RO   | RO   | RO                 |
| r\#  | Registre temporaire | L/E       | L/E   | L/E   | L/E                 |
| t\#  | Registre de texture   | L/E       | L/E   | L/E   | Voir la remarque suivante |
| v\#  | Registre des couleurs     | RO       | RO   | RO   | RO                 |



 

Les registres prenant en charge RW peuvent être utilisés pour stocker les résultats intermédiaires. Cela comprend les registres temporaires et les registres de texture pour certaines versions de nuanceur.

> [!Note]  
>
> -   Pour le nuanceur de pixels version 1 \_ 4, les registres de texture sont roulis pour les instructions d’adressage de texture et les registres de texture ne peuvent être ni lus ni écrits par des instructions arithmétiques. En outre, étant donné que les registres de texture sont devenus des registres de coordonnées de texture, le fait de disposer d’un accès Roll n’est pas une régression des fonctionnalités précédentes.

 

## <a name="range"></a>Plage

La plage est la valeur de données de Registre maximale et minimale. Les plages varient en fonction du type de registre. Les plages de certains registres peuvent être interrogées à partir de l’extrémité de l’appareil à l’aide de [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).



| Nom | Type               | Plage                                               | Versions     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Registre de constante  | -1 à + 1                                            | Toutes les versions |
| r\#  | Registre temporaire | \- PixelShader1xMaxValue à + PixelShader1xMaxValue | Toutes les versions |
| t\#  | Registre de texture   | \- MaxTextureRepeat à + MaxTextureRepeat           | Toutes les versions |
| v\#  | Registre des couleurs     | 0 à 1                                              | Toutes les versions |



 

Le matériel de nuanceur de pixels précoce représente des données dans les registres à l’aide d’un nombre à virgule fixe. Cela limite la précision à un maximum de huit bits pour la partie fractionnaire d’un nombre. Gardez cela à l’esprit lors de la conception d’un nuanceur.

Pour le nuanceur de pixels version 1 \_ 1 à 1 \_ 3, MaxTextureRepeat doit être au minimum un. Pour 1 \_ 4, MaxTextureRepeat doit avoir une valeur minimale de huit.

Pour plus d’informations sur PixelShader1xMaxValue, consultez [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
