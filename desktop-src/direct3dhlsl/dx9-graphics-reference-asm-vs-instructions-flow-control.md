---
title: Limites d’imbrication du contrôle de Flow
description: Les instructions de contrôle de workflow de nuanceur de sommets présentent deux restrictions spéciales.
ms.assetid: c9f80a97-8245-4974-a284-7974e2d2e504
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ebb5b491e074c2275081aa3fe629a2486a24c6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675861"
---
# <a name="flow-control-nesting-limits"></a>Limites d’imbrication du contrôle de Flow

Les instructions de contrôle de workflow de nuanceur de sommets présentent deux restrictions spéciales. Les profondeurs d’imbrication limitent le nombre d’instructions qui peuvent être appelées l’une à l’autre. En outre, chaque instruction a un nombre d’emplacements d’instructions qui s’applique au nombre maximal d’instructions qu’un nuanceur peut prendre en charge.

> [!Note]  
> Lorsque vous utilisez les \* \_ \_ \_ \_ \_ profils de nuanceur HLSL de 4 niveaux 9 x, vous utilisez implicitement les profils [Shader Model 2. x](dx-graphics-hlsl-sm2.md) pour prendre en charge le matériel compatible Direct3D 9. Les profils Shader Model 2. x prennent en charge un comportement de contrôle de Flow plus limité que le [modèle de nuanceur 4. x](dx-graphics-hlsl-sm4.md) et versions ultérieures.

 

## <a name="depth-count-per-instruction-for-vs_2_0"></a>Nombre de niveaux par instruction pour vs \_ 2 \_ 0

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Ce tableau indique le nombre de profondeurs que chaque instruction ajoute ou soustrait de la profondeur existante :



| Instruction                              | Imbrication statique | Imbrication dynamique | imbrication de boucles/REP | appeler l’imbrication | Nombre de flows statiques                        |
|------------------------------------------|----------------|-----------------|------------------|--------------|------------------------------------------|
| [Si bool-vs](if-bool---vs.md)         | 0              | 0               | 0                | 0            | 1                                        |
| [Si \_ COMP-vs](if-comp---vs.md)        | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [Si prédit-vs](if-pred---vs.md)         | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [else-vs](else---vs.md)               | 0              | 0               | 0                | 0            | 1 ([si bool-vs](if-bool---vs.md) uniquement) |
| [endif-vs](endif---vs.md)             | -1             | 0               | 0                | 0            | 0                                        |
| [REP-vs](rep---vs.md)                 | 0              | 0               | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0              | 0               | -1               | 0            | 0                                        |
| [boucle-vs](loop---vs.md)               | 0              | 0               | 1                | 0            | 1                                        |
| [ENDLOOP-vs](endloop---vs.md)         | 0              | 0               | -1               | 0            | 0                                        |
| [Break-vs](break---vs.md)             | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [arrêt \_ COMP-vs](break-comp---vs.md)  | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [breakp-vs](breakp---vs.md)           | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [appel-vs](call---vs.md)               | 0              | 0               | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0              | 0               | 0                | 1            | 1                                        |
| [callnz prédit-vs](callnz-pred---vs.md) | n/a            | n/a             | n/a              | n/a          | n/a                                      |
| [RET-vs](ret---vs.md)                 | 0              | 0               | 0                | -1           | 0                                        |
| [\_COMP setp-vs](setp-comp---vs.md)    | n/a            | n/a             | n/a              | n/a          | n/a                                      |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définissez le nombre d’instructions qui peuvent être appelées l’une à l’autre. Chaque type d’instruction a une ou plusieurs limites d’imbrication :



| Type d’instruction  | Maximale                               |
|-------------------|---------------------------------------|
| Imbrication statique    | Limité uniquement par le nombre de flows statiques |
| Imbrication dynamique   | n/a                                   |
| imbrication de boucles/REP  | 1                                     |
| appeler l’imbrication      | 1                                     |
| Nombre de flows statiques | 16                                    |



 

## <a name="depth-count-per-instruction-for-vs_2_x"></a>Nombre de niveaux par instruction pour vs \_ 2 \_ x

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Ce tableau indique le nombre de profondeurs que chaque instruction ajoute ou soustrait de la profondeur existante :



