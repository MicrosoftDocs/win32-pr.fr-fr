---
description: Une fonction est le bloc de construction d’un nuanceur créé dans le langage de haut niveau. Si vous préférez écrire des nuanceurs dans un langage de style C plutôt que dans un langage assembleur, vous souhaiterez peut-être écrire des fonctions.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Syntaxe des fonctions Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520908"
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

 

 
