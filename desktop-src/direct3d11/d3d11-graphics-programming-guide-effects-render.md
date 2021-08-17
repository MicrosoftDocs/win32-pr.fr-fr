---
title: Rendu d’un effet (Direct3D 11)
description: En savoir plus sur le rendu d’un effet pour Direct3D 11. Un effet peut être utilisé pour stocker des informations ou pour effectuer un rendu à l’aide d’un groupe d’États.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ba8ebbc1ac8989ac10568a00f26b26370c4bb8e7710098733dad74618e53af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913599"
---
# <a name="rendering-an-effect-direct3d-11"></a>Rendu d’un effet (Direct3D 11)

Un effet peut être utilisé pour stocker des informations ou pour effectuer un rendu à l’aide d’un groupe d’États. Chaque technique spécifie un ensemble de nuanceurs de vertex, de nuanceurs de coque, de nuanceurs de domaine, de nuanceurs de géométrie, de nuanceurs de pixels, de nuanceurs de calcul, d’état de nuanceur, d’échantillonnage et d’état de texture, d’état d’affichage d’accès non ordonné et d’autre État de pipeline. Ainsi, une fois que vous avez organisé l’État en conséquence, vous pouvez encapsuler l’effet de rendu résultant de cet État en créant et en rendant l’effet.

Il existe quelques étapes pour préparer un effet pour le rendu. La première consiste à compiler, qui vérifie le code HLSL comme par rapport à la syntaxe du langage HLSL et aux règles de l’infrastructure d’effet. Vous pouvez compiler un effet à partir de votre application à l’aide d’appels d’API ou vous pouvez compiler un effet hors connexion à l’aide de l’utilitaire Effect compiler Utility [fxc.exe](/windows/desktop/direct3dtools/fxc). Une fois que votre effet a été compilé avec succès, créez-le en appelant un ensemble d’API différent (mais très similaire).

Une fois l’effet créé, il y a deux étapes restantes pour l’utiliser. Tout d’abord, vous devez initialiser les valeurs d’état des effets (les valeurs des variables d’effet) à l’aide d’un certain nombre de méthodes pour définir l’État si elles ne sont pas initialisées en HLSL. Pour certaines variables, cette opération peut être effectuée une fois lors de la création d’un effet ; d’autres doivent être mis à jour chaque fois que votre application appelle la boucle de rendu. Une fois les variables d’effet définies, vous indiquez au runtime d’afficher l’effet en appliquant une technique. Ces rubriques sont abordées plus en détail ci-dessous.

Naturellement, il existe des considérations relatives aux performances pour l’utilisation des effets. Ces considérations sont en grande partie les mêmes si vous n’utilisez pas d’effet. Des opérations telles que la réduction du nombre de modifications d’État et l’Organisation des variables par fréquence de mise à jour. Ces tactiques permettent de réduire la quantité de données qui doivent être envoyées du processeur au GPU, et donc de réduire les problèmes potentiels de synchronisation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                        | Description                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compiler un effet](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Une fois qu’un effet a été créé, l’étape suivante consiste à compiler le code pour vérifier les problèmes de syntaxe.<br/>                                                                                                                                                                                                          |
| [Créer un effet](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Un effet est créé en chargeant le bytecode d’effet compilé dans le Framework Effects. Contrairement à Effects 10, l’effet doit être compilé avant de créer l’effet. Les effets chargés en mémoire peuvent être créés en appelant [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).<br/>                 |
| [Définir l’état de l’effet](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Certaines constantes d’effet doivent uniquement être initialisées. Une fois initialisé, l’état de l’effet est défini sur l’appareil pour l’ensemble de la boucle de rendu. D’autres variables doivent être mises à jour chaque fois que la boucle de rendu est appelée. Le code de base pour définir des variables d’effet est illustré ci-dessous, pour chacun des types de variables.<br/> |
| [Appliquer une technique](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Avec les constantes, les textures et l’état du nuanceur déclarés et initialisés, la seule chose à faire est de définir l’état de l’effet dans l’appareil.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

