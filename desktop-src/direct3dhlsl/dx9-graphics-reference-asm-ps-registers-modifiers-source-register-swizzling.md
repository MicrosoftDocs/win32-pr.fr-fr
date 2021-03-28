---
title: Registre source swizzling (référence du PS HLSL)
description: Swizzling fait référence à la capacité de copier n’importe quel composant Registre source vers un composant de registre temporaire. Swizzling n’affecte pas les données du Registre source. Avant l’exécution d’une instruction, les données d’un registre source sont copiées dans un registre temporaire.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313792"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>Registre source swizzling (référence du PS HLSL)

Swizzling fait référence à la capacité de copier n’importe quel composant Registre source vers un composant de registre temporaire. Swizzling n’affecte pas les données du Registre source. Avant l’exécution d’une instruction, les données d’un registre source sont copiées dans un registre temporaire.

## <a name="source-swizzling"></a>Swizzling source

La source Swizzle permet à un composant individuel d’un registre source de prendre la valeur de l’un des quatre composants du même registre source avant que le registre ne soit lu pour le calcul.

Par exemple, le Swizzle. zxxy signifie :

-   le composant. x prendra la valeur du composant. z
-   le composant. y prendra la valeur du composant. x
-   le composant. z prendra la valeur du composant. x
-   . w le composant prendra la valeur du composant. y

Les composants peuvent apparaître dans n’importe quel ordre. Si moins de quatre composants sont spécifiés, le dernier composant est répété. Par exemple :


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



Si aucun composant n’est spécifié, aucun swizzling n’est appliqué.

Certaines instructions présentent des restrictions pour les Swizzle sources. Ils sont répertoriés dans les pages de référence des instructions respectées.



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . z                    | x\*  | x\*  | x\*  | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . XYZW (par défaut)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .wzyx                 |      |      |      |      | x    | x    | x     | x    | x     |
| Swizzle arbitraire     |      |      |      |      |      | x    | x     | x    | x     |



 

\* Disponible uniquement si le masque d’écriture de destination est. w (. a).

## <a name="arbitrary-swizzle"></a>Swizzle arbitraire

Les Swizzles peuvent être appliqués aux registres sources dans un ordre arbitraire. autrement dit, tout registre source peut prendre n’importe quel masque de composant, dans n’importe quel ordre.

## <a name="replicate-swizzle"></a>Répliquer Swizzle

Répliquer Swizzle copie un composant vers un autre. Il s’agit d’un seul des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalent) doit être spécifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[registres PS 1 \_ \_ 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ 3 PS 1 \_ \_ \_ \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[\_registres PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[\_registres PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[\_registres PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




