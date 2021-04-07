---
description: Chaînes de filtre
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Chaînes de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e374aca71b024773e4177d09e67c7ee6034ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846598"
---
# <a name="filter-chains"></a>Chaînes de filtre

Une *chaîne de filtre* est une séquence de filtres qui remplit les conditions suivantes :

-   Chaque filtre de la chaîne a au plus une broche d’entrée connectée et une broche de sortie connectée.
-   Il est possible de traverser chaque filtre de la chaîne sans traverser les filtres en dehors de la chaîne.

Par exemple, dans le diagramme suivant, les filtres A – B, C – D et F – G-H sont des chaînes de filtre. Chaque sous-chaîne dans F – G – H (F – G et G – H) est également une chaîne de filtres. Une chaîne de filtres peut se composer d’un filtre unique. les filtres A, B, C, D, F, G et H sont donc également des chaînes de filtre distinctes. Le filtre E a deux connexions d’entrée, donc toute séquence de filtres incluant le filtre E n’est pas une chaîne de filtres.

![chaîne de filtre (exemple 1)](images/filter-chain1.png)

L’interface [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) fournit les méthodes suivantes pour contrôler les chaînes de filtre :



|                                                               |                                 |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain::StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Démarre une chaîne.                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Arrête une chaîne.                  |
| [**IFilterChain ::P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Suspend une chaîne.                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Supprime une chaîne du graphique. |



 

Il n’existe aucune méthode spécifique pour ajouter une chaîne. Pour ajouter une chaîne, insérez les nouveaux filtres à l’aide de la méthode [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Ensuite, connectez les filtres en appelant [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)ou des méthodes similaires.

Lorsque le graphique est en cours d’exécution, une chaîne de filtres peut basculer entre l’exécution et l’arrêt. Lorsque le graphique est suspendu, il peut passer de l’état suspendu à l’état arrêté. Il s’agit des seules transitions d’État possibles avec les chaînes de filtre.

## <a name="filter-chain-guidelines"></a>Instructions relatives à la chaîne de filtre

Lorsque vous utilisez des méthodes **IFilterChain** , il est important de s’assurer que les filtres du graphique peuvent prendre en charge les opérations de chaînage de filtres. Dans le cas contraire, vous risquez de provoquer des blocages ou des erreurs de graphe. Les filtres connectés à la chaîne doivent fonctionner correctement après la modification de l’état de la chaîne.

La meilleure façon d’utiliser **IFilterChain** est d’utiliser un ensemble de filtres que vous avez spécifiquement conçus pour le chaînage. Suivez les indications ci-dessous pour vous assurer que vos filtres sont sécurisés pour les opérations de chaîne de filtre. Ces points font référence au diagramme suivant.

![chaîne de filtre (exemple 2)](images/filter-chain2.png)

-   Avant la modification de l’état de la chaîne de filtre, tous les appels de traitement des données à la limite de la chaîne de filtre doivent être terminés. Cette règle s’applique aux méthodes [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)et [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream). Les filtres de la chaîne doivent retourner des appels à ces méthodes effectuées par les filtres en dehors de la chaîne ; les filtres en dehors de la chaîne doivent retourner des appels effectués par des filtres au sein de la chaîne.

Par exemple, dans le diagramme précédent, le filtre B doit effectuer tous les appels de traitement de données à partir du filtre A, et le filtre E doit terminer tous les appels du filtre D. Si les codes confidentiels exposent les interfaces [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) et [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) , vous pouvez envoyer les données à travers le graphique en appelant les méthodes [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) et [**IGraphConfig ::P Ushthroughdata**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) , comme décrit dans [reconnexion dynamique](dynamic-reconnection.md). Les filtres peuvent également prendre en charge des méthodes privées pour le push des données.

-   Les filtres en amont doivent s’attendre à ce que l’état de la chaîne change. Par exemple, dans le diagramme précédent, supposons que la chaîne soit arrêtée mais filtre un appel à **IMemInputPin :: Receive**. L’appel échoue et la réponse du filtre A consiste à arrêter la diffusion en continu. Lorsque l’application redémarre la chaîne, elle n’a aucun effet, car le filtre A ne diffuse plus de données.
-   Les filtres en aval doivent également s’attendre à ce que l’état de la chaîne change. Si ce n’est pas le cas, le filtre en aval peut se bloquer pendant qu’il attend des exemples qui n’arrivent jamais. Par exemple, les filtres multiplexeur (MUX) requièrent souvent des données provenant de toutes leurs broches d’entrée. L’arrêt du flux de données à partir d’une broche d’entrée peut empêcher le traitement des autres flux. Cela peut entraîner un blocage du graphique.
-   Chaque connexion de code confidentiel d’un filtre en dehors de la chaîne à un filtre au sein de la chaîne doit avoir son propre allocateur, qui n’est pas partagé par d’autres connexions. Lorsque la chaîne change d’État ou est supprimée du graphique, l’allocateur peut être dévalidée. Si d’autres connexions utilisent le même allocateur, elles ne peuvent plus traiter des exemples.
-   Ne supprimez pas une chaîne à moins que les filtres connectés à la chaîne ne prennent en charge la déconnexion dynamique. En règle générale, les filtres connectés prennent en charge l’interface **IPinConnection** ou **IPinFlowControl** , mais peuvent prendre en charge des interfaces privées à la place.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération de graphiques dynamiques](dynamic-graph-building.md)
</dt> </dl>

 

 



