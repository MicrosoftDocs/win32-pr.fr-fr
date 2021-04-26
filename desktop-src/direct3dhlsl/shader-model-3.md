---
title: Shader Model 3 (référence HLSL)
description: Les nuanceurs de sommets et les nuanceurs de pixels sont considérablement simplifiés par rapport aux versions précédentes du nuanceur.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c277723628d5337e41e5fbf83baa9fda8af16adf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993866"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader Model 3 (référence HLSL)

Les nuanceurs de sommets et les nuanceurs de pixels sont considérablement simplifiés par rapport aux versions précédentes du nuanceur. Si vous implémentez des nuanceurs dans le matériel, vous ne pouvez pas utiliser vs \_ 3 \_ 0 ou PS \_ 3 \_ 0 avec d’autres versions de nuanceur, et vous ne pouvez pas utiliser un type de nuanceur avec le pipeline de fonction fixe. Ces modifications permettent de simplifier les pilotes et le Runtime. La seule exception est que les nuanceurs logiciels uniquement et \_ 3 \_ 0 peuvent être utilisés avec une version de nuanceur de pixels. En outre, si vous utilisez un nuanceur logiciel-uniquement vs \_ 3 \_ 0 avec une version de nuanceur de pixels précédente, le nuanceur vertex peut uniquement utiliser la sémantique de sortie qui est compatible avec les codes de format de vertex flexible.

La sémantique utilisée sur les sorties de nuanceur de sommets doit être utilisée sur les entrées de nuanceur de pixels. La sémantique est utilisée pour mapper les sorties du nuanceur de sommets aux entrées de nuanceur de pixels, de la même façon que la déclaration de vertex est mappée aux registres d’entrée du nuanceur de sommets et aux modèles de nuanceur précédents. Consultez sémantique de correspondance sur les nuanceurs vs 3,0 et PS 3,0.

Des États de rendu supplémentaires du mode habillage ont été ajoutés pour couvrir la possibilité de coordonnées de texture supplémentaires dans ce nouveau schéma. Les attributs avec D3DDECLUSAGE \_ texcoord et l’index d’utilisation de 0 à 15 sont interpolés en mode Wrap lorsque la valeur de retour à la [**\_ ligne \* D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) correspondante est définie.