| Instruction                              | Imbrication statique                       | Imbrication dynamique                                                           | imbrication de boucles/REP | appeler l’imbrication | Nombre de flows statiques                        |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|------------------------------------------|
| [Si bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | 1                                        |
| [Si \_ COMP-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [Si prédit-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | 1 ([si bool-vs](if-bool---vs.md) uniquement) |
| [endif-vs](endif---vs.md)             | -1 ([si bool-vs](if-bool---vs.md)) | -1 ([si prédit-vs](if-pred---vs.md) ou [si \_ COMP-vs](if-comp---vs.md)) | 0                | 0            | 0                                        |
| [REP-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [boucle-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [arrêt \_ COMP-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | 0                                        |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [appel-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz prédit-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | 0                                        |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz prédit-vs](callnz-pred---vs.md))                             | 0                | -1           | 0                                        |
| [\_COMP setp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | 0                                        |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définissez le nombre d’instructions qui peuvent être appelées l’une à l’autre. Chaque type d’instruction a une ou plusieurs limites d’imbrication :



| Type d’instruction  | Maximale                                                                              |
|-------------------|--------------------------------------------------------------------------------------|
| Imbrication statique    | Limité uniquement par le nombre de flows statiques                                                |
| Imbrication dynamique   | 0 ou 24, consultez D3DCAPS9. VS20Caps.DynamicFlowControlDepth                               |
| imbrication de boucles/REP  | de 1 à 4, consultez D3DCAPS9. VS20Caps.StaticFlowControlDepth                                 |
| appeler l’imbrication      | de 1 à 4, consultez D3DCAPS9. VS20Caps. StaticFlowControlDepth (indépendant de la limite de boucle/REP) |
| Nombre de flows statiques | 16                                                                                   |



 

## <a name="depth-count-per-instruction-for-vs_2_sw"></a>Nombre de niveaux par instruction pour vs \_ 2 \_ SW

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Ce tableau indique le nombre de profondeurs que chaque instruction ajoute ou soustrait de la profondeur existante :



| Instruction                              | Imbrication statique                       | Imbrication dynamique                                                           | imbrication de boucles/REP | appeler l’imbrication | Nombre de flows statiques |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Si bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/a               |
| [Si \_ COMP-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [Si prédit-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [endif-vs](endif---vs.md)             | -1 ([si bool-vs](if-bool---vs.md)) | -1 ([si prédit-vs](if-pred---vs.md) ou [si \_ COMP-vs](if-comp---vs.md)) | 0                | 0            | n/a               |
| [REP-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [boucle-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [arrêt \_ COMP-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | n/a               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [appel-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz prédit-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/a               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz prédit-vs](callnz-pred---vs.md))                             | 0                | -1           | n/a               |
| [\_COMP setp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/a               |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définissez le nombre d’instructions qui peuvent être appelées l’une à l’autre. Chaque type d’instruction a une ou plusieurs limites d’imbrication :



| Type d’instruction  | Maximale  |
|-------------------|----------|
| Imbrication statique    | 24       |
| Imbrication dynamique   | 24       |
| imbrication de boucles/REP  | 4        |
| appeler l’imbrication      | 4        |
| Nombre de flows statiques | Aucune limite |



 

## <a name="depth-count-per-instruction-for-vs_3_0"></a>Nombre de niveaux par instruction pour vs \_ 3 \_ 0

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Ce tableau indique le nombre de profondeurs que chaque instruction ajoute ou soustrait de la profondeur existante :



| Instruction                              | Imbrication statique                       | Imbrication dynamique                                                           | imbrication de boucles/REP | appeler l’imbrication | Nombre de flows statiques |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Si bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/a               |
| [Si \_ COMP-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [Si prédit-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [endif-vs](endif---vs.md)             | -1 ([si bool-vs](if-bool---vs.md)) | -1 ([si prédit-vs](if-pred---vs.md) ou [si \_ COMP-vs](if-comp---vs.md)) | 0                | 0            | n/a               |
| [REP-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [boucle-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [arrêt \_ COMP-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | n/a               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [appel-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz prédit-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/a               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz prédit-vs](callnz-pred---vs.md))                             | 0                | -1           | n/a               |
| [\_COMP setp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/a               |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définissez le nombre d’instructions qui peuvent être appelées l’une à l’autre. Chaque type d’instruction a une ou plusieurs limites d’imbrication :



| Type d’instruction  | Maximale  |
|-------------------|----------|
| Imbrication statique    | 24       |
| Imbrication dynamique   | 24       |
| imbrication de boucles/REP  | 4        |
| appeler l’imbrication      | 4        |
| Nombre de flows statiques | Aucune limite |



 

## <a name="depth-count-per-instruction-for-vs_3_sw"></a>Nombre de niveaux par instruction pour vs \_ 3 \_ SW

Chaque instruction compte sur une ou plusieurs limites de profondeur d’imbrication. Ce tableau indique le nombre de profondeurs que chaque instruction ajoute ou soustrait de la profondeur existante :



| Instruction                              | Imbrication statique                       | Imbrication dynamique                                                           | imbrication de boucles/REP | appeler l’imbrication | Nombre de flows statiques |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Si bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | n/a               |
| [Si \_ COMP-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [Si prédit-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | n/a               |
| [else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [endif-vs](endif---vs.md)             | -1 ([si bool-vs](if-bool---vs.md)) | -1 ([si prédit-vs](if-pred---vs.md) ou [si \_ COMP-vs](if-comp---vs.md)) | 0                | 0            | n/a               |
| [REP-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [boucle-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | n/a               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | n/a               |
| [Break-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [arrêt \_ COMP-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | n/a               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | n/a               |
| [appel-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | n/a               |
| [callnz prédit-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | n/a               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz prédit-vs](callnz-pred---vs.md))                             | 0                | -1           | n/a               |
| [\_COMP setp-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | n/a               |



 

### <a name="nesting-depth"></a>Profondeur d’imbrication

Profondeur d’imbrication définissez le nombre d’instructions qui peuvent être appelées l’une à l’autre. Chaque type d’instruction a une ou plusieurs limites d’imbrication :



| Type d’instruction  | Maximale  |
|-------------------|----------|
| Imbrication statique    | 24       |
| Imbrication dynamique   | 24       |
| imbrication de boucles/REP  | 4        |
| appeler l’imbrication      | 4        |
| Nombre de flows statiques | Aucune limite |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




