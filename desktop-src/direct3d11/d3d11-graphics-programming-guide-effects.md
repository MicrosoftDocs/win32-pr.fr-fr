---
title: Effets (Direct3D 11)
description: En savoir plus sur les effets Direct3D 11. Un effet est l’état du pipeline, défini par des expressions écrites en HLSL et une syntaxe spécifique à l’infrastructure d’effet.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe4cdb204e498a0c6a8f4d5f6e4656446c0f0a3f4d660f2e0e2a33e8515a0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990099"
---
# <a name="effects-direct3d-11"></a>Effets (Direct3D 11)

Un effet DirectX est une collection d’États de pipeline, définie par des expressions écrites en [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) et une syntaxe spécifique à l’infrastructure Effect.

Après avoir compilé un effet, utilisez les API d’infrastructure Effects pour effectuer le rendu. Les fonctionnalités d’effet peuvent aller d’un point de vue simple à un nuanceur de sommets qui transforme la géométrie et un nuanceur de pixels qui génère une couleur unie, à une technique de rendu qui requiert plusieurs passes, utilise chaque étape du pipeline graphique et manipule l’état du nuanceur, ainsi que l’état du pipeline non associé aux nuanceurs programmables.

La première étape consiste à organiser l’état que vous souhaitez contrôler dans un effet. Cela comprend l’état du nuanceur (vertex, coque, Domain, Geometry, pixel et nuanceurs de calcul), l’état de la texture et de l’échantillonneur utilisé par les nuanceurs et d’autres États de pipeline non programmables. Vous pouvez créer un effet en mémoire sous la forme d’une chaîne de texte, mais en général, la taille est suffisamment grande pour qu’il soit pratique de stocker l’état de l’effet dans un fichier d’effet (fichier texte se terminant par une extension. FX). Pour utiliser un effet, vous devez le compiler (pour vérifier la syntaxe HLSL et la syntaxe de l’infrastructure d’effet), initialiser l’état de l’effet par le biais d’appels d’API et modifier votre boucle de rendu pour appeler les API de rendu.

Un effet encapsule tout l’état de rendu requis par un effet particulier dans une fonction de rendu unique appelée technique. Une passe est un sous-ensemble d’une technique, qui contient l’état de rendu. Pour implémenter un effet de rendu de passe multiple, implémentez une ou plusieurs passes au sein d’une technique. Par exemple, imaginons que vous souhaitiez afficher une géométrie avec un ensemble de tampons de profondeur/stencil, puis dessiner quelques sprites en plus. Vous pouvez implémenter le rendu géométrique dans la première passe et le sprite dans la deuxième passe. Pour afficher l’effet, vous affichez simplement les deux passes dans votre boucle de rendu. Vous pouvez implémenter n’importe quel nombre de techniques en effet. Bien sûr, plus le nombre de techniques est élevé, plus le temps de compilation de l’effet est élevé. Une façon d’exploiter cette fonctionnalité consiste à créer des effets avec des techniques conçues pour s’exécuter sur un matériel différent. Cela permet à une application de rétrograder correctement les performances en fonction des fonctionnalités matérielles détectées.

Un ensemble de techniques peut être regroupé dans un groupe (qui utilise la syntaxe « fxgroup »). Les techniques peuvent être regroupées de quelque manière que ce soit. Par exemple, plusieurs groupes peuvent être créés, un par document ; chaque matériel peut avoir une technique pour chaque niveau matériel ; chaque technique aurait un ensemble de passes qui définissent le matériel sur le matériel particulier.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                | Description                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organisation de l’État dans un effet](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Avec Direct3D 11, l’état d’effet de certaines étapes de pipeline est organisé par structures.<br/>                                                                   |
| [Appliquer les interfaces système](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet.<br/>                                                                                  |
| [Spécialisation des interfaces](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin.<br/> |
| [Interfaces et classes dans Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Il existe de nombreuses façons d’utiliser des classes et des interfaces dans Effects 11.<br/>                                                                                         |
| [Rendu d’un effet](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Un effet peut être utilisé pour stocker des informations ou pour effectuer un rendu à l’aide d’un groupe d’États.<br/>                                                                         |
| [Clonage d’un effet](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | Le clonage d’un effet crée une deuxième copie quasiment identique de l’effet.<br/>                                                                                 |
| [Syntaxe du flux de sortie](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Un nuanceur Geometry avec flux sortant est déclaré avec une syntaxe particulière.<br/>                                                                                  |
| [Différences entre les effets 10 et les effets 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | Cette rubrique présente les différences entre les effets 10 et 11.<br/>                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

