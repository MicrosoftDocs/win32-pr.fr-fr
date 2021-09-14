---
title: Registre des couleurs de sortie
description: Les registres de sortie de couleur de nuanceur de pixels (oC \) sont des registres en écriture seule qui génèrent les résultats dans plusieurs cibles de rendu.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232307"
---
# <a name="output-color-register"></a>Registre des couleurs de sortie

Les registres de sortie de couleur de nuanceur de pixels (oC #) sont des registres en écriture seule qui génèrent les résultats dans plusieurs cibles de rendu.

Syntax



| c # |
|------|



 

Où :



| Nom | Description       |
|------|-------------------|
| oC0  | cible de rendu \# 0 |
| oC1  | cible de rendu \# 1 |
| oC2  | cible de rendu \# 2 |
| oC3  | cible de rendu \# 3 |



 

## <a name="remarks"></a>Remarques

-   Si oCn est écrit, mais qu’il n’existe aucune cible de rendu correspondante, cette écriture dans oCn est ignorée.
-   Les États de rendu D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 et D3DRS \_ COLORWRITEENABLE3 déterminent les composants de oCn qui sont finalement écrits dans la cible de rendu (après Blend, le cas échéant). Si le nuanceur écrit, mais pas tous les composants définis par les \_ \* États de rendu D3DRS COLORWRITEENABLE pour un registre oCn donné, les canaux non écrits produisent des valeurs non définies dans la cible de rendu correspondante. Si aucun des composants d’un oCn n’est écrit, la cible de rendu correspondante ne doit pas être mise à jour (comme indiqué ci-dessus), de sorte que les \_ États de rendu D3DRS COLORWRITEENABLE \* ne s’appliquent pas.

### <a name="shader-model-2-restrictions"></a>Restrictions du modèle de nuanceur 2

-   oCn peut uniquement être écrit avec l’instruction [MOV-PS](mov---ps.md) .
-   oC0 doit toujours être écrit dans le nuanceur.
-   Aucun Swizzle source (sauf. XYZW = default Swizzle) ou le modificateur source n’est autorisé lors de l’écriture dans un oCn.
-   Aucun masque d’écriture de destination (à l’exception de XYZW = masque par défaut) ou modificateur d’instruction n’est autorisé lors de l’écriture dans un oCn.
-   Si oCn est écrit, oC0-oCn-1 doit également être écrit. Par exemple, pour écrire dans oC2, vous devez également écrire dans oC0 et oC1.
-   Au plus une écriture vers n’importe quel nuanceur oC par nuanceur est autorisé.
-   Pour PS \_ 2 \_ x et PS \_ 3 \_ 0, vous ne pouvez pas écrire dans les registres OC # et OD \# au sein d’un contrôle de workflow dynamique ou d’un prédicat (les écritures dans le contrôle de workflow statique ne sont pas correctes).

### <a name="shader-model-3-restrictions"></a>Restrictions du modèle de nuanceur 3

-   Pour PS \_ 3 \_ 0, les registres de sortie OC # et OD \# peuvent être écrits un nombre quelconque de fois. La sortie du nuanceur de pixels provient du contenu des registres de sortie à la fin de l’exécution du nuanceur. Si une écriture dans un registre de sortie ne se produit pas, peut-être en raison du contrôle de la transmission ou si le nuanceur ne l’a pas écrit, le renderTarget correspondant n’est pas non plus mis à jour. Si un sous-ensemble des canaux d’un registre de sortie est écrit, les valeurs non définies sont écrites sur les autres canaux.
-   Pour PS \_ 3 \_ 0, les registres OC # peuvent être écrits avec n’importe quel writemasks.
-   Pour PS \_ 2 \_ x et PS \_ 3 \_ 0, vous ne pouvez pas écrire dans les registres OC # et OD \# au sein d’un contrôle de workflow dynamique ou d’un prédicat (les écritures dans le contrôle de workflow statique ne sont pas correctes).
-   Vous n’êtes pas autorisé à effectuer des calculs de dégradés (ou des opérations qui appellent implicitement des calculs de gradient tels que [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) à l’intérieur d’instructions de contrôle de Flow dont les conditions de création de branche varient en fonction de la primitive (c’est-à-dire : instructions de contrôle de workflow dynamique). La prédicat d’instruction n’est pas considéré comme un contrôle de workflow dynamique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Plusieurs cibles de rendu (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 