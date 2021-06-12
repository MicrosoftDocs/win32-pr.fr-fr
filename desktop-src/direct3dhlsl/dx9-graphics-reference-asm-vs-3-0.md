---
title: vs_3_0
description: En savoir plus sur vs_3_0, un nuanceur de sommet programmable, qui est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 310d64170280053c34766f214969f78d66560ea3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011072"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.

La version du nuanceur de sommets et \_ 3 \_ 0 étend l’ensemble des fonctionnalités prises en charge par vs \_ 2 \_ x. Chacune des fonctionnalités de vs \_ 2 X nécessitant \_ une limite définie est disponible dans vs \_ 3 \_ 0 sans nécessiter d’extrémité.

-   [Instructions-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contient une liste des instructions disponibles.
-   [Registres-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.
-   Les [modificateurs de Registre du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers.md) permettent de modifier la façon dont une instruction fonctionne.
-   Les [modificateurs de Registre source du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.
-   Le [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.
-   Le [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) détermine les composants du registre de destination qui sont écrits.

## <a name="new-features"></a>Nouvelles fonctionnalités

Les nouvelles fonctionnalités de la version de nuanceur de sommets et \_ 3 \_ 0 sont répertoriées dans les sections suivantes.

### <a name="indexing-registers"></a>Indexation des registres

Dans les modèles de nuanceur précédents, seule la Banque de registres constantes peut être indexée. Dans ce modèle, les banques de registres suivantes peuvent être indexées à l’aide du registre de compteur de boucle (aL) :

-   Registre d’entrée (v \# )
-   Registre de sortie (o \# )

### <a name="vertex-textures"></a>Textures de vertex

Ce modèle de nuanceur prend en charge la recherche de texture dans le nuanceur vertex à l’aide de texldl. Le moteur de vertex a quatre étapes d’échantillonnage de texture (distinctes de l’échantillonneur de mappage de déplacement et les échantillonneurs de texture dans le moteur de pixels) qui peuvent être utilisés pour échantillonner des textures définies à ces étapes. Consultez [textures de vertex dans vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).

### <a name="vertex-stream-frequency"></a>Fréquence du flux de vertex

Cette fonctionnalité permet à un sous-ensemble des registres d’entrée d’être initialisés à un taux différent d’une fois par vertex. Consultez [dessin de géométrie non indexée](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).

### <a name="shader-output"></a>Sortie du nuanceur

Comme pour vs \_ 2 \_ 0, la sortie du nuanceur peut varier en fonction du contrôle de Flow statique. Soyez vigilant avec la branche dynamique, car cela peut entraîner une variation des sorties de nuanceur par vertex. Cela produira des résultats imprévisibles sur un matériel différent.

### <a name="dynamic-flow-control"></a>Contrôle de Flow dynamique

Toutes les instructions de contrôle de Flow dynamique sont prises en charge. La valeur de profondeur d’imbrication maximale autorisée est 24. (Pour plus d’informations, consultez [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .)

### <a name="temporary-registers"></a>Registres temporaires

Un total de 32 registres temporaires (r \# ) est pris en charge.

### <a name="static-flow-control"></a>Contrôle de Flow statique

La profondeur d’imbrication maximale pour [Loop-vs](loop---vs.md) / [REP-vs](rep---vs.md) est 4. La profondeur d’imbrication maximale pour [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz prédit-vs](callnz-pred---vs.md) est 4. Pour [si bool-vs](if-bool---vs.md), la valeur de profondeur d’imbrication maximale autorisée est 24. (Pour plus d’informations, consultez [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .)

### <a name="predication"></a>Prédicat

Le prédicat d’instruction est pris en charge. Utilisez [setp \_ COMP-vs](setp-comp---vs.md) pour définir le registre de prédicat.

### <a name="instruction-count"></a>Nombre d’instructions

Chaque nuanceur vertex est autorisé à partir de 512 jusqu’au nombre d’emplacements dans MaxVertexShader30InstructionSlots dans [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). Le nombre d’instructions exécutées peut être bien plus élevé en raison de la prise en charge de la boucle/REP ; Toutefois, cela est limité par MaxVShaderInstructionsExecuted dans D3DCAPS9, qui doit être au moins 0xFFFF.

### <a name="device-caps"></a>Cap de l’appareil

Si le nuanceur de sommets 3 \_ 0 est pris en charge, les limites suivantes sont prises en charge dans le matériel (au minimum) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Encapsul</th>
<th>Fonctionnalité</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bouchons de nuanceur</td>
<td><ul>
<li>DynamicFlowControlDepth est 24</li>
<li>NumTemps est 32</li>
<li>StaticFlowControlDepth est 4</li>
<li>Le prédicat est pris en charge.</li>
</ul></td>
</tr>
<tr class="even">
<td>GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</td>
<td>8 Ko</td>
</tr>
<tr class="odd">
<td>VertexShaderVersion</td>
<td>3_0</td>
</tr>
<tr class="even">
<td>MaxVertexShaderConst</td>
<td>256</td>
</tr>
<tr class="odd">
<td>MaxVertexShader30InstructionSlots</td>
<td>512</td>
</tr>
<tr class="even">
<td>Prise en charge du brouillard</td>
<td>D3DPRASTERCAPS_FOGVERTEX</td>
</tr>
<tr class="odd">
<td>VertexTextureFilterCaps</td>
<td><ul>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></td>
<td>Les éléments vertex dans une déclaration de vertex peuvent partager le même décalage de flux.</td>
</tr>
<tr class="odd">
<td>Formats de vertex</td>
<td><ul>
<li>D3DDECLTYPE_UBYTE4</li>
<li>D3DDECLTYPE_UBYTE4N</li>
<li>D3DDECLTYPE_SHORT2N</li>
<li>D3DDECLTYPE_SHORT4N</li>
<li>D3DDECLTYPE_FLOAT16_2</li>
<li>D3DDECLTYPE_FLOAT16_4</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs vertex](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 