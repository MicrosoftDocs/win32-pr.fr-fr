---
description: Supprimer tous les filtres dans le graphique
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Supprimer tous les filtres dans le graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746301"
---
# <a name="remove-all-the-filters-in-the-graph"></a>Supprimer tous les filtres dans le graphique

Le moyen le plus simple de supprimer tous les filtres dans un graphique de filtre consiste simplement à libérer le gestionnaire du graphique de filtres et à en créer un nouveau. Veillez à libérer chaque pointeur de votre application sur les interfaces des gestionnaires de graphique de filtre, ainsi que les pointeurs vers des objets dans le graphique, y compris des filtres, des codes confidentiels, l’horloge de référence, etc.

Vous pouvez également supprimer les filtres un par un, à l’aide de la méthode [**IFilterGraph :: removeFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



Cet exemple utilise la méthode [**IFilterGraph :: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) pour énumérer les filtres dans le graphique. La suppression d’un filtre entraîne le désynchronisation de l’objet énumérateur avec le graphique. Utilisez la méthode [**IEnumFilters :: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) pour réinitialiser l’énumérateur. Dans le cas contraire, tout appel ultérieur à [**IEnumFilters :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) échoue.

 

 



