---
description: Filtres de pilote de classe WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Filtres de pilote de classe WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863394"
---
# <a name="wdm-class-driver-filters"></a><span data-ttu-id="acda6-103">Filtres de pilote de classe WDM</span><span class="sxs-lookup"><span data-stu-id="acda6-103">WDM Class Driver Filters</span></span>

<span data-ttu-id="acda6-104">Si un périphérique de capture utilise un pilote Windows Driver Model (WDM), le graphique peut nécessiter certains filtres en amont du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="acda6-104">If a capture device uses a Windows Driver Model (WDM) driver, the graph might require certain filters upstream from the capture filter.</span></span> <span data-ttu-id="acda6-105">Ces filtres sont appelés filtres de pilote de classe de flux ou filtres WDM.</span><span class="sxs-lookup"><span data-stu-id="acda6-105">These filters are called stream-class driver filters or WDM filters.</span></span> <span data-ttu-id="acda6-106">Ils prennent en charge des fonctionnalités supplémentaires fournies par le matériel.</span><span class="sxs-lookup"><span data-stu-id="acda6-106">They support additional functionality provided by the hardware.</span></span> <span data-ttu-id="acda6-107">Par exemple, une carte tuner TV possède des fonctions permettant de définir le canal.</span><span class="sxs-lookup"><span data-stu-id="acda6-107">For example, a TV tuner card has functions for setting the channel.</span></span> <span data-ttu-id="acda6-108">Le filtre correspondant est le filtre [Tuner TV](tv-tuner-filter.md) , qui expose l’interface [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="acda6-108">The corresponding filter is the [TV Tuner](tv-tuner-filter.md) filter, which exposes the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="acda6-109">Pour rendre cette fonctionnalité accessible à l’application, vous devez connecter le filtre Tuner TV au filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="acda6-109">To make this functionality available to the application, you must connect the TV Tuner filter to the capture filter.</span></span>

<span data-ttu-id="acda6-110">L’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fournit le moyen le plus simple d’ajouter des filtres WDM au graphique.</span><span class="sxs-lookup"><span data-stu-id="acda6-110">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface provides the easiest way to add WDM filters to the graph.</span></span> <span data-ttu-id="acda6-111">À un moment donné, lors de la génération du graphique, appelez [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) ou [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="acda6-111">At some point while building the graph, call [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) or [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="acda6-112">L’une de ces méthodes localise automatiquement les filtres WDM nécessaires et les connecte au filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="acda6-112">Either one of these methods will automatically locate the necessary WDM filters and connect them to the capture filter.</span></span> <span data-ttu-id="acda6-113">Le reste de cette section décrit comment ajouter des filtres WDM manuellement.</span><span class="sxs-lookup"><span data-stu-id="acda6-113">The rest of this section describes how to add WDM filters manually.</span></span> <span data-ttu-id="acda6-114">Toutefois, n’oubliez pas que l’approche recommandée consiste simplement à appeler l’une de ces méthodes **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="acda6-114">However, be aware that the recommend approach is simply to call one of these **ICaptureGraphBuilder2** methods.</span></span>

<span data-ttu-id="acda6-115">Les broches d’un filtre WDM prennent en charge un ou plusieurs supports.</span><span class="sxs-lookup"><span data-stu-id="acda6-115">The pins on a WDM filter support one or more mediums.</span></span> <span data-ttu-id="acda6-116">Un support définit une méthode de communication, telle qu’un bus.</span><span class="sxs-lookup"><span data-stu-id="acda6-116">A medium defines a method of communication, such as a bus.</span></span> <span data-ttu-id="acda6-117">Vous devez connecter des broches qui prennent en charge le même support.</span><span class="sxs-lookup"><span data-stu-id="acda6-117">You must connect pins that support the same medium.</span></span> <span data-ttu-id="acda6-118">La structure [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , qui est équivalente à la structure **KSPIN \_ moyenne** utilisée pour les pilotes de streaming de noyau, définit un support dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="acda6-118">The [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structure, which is equivalent to the **KSPIN\_MEDIUM** structure used for kernel streaming drivers, defines a medium in DirectShow.</span></span> <span data-ttu-id="acda6-119">Le membre **clsMedium** de la structure **REGPINMEDIUM** spécifie l’identificateur de classe (CLSID) pour le support.</span><span class="sxs-lookup"><span data-stu-id="acda6-119">The **clsMedium** member of the **REGPINMEDIUM** structure specifies the class identifier (CLSID) for the medium.</span></span> <span data-ttu-id="acda6-120">Pour récupérer le support d’un pin, appelez la méthode [**IKsPin :: KsQueryMediums**](ikspin-ksquerymediums.md) .</span><span class="sxs-lookup"><span data-stu-id="acda6-120">To retrieve a pin's medium, call the [**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md) method.</span></span> <span data-ttu-id="acda6-121">Cette méthode retourne un pointeur vers un bloc de mémoire qui contient une structure d' [**\_ élément KSMULTIPLE**](ksmultiple-item.md) , suivie de zéro ou plusieurs structures **REGPINMEDIUM** .</span><span class="sxs-lookup"><span data-stu-id="acda6-121">This method returns a pointer to a block of memory that contains a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, followed by zero or more **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="acda6-122">Chaque structure **REGPINMEDIUM** identifie un support pris en charge par le pin.</span><span class="sxs-lookup"><span data-stu-id="acda6-122">Each **REGPINMEDIUM** structure identifies a medium the pin supports.</span></span>

<span data-ttu-id="acda6-123">Ne connectez pas un code confidentiel si le support a un CLSID de GUID \_ null ou KSMEDIUMSETID \_ standard.</span><span class="sxs-lookup"><span data-stu-id="acda6-123">Do not connect a pin if the medium has a CLSID of GUID\_NULL or KSMEDIUMSETID\_Standard.</span></span> <span data-ttu-id="acda6-124">Il s’agit de valeurs par défaut indiquant que le code confidentiel ne prend pas en charge les supports.</span><span class="sxs-lookup"><span data-stu-id="acda6-124">These are default values indicating that the pin does not support mediums.</span></span>

<span data-ttu-id="acda6-125">En outre, ne connectez pas un code confidentiel, sauf si le filtre requiert exactement une instance connectée de ce code PIN.</span><span class="sxs-lookup"><span data-stu-id="acda6-125">Also, do not connect a pin unless the filter requires exactly one connected instance of that pin.</span></span> <span data-ttu-id="acda6-126">Dans le cas contraire, votre application peut essayer de connecter différents codes confidentiels qui ne doivent pas avoir de connexions, ce qui peut provoquer le blocage du programme.</span><span class="sxs-lookup"><span data-stu-id="acda6-126">Otherwise, your application might try to connect various pins that shouldn't have connections, which can cause the program to stop responding.</span></span> <span data-ttu-id="acda6-127">Pour déterminer le nombre d’instances requises, récupérez le \_ jeu de propriétés NECESSARYINSTANCES du code confidentiel KSPROPERTY \_ , comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="acda6-127">To find out the number of required instances, retrieve the KSPROPERTY\_PIN\_NECESSARYINSTANCES property set, as shown in the following code example.</span></span> <span data-ttu-id="acda6-128">(Par souci de concision, cet exemple ne teste pas les codes de retour ou ne libère aucune interface.</span><span class="sxs-lookup"><span data-stu-id="acda6-128">(For brevity, this example does not test any return codes or release any interfaces.</span></span> <span data-ttu-id="acda6-129">Votre application doit faire les deux, bien sûr.)</span><span class="sxs-lookup"><span data-stu-id="acda6-129">Your application should do both, of course.)</span></span>


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



<span data-ttu-id="acda6-130">Le pseudo-code suivant est un bref aperçu qui montre comment rechercher et connecter les filtres WDM.</span><span class="sxs-lookup"><span data-stu-id="acda6-130">The following pseudocode is an extremely brief outline showing how to find and connect the WDM filters.</span></span> <span data-ttu-id="acda6-131">Il omet de nombreux détails et est destiné uniquement à illustrer les étapes générales que votre application doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="acda6-131">It omits many details, and is only meant to show the general steps your application would need to take.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="acda6-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acda6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acda6-133">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="acda6-133">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



