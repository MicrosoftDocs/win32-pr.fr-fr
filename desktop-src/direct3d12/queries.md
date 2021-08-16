---
title: Requêtes
description: Dans Direct3D 12, les requêtes sont regroupées en tableaux de requêtes appelé segment de requête. Un segment de mémoire de requête a un type qui définit les types de requêtes valides qui peuvent être utilisés avec ce tas.
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71279c09b59b417535f3155683747ac4c153d7d0fd9f668f79cab9b63ca79805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241949"
---
# <a name="queries"></a>Requêtes

Dans Direct3D 12, les requêtes sont regroupées en tableaux de requêtes appelé segment de requête. Un segment de mémoire de requête a un type qui définit les types de requêtes valides qui peuvent être utilisés avec ce tas.

-   [Différences dans les requêtes de Direct3D 11 à Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Interroger des segments de mémoire](#query-heaps)
-   [Création de segments de requête](#creating-query-heaps)
-   [Extraction de données à partir d’une requête](#extracting-data-from-a-query)
-   [Rubriques connexes](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Différences dans les requêtes de Direct3D 11 à Direct3D 12

Les types de requêtes suivants ne sont plus présents dans Direct3D 12, leurs fonctionnalités étant incorporées dans d’autres processus :

-   Les **requêtes d’événement** -événement sont maintenant gérées par les délimiteurs.
-   **Requêtes d’horodateur disjoint** -les horloges GPU peuvent être définies sur un état stable dans Direct3D 12 (voir la section [minutage](timing.md) ). Les comparaisons d’horloge GPU ne sont pas significatives si le GPU est inactif du tout entre les horodateurs (appelée requête disjointe). Les requêtes d’horodatage stables avec deux horodateurs émises à partir de différentes listes de commandes sont comparables de manière fiable. Deux horodateurs au sein de la même liste de commandes sont toujours comparables de manière fiable.
-   **Requêtes de statistiques de sortie de flux** : dans Direct3D 12, il n’y a pas de requête de dépassement de sortie de flux unique (SO) pour tous les flux de sortie. Les applications doivent émettre plusieurs requêtes à un seul flux, puis mettre en corrélation les résultats.
-   Les requêtes de prédicat de **statistiques de sortie de flux et de prédicat d’occlusion** -les requêtes (qui écrivent dans la mémoire) et le [prédicat](predication.md) (qui lit à partir de la mémoire) ne sont plus couplés, ce qui signifie que ces types de requêtes ne sont pas nécessaires.

Un nouveau type de requête d’occlusion binaire a été ajouté à Direct3D 12. Cela permet aux stratégies de prédicat qui vous intéressent uniquement si un objet était entièrement bloqués ou non (au lieu du nombre de pixels bloqués) de l’indiquer à l’appareil, ce qui peut être en mesure d’effectuer plus efficacement les requêtes.

## <a name="query-heaps"></a>Interroger des segments de mémoire

Les requêtes peuvent être de type un à partir d’un certain nombre de types ([**\_ type de \_ tas \_ de requêtes D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) et sont regroupées dans des segments de requête avant d’être envoyées au GPU.

Un nouveau type de requête D3D12 l’occlusion binaire de type de requête \_ \_ \_ \_ est disponible et agit comme \_ une occlusion de type de requête D3D12 \_ \_ , à ceci près qu’elle retourne un résultat binaire 0/1:0 indique qu’aucun exemple ne réussit le test de profondeur et de stencil, 1 indique qu’au moins un exemple a réussi le test de profondeur et de stencil. Cela permet aux requêtes d’occlusion de ne pas interférer avec l’optimisation des performances GPU associée au test de profondeur/stencil.

## <a name="creating-query-heaps"></a>Création de segments de requête

Les API relatives à la création de segments de requête sont [**le \_ \_ \_ type de segment de mémoire de requête D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)enum, le struct [**D3D12 \_ query \_ segment \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)et la méthode [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

Le runtime principal valide le type de segment de mémoire de la requête comme étant un membre valide de l’énumération du [**\_ \_ type de tas D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) et que le nombre est supérieur à 0.

Chaque élément de requête individuel au sein d’un segment de requête peut être démarré et arrêté séparément.

Les API d’utilisation des segments de requête sont le [**type de \_ requête \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)enum et les méthodes [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) et [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

\_ \_ \_ L’horodateur du type de requête D3D12 est la seule requête qui prend en charge [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) uniquement. Tous les autres types de requêtes requièrent [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) et **EndQuery**.

La couche de débogage permet de valider les éléments suivants :

-   Il n’est pas possible de commencer une requête d’horodatage &mdash; , vous pouvez uniquement l’arrêter
-   Il n’est pas autorisé de commencer une requête deux fois sans la terminer (pour un élément donné). Pour les requêtes qui requièrent à la fois Begin et end, il est illégal de terminer une requête avant le BEGIN correspondant (pour un élément donné).
-   Le type de requête passé à [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) doit correspondre au type de requête passé à [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

Le runtime principal validera les éléments suivants :

-   [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) ne peut pas être appelé sur une requête d’horodatage.
-   Pour les types de requêtes qui prennent en charge à la fois [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) et [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) (sauf pour timestamp), une requête pour un élément donné ne doit pas couvrir les limites de la liste de commandes.
-   *ElementIndex* doit être compris dans la plage.
-   Le type de requête est un membre valide de l’énumération de [**\_ \_ type de requête D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) .
-   Le type de requête doit être compatible avec le segment de mémoire de la requête. Le tableau suivant indique le type de segment de requête requis pour chaque type de requête :

    

    | Type de requête                                  | Type de segment de requête                                |
    |---------------------------------------------|------------------------------------------------|
    | \_Type de requête D3D12 \_ \_ occlusion               | \_Type de tas de requête D3D12 \_ \_ \_ occlusion            |
    | \_Type de requête D3D12 \_ \_ \_ occlusion binaire       | \_Type de tas de requête D3D12 \_ \_ \_ occlusion            |
    | \_Horodatage du \_ type de requête D3D12 \_               | \_Horodateur du \_ type de segment de requête D3D12 \_ \_            |
    | \_Statistiques de \_ \_ pipeline de type de requête D3D12 \_    | \_Statistiques de \_ \_ \_ pipeline de type de segment de requête D3D12 \_ |
    | \_Type de requête D3D12 \_ \_ so \_ Statistics \_ STREAM0 | \_Statistiques du \_ type de segment de requête D3D12 \_ \_ \_       |
    | \_Type de requête D3D12 \_ \_ so \_ Statistics \_ STREAM1 | \_Statistiques du \_ type de segment de requête D3D12 \_ \_ \_       |
    | \_Type de requête D3D12 \_ \_ so \_ Statistics \_ STREAM2 | \_Statistiques du \_ type de segment de requête D3D12 \_ \_ \_       |
    | \_Type de requête D3D12 \_ \_ so \_ Statistics \_ STREAM3 | \_Statistiques du \_ type de segment de requête D3D12 \_ \_ \_       |

    

     

-   Le type de requête est pris en charge par le type de liste de commandes. Le tableau suivant indique les requêtes prises en charge sur les types de listes de commandes.

    

    | Type de requête                                  | Types de listes de commandes pris en charge         |
    |---------------------------------------------|--------------------------------------|
    | \_Type de requête D3D12 \_ \_ occlusion               | Direct                               |
    | \_Type de requête D3D12 \_ \_ \_ occlusion binaire       | Direct                               |
    | \_Horodatage du \_ type de requête D3D12 \_               | Direct, Compute et éventuellement copier |
    | \_Statistiques de \_ \_ pipeline de type de requête D3D12 \_    | Direct                               |
    | \_Type de requête D3D12 \_ \_ so \_ Statistics \_ STREAM0 | Direct                               |
    | \_Type de requête D3D12 \_ \_ so \_ Statistics \_ STREAM1 | Direct                               |
    | \_Type de requête D3D12 \_ \_ so \_ Statistics \_ STREAM2 | Direct                               |
    | \_Type de requête D3D12 \_ \_ so \_ Statistics \_ STREAM3 | Direct                               |

    

     

## <a name="extracting-data-from-a-query"></a>Extraction de données à partir d’une requête

Pour extraire des données d’une requête, vous pouvez utiliser la méthode [**ResolveQueryData**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) . **ResolveQueryData** fonctionne avec tous les types de mémoire (qu’il s’agisse de mémoire système ou de mémoire locale du périphérique), mais nécessite que la ressource de destination se trouve dans [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). 

## <a name="related-topics"></a>Rubriques connexes

* [Compteurs et requêtes](counters-and-queries.md)
* [Parcours des requêtes de prédicat](predication-queries.md)
