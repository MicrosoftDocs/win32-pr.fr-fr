---
title: Registre des couleurs d’entrée
description: Registre d’entrée de nuanceur de pixels contenant la couleur du vertex.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcabc6dcf5043c23be252fe6ac25c99da505e33b7c670c95ee5672b50ddb74bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744629"
---
# <a name="input-color-register"></a>Registre des couleurs d’entrée

Registre d’entrée de nuanceur de pixels contenant la couleur du vertex.

## <a name="syntax"></a>Syntaxe


```
dcl v#.writeMask
```



où :

-   [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) est une instruction de déclaration de registre.
-   v est un registre d’entrée et \# est le numéro du Registre. Le nombre de registres autorisés est déterminé par la version du nuanceur.
-   writeMask détermine les composants (jusqu’à quatre) qui sont écrits. Les composants valides sont : (x, y, z, w) ou (r, g, b, a).

## <a name="remarks"></a>Remarques

Les registres de couleurs sont des registres en lecture seule. Chaque registre contient des valeurs RVBA à quatre composants itérées à partir des vertex d’entrée. Ils ont une précision inférieure à la plupart des registres, garanti qu’ils disposent de 8 bits de données non signées dans la plage (0, + 1). Vous ne pouvez pas en utiliser plusieurs dans une seule instruction.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[registres PS 1 \_ \_ 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ 3 PS 1 \_ \_ \_ \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[\_registres PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[\_registres PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[\_registres PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




