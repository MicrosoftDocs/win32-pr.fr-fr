---
description: Sources en direct
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: Sources en direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43486cf3db797f493c9446bf782989b8beaae829
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481752"
---
# <a name="live-sources"></a>Sources en direct

Une source dynamique, également appelée *source Push*, reçoit des données en temps réel. Les exemples incluent la capture vidéo et les diffusions réseau. En général, une source dynamique ne peut pas contrôler la vitesse à laquelle les données arrivent.

Un filtre est considéré comme une source dynamique si l’une des conditions suivantes est vraie :

-   Le filtre retourne le filtre AM les \_ \_ \_ indicateurs divers est un \_ \_ indicateur de source de la méthode [**IAMFilterMiscFlags :: GetMiscFlags**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) , et au moins l’une de ses broches de sortie expose l’interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) .
-   Le filtre expose l’interface [**IKsPropertySet**](ikspropertyset.md) et a une broche de capture ( \_ capture de catégorie pin \_ ). Pour plus d’informations, consultez la [propriété épingle définie](pin-property-set.md) .

Si un filtre de source dynamique fournit une horloge, le gestionnaire de graphique de filtre préfèrera cette horloge lorsqu’il choisit l’horloge de référence du graphique. Pour plus d’informations, consultez [horloges de référence](reference-clocks.md) .

**Latence**

La latence d’un filtre correspond à la durée pendant laquelle il prend le filtre pour traiter un exemple. Pour les sources en direct, la latence est déterminée par la taille de la mémoire tampon utilisée pour contenir des échantillons. Par exemple, supposons que le graphique de filtre ait une source vidéo avec une latence de 33 millisecondes (MS) et une source audio avec une latence de 500 ms. Chaque image vidéo arrive au convertisseur vidéo environ 470 ms avant que l’exemple audio correspondant n’atteigne le convertisseur audio. À moins que le graphique compense la différence, le son et la vidéo ne sont pas synchronisés.

Les sources dynamiques peuvent être synchronisées par le biais de l’interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) . Le gestionnaire de graphes de filtre ne synchronise pas les sources dynamiques, sauf si l’application active la synchronisation en appelant la méthode [**IAMGraphStreams :: SyncUsingStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) . Si la synchronisation est activée, le gestionnaire de graphes de filtres interroge chaque filtre source pour **IAMPushSource**. Si le filtre prend en charge **IAMPushSource**, le gestionnaire de graphique de filtre appelle [**IAMLatency :: GetLatency**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) pour récupérer la latence attendue du filtre. (L’interface **IAMPushSource** hérite de [**IAMLatency**](/windows/desktop/api/Strmif/nn-strmif-iamlatency).) À partir des valeurs de latence combinées, le gestionnaire de graphes de filtre détermine la latence maximale attendue dans le graphique. Il appelle ensuite [**IAMPushSource :: SetStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) pour attribuer à chaque filtre source un décalage de flux, que le filtre ajoute aux horodatages qu’il génère.

Cette méthode est principalement destinée à l’aperçu instantané. Toutefois, Notez qu’un code PIN sur un appareil de capture dynamique (par exemple, un appareil photo) ne définit pas d’horodatage sur les échantillons qu’il livre. Par conséquent, pour utiliser cette méthode avec un appareil de capture dynamique, vous devez afficher un aperçu à partir du code confidentiel de capture. Pour plus d’informations, consultez [filtres de capture vidéo DirectShow](directshow-video-capture-filters.md).

Actuellement, l’interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) est prise en charge par le filtre de [capture VFW](vfw-capture-filter.md) et le filtre de [capture audio](audio-capture-filter.md) .

**Correspondance des taux**

Si un filtre de convertisseur planifie des exemples à l’aide d’une horloge de référence, mais que le filtre source les produit à l’aide d’une horloge différente, des problèmes peuvent se produire lors de la lecture. Le convertisseur peut s’exécuter plus rapidement que la source, provoquant ainsi des écarts dans les données. Ou elle peut s’exécuter plus lentement que la source, provoquant ainsi des échantillons « bottes » jusqu’à un moment où le graphique dépose des exemples. En règle générale, une source dynamique ne peut pas contrôler son taux de production. au lieu de cela, le convertisseur doit faire correspondre les tarifs avec la source.

Actuellement, seul le convertisseur audio effectue la correspondance des taux, car les problèmes de lecture audio sont plus perceptibles que les problèmes dans la vidéo. Pour effectuer la mise en correspondance des taux, le convertisseur audio doit sélectionner un texte sur lequel il correspondra aux tarifs. Il utilise l’algorithme suivant :

-   Si le graphique n’utilise pas une horloge de référence, le convertisseur audio ne tente pas de faire correspondre les taux. (Chaque fois que le graphique n’a aucune horloge de référence, les échantillons sont toujours restitués immédiatement à mesure qu’ils arrivent.)
-   Sinon, s’il existe une horloge de référence pour le graphique, le convertisseur audio vérifie s’il existe une source dynamique en direct, à l’aide des critères décrits précédemment. Si ce n’est pas le cas, le convertisseur audio ne correspond pas aux tarifs.
-   S’il existe une source dynamique en amont et que cette source expose l’interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) sur sa broche de sortie, le convertisseur audio appelle [**IAMPushSource :: GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags). Il recherche l’un des indicateurs suivants :
    -   \_RM PUSHSOURCECAPS \_ interne \_ . Cet indicateur signifie que le filtre source a son propre mécanisme de correspondance des taux, de sorte que le convertisseur audio ne correspond pas aux tarifs.
    -   AM \_ PUSHSOURCECAPS \_ pas en \_ ligne. Cet indicateur signifie que le filtre source n’est pas vraiment une source dynamique, même s’il expose l’interface [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) . Par conséquent, le convertisseur audio ne correspond pas aux tarifs.
    -   \_ \_ heure privée am PUSHSOURCECAPS \_ . Cet indicateur signifie que le filtre source utilise une horloge privée pour générer des horodatages. Dans ce cas, le convertisseur audio correspond aux tarifs par rapport aux horodatages. (Si les exemples n’ont pas de datage, toutefois, le convertisseur ignore cet indicateur.)
-   Si [**GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) ne retourne aucun indicateur (zéro), le comportement du convertisseur audio dépend de l’horloge du graphique et si les exemples ont des horodatages :
    -   Si le convertisseur audio n’est pas l’horloge graphique et que les échantillons ont des horodateurs, le convertisseur audio fait correspondre les taux aux horodatages.
    -   Si les exemples n’ont pas de datage, le convertisseur audio tente de faire correspondre le taux de données audio entrantes.
    -   Si le convertisseur audio est l’horloge graphique, il tente de faire correspondre le débit des données entrantes.

La raison du dernier cas est la suivante : si le convertisseur audio est l’horloge de référence et que le filtre source utilise la même horloge pour générer des horodatages, le convertisseur audio ne peut pas faire correspondre les taux aux horodatages. Si c’est le cas, il tenterait de faire correspondre les vitesses avec lui-même, ce qui pourrait entraîner la dérive de l’horloge. Par conséquent, dans ce cas, le convertisseur correspond au taux de données audio entrantes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



