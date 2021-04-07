---
description: Direct3D peut mélanger jusqu’à huit textures sur des primitives en une seule passe.
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: Fusion de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a89a87160bb85c1f62339380d46fa4b39736609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747620"
---
# <a name="texture-blending-direct3d-9"></a>Fusion de texture (Direct3D 9)

Direct3D peut mélanger jusqu’à huit textures sur des primitives en une seule passe. L’utilisation de plusieurs fusions de textures peut augmenter de façon indéterminée la fréquence d’images d’une application Direct3D. Une application utilise plusieurs fusions de texture pour appliquer des textures, des ombres, de l’éclairage spéculaire, un éclairage diffus et d’autres effets spéciaux en une seule passe.

Pour utiliser la fusion de texture, votre application doit d’abord vérifier si le matériel de l’utilisateur la prend en charge. Ces informations se trouvent dans le membre TextureCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Pour plus d’informations sur la façon d’interroger le matériel de l’utilisateur sur les fonctionnalités de fusion de texture, consultez [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="texture-stages-and-the-texture-blending-cascade"></a>Étapes de texture et cascade de fusion

Direct3D prend en charge la fusion de plusieurs textures à passage unique par le biais de l’utilisation d’étapes de texture. Une étape de texture accepte deux arguments et effectue une opération de fusion sur ces derniers, en passant le résultat pour un traitement ultérieur ou pour la pixellisation. Vous pouvez visualiser une étape de texture comme indiqué dans le diagramme suivant.

![diagramme d’une étape de texture](images/texstg.png)

Comme le montre le diagramme précédent, les étapes de texture fusionnent deux arguments à l’aide d’un opérateur spécifié. Les opérations courantes incluent la modulation simple ou l’ajout de la couleur ou des composants alpha des arguments, mais plus de deux douzaines d’opérations sont prises en charge. Les arguments d’une phase peuvent être associés à une texture, à la couleur itérée ou à l’alpha (itération au cours de l’ombrage Gouraud), à la couleur et à l’alpha arbitraires ou au résultat de l’étape de texture précédente. Pour plus d’informations, consultez [opérations et arguments de fusion de texture (Direct3D 9)](texture-blending-operations-and-arguments.md).

> [!Note]  
> Direct3D distingue la fusion des couleurs de la fusion alpha. Les applications définissent des opérations de fusion et des arguments pour la couleur et l’alpha individuellement, et les résultats de ces paramètres sont indépendants les uns des autres.

 

La combinaison des arguments et des opérations utilisées par plusieurs étapes de fusion définit un langage de fusion simple basé sur un fluide. Les résultats d’une étape passent à une autre étape, de cette étape à la suivante, et ainsi de suite. Le concept de résultats allant d’un niveau à l’autres à une étape finale sur un polygone est souvent appelé la texture de la fusion. Le diagramme suivant montre comment les différentes étapes de texture composent la texture en cascade.

![diagramme des étapes de texture dans la cascade de fusion](images/tcascade.png)

Chaque étape d’un appareil a un index de base zéro. Direct3D autorise jusqu’à huit étapes de fusion, même si vous devez toujours vérifier les capacités de l’appareil pour déterminer le nombre d’étapes prises en charge par le matériel actuel. La première étape de fusion se trouve à l’index 0, la seconde à 1, et ainsi de suite, jusqu’à l’index 7. Le système fusionne les étapes dans l’ordre d’index de plus en plus important.

Utilisez uniquement le nombre d’étapes dont vous avez besoin. les étapes de fusion inutilisées sont désactivées par défaut. Par conséquent, si votre application utilise uniquement les deux premières étapes, elle doit uniquement définir des opérations et des arguments pour les étapes 0 et 1. Le système fusionne les deux étapes et ignore les étapes désactivées.

> [!Note]  
> Si votre application varie le nombre d’étapes qu’elle utilise pour différentes situations, par exemple quatre étapes pour certains objets, et seulement deux pour d’autres, vous n’avez pas besoin de désactiver explicitement toutes les étapes précédemment utilisées. L’une des options consiste à désactiver l’opération de couleur pour la première étape non utilisée, alors toutes les étapes avec un index plus élevé ne sont pas appliquées. Une autre option consiste à désactiver complètement le mappage de texture en définissant l’opération de couleur pour la première étape de texture (étape 0) sur D3DTOP \_ Désactiver. Une troisième option est lorsqu’une étape de texture a D3DTSS \_ COLORARG1 égal à D3DTA \_ texture et que le pointeur de texture pour l’étape est **null**, cette étape et toutes les étapes après qu’elle n’est pas traitée.

 

Des informations supplémentaires sont contenues dans les rubriques suivantes.

-   [Opérations et arguments de fusion de texture (Direct3D 9)](texture-blending-operations-and-arguments.md)
-   [Affectation des textures actuelles (Direct3D 9)](assigning-the-current-textures.md)
-   [Création de phases de fusion (Direct3D 9)](creating-blending-stages.md)
-   [Fusion de texture alpha (Direct3D 9)](alpha-texture-blending.md)
-   [Fusion de texture multipasse (Direct3D 9)](multipass-texture-blending.md)
-   [Mise en correspondance de la lumière avec les textures (Direct3D 9)](light-mapping-with-textures.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
