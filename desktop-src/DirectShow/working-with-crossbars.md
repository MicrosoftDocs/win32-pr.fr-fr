---
description: Utilisation des conversions
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Utilisation des conversions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539735"
---
# <a name="working-with-crossbars"></a><span data-ttu-id="f2ca0-103">Utilisation des conversions</span><span class="sxs-lookup"><span data-stu-id="f2ca0-103">Working with Crossbars</span></span>

<span data-ttu-id="f2ca0-104">Si une carte de capture vidéo a plusieurs entrées physiques, ou si elle prend en charge plusieurs chemins d’accès matériels pour les données, le graphique de filtre peut contenir le filtre de la barre d' [affichage vidéo analogique](analog-video-crossbar-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f2ca0-104">If a video capture card has more than one physical input, or supports more than one hardware path for data, then the filter graph may contain the [Analog Video Crossbar Filter](analog-video-crossbar-filter.md).</span></span> <span data-ttu-id="f2ca0-105">Le générateur de graphiques de capture ajoute automatiquement ce filtre si nécessaire. il sera amont du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-105">The Capture Graph Builder automatically adds this filter when needed; it will be upstream from the capture filter.</span></span> <span data-ttu-id="f2ca0-106">Selon le matériel, le graphique de filtre peut contenir plusieurs instances du filtre de la barre.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-106">Depending on the hardware, the filter graph might contain more than one instance of the crossbar filter.</span></span>

<span data-ttu-id="f2ca0-107">Le filtre de distributeur expose l’interface [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , que vous pouvez utiliser pour acheminer une entrée particulière vers une sortie particulière.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-107">The crossbar filter exposes the [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) interface, which you can use to route a particular input to a particular output.</span></span> <span data-ttu-id="f2ca0-108">Par exemple, une carte vidéo peut avoir un connecteur coaxial et une entrée S-Video.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-108">For example, a video card might have a coaxial connector and an S-Video input.</span></span> <span data-ttu-id="f2ca0-109">Celles-ci sont représentées en tant que broches d’entrée sur le filtre de la barre.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-109">These would be represented as input pins on the crossbar filter.</span></span> <span data-ttu-id="f2ca0-110">Pour sélectionner une entrée, acheminez la broche d’entrée correspondante vers la broche de sortie du distributeur, à l’aide de la méthode [**IAMCrossbar :: route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="f2ca0-110">To select an input, route the corresponding input pin to the crossbar's output pin, using the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

<span data-ttu-id="f2ca0-111">Pour rechercher des filtres de barre dans le graphique, vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) pour rechercher des filtres qui prennent en charge **IAMCrossbar**.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-111">To locate crossbar filters in the graph, you can use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to search for filters that support **IAMCrossbar**.</span></span> <span data-ttu-id="f2ca0-112">Par exemple, le code suivant recherche deux transformateurs :</span><span class="sxs-lookup"><span data-stu-id="f2ca0-112">For example, the following code searches for two crossbars:</span></span>


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



<span data-ttu-id="f2ca0-113">Pour une approche plus généralisée, consultez la classe CCrossbar dans l' [exemple AMCAP](amcap-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f2ca0-113">For a more generalized approach, see the CCrossbar class in the [AmCap Sample](amcap-sample.md).</span></span>

<span data-ttu-id="f2ca0-114">Une fois que vous avez un pointeur vers l’interface **IAMCrossbar** , vous pouvez obtenir des informations sur le filtre de la barre, y compris le type physique de chaque pin, et la matrice de laquelle les broches d’entrée peuvent être routées vers les broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-114">Once you have a pointer to the **IAMCrossbar** interface, you can get information about the crossbar filter, including the physical type of each pin, and the matrix of which input pins can be routed to which output pins.</span></span>

