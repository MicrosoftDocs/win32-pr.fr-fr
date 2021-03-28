---
title: Fonctionnalités Direct3D 11
description: Le Guide de programmation contient des informations sur l’utilisation du pipeline programmable Direct3D 11 pour créer des graphiques 3D en temps réel pour les jeux, et pour les applications scientifiques et de bureau.
ms.assetid: ee4dae04-1a52-4587-87c1-006abb687a91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b6ec64e315275ca6faaf513d04f996609615a2
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032067"
---
# <a name="direct3d-11-features"></a>Fonctionnalités Direct3D 11

Le Guide de programmation contient des informations sur l’utilisation du pipeline programmable Direct3D 11 pour créer des graphiques 3D en temps réel pour les jeux, et pour les applications scientifiques et de bureau.

-   [Nuanceur de calcul](#compute-shader)
-   [Liaison de nuanceur dynamique](#dynamic-shader-linking)
-   [Traitement multithread](#multithreading)
-   [Mosaïque](#tessellation)
-   [Liste complète des fonctionnalités](#full-listing-of-features)
-   [Fonctionnalités ajoutées dans les versions précédentes](#features-added-in-previous-releases)
-   [Rubriques connexes](#related-topics)

## <a name="compute-shader"></a>Nuanceur de calcul

Un nuanceur de calcul est un nuanceur programmable conçu pour un traitement en parallèle de données à usage général. En d’autres termes, les nuanceurs de calcul autorisent l’utilisation d’un GPU comme un processeur parallèle à usage général. Le nuanceur de calcul est similaire aux autres nuanceurs de pipeline programmables (tels que vertex, pixel, Geometry) en ce sens qu’il accède aux entrées et aux sorties. La technologie de nuanceur de calcul est également appelée technologie DirectCompute. Un nuanceur de calcul est intégré à Direct3D et est accessible via un appareil Direct3D. Il peut partager directement des ressources mémoire avec des nuanceurs graphiques à l’aide de l’appareil Direct3D. Toutefois, il n’est pas directement connecté à d’autres étapes du nuanceur.

Un nuanceur de calcul est conçu pour les applications de marché de masse qui effectuent des calculs à des tarifs interactifs, lorsque le coût de la transition entre l’API (et sa pile logicielle associée) et un processeur consomment trop de surcharge.

Un nuanceur de calcul possède son propre ensemble d’États. Un nuanceur de calcul n’a pas nécessairement un mappage 1-1 forcé à des enregistrements d’entrée (comme un nuanceur de vertex) ou des enregistrements de sortie (comme le nuanceur de pixels). Certaines fonctionnalités du nuanceur Graphics sont prises en charge, mais d’autres ont été supprimées afin que de nouvelles fonctionnalités spécifiques au nuanceur de calcul puissent être ajoutées.

Pour prendre en charge les fonctionnalités spécifiques au nuanceur de calcul, plusieurs nouveaux types de ressources sont désormais disponibles, tels que les mémoires tampons de lecture/écriture, les textures et les mémoires tampons structurées.

Pour plus d’informations, consultez [vue d’ensemble du nuanceur de calcul](direct3d-11-advanced-stages-compute-shader.md) .

## <a name="dynamic-shader-linking"></a>Liaison de nuanceur dynamique

Les systèmes de rendu doivent faire face à une complexité significative lorsqu’ils gèrent des nuanceurs, tout en offrant la possibilité d’optimiser le code du nuanceur. Cela devient encore plus complexe, car les nuanceurs doivent prendre en charge une variété de documents différents dans une scène rendue sur différentes configurations matérielles. Pour relever ce défi, les développeurs de nuanceur ont souvent recours à l’une des deux approches générales. Ils ont créé des nuanceurs à usage général de grande taille, qui peuvent être utilisés par un large éventail d’éléments de scène, ce qui a pour effet de compromettre la flexibilité, ou de créer des nuanceurs individuels pour chaque flux de géométrie, type de matériau ou combinaison de types de lumière nécessaire.

Ces nuanceurs à usage général gèrent ce défi en recompilant le même nuanceur avec différentes définitions de préprocesseur, et la dernière méthode utilise la puissance de développeur en force brute pour obtenir le même résultat. L’explosion de permutation de nuanceur a souvent été un problème pour les développeurs qui doivent désormais gérer des milliers de permutations de nuanceurs au sein de leur jeu et de leur pipeline d’actifs.

Direct3D 11 et Shader Model 5 introduisent des constructions de langage orienté objet et fournissent la prise en charge de l’exécution de la liaison de nuanceur pour aider les nuanceurs de programme aux développeurs.

Pour plus d’informations, consultez [liaison dynamique](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) .

## <a name="multithreading"></a>Multithreading

De nombreuses applications graphiques sont liées à l’UC en raison d’activités coûteuses telles que la traversée de graphique de scène, le tri d’objets et les simulations physiques. Étant donné que les systèmes multicœurs deviennent de plus en plus disponibles, Direct3D 11 a amélioré la prise en charge de multithreads pour permettre une interaction efficace entre plusieurs threads d’UC et les API D3D11 Graphics.

Direct3D 11 offre les fonctionnalités suivantes pour prendre en charge le multithreading :

-   Les objets simultanés sont maintenant créés dans des threads distincts : la création de fonctions de point d’entrée qui créent des objets thread libre permet à de nombreux threads de créer des objets simultanément. Par exemple, une application peut maintenant compiler un nuanceur ou charger une texture sur un thread pendant le rendu sur un autre.
-   Les listes de commandes peuvent être créées sur plusieurs threads : une liste de commandes est une séquence enregistrée de commandes graphiques. Avec Direct3D 11, vous pouvez créer des listes de commandes sur plusieurs threads d’UC, ce qui permet un parcours parallèle de la base de données de scènes ou un traitement physique sur plusieurs threads. Cela libère le thread de rendu principal pour distribuer les tampons de commande au matériel.

Pour plus d’informations, consultez [Multithreading](overviews-direct3d-11-render-multi-thread.md) .

## <a name="tessellation"></a>Pavage

Le pavage peut être utilisé pour restituer un modèle unique avec différents niveaux de détail. Cette approche génère un modèle plus précis pour la géométrique qui dépend du niveau de détail requis pour une scène. Utilisez la polygonalisation dans une scène dans laquelle le niveau de détail autorise un modèle de géométrie inférieure, ce qui réduit la demande de bande passante de mémoire consommée pendant le rendu.

Dans Direct3D, la facettisation est implémentée sur le GPU pour calculer une surface incurvée plus lisse à partir d’un correctif d’entrée grossier (moins détaillé). Chaque facette de correctif (quadruple ou triangle) est divisée en faces triangulaires plus petites qui améliorent la surface souhaitée.

Pour plus d’informations sur l’implémentation du pavage dans le pipeline graphique, consultez [vue d’ensemble de la polygonalisation](direct3d-11-advanced-stages-tessellation.md).

## <a name="full-listing-of-features"></a>Liste complète des fonctionnalités

Il s’agit d’une liste complète des fonctionnalités de Direct3D 11.

-   Vous pouvez exécuter Direct3D 11 sur du matériel de niveau [inférieur](overviews-direct3d-11-devices-downlevel.md) en spécifiez un [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) lorsque vous créez un appareil.
-   Vous pouvez effectuer le pavage (consultez [vue d’ensemble de pavage](direct3d-11-advanced-stages-tessellation.md)) à l’aide des types de nuanceurs suivants :

    -   Nuanceur de coque
    -   Nuanceur de domaine

-   Direct3D 11 prend en charge le multithreading (voir [multithread](overviews-direct3d-11-render-multi-thread.md))

    -   Création de ressources/nuanceur/objet multithread
    -   Création d’une liste d’affichage multithread

-   Direct3D 11 développe les nuanceurs avec les fonctionnalités suivantes (voir [nuancier Model 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)).

    -   Ressources adressables-textures, mémoires tampons constantes et échantillonneurs
    -   Types de ressources supplémentaires, tels que les mémoires tampons de lecture/écriture et les textures (consultez [nouveaux types de ressources](direct3d-11-advanced-stages-cs-resources.md)).
    -   Sous-routines
    -   Nuanceur de calcul (voir [vue d’ensemble du nuanceur de calcul](direct3d-11-advanced-stages-compute-shader.md))-nuanceur qui accélère les calculs en répartissant l’espace de problème entre plusieurs threads logiciels ou groupes de threads, et le partage de données entre les registres de nuanceurs pour réduire considérablement la quantité de données requises pour l’entrée dans un nuanceur. Les algorithmes que le nuanceur de calcul peut améliorer de manière significative incluent le traitement de la publication, l’animation, la physique et l’intelligence artificielle.
    -   Nuanceur Geometry (voir [fonctionnalités du nuanceur Geometry](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features))

        -   Instanciation : permet au nuanceur Geometry de générer un maximum de 1024 sommets, ou n’importe quelle combinaison d’instances et de vertex jusqu’à 1024 (maximum de 32 instances de vertex 32 chacune).

    -   Nuanceur de pixels

        -   Couverture en tant qu’entrée PS
        -   Interpolation programmable des entrées-le nuanceur de pixels peut évaluer des attributs au sein du pixel, n’importe où sur la grille d’échantillonnage
        -   L’échantillonnage de centre de gravité des attributs doit respecter les règles suivantes :

            -   Si tous les échantillons de la primitive sont couverts, l’attribut est évalué au niveau du centre de pixels, que l’exemple de modèle ait un emplacement d’échantillon au centre de pixels.
            -   Dans le cas contraire, l’attribut est évalué au premier échantillon couvert, c’est-à-dire l’exemple avec l’index le plus bas parmi tous les exemples d’index. Dans ce cas, la couverture de l’échantillon est déterminée après l’application de l’opération AND logique à la couverture et à l’état de rastérisation de l’échantillon de masque.
            -   Si aucun échantillon n’est couvert (par exemple, sur les pixels d’assistance qui sont exécutés à partir des limites d’une primitive pour remplir des tampons de 1 x 1), l’attribut est évalué de l’une des manières suivantes :

                -   Si l’état du rastériseur Sample-Mask est un sous-ensemble des échantillons du pixel, le premier échantillon qui est couvert par l’état de rastériseur Sample-Mask est le point d’évaluation.
                -   Dans le cas contraire, dans la condition de masque d’échantillon complet, le centre de pixels est le point d’évaluation.

-   Direct3D 11 étend les textures (consultez [vue d’ensemble des textures](overviews-direct3d-11-resources-textures.md)) avec les fonctionnalités suivantes

    -   Gather4

        -   Prise en charge des textures à plusieurs composants-spécifier un canal à partir duquel effectuer le chargement
        -   Prise en charge des décalages programmables

    -   Diffusion en continu

        -   Pinces de texture pour limiter le préchargement du WDDM

    -   16 000 limites de texture
    -   Exiger 8 bits de sous-Texel et précision sous-MIP sur le filtrage de texture
    -   Nouveaux formats de compression de texture (1 nouveau format LDR et 1 nouveau format HDR)

-   Direct3D 11 prend en charge les oDepths conservateurs-cet algorithme permet à un nuanceur de pixels de comparer la valeur de profondeur par pixel du nuanceur de pixels avec celui dans le rastériseur. Le résultat permet d’effectuer des opérations d’élimination de profondeur précoce tout en conservant la capacité à sortir des oDepth à partir d’un nuanceur de pixels.
-   Direct3D 11 prend en charge une grande quantité de mémoire

    -   Autoriser les ressources > 4 Go
    -   Conservez les index des ressources 32 bits, mais les ressources sont plus volumineuses

-   Direct3D 11 prend en charge les améliorations de sortie de flux

    -   Sortie de flux adressable
    -   Augmenter le nombre de sorties de flux à 4
    -   Remplacer toutes les mémoires tampons de sortie de flux par plusieurs éléments

-   Direct3D 11 prend en charge Shader Model 5 (voir [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5))

    -   Doubles avec des dénormes
    -   Instruction Count bits Set
    -   Instruction Find First bit Set
    -   Gestion du transport et du dépassement de capacité
    -   Instructions de contrepassation des bits pour FFTs
    -   Permutation conditionnelle intrinsèque
    -   ResInfo sur les mémoires tampons
    -   Réciproque à précision réduite
    -   Instructions de conversion du nuanceur-FP16 à fp32 et vice versa
    -   La mémoire tampon structurée, qui est un nouveau type de mémoire tampon contenant des éléments structurés.

-   Direct3D 11 prend en charge les affichages de stencil et de profondeur en lecture seule

    -   Désactive les écritures dans le composant en lecture seule, autorise l’utilisation de la texture comme entrée et pour le Culling-Depth

-   Direct3D 11 prend en charge le dessin indirect-Direct3D 10 implémente DrawAuto, qui prend le contenu (généré par le GPU) et le restitue (sur le GPU). Direct3D 11 généralise DrawAuto afin qu’il puisse être appelé par un nuanceur de calcul à l’aide de DrawInstanced et DrawIndexedInstanced.
-   Direct3D 11 prend en charge diverses fonctionnalités

    -   Viewports à virgule flottante
    -   Verrouillage des mipmaps par ressource
    -   Décalage de profondeur : cet algorithme met à jour le comportement du décalage de profondeur, à l’aide de l’état de rastériseur. Le résultat élimine les scénarios où le décalage calculé peut être NaN.
    -   Limites de ressources : les index de ressources doivent toujours être <= 32 bits, mais les ressources peuvent être supérieures à 4 Go.
    -   Précision du rastériseur
    -   Exigences MSAA
    -   Compteurs réduits
    -   Format 1-bit et filtre de texte supprimé

## <a name="features-added-in-previous-releases"></a>Fonctionnalités ajoutées dans les versions précédentes

Pour obtenir la liste des fonctionnalités ajoutées dans les versions précédentes, consultez les rubriques suivantes :

-   [Nouveautés du kit de développement logiciel (SDK) Windows 7/Direct3D 11 d’août 2009](dx11-whats-new.md)
-   [Nouveautés de la version d’évaluation technique de Direct3D 11 de novembre 2008](dx11-08nov-whats-new.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nouveautés de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 