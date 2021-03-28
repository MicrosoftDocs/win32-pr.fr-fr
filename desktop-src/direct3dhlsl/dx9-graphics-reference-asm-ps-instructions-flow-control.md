---
title: Limitations du contrôle de Flow
description: Les instructions de contrôle de workflow de nuanceur de pixels ont des limites affectant le nombre de niveaux d’imbrication pouvant être inclus dans les instructions. En outre, il existe certaines limitations relatives à l’implémentation du contrôle de Flow par pixel avec des instructions de dégradé.
ms.assetid: 17a902cd-16a4-4065-9249-01f9b1f40506
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34891e29a1bb27aead629db2cc7473c7d4329af5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840845"
---
# <a name="flow-control-limitations"></a>Limitations du contrôle de Flow

Les instructions de contrôle de workflow de nuanceur de pixels ont des limites affectant le nombre de niveaux d’imbrication pouvant être inclus dans les instructions. En outre, il existe certaines limitations relatives à l’implémentation du contrôle de Flow par pixel avec des instructions de dégradé.

> [!Note]  
> Lorsque vous utilisez les \* \_ \_ \_ \_ \_ profils de nuanceur HLSL de 4 niveaux 9 x, vous utilisez implicitement les profils [Shader Model 2. x](dx-graphics-hlsl-sm2.md) pour prendre en charge le matériel compatible Direct3D 9. Les profils Shader Model 2. x prennent en charge un comportement de contrôle de Flow plus limité que le [modèle de nuanceur 4. x](dx-graphics-hlsl-sm4.md) et versions ultérieures.

 

-   [Nombre de niveaux de profondeur des instructions de nuanceur de pixels](#pixel-shader-instruction-depth-counts)
-   [Interaction d' Per-Pixel contrôle de Flow avec des dégradés d’écran](#interaction-of-per-pixel-flow-control-with-screen-gradients)

## <a name="pixel-shader-instruction-depth-counts"></a>Nombre de niveaux de profondeur des instructions de nuanceur de pixels

PS \_ 2 \_ 0 ne prend pas en charge le contrôle de Flow. Les limitations pour les autres versions de nuanceur de pixels sont répertoriées ci-dessous.

### <a name="instruction-depth-count-for-ps_2_x"></a>Nombre de profondeur d’instruction pour PS \_ 2 \_ x

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Le tableau suivant répertorie le nombre de profondeur que chaque instruction ajoute ou soustrait de la profondeur existante.



| Instruction                              | Imbrication statique                       | Imbrication dynamique                                                           | imbrication de boucles/REP | appeler l’imbrication |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Si bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Si \_ COMP-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Si prédit-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([si bool-PS](if-bool---ps.md)) | -1 ([si prédit-PS](if-pred---ps.md) ou [si \_ COMP-PS](if-comp---ps.md)) | 0                | 0            |
| [REP-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [arrêter \_ COMP-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [appeler-PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz prédit-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz prédit-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ COMP-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définit le nombre d’instructions qui peuvent être appelées à l’intérieur les unes des autres. Chaque type d’instruction a une ou plusieurs limites d’imbrication comme indiqué dans le tableau suivant.



| Type d’instruction | Maximale                                                                                   |
|------------------|-------------------------------------------------------------------------------------------|
| Imbrication statique   | 24 si (D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth > 0); 0 sinon            |
| Imbrication dynamique  | de 0 à 24, consultez D3DCAPS9. D3DPSHADERCAPS2 \_ 0. DynamicFlowControlDepth                          |
| imbrication des REP      | de 0 à 4, consultez D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth                            |
| appeler l’imbrication     | de 0 à 4, consultez D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth (indépendant de la limite du REP) |



 

### <a name="instruction-depth-count-for-ps_2_sw"></a>Nombre de profondeur d’instruction pour les \_ logiciels PS 2 \_

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Ce tableau indique le nombre de profondeur que chaque instruction ajoute ou soustrait de la profondeur existante.



| Instruction                              | Imbrication statique                       | Imbrication dynamique                                                           | imbrication de boucles/REP | appeler l’imbrication |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Si bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Si prédit-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Si \_ COMP-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([si bool-PS](if-bool---ps.md)) | -1 ([si prédit-PS](if-pred---ps.md) ou [si \_ COMP-PS](if-comp---ps.md)) | 0                | 0            |
| [REP-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [boucle-PS](loop---ps.md)               | n/a                                  | n/a                                                                       | n/a              | n/a          |
| [ENDLOOP-PS](endloop---ps.md)         | n/a                                  | n/a                                                                       | n/a              | n/a          |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [arrêter \_ COMP-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [appeler-PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz prédit-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz prédit-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ COMP-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définit le nombre d’instructions qui peuvent être appelées de l’une à l’autre. Chaque type d’instruction a une ou plusieurs limites d’imbrication comme indiqué dans le tableau suivant.



| Type d’instruction | Maximale |
|------------------|---------|
| Imbrication statique   | 24      |
| Imbrication dynamique  | 24      |
| imbrication des REP      | 4       |
| appeler l’imbrication     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_0"></a>Nombre de profondeur d’instruction pour PS \_ 3 \_ 0

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Ce tableau indique le nombre de profondeur que chaque instruction ajoute ou soustrait de la profondeur existante.



| Instruction                              | Imbrication statique                       | Imbrication dynamique                                                           | imbrication de boucles/REP | appeler l’imbrication |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Si bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Si prédit-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Si \_ COMP-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([si bool-PS](if-bool---ps.md)) | -1 ([si prédit-PS](if-pred---ps.md) ou [si \_ COMP-PS](if-comp---ps.md)) | 0                | 0            |
| [REP-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [boucle-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [ENDLOOP-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [arrêter \_ COMP-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [appeler-PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz prédit-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz prédit-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ COMP-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définit le nombre d’instructions qui peuvent être appelées de l’une à l’autre. Chaque type d’instruction a une ou plusieurs limites d’imbrication comme indiqué dans le tableau suivant.



| Type d’instruction | Maximale |
|------------------|---------|
| Imbrication statique   | 24      |
| Imbrication dynamique  | 24      |
| imbrication de boucles/REP | 4       |
| appeler l’imbrication     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_sw"></a>Nombre de profondeur d’instruction pour les \_ logiciels PS 3 \_

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Ce tableau indique le nombre de profondeur que chaque instruction ajoute ou soustrait de la profondeur existante.



| Instruction                              | Imbrication statique                       | Imbrication dynamique                                                           | imbrication de boucles/REP | appeler l’imbrication |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Si bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Si prédit-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Si \_ COMP-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([si bool-PS](if-bool---ps.md)) | -1 ([si prédit-PS](if-pred---ps.md) ou [si \_ COMP-PS](if-comp---ps.md)) | 0                | 0            |
| [REP-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [boucle-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [ENDLOOP-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [arrêter \_ COMP-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [appeler-PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz prédit-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz prédit-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ COMP-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définit le nombre d’instructions qui peuvent être appelées de l’une à l’autre. Chaque type d’instruction a une ou plusieurs limites d’imbrication comme indiqué dans le tableau suivant.



| Type d’instruction | Maximale |
|------------------|---------|
| Imbrication statique   | 24      |
| Imbrication dynamique  | 24      |
| imbrication de boucles/REP | 4       |
| appeler l’imbrication     | 4       |



 

## <a name="interaction-of-per-pixel-flow-control-with-screen-gradients"></a>Interaction d' Per-Pixel contrôle de Flow avec des dégradés d’écran

Le jeu d’instructions de nuanceur de pixels comprend plusieurs instructions qui produisent ou utilisent des dégradés de quantités par rapport à l’espace d’écran x et y. L’utilisation la plus courante pour les dégradés consiste à calculer les calculs de niveau de détail pour l’échantillonnage de texture et, dans le cas du filtrage anisotrope, à sélectionner des échantillons le long de l’axe de l’anisotropie. En règle générale, les implémentations matérielles exécutent le nuanceur de pixels simultanément sur plusieurs pixels (par exemple, une grille 2x2), de sorte que les dégradés de quantités calculées dans le nuanceur peuvent être raisonnablement approchés comme des deltas des valeurs au même point d’exécution, en pixels adjacents.

Lorsque le contrôle de Flow est présent dans un nuanceur, le résultat d’un calcul de dégradé demandé dans un chemin de branche donné est ambigu quand des pixels adjacents peuvent exécuter des chemins de contrôle de Flow distincts. Par conséquent, il est jugé illégal d’utiliser toute opération de nuanceur de pixels qui demande un calcul de dégradé à un emplacement qui se trouve à l’intérieur d’une construction de contrôle de Flow qui peut varier d’un pixel à l’autre, pour une primitive donnée en cours de pixellisation.

Toutes les instructions de nuanceur de pixels sont partitionnées dans les opérations autorisées et dans celles qui ne sont pas autorisées à l’intérieur d’un contrôle de flow :

-   Scénario A : opérations qui ne sont pas autorisées dans un contrôle de Flow qui peut varier entre les pixels d’une primitive. Celles-ci incluent les opérations indiquées dans le tableau suivant. 

    | Instruction                                                                                                      | Est autorisé dans le contrôle de Flow lorsque :                       |
    |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) et [texldp-PS](texldp---ps.md) | Un registre temporaire est utilisé pour la coordonnée de texture. |
    | [DSX-PS](dsx---ps.md) et [DSY-PS](dsy---ps.md)                                                            | Un registre temporaire est utilisé pour l’opérande.            |

    

     

-   Scénario B : opérations autorisées n’importe où. Celles-ci incluent les opérations indiquées dans le tableau suivant. 

    | Instruction                                                                                                      | Est autorisé n’importe où lorsque :                                                                                             |
    |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) et [texldp-PS](texldp---ps.md) | Une quantité en lecture seule est utilisée pour la coordonnée de texture (peut varier selon le pixel, par exemple les coordonnées de texture interpolée). |
    | [DSX-PS](dsx---ps.md) et [DSY-PS](dsy---ps.md)                                                            | Une quantité en lecture seule est utilisée pour l’opérande d’entrée (peut varier par pixel, par exemple les coordonnées de texture interpolée).      |
    | [texldl-PS](texldl---ps.md)                                                                                   | L’utilisateur fournit un niveau de détail comme argument, il n’y a donc pas de dégradés et donc aucun problème avec le contrôle de Flow.       |
    | [texldd-PS](texldd---ps.md)                                                                                   | L’utilisateur fournit des dégradés comme arguments d’entrée, ce qui signifie qu’il n’y a aucun problème avec le contrôle de Flow.                                 |

    

     

Ces restrictions sont strictement appliquées dans la validation du nuanceur. Les scénarios avec une condition de branche qui ressemble à une branche est cohérente dans une primitive, bien qu’un opérande dans l’expression de condition soit une quantité calculée par nuanceur de pixels, mais toujours dans le scénario A et ne sont pas autorisés. De même, les scénarios dans lesquels des dégradés sont demandés sur certaines quantités calculées par le nuanceur x à partir de l’intérieur du contrôle de transit dynamique, mais qui semblent que x n’est pas modifié dans l’une des branches, continuent de tomber dans le scénario A et ne sont pas autorisés.

Le prédicat est inclus dans ces restrictions sur le contrôle de Flow, afin que les implémentations restent libres d’échanger de manière triviale l’implémentation des instructions de branche avec des instructions prédicats.

L’utilisateur peut utiliser les instructions des scénarios A et B ensemble. Supposons, par exemple, que l’utilisateur a besoin d’un échantillon de texture anisotrope en fonction d’une coordonnée de texture calculée de nuanceur. Toutefois, la charge de texture n’est nécessaire que pour les pixels répondant à une condition par pixel. Pour répondre à ces exigences, l’utilisateur peut calculer la coordonnée de texture pour tous les pixels, en dehors du contrôle de déroulement par pixel variable, en calculant immédiatement les dégradés à l’aide des instructions [DSX-PS](dsx---ps.md) et [DSY-PS](dsy---ps.md) . Ensuite, dans un pixel par pixel [si bool-PS](if-bool---ps.md) / [endif-PS](endif---ps.md) Block, l’utilisateur peut utiliser [texldd-PS](texldd---ps.md) (charge de texture avec des dégradés fournis par l’utilisateur), en passant les dégradés précalculés. Une autre façon de décrire ce modèle d’utilisation est que, tandis que tous les pixels de la primitive devaient calculer les coordonnées de la texture et être impliqués dans le calcul du dégradé, seuls les pixels nécessaires à l’échantillonnage d’une texture ont fait cela.

Indépendamment de ces règles, la charge est toujours sur l’utilisateur pour s’assurer qu’avant de calculer un dégradé (ou d’effectuer un exemple de texture qui calcule implicitement un dégradé), le registre contenant les données sources doit avoir été initialisé pour tous les chemins d’exécution au préalable. L’initialisation des registres temporaires n’est pas validée ou appliquée en général.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




