---
description: Une fonction est le bloc de construction d’un nuanceur créé dans le langage de haut niveau. Si vous préférez écrire des nuanceurs dans un langage de style C plutôt que dans un langage assembleur, vous souhaiterez peut-être écrire des fonctions.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Syntaxe des fonctions Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9de680f2f892e59f49e1dfd0850a128ca9ba34e2588e416059251d5058c44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297107"
---
# <a name="effect-function-syntax-direct3d-9"></a>Syntaxe des fonctions Effect (Direct3D 9)

Une fonction est le bloc de construction d’un nuanceur créé dans le langage de haut niveau. Si vous préférez écrire des nuanceurs dans un langage de style C plutôt que dans un langage assembleur, vous souhaiterez peut-être écrire des fonctions.

## <a name="syntax"></a>Syntaxe


```
type id ( [ parameters ] )  
    { body }
```



Les fonctions ne modifient pas les valeurs de paramètre dans un effet.

-   type : toute [référence valide pour](../direct3dhlsl/dx-graphics-hlsl-reference.md) le type HLSL.
-   ID : nom unique.
-   paramètres : paramètres de fonction.
-   Body : corps de la fonction.

Les fonctions sont générées à partir du langage de haut niveau. Consultez [référence pour le langage HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
