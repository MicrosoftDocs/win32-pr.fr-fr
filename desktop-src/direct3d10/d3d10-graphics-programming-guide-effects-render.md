---
description: En savoir plus sur le rendu d’un effet pour Direct3D 10. Un effet peut être utilisé pour stocker des informations ou pour effectuer un rendu à l’aide d’un groupe d’États.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendu d’un effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262571"
---
# <a name="rendering-an-effect-direct3d-10"></a>Rendu d’un effet (Direct3D 10)

Un effet peut être utilisé pour stocker des informations ou pour effectuer un rendu à l’aide d’un groupe d’États. Chaque technique spécifie les nuanceurs de vertex, les nuanceurs de géométrie, les nuanceurs de pixels, l’état du nuanceur, l’échantillonnage et l’état de la texture, ainsi que l’état du pipeline. Ainsi, une fois que vous avez organisé l’État en conséquence, vous pouvez encapsuler l’effet de rendu résultant de cet État en créant et en rendant l’effet.

Il existe quelques étapes pour préparer un effet pour le rendu. La première consiste à compiler, qui vérifie le code HLSL comme par rapport à la syntaxe du langage HLSL et aux règles de l’infrastructure d’effet. Vous pouvez compiler un effet à partir de votre application à l’aide d’appels d’API ou vous pouvez compiler un effet hors connexion à l’aide de l’utilitaire Effect compiler. Une fois que votre effet a été compilé avec succès, créez-le en appelant un ensemble d’API différent (mais très similaire).

Une fois l’effet créé, il y a deux étapes restantes pour l’utiliser. Tout d’abord, vous devez initialiser les valeurs d’état des effets (les valeurs des variables d’effet) à l’aide d’un certain nombre de méthodes pour définir l’État. Pour certaines variables, cette opération peut être effectuée une fois lors de la création d’un effet ; d’autres doivent être mis à jour chaque fois que votre application appelle la boucle de rendu. Une fois les variables d’effet définies, vous indiquez au runtime d’afficher les effets en appliquant une technique. Ces rubriques sont abordées plus en détail ci-dessous.

-   [Compiler un effet (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Créer un effet (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Définir l’état de l’effet (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Appliquer une technique (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Naturellement, il existe des [considérations relatives aux performances](d3d10-graphics-programming-guide-effects-performance.md) pour l’utilisation des effets. Ces considérations sont en grande partie les mêmes si vous n’utilisez pas d’effet. Par exemple, la réduction du nombre de modifications d’État ou l’Organisation des variables qui doivent être mises à jour par fréquence. Ces tactiques permettent de réduire la quantité de données qui doivent être envoyées du processeur au GPU, et donc de réduire les problèmes potentiels de synchronisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