-   <span data-ttu-id="f2ca0-115">Pour déterminer le type de connecteur physique auquel correspond un code confidentiel, appelez la méthode [**IAMCrossbar :: obtenir \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) .</span><span class="sxs-lookup"><span data-stu-id="f2ca0-115">To determine the type of physical connector to which a pin corresponds, call the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method.</span></span> <span data-ttu-id="f2ca0-116">La méthode retourne un membre de l’énumération [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) .</span><span class="sxs-lookup"><span data-stu-id="f2ca0-116">The method returns a member of the [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) enumeration.</span></span> <span data-ttu-id="f2ca0-117">Par exemple, un code confidentiel S-Video retourne la valeur PhysConn \_ Video \_ SVIDEO.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-117">For example, an S-Video pin returns the value PhysConn\_Video\_SVideo.</span></span>

    <span data-ttu-id="f2ca0-118">La méthode d' **extraction \_ CrossbarInfo** indique également si deux broches sont liées les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-118">The **get\_CrossbarInfo** method also indicates whether two pins are related to each other.</span></span> <span data-ttu-id="f2ca0-119">Par exemple, un code confidentiel vidéo peut être associé à un code confidentiel audio.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-119">For example, a video tuner pin might be related to an audio tuner pin.</span></span> <span data-ttu-id="f2ca0-120">Les broches associées ont le même sens du code confidentiel et font généralement partie du même connecteur ou de la même prise physique sur la carte.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-120">Related pins have the same pin direction, and are typically part of the same physical jack or connector on the card.</span></span>

-   <span data-ttu-id="f2ca0-121">Pour déterminer si vous pouvez acheminer une broche d’entrée vers une broche de sortie particulière, appelez la méthode [**IAMCrossbar :: CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .</span><span class="sxs-lookup"><span data-stu-id="f2ca0-121">To determine whether you can route an input pin to a particular output pin, call the [**IAMCrossbar::CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) method.</span></span>
-   <span data-ttu-id="f2ca0-122">Pour déterminer le routage actuel entre les codes confidentiels, appelez la méthode [**IAMCrossbar :: obtenir \_ IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .</span><span class="sxs-lookup"><span data-stu-id="f2ca0-122">To determine the current routing between pins, call the [**IAMCrossbar::get\_IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) method.</span></span>

<span data-ttu-id="f2ca0-123">Les méthodes précédentes spécifient toutes les broches par numéro d’index, les broches de sortie et les broches d’entrée étant indexées à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-123">The previous methods all specify pins by index number, with output pins and input pins both indexed from zero.</span></span> <span data-ttu-id="f2ca0-124">Appelez la méthode **IAMCrossbar :: obtenir \_ PinCounts** pour rechercher le nombre de broches sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-124">Call the **IAMCrossbar::get\_PinCounts** method to find the number of pins on the filter.</span></span>

<span data-ttu-id="f2ca0-125">Par exemple, le code suivant affiche des informations sur un filtre de barre transversale dans la fenêtre de console :</span><span class="sxs-lookup"><span data-stu-id="f2ca0-125">For example, the following code displays information about a crossbar filter to the console window:</span></span>


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



<span data-ttu-id="f2ca0-126">Pour une carte hypothétique, cette fonction peut produire la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="f2ca0-126">For a hypothetical card, this function might produce the following output:</span></span>


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



<span data-ttu-id="f2ca0-127">Du côté de la sortie, le S-Video et le tuner vidéo sont tous deux liés au décodeur audio.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-127">On the output side, the S-Video and the video tuner are both related to the audio decoder.</span></span> <span data-ttu-id="f2ca0-128">Du côté de l’entrée, le tuner vidéo est lié au tuner audio et la vidéo S est associée à la ligne audio dans.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-128">On the input side, the video tuner is related to the audio tuner, and the S-Video is related to the audio line in.</span></span> <span data-ttu-id="f2ca0-129">L’entrée S-Video est routée vers la sortie S-Video ; et l’entrée du syntoniseur vidéo est acheminée vers la sortie du tuner vidéo.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-129">The S-Video input is routed to the S-Video output; and the video tuner input is routed to the video tuner output.</span></span> <span data-ttu-id="f2ca0-130">Actuellement, rien n’est routé vers le décodeur audio, mais la ligne audio dans ou le tuner audio peuvent être routés vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="f2ca0-130">Currently nothing is routed to the audio decoder, but either the audio line in or the audio tuner could be routed to it.</span></span>

<span data-ttu-id="f2ca0-131">Vous pouvez modifier le routage existant en appelant la méthode [**IAMCrossbar :: route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="f2ca0-131">You can change the existing routing by calling the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

 

 



