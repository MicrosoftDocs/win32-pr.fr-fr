---
description: En savoir plus sur les effets Direct3D 10. Un effet est l’état du pipeline, défini par des expressions écrites en HLSL et une syntaxe spécifique à l’infrastructure d’effet.
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: Effets (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70a9a863fd34c5bb99389139d09860812b16b4fa
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010912"
---
# <a name="effects-direct3d-10"></a>Effets (Direct3D 10)

Un effet DirectX est une collection d’États de pipeline, définie par des expressions écrites en [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) et une syntaxe spécifique à l’infrastructure Effect. Après avoir compilé un effet, utilisez les API d’infrastructure Effects pour effectuer le rendu. Les fonctionnalités d’effet peuvent aller d’un point de vue simple à un nuanceur de sommets qui transforme la géométrie et un nuanceur de pixels qui génère une couleur unie, à une technique de rendu qui requiert plusieurs passes, utilise chaque étape du pipeline graphique et manipule l’état du nuanceur, ainsi que l’état du pipeline non associé aux nuanceurs programmables.

La première étape consiste à organiser l’état que vous souhaitez contrôler dans un effet. Cela comprend l’état du nuanceur (vertex, géométrie et nuanceurs de pixels), l’état de la texture et de l’échantillonneur utilisé par les nuanceurs et d’autres États de pipeline non programmables. Vous pouvez créer un effet en mémoire sous la forme d’une chaîne de texte, mais en général, la taille est suffisamment grande pour qu’il soit pratique de stocker l’état de l’effet dans un fichier d’effet (fichier texte se terminant par une extension. FX). Pour utiliser un effet, vous devez le compiler (pour vérifier la syntaxe HLSL et la syntaxe de l’infrastructure d’effet), initialiser l’état de l’effet par le biais d’appels d’API et modifier votre boucle de rendu pour appeler les API de rendu.

-   [Organisation de l’État dans un effet](d3d10-graphics-programming-guide-effects-organize.md)
-   [Appliquer les interfaces système](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [Spécialisation des interfaces](d3d10-graphics-reference-effect-specializing.md)
-   [Rendu d’un effet](d3d10-graphics-programming-guide-effects-render.md)

Un effet encapsule tout l’état de rendu requis par un effet particulier dans une fonction de rendu unique appelée technique. Une passe est un sous-ensemble d’une technique, qui contient l’état de rendu. Pour implémenter un effet de rendu de passe multiple, implémentez une ou plusieurs passes au sein d’une technique. Par exemple, imaginons que vous souhaitiez afficher une géométrie avec un ensemble de tampons de profondeur/stencil, puis dessiner quelques sprites en plus. Vous pouvez implémenter le rendu géométrique dans la première passe et le sprite dans la deuxième passe. Pour afficher l’effet, vous affichez simplement les deux passes dans votre boucle de rendu. Vous pouvez implémenter n’importe quel nombre de techniques en effet. Bien sûr, plus le nombre de techniques est élevé, plus le temps de compilation de l’effet est élevé. Une façon d’exploiter cette fonctionnalité consiste à créer des effets avec des techniques conçues pour s’exécuter sur un matériel différent. Cela permet à une application de rétrograder correctement les performances en fonction des fonctionnalités matérielles détectées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
