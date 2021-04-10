---
description: Cette rubrique décrit comment un filtre de capture DirectShow personnalisé doit générer des données de sortie.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Génération de données dans un filtre de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950217"
---
# <a name="producing-data-in-a-capture-filter"></a>Génération de données dans un filtre de capture

Cette rubrique décrit comment un filtre de capture DirectShow personnalisé doit générer des données de sortie.

## <a name="filter-state-changes"></a>Modifications de l’état du filtre

Un filtre de capture doit produire des données uniquement lorsque le filtre est en cours d’exécution. N’envoyez pas de données à partir de vos codes confidentiels lorsque le filtre est suspendu. Retournez également **VFW S ne peut pas être \_ \_ \_** renvoyé à partir de la méthode [**CBaseFilter :: GetState**](cbasefilter-getstate.md) lorsque le filtre est suspendu. Cette valeur de retour indique au gestionnaire de graphique de filtre qu’il ne doit pas attendre les données de votre filtre pendant que le filtre est suspendu. Pour plus d’informations, consultez [États de filtre](filter-states.md).

Le code suivant montre comment implémenter la méthode [**IMediaFilter :: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) :


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a>Contrôle de flux individuels

Les broches de sortie d’un filtre de capture doivent prendre en charge l’interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , afin qu’une application puisse activer ou désactiver chaque pin individuellement. Par exemple, une application peut afficher un aperçu sans capture, puis passer en mode capture sans reconstruire le graphique de filtre. Vous pouvez utiliser la classe [**CBaseStreamControl**](cbasestreamcontrol.md) pour implémenter cette interface.

## <a name="time-stamps"></a>Horodatages

Quand le filtre capture un exemple, horodatage l’exemple avec l’heure actuelle du flux. L’heure de fin est l’heure de début plus la durée. Par exemple, si le filtre capture 10 échantillons par seconde et que la durée du flux est de 200 millions unités lorsque le filtre capture l’échantillon, les horodatages doivent être 200 millions et 201 millions. (Il y a 10 millions unités par seconde.)

Pour calculer le temps de flux, appelez la méthode [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) pour obtenir le temps de référence actuel, puis soustraction l’heure de début d’origine. Vous pouvez également appeler la méthode [**CBaseFilter :: StreamTime**](cbasefilter-streamtime.md) , qui effectue le même calcul. Pour définir l’horodatage sur un exemple, appelez la méthode [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

Toutefois, si le filtre a un code pin d’aperçu, les exemples du code PIN de préversion ne doivent pas avoir de datage. En effet, les exemples atteindront toujours le convertisseur légèrement après l’heure de la capture. Si les exemples sont horodatés, le convertisseur les traite comme tard et peut tenter de rattraper le problème en supprimant des exemples. (Pour plus d’informations, consultez [filtres de capture vidéo DirectShow](directshow-video-capture-filters.md).) Notez que l’interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) requiert le code confidentiel pour effectuer le suivi des temps d’échantillonnage. Pour un code pin d’aperçu, vous devrez peut-être modifier l’implémentation afin qu’elle ne repose pas sur les horodatages.

Les horodatages doivent toujours augmenter d’un échantillon à l’autre. Cela est vrai même lorsque le filtre est suspendu. Si le filtre est exécuté, s’interrompt, puis s’exécute à nouveau, le premier échantillon après la pause doit avoir un horodatage plus grand que le dernier échantillon avant la pause.

En fonction des données que vous capturez, il peut être utile de définir l’heure du média sur les échantillons.

Pour plus d’informations, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres de capture vidéo DirectShow](directshow-video-capture-filters.md)
</dt> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Écriture de filtres de capture](writing-capture-filters.md)
</dt> </dl>

 

 



