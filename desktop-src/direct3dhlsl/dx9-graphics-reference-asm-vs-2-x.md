---
title: vs_2_x
description: Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463463"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.

La version du nuanceur de sommets vs \_ 2 \_ x étend l’ensemble des fonctionnalités prises en charge par vs \_ 2 \_ 0. Chaque fonctionnalité supplémentaire est représentée par une extrémité correspondante dans la structure [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dans [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps). Pour utiliser l’une des fonctionnalités améliorées représentées par ces majuscules, la version du nuanceur de sommets doit être spécifiée sous la forme vs \_ 2 \_ x.

-   [Instructions-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contient une liste des instructions disponibles.
-   [Registres-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.
-   Les [modificateurs de Registre du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers.md) permettent de modifier la façon dont une instruction fonctionne.
-   Les [modificateurs de Registre source du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.
-   Le [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.
-   Le [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) détermine les composants du registre de destination qui sont écrits.

## <a name="new-features"></a>Nouvelles fonctionnalités

Les nouvelles fonctionnalités sont les suivantes :

### <a name="dynamic-flow-control"></a>Contrôle de Flow dynamique

Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, les instructions de contrôle de workflow dynamique suivantes sont prises en charge :

-   [Si \_ COMP-vs](if-comp---vs.md)
-   [Break-vs](break---vs.md)
-   [arrêt \_ COMP-vs](break-comp---vs.md)

Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) est également défini, les instructions de contrôle de Flow supplémentaires suivantes sont prises en charge :

-   [\_COMP setp-vs](setp-comp---vs.md)
-   [Si prédit-vs](if-pred---vs.md)
-   [callnz prédit-vs](callnz-pred---vs.md)
-   [breakp-vs](breakp---vs.md)

La plage de valeurs pour la profondeur du contrôle de transmission dynamique est comprise entre 0 et 24 et est égale à la profondeur d’imbrication des instructions de contrôle de Flow dynamique (voir [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) pour plus d’informations). Si cette limite est égale à zéro, l’appareil ne prend pas en charge les instructions de contrôle de Flow dynamique.

### <a name="number-of-temporary-registers"></a>Nombre de registres temporaires

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) représente le nombre de [registres temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)pris en charge par l’appareil. La plage de valeurs de cette limite est comprise entre 12 et 32.

### <a name="static-flow-control-nesting-depth"></a>Profondeur d’imbrication du contrôle de Flow statique

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) représente la profondeur d’imbrication de deux types d’instructions de contrôle de Flow statique : [Loop-vs](loop---vs.md) / [REP-vs](rep---vs.md) et [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [If bool-vs](if-bool---vs.md). les instructions Loop-vs/REP-VS peuvent être imbriquées jusqu’à D3DVS20CAPS Deep. De manière indépendante, les instructions Call-vs/callnz bool-VS peuvent être imbriquées jusqu’à D3DVS20CAPS Deep. Si D3DVS20CAPS est également défini, [callnz prédit-vs](callnz-pred---vs.md) est compté vers la profondeur d’imbrication de l’appel-vs/callnz bool-vs/if bool-vs (voir [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) pour plus d’informations).

### <a name="predication"></a>Prédicat

Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) est défini, l’appareil prend en charge [setp \_ COMP-vs](setp-comp---vs.md) et la prédicat d’instruction. Si D3DVS20CAPS est également supérieur à 0, les instructions de contrôle de workflow dynamique supplémentaires suivantes sont prises en charge :

-   [Si prédit-vs](if-pred---vs.md)
-   [callnz prédit-vs](callnz-pred---vs.md)
-   [breakp-vs](breakp---vs.md)

### <a name="instruction-count"></a>Nombre d’instructions

Chaque nuanceur de sommets peut avoir jusqu’à 256 instructions stockées. Le nombre d’instructions exécutées peut être bien plus élevé (en raison de la prise en charge de la boucle/REP) et est limité par [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), qui doit être au moins 0xFFFF.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs vertex](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 