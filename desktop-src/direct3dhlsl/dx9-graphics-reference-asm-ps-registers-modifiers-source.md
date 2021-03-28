---
title: Modificateurs de Registre source du nuanceur de pixels
description: Utilisez les modificateurs de Registre source pour modifier la valeur lue dans un registre avant l’exécution d’une instruction.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311491"
---
# <a name="pixel-shader-source-register-modifiers"></a>Modificateurs de Registre source du nuanceur de pixels

Utilisez les modificateurs de Registre source pour modifier la valeur lue dans un registre avant l’exécution d’une instruction. Le contenu d’un registre source reste inchangé. Les modificateurs sont utiles pour ajuster la plage de données de registre en vue de la préparation de l’instruction. Un ensemble de modificateurs appelés sélecteurs copie ou réplique les données à partir d’un seul canal (r, g, b, a) dans les autres canaux.

## <a name="ps_1_1---ps_1_4"></a>PS \_ 1 \_ 1-PS \_ 1 \_ 4

Ce tableau identifie les versions qui prennent en charge chaque modificateur :



| Modificateurs de Registre source                                                                                    | Syntaxe         | Version |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |     |     |
| [biais](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | inscrire un \_ décalage | X       | X    | X    | X    |     |     |
| [alternatif](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1-s’inscrire   | X       | X    | X    | X    |     |     |
| [negate](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- annuler    | X       | X    | X    | X    |     |     |
| [mettre à l’échelle par 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | inscrire \_ x2   |         |      |      | X    |     |     |
| [mise à l’échelle signée](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | inscrire \_ BX2  | X       | X    | X    | X    |     |     |
| [modificateurs texld et texcrd](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | inscrire \_ d\*  | X       | X    | X    | X    |     |     |
| [Registre source swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | Register. XYZW  | X       | X    | X    | X    |     |     |



 

Les modificateurs de Registre source ne peuvent être utilisés que sur des instructions arithmétiques. Elles ne peuvent pas être utilisées sur des instructions d’adresse de texture. L’exception est le modificateur [Scale de 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) . Pour la version 1 \_ 1, la mise à l’échelle signée peut être utilisée sur l’argument source de toute \* instruction texm. Pour la version 1 \_ 2 ou 1 \_ 3, l’échelle signée peut être utilisée sur l’argument source d’une instruction d’adresse de texture.

Restrictions spécifiques aux modificateurs :

-   L’inverse peut être associé à l’écart, à la mise à l’échelle signée ou au modificateur scalex2. En cas de combinaison, la négation est exécutée en dernier.
-   Inverser ne peut pas être combiné avec un autre modificateur.
-   Inverser, inverser, écarter, mettre à l’échelle signée et scalex2 peuvent être combinés avec l’un des sélecteurs.
-   Les modificateurs de Registre source ne doivent pas être utilisés sur des registres constants, car ils entraînent des résultats indéfinis. Pour la version 1 \_ 4, les modificateurs sur les constantes ne sont pas autorisés et ne pourront pas être validés.

## <a name="ps_2_0-and-above"></a>PS \_ 2 \_ 0 et versions ultérieures

Pour la version PS \_ 2 \_ et les versions, le nombre de modificateurs a été simplifié.

### <a name="negate"></a>Negate

Nie le contenu du Registre source.



| Modificateur de composant | Description     |
|--------------------|-----------------|
| \- r               | Négation source |



 

Le modificateur de négation ne peut pas être utilisé dans le deuxième Registre source de ces instructions : [M3X2-PS](m3x2---ps.md), [M3x3-](m3x3---ps.md)PS, [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)et [M4X4-PS](m4x4---ps.md).



| Versions de nuanceur de pixels | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>Valeur absolue

Prenez la valeur absolue du Registre.



| Versions de nuanceur de pixels | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

Si un nuanceur de version 3 lit à partir d’un ou de plusieurs registres à virgule flottante constants (c \# ), l’une des conditions suivantes doit être vraie.

-   Tous les registres à virgule flottante constantes doivent utiliser le modificateur ABS.
-   Aucun des registres à virgule flottante constantes ne peut utiliser le modificateur ABS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de registre de nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




