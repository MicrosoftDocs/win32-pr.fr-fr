---
description: Filtres de pilote de classe WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Filtres de pilote de classe WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd93db09c638ed7a8a217bec28a565086dcbfcae2b5702c9e1d07778c338646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071893"
---
# <a name="wdm-class-driver-filters"></a>Filtres de pilote de classe WDM

si un périphérique de capture utilise un pilote Windows Driver Model (WDM), le graphique peut nécessiter certains filtres en amont du filtre de capture. Ces filtres sont appelés filtres de pilote de classe de flux ou filtres WDM. Ils prennent en charge des fonctionnalités supplémentaires fournies par le matériel. Par exemple, une carte tuner TV possède des fonctions permettant de définir le canal. Le filtre correspondant est le filtre [Tuner TV](tv-tuner-filter.md) , qui expose l’interface [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . Pour rendre cette fonctionnalité accessible à l’application, vous devez connecter le filtre Tuner TV au filtre de capture.

L’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fournit le moyen le plus simple d’ajouter des filtres WDM au graphique. À un moment donné, lors de la génération du graphique, appelez [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) ou [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). L’une de ces méthodes localise automatiquement les filtres WDM nécessaires et les connecte au filtre de capture. Le reste de cette section décrit comment ajouter des filtres WDM manuellement. Toutefois, n’oubliez pas que l’approche recommandée consiste simplement à appeler l’une de ces méthodes **ICaptureGraphBuilder2** .

Les broches d’un filtre WDM prennent en charge un ou plusieurs supports. Un support définit une méthode de communication, telle qu’un bus. Vous devez connecter des broches qui prennent en charge le même support. La structure [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , qui est équivalente à la structure **KSPIN \_ moyenne** utilisée pour les pilotes de streaming de noyau, définit un support dans DirectShow. Le membre **clsMedium** de la structure **REGPINMEDIUM** spécifie l’identificateur de classe (CLSID) pour le support. Pour récupérer le support d’un pin, appelez la méthode [**IKsPin :: KsQueryMediums**](ikspin-ksquerymediums.md) . Cette méthode retourne un pointeur vers un bloc de mémoire qui contient une structure d' [**\_ élément KSMULTIPLE**](ksmultiple-item.md) , suivie de zéro ou plusieurs structures **REGPINMEDIUM** . Chaque structure **REGPINMEDIUM** identifie un support pris en charge par le pin.

Ne connectez pas un code confidentiel si le support a un CLSID de GUID \_ null ou KSMEDIUMSETID \_ standard. Il s’agit de valeurs par défaut indiquant que le code confidentiel ne prend pas en charge les supports.

En outre, ne connectez pas un code confidentiel, sauf si le filtre requiert exactement une instance connectée de ce code PIN. Dans le cas contraire, votre application peut essayer de connecter différents codes confidentiels qui ne doivent pas avoir de connexions, ce qui peut provoquer le blocage du programme. Pour déterminer le nombre d’instances requises, récupérez le \_ jeu de propriétés NECESSARYINSTANCES du code confidentiel KSPROPERTY \_ , comme indiqué dans l’exemple de code suivant. (Par souci de concision, cet exemple ne teste pas les codes de retour ou ne libère aucune interface. Votre application doit faire les deux, bien sûr.)


```C++
// Obtain the pin factory identifier.
IKsPinFactory *pPinFactory;
hr = pPin->QueryInterface(IID_IKsPinFactory, (void **)&pPinFactory);

ULONG ulFactoryId;
hr = pPinFactory->KsPinFactory(&ulFactoryId);

// Get the "instance" property from the filter.
IKsControl *pKsControl;
hr = pFilter->QueryInterface(IID_IKsControl, (void **)&pKsControl);

KSP_PIN ksPin;
ksPin.Property.Set = KSPROPSETID_Pin;
ksPin.Property.Id = KSPROPERTY_PIN_NECESSARYINSTANCES;
ksPin.Property.Flags = KSPROPERTY_TYPE_GET;
ksPin.PinId = ulFactoryId;
ksPin.Reserved = 0; 

KSPROPERTY ksProp;
ULONG ulInstances, bytes;
pKsControl->KsProperty((PKSPROPERTY)&ksPin, sizeof(ksPin), 
    &ulInstances, sizeof(ULONG), &bytes);

if (hr == S_OK && bytes == sizeof(ULONG)) 
{
    if (ulInstances == 1) 
    {
        // Filter requires one instance of this pin.
        // This pin is OK.
    } 
}
```



Le pseudo-code suivant est un bref aperçu qui montre comment rechercher et connecter les filtres WDM. Il omet de nombreux détails et est destiné uniquement à illustrer les étapes générales que votre application doit effectuer.


```C++
Add supporting filters:
{
    foreach input pin:
        skip if (pin is connected)
    
        Get pin medium
        skip if (medium is GUID_NULL or KSMEDIUMSETID_Standard)
    
        Query filter for KSPROPERTY_PIN_NECESSARYINSTANCES property
        skip if (necessary instances != 1)

        Match an existing pin || Find a matching filter
}    

Match an existing pin:
{
    foreach filter in the graph
        foreach unconnected pin
            Get pin medium
            if (mediums match)
                connect the pins    
}

Find a matching filter:
{    
    Query the filter graph manager for IFilterMapper2.
    Find a filter with an output pin that matches the medium.
    Add the filter to the graph.
    Connect the pins.
    Add supporting filters. (Recursive call.)
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> </dl>

 

 



