---
title: dcl_interface_dynamicindexed (SM5-ASM)
description: Déclarez les pointeurs de table de fonction (interfaces). | dcl_interface_dynamicindexed (SM5-ASM)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78bb0152b44f7e29b9e76221db13da0c465a434
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992069"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a>\_dynamicindexed d’interface DCL \_ (SM5-ASM)

Déclarez les pointeurs de table de fonction (interfaces).



| DCL \_ interface \_ dynamicindexed FP \# \[ arraySize \] \[ numCallSites \] = {ft \# , ft \# ,...} |
|--------------------------------------------------------------------------------------|



 



| Élément                                                          | Description                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*ép\#*<br/> | \[dans \] les pointeurs de table de fonctions.<br/> |



 

## <a name="remarks"></a>Notes

Chaque interface doit être liée à partir de l’API avant que le nuanceur ne soit utilisable. La liaison fournit une référence à l’une des tables de fonctions afin que les emplacements de méthode puissent être remplis. Le compilateur ne génère pas de pointeurs pour les objets non référencés.

Un pointeur de table de fonction a un jeu complet d’emplacements de méthode pour éviter le niveau supplémentaire d’indirection qu’une représentation de pointeur vers vtable C++ nécessiterait. Cela nécessite également que les pointeurs soient de 5 tuples. Dans le modèle d’incorporation virtuel HLSL, il est toujours connu de quelle variable/entrée globale est utilisée pour un appel afin de pouvoir configurer des tables par objet racine.

Les déclarations de pointeur de fonction indiquent les tables de fonctions qui sont autorisées à être utilisées avec elles. Cela permet également la dérivation des informations de corrélation de méthode.

La première \[ \] d’une déclaration d’interface correspond à la taille du tableau. Si l’indexation dynamique est utilisée, la déclaration indiquera que comme indiqué. Un tableau de pointeurs d’interface peut également être indexé de manière statique. en outre, il n’est pas nécessaire que les tableaux de pointeurs d’interface représentent l’indexation dynamique.

La numérotation des pointeurs d’interface commence à 0 pour la première déclaration et prend ensuite en compte la taille du tableau. le premier pointeur après un tableau d’entrée FP0 \[ 4 \] \[ 1 \] est donc FP4 \[ \] \[ \] .

La deuxième \[ \] d’une déclaration d’interface est le nombre de sites d’appel, qui doivent correspondre au nombre de corps dans chaque table référencée dans la déclaration.

Il n’existe aucune limite au nombre de choix de table de fonctions (ft \# ) pouvant être répertoriés dans une déclaration d’interface.

Une table de fonctions donnée \# peut apparaître plusieurs fois dans une ou plusieurs déclarations d’interface.

### <a name="restrictions"></a>Restrictions

-   Le nombre de sites d’objets dans un nuanceur, qui est la somme de toutes les déclarations *FP \#* de leurs \[ \] déclarations arraySize, ne doit pas être supérieur à 253. Ce nombre correspond au nombre de **ces** pointeurs pouvant être présents. Le runtime applique cette limite de 253 pour conserver une limite sur la taille de l’interface DDI pour communiquer ces données de pointeur.
-   Le nombre de sites d’appel dans un nuanceur, qui est la somme de toutes les instructions FCALL du nombre de cibles de branche potentielles, ne doit pas être supérieur à 4096.

    Par exemple, un [FCALL](fcall--sm5---asm-.md) qui utilise un index statique pour la première *dimension \[ \] \[ \] FP* compte comme un :

    `                       fcall fp0[0][0]         // +1`

    Un **FCALL** qui utilise un index dynamique compte comme nombre d’éléments dans le tableau (premier \[ \] de l' **\_ interface DCL**) :

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Cette limite aide certaines implémentations à adapter facilement les tables des sélections de corps de fonction dans un stockage de type mémoire tampon constant.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV et SRV.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





