---
title: Registre de profondeur de sortie
description: Le registre de profondeur de sortie du nuanceur de pixels (oDepth) est un registre scalaire en écriture seule avec la plage \ 0.. 1 \ qui retourne une nouvelle valeur de profondeur pour un test de profondeur par rapport à la mémoire tampon du stencil de profondeur.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 041ffccb3301831c91554ef3cda835d3f2e79204730e838b25f26660e76d9a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119723"
---
# <a name="output-depth-register"></a>Registre de profondeur de sortie

Le registre de profondeur de sortie du nuanceur de pixels (oDepth) est un registre scalaire en écriture seule avec la plage \[ 0.. 1 \] qui retourne une nouvelle valeur de profondeur pour un test de profondeur par rapport à la mémoire tampon du stencil de profondeur.

Syntaxe



| oDepth |
|--------|



 

Où :



| Nom   | Description                                                       |
|--------|-------------------------------------------------------------------|
| oDepth | Nouvelle valeur de profondeur pour un test de profondeur par rapport à la mémoire tampon du stencil de profondeur |



 

Il est important de savoir que l’écriture dans oDepth provoque la perte des algorithmes d’optimisation de la mémoire tampon de profondeur matérielle (Z) qui accélèrent les performances des tests de profondeur.

REPLICATE source Swizzle (. x.y. \| \| z. z \| ) est requis lors de l’écriture dans oDepth. Les masques d’écriture explicites ne sont pas autorisés.

L’écriture dans le registre oDepth remplace la valeur de profondeur interpolée (et ignore tous les décalages de profondeur/slopescale renderstates). Si aucune mémoire tampon de profondeur n’a été créée ou attachée à l’appareil, l’écriture dans oDepth est ignorée.

Si vous effectuez un échantillonnage multiple et écrivez dans oDepth, étant donné que le nuanceur de pixels ne s’exécute qu’une seule fois par pixel, la valeur de votre profondeur est répliquée pour tous les emplacements sous-échantillons couverts. Le test de profondeur se produit toujours par échantillon, mais vous n’avez pas de valeur de profondeur par exemple dans la comparaison du nuanceur de pixels comme vous le feriez si vous n’aviez pas écrit de oDepth.

Si une application a une mémoire tampon w définie en tant que tampon de profondeur, elle doit en tenir compte lors de l’écriture dans oDepth. Il doit éventuellement envoyer des informations w-Range au nuanceur de pixels et calculer la plage w pour mettre à l’échelle les valeurs w écrites sur oDepth.

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>\_restrictions PS 2 \_ 0 et PS \_ 2 \_ x

-   oDepth peut uniquement être écrit avec l’instruction [MOV-PS](mov---ps.md) et ne peut être fait qu’une seule fois.
-   Aucun modificateur source n’est autorisé lors de l’écriture dans oDepth.
-   Aucun modificateur d’instruction n’est autorisé lors de l’écriture dans oDepth.
-   Aucune écriture dans oDepth à partir d’une construction de contrôle de Flow, ou lors de l’utilisation d’un prédicat.

### <a name="ps_3_0-restrictions"></a>\_restrictions PS 3 \_ 0

-   Pour PS \_ 3 \_ 0, les registres de sortie OC # et OD \# peuvent être écrits un nombre quelconque de fois. La sortie du nuanceur de pixels provient du contenu des registres de sortie à la fin de l’exécution du nuanceur. Si une écriture dans un registre de sortie ne se produit pas, peut-être en raison du contrôle de flow ou si le nuanceur ne l’a pas écrit, la cible de rendu correspondante n’est pas non plus mise à jour. Si un sous-ensemble des canaux d’un registre de sortie est écrit, les valeurs non définies sont écrites sur les autres canaux.
-   Vous pouvez écrire dans oDepth dans un contrôle de flow ou un prédicat, à condition que tous les chemins d’accès possibles écrivent dans le registre.
-   Vous n’êtes pas autorisé à effectuer des calculs de dégradés (ou des opérations qui appellent implicitement des calculs de gradient tels que [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) à l’intérieur d’instructions de contrôle de Flow dont les conditions de création de branche varient en fonction de la primitive (c’est-à-dire : instructions de contrôle de workflow dynamique). La prédicat d’instruction n’est pas considéré comme un contrôle de workflow dynamique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscrit](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




