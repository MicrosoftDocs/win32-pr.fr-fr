---
description: Ces constantes sont utilisées lors de la création d’un effet pour définir le comportement de compilation ou le comportement de l’effet d’exécution.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: Constantes D3D10_EFFECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3738a95a843020f7c0f8af30e8c5d035f0a86ac7098d36cae422eb01ed4dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736048"
---
# <a name="d3d10_effect-constants"></a>\_Constantes d’effet D3D10

Ces constantes sont utilisées lors de la création d’un effet pour définir le comportement de compilation ou le comportement de l’effet d’exécution.



| \#définition                                 | Valeur        | Description                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Effet D3D10 compiler l’effet \_ \_ \_ enfant \_    | 1 << 0 | Compilez le fichier. FX à un effet enfant. Les effets enfants n’ont aucune initialisation pour les valeurs partagées, car celles-ci sont initialisées dans le pool d’effets.                                                                                                           |
| D3D10 \_ effet \_ compiler \_ autoriser \_ les \_ opérations lentes | 1 << 1 | Par défaut, le mode de performance est activé. Le mode de performance interdit les objets d’État mutable en empêchant les expressions non littérales d’apparaître dans les définitions d’objets d’État. La spécification de cet indicateur désactivera le mode et autorisera les objets d’État mutable. |
| D3D10 \_ effet \_ à \_ thread unique          | 1 << 3 | N’essayez pas de synchroniser avec d’autres threads qui chargent des effets dans le même pool.                                                                                                                                                                        |



 

Ces constantes sont définies en tant que macros dans d3d10effect. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets, constantes (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