-   [Fonctionnalités du modèle de nuanceur de sommets 3](#vertex-shader-model-3-features)
-   [Caractéristiques du modèle de nuanceur de pixels 3](#pixel-shader-model-3-features)
-   [Sémantique de correspondance sur \_ \_ les nuanceurs vs 3 0 et PS \_ 3 \_ 0](/windows)
-   [Modifications du mode de brouillard, de profondeur et d’ombrage](#fog-depth-and-shading-mode-changes)
-   [Conversions à virgule flottante et entiers](#floating-point-and-integer-conversions)
-   [Spécification de la précision complète ou partielle](#specifying-full-or-partial-precision)
-   [Nuanceur de pixels et vertex logiciels](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Fonctionnalités du modèle de nuanceur de sommets 3

Les types de registres de sortie du nuanceur de sommets ont été réduits en douze registres (consultez [registres de sortie](dx9-graphics-reference-asm-vs-registers-output.md)). Chaque registre utilisé doit être déclaré à l’aide de l’instruction [DCL](dcl-usage---ps.md) et d’une sémantique (par exemple, DCL \_ Color0 o0. XYZW).

Le \_ modèle de nuanceur de sommets 3 0 (vs \_ 3 \_ 0) étend les fonctionnalités de vs \_ 2 \_ 0 avec l’indexation de registre plus puissante, un ensemble de registres de sortie simplifiés, la possibilité d’échantillonner une texture dans un nuanceur de vertex et la possibilité de contrôler la vitesse à laquelle les entrées du nuanceur sont initialisées.

### <a name="index-any-register"></a>Indexer un registre

Tous les registres (Registre [d’entrée](dx9-graphics-reference-asm-vs-registers-input.md) et [registres de sortie](dx9-graphics-reference-asm-vs-registers-output.md)) peuvent être indexés à l’aide du registre de compteur de [boucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (seuls les registres constants peuvent être indexés dans les versions antérieures.)

Vous devez déclarer les registres d’entrée et de sortie avant de les indexer. Toutefois, vous ne pouvez pas indexer un registre de sortie qui a été déclaré avec une sémantique de taille de position ou de point. En fait, si l’indexation est utilisée, les sémantiques position et psize doivent être déclarées respectivement dans les registres o0 et O1.

Vous êtes uniquement autorisé à indexer une plage continue de registres. autrement dit, vous ne pouvez pas indexer entre des registres qui n’ont pas été déclarés. Bien que cette restriction puisse être gênante, elle permet l’optimisation du matériel. Toute tentative d’indexation dans des registres non contigus produira des résultats indéfinis. La validation du nuanceur n’applique pas cette restriction.

### <a name="simplify-output-registers"></a>Simplifier les registres de sortie

Tous les différents types de registres de sortie ont été réduits dans douze registres de sortie : 1 pour la position, 2 pour la couleur, 8 pour la texture et 1 pour la taille du brouillard ou du point. Ces registres interpolent les données qu’ils contiennent pour le nuanceur de pixels. Les déclarations de registre de sortie sont obligatoires et la sémantique est assignée à chaque registre.

Les registres peuvent être décomposés comme suit :

-   Au moins un registre doit être déclaré en tant que Registre de position à quatre composants. Il s’agit du seul registre de nuanceur de vertex requis.
-   Les dix premiers registres consommés par un nuanceur peuvent utiliser jusqu’à quatre composants (XYZW) au maximum.
-   Le dernier (ou douzième) Registre peut uniquement contenir une valeur scalaire (par exemple, la taille du point).

Pour obtenir la liste des registres, consultez [registres-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Échantillon de texture dans un nuanceur de sommets

Vertex Shader 3 \_ 0 prend en charge la recherche de texture dans le nuanceur de sommets à l’aide de [texldl-vs](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Caractéristiques du modèle de nuanceur de pixels 3

Les registres de couleur et de texture du nuanceur de pixels ont été réduits en dix registres d’entrée (voir [types de registres d’entrée](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). Le registre de visages est un registre scalaire à virgule flottante. Seul le signe de ce registre est valide. Si le signe est négatif, la primitive est une face arrière. Cela peut être utilisé à l’intérieur d’un nuanceur de pixels pour obtenir un éclairage à deux côtés, par exemple. Le registre de position fait référence aux pixels actifs (x, y).

Les registres de constantes de nuanceur peuvent être définis à l’aide de :

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Sémantique de correspondance sur \_ \_ les nuanceurs vs 3 0 et PS \_ 3 \_ 0

Il existe des restrictions sur l’utilisation de la sémantique avec vs \_ 3 \_ 0 et PS \_ 3 \_ 0. En général, vous devez être prudent lors de l’utilisation d’une sémantique pour une entrée de nuanceur qui correspond à une sémantique utilisée sur une sortie de nuanceur.

Par exemple, ce nuanceur de pixels compresse plusieurs noms dans un seul registre :


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Chaque registre a une sémantique différente. Notez que vous pouvez également nommer v0. x et v0. YZ avec une sémantique différente (multiple) en raison de l’utilisation du masque d’écriture.

Étant donné le nuanceur de pixels, \_ le \_ nuanceur vs 3 0 suivant ne peut pas être associé :


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Ces deux nuanceurs sont en conflit avec leur utilisation de la sémantique [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) et **D3DDECLUSAGE \_ TEXCOORD1** .

Réécrivez le nuanceur de sommets comme suit pour éviter la collision sémantique :


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



De même, un nom sémantique déclaré sur des registres d’entrée différents dans le nuanceur de pixels (v0 et V1 dans le nuanceur de pixels) ne peut pas être utilisé dans un registre de sortie unique dans ce nuanceur de sommets. Par exemple, ce nuanceur vertex ne peut pas être couplé au nuanceur de pixels, car D3DDECLUSAGE \_ TEXCOORD1 est utilisé pour les registres d’entrée de nuanceur de pixels (v0, v1) et le registre de sortie du nuanceur de sommets O3.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



En revanche, ce nuanceur vertex ne peut pas être couplé au nuanceur de pixels, car le masque de sortie d’un paramètre avec une sémantique donnée ne fournit pas les données demandées par le nuanceur de pixels :


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



Ce nuanceur vertex ne fournit pas de sortie avec l’un des noms sémantiques demandés par le nuanceur de pixels, de sorte que l’appariement du nuanceur n’est pas valide :


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a>Modifications du mode de brouillard, de profondeur et d’ombrage

Lorsque D3DRS \_ SHADEMODE est défini pour l’ombrage plat lors du découpage et de la pixellisation des triangles, les attributs avec \_ couleur D3DDECLUSAGE sont interpolés comme étant à deux dimensions. Si des composants d’un registre sont déclarés avec une sémantique de couleur, mais que d’autres composants du même registre reçoivent une sémantique différente, l’interpolation d’ombrage plat (linéaire ou plat) est non définie sur les composants de ce registre sans sémantique de couleur.

Si le rendu de brouillard est souhaité \_ , \_ les nuanceurs vs 3 0 et PS \_ 3 \_ 0 doivent implémenter le brouillard. Aucun calcul de brouillard n’est effectué en dehors des nuanceurs. Il n’y a pas de registre de brouillard dans vs \_ 3 \_ 0, et la sémantique supplémentaire D3DDECLUSAGE \_ brouillard (pour le facteur de fusion de brouillard calculé par vertex) et la \_ profondeur D3DDECLUSAGE (pour transmettre une valeur de profondeur au nuanceur de pixels pour calculer le facteur de mélange de brouillard) ont été ajoutées.

L’état de l’étape de texture D3DTSS \_ TEXCOORDINDEX est ignoré lors de l’utilisation du nuanceur de pixels 3,0.

Les valeurs suivantes ont été ajoutées pour prendre en compte les modifications suivantes :


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a>Conversions à virgule flottante et entiers

La mathématique à virgule flottante se produit à des plages et à une précision différentes (16 bits, 24 bits et 32 bits) dans différentes parties du pipeline. Une valeur supérieure à la plage dynamique du pipeline qui entre dans ce pipeline (par exemple, une carte de texture flottante de 32 bits est échantillonnée dans un pipeline à virgule flottante de 24 bits dans PS \_ 2 \_ 0) crée un résultat non défini. Pour un comportement prévisible, vous devez fixer une telle valeur au maximum de la plage dynamique.

La conversion d’une valeur à virgule flottante en un entier se produit à plusieurs endroits, par exemple :

-   Lorsque vous rencontrez une instruction [Mova-vs](mova---vs.md) .
-   Pendant l’adressage de la texture.
-   Lors de l’écriture dans une cible de rendu à virgule non flottante.

## <a name="specifying-full-or-partial-precision"></a>Spécification de la précision complète ou partielle

PS \_ 3 \_ 0 et PS \_ 2 \_ x assurent la prise en charge de deux niveaux de précision :



| PS \_ 3 \_ 0 | PS \_ 2 \_ 0 | Precision         | Value                |
|----------|----------|-------------------|----------------------|
| x        |          | Complète              | fp32 ou version ultérieure       |
| x        |          | Précision partielle | FP16 = s10e5           |
| x        | x        | Complète              | fp24 = s16e7 ou version ultérieure |
| x        | x        | Précision partielle | FP16 = s10e5           |



 

PS \_ 3 \_ 0 prend en charge une précision supérieure à celle de PS \_ 2 \_ 0. Par défaut, toutes les opérations se produisent au niveau de précision complet.

La précision partielle (consultez [modificateurs de registre de nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers.md)) est demandée en ajoutant le \_ modificateur pp au code du nuanceur (à condition que l’implémentation sous-jacente le prenne en charge). Les implémentations sont toujours gratuites pour ignorer le modificateur et effectuer les opérations affectées en toute précision.

Le \_ modificateur pp peut se produire dans deux contextes :

-   Sur une déclaration de coordonnée de texture pour passer des coordonnées de texture de précision partielle au nuanceur de pixels. Cela peut être utilisé lorsque les coordonnées de texture relayent les données de couleur vers le nuanceur de pixels, ce qui peut être plus rapide avec une précision partielle qu’avec une précision totale dans certaines implémentations.
-   Sur n’importe quelle instruction pour demander l’utilisation de la précision partielle, y compris des instructions de chargement de texture. Cela indique que l’implémentation est autorisée à exécuter l’instruction avec une précision partielle et à stocker un résultat de précision partielle. En l’absence d’un modificateur explicite, l’instruction doit être exécutée à la précision totale (quelle que soit la précision des opérandes d’entrée).

Une application peut choisir délibérément de commercialiser la précision des performances. Il existe plusieurs types de données d’entrée de nuanceur qui sont des candidats naturels pour le traitement de la précision partielle :

-   Les itérateurs de couleur sont bien représentés par des valeurs de précision partielle.
-   Les valeurs de texture de la plupart des formats peuvent être correctement représentées par des valeurs de précision partielle (les valeurs échantillonnées à partir de 32 bits, les textures de format à virgule flottante sont une exception évidente).
-   Les constantes peuvent être représentées par une représentation partielle de précision appropriée au nuanceur.

Dans tous ces cas, le développeur peut choisir de spécifier une précision partielle pour traiter les données, sachant qu’aucune précision de données d’entrée n’est perdue. Dans certains cas, un nuanceur peut exiger que les étapes internes d’un calcul soient effectuées à pleine précision même lorsque les valeurs de sortie d’entrée et finales n’ont pas plus que la précision partielle.

## <a name="software-vertex-and-pixel-shaders"></a>Nuanceur de pixels et vertex logiciels

Les implémentations logicielles (au moment de l’exécution et la référence pour les nuanceurs vertex et la référence pour les nuanceurs de pixels) des nuanceurs de version 2 \_ 0 et versions ultérieures ont une validation assouplie. Cela est utile à des fins de débogage et de prototypage. L’application indique au runtime/assembleur qu’elle a besoin d’une partie de la validation assouplie à l’aide de l' \_ indicateur SW dans l’assembleur (par exemple, vs \_ 2 \_ SW). Un nuanceur de logiciels ne fonctionnera pas avec le matériel.

vs \_ 2 \_ SW est un assouplissement aux limites maximales de vs \_ 2 \_ x ; de même, \_ \_ le logiciel PS 2 est une relaxation aux limites maximales de PS \_ 2 \_ x. Plus précisément, les validations suivantes sont assouplies :



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Modèle de nuanceur                               | Ressource                             | Limite                                                                                                                             |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Nombre d’instructions                   | Illimité                                                                                                                         |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registres à constante flottante             | 8 192                                                                                                                              |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registres de constantes entières           | 2 048                                                                                                                              |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registres de constantes booléennes           | 2 048                                                                                                                              |
| \_logiciel PS 2 \_                                  | Profondeur de lecture dépendante                 | Illimité                                                                                                                         |
| vs \_ 2 \_ SW                                  | instructions et étiquettes de contrôle de Flow | Illimité                                                                                                                         |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Nombre de boucles Start/Step/Count               | Le début de l’itération et la taille de l’étape de l’itération pour les instructions du REP et de la boucle sont des entiers signés 32 bits. Le nombre peut atteindre un maximum de \_ int/64. |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Limites de port                          | Les limites de port pour tous les fichiers de Registre sont assouplies.                                                                                   |
| vs \_ 3 \_ SW                                  | Nombre d’interpolateurs              | 16 registres de sortie dans vs \_ 3 \_ SW.                                                                                                 |
| \_logiciel PS 3 \_                                  | Nombre d’interpolateurs              | 14 (16-2) registres d’entrée pour le \_ logiciel PS 3 \_ .                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
