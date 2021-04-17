---
description: Aperçu de l’audio TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Aperçu de l’audio TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481481"
---
# <a name="previewing-tv-audio"></a><span data-ttu-id="030f8-103">Aperçu de l’audio TV</span><span class="sxs-lookup"><span data-stu-id="030f8-103">Previewing TV Audio</span></span>

<span data-ttu-id="030f8-104">Pour prévisualiser l’audio TV, acheminez le code confidentiel du décodeur audio sur le filtre de la barre transversale vers le code confidentiel du tuner audio.</span><span class="sxs-lookup"><span data-stu-id="030f8-104">To preview TV audio, route the Audio Decoder pin on the crossbar filter to the Audio Tuner pin.</span></span> <span data-ttu-id="030f8-105">Pour désactiver le son, acheminez le code confidentiel du décodeur audio à-1, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="030f8-105">To mute the audio, route the Audio Decoder pin to -1, as shown in the following diagram.</span></span> <span data-ttu-id="030f8-106">(Les filtres de distributeur sont décrits dans [utilisation des](working-with-crossbars.md)FlowFilters.)</span><span class="sxs-lookup"><span data-stu-id="030f8-106">(Crossbar filters are described in [Working with Crossbars](working-with-crossbars.md).)</span></span>

![routage du code confidentiel du décodeur audio](images/vidcap07.png)

<span data-ttu-id="030f8-108">L’approche de base est la suivante :</span><span class="sxs-lookup"><span data-stu-id="030f8-108">The basic approach is as follows:</span></span>

1.  <span data-ttu-id="030f8-109">Utilisez la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) pour localiser le filtre de barre.</span><span class="sxs-lookup"><span data-stu-id="030f8-109">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the crossbar filter.</span></span>
2.  <span data-ttu-id="030f8-110">Utilisez la méthode [**IAMCrossbar :: obten \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) pour énumérer les broches d’entrée et de sortie du filtre de la barre transversale.</span><span class="sxs-lookup"><span data-stu-id="030f8-110">Use the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method to enumerate the crossbar filter's input and output pins.</span></span> <span data-ttu-id="030f8-111">Recherchez une broche de sortie décodeur audio et une broche d’entrée de syntoniseur audio.</span><span class="sxs-lookup"><span data-stu-id="030f8-111">Search for an audio decoder output pin and an audio tuner input pin.</span></span>
3.  <span data-ttu-id="030f8-112">Si vous trouvez les bons pin, appelez [**IAMCrossbar :: route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) pour acheminer les broches.</span><span class="sxs-lookup"><span data-stu-id="030f8-112">If you find the correct pins, call [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) to route the pins.</span></span> <span data-ttu-id="030f8-113">Si ce n’est pas le cas, recherchez en amont un autre distributeur et répétez le processus.</span><span class="sxs-lookup"><span data-stu-id="030f8-113">If not, look upstream for another crossbar and repeat the process.</span></span>
4.  <span data-ttu-id="030f8-114">Pour désactiver le son, acheminez le code confidentiel du décodeur audio à-1.</span><span class="sxs-lookup"><span data-stu-id="030f8-114">To mute the audio, route the audio decoder pin to -1.</span></span>

<span data-ttu-id="030f8-115">La plupart des tuners TV utilisent un seul filtre de distributeur, mais certains utilisent deux filtres de distributeur.</span><span class="sxs-lookup"><span data-stu-id="030f8-115">Most TV tuners use a single crossbar filter, but some use two crossbar filters.</span></span> <span data-ttu-id="030f8-116">Par conséquent, vous devrez peut-être Rechercher un deuxième distributeur si le premier échoue.</span><span class="sxs-lookup"><span data-stu-id="030f8-116">Therefore, you might have to search for a second crossbar if the first one fails.</span></span>

> [!Note]  
> <span data-ttu-id="030f8-117">Contrairement à ce que vous pourriez espérer, aucun filtre de capture audio ou rendu audio n’est requis pour prévisualiser l’audio, car il existe une connexion physique entre la carte tuner et la carte son.</span><span class="sxs-lookup"><span data-stu-id="030f8-117">Contrary to what you might expect, no audio capture filter or audio renderer is required to preview the audio, because there is a physical connection between the tuner card and the sound card.</span></span>

 

<span data-ttu-id="030f8-118">Le code suivant illustre ces étapes plus en détail.</span><span class="sxs-lookup"><span data-stu-id="030f8-118">The following code shows these steps in more detail.</span></span> <span data-ttu-id="030f8-119">Tout d’abord, voici une fonction d’assistance qui recherche un type de code confidentiel spécifié dans un filtre de barre.</span><span class="sxs-lookup"><span data-stu-id="030f8-119">First, here is a helper function that searches a crossbar filter for a specified pin type:</span></span>


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



<span data-ttu-id="030f8-120">La fonction Next tente d’activer ou de désactiver l’audio, en fonction de la valeur du paramètre *bActivate* .</span><span class="sxs-lookup"><span data-stu-id="030f8-120">The next function attempts to activate or mute the audio, depending on the value of the *bActivate* parameter.</span></span> <span data-ttu-id="030f8-121">Il recherche les codes confidentiels requis dans le filtre de la barre de filtres spécifié.</span><span class="sxs-lookup"><span data-stu-id="030f8-121">It searches the specified crossbar filter for the required pins.</span></span> <span data-ttu-id="030f8-122">S’il ne peut pas les trouver, il retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="030f8-122">If it cannot find them, it returns an error code.</span></span>


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



<span data-ttu-id="030f8-123">La fonction Next recherche un filtre de barre dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="030f8-123">The next function searches the filter graph for a crossbar filter.</span></span> <span data-ttu-id="030f8-124">S’il en trouve un, il tente d’activer ou de désactiver le son (à l’aide de la fonction précédente).</span><span class="sxs-lookup"><span data-stu-id="030f8-124">If it finds one, it attempts to activate or mute the audio (using the previous function).</span></span> <span data-ttu-id="030f8-125">Si cette opération échoue, la méthode effectue une recherche dans le flux de données pour un deuxième distributeur et tente à nouveau.</span><span class="sxs-lookup"><span data-stu-id="030f8-125">If that operation fails, the method searches upstream for a second crossbar and tries again.</span></span> <span data-ttu-id="030f8-126">Pour une approche plus généralisée de la gestion de plusieurs filtres de distributeur dans un graphique, consultez la classe CCrossbar dans l’exemple d’application AmCap.</span><span class="sxs-lookup"><span data-stu-id="030f8-126">For a more generalized approach to managing multiple crossbar filters in a graph, see the CCrossbar class in the AmCap sample application.</span></span>


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



<span data-ttu-id="030f8-127">Le code suivant montre comment appeler ces fonctions :</span><span class="sxs-lookup"><span data-stu-id="030f8-127">The following code shows how to call these functions:</span></span>


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



<span data-ttu-id="030f8-128">Notez que ces exemples de fonctions répètent un grand nombre des appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="030f8-128">Note that these example functions repeat many of the same function calls.</span></span> <span data-ttu-id="030f8-129">Par exemple, ils énumèrent les codes confidentiels du distributeur à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="030f8-129">For example, they enumerate the crossbar pins each time.</span></span> <span data-ttu-id="030f8-130">Dans une application réelle, vous pouvez mettre en cache certaines de ces informations.</span><span class="sxs-lookup"><span data-stu-id="030f8-130">In a real application, you might cache some of this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="030f8-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="030f8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="030f8-132">Télévision analogique audio</span><span class="sxs-lookup"><span data-stu-id="030f8-132">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="030f8-133">Utilisation des conversions</span><span class="sxs-lookup"><span data-stu-id="030f8-133">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



