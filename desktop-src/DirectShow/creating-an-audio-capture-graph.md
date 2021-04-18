---
description: Création d’un graphique de capture audio
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Création d’un graphique de capture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515912"
---
# <a name="creating-an-audio-capture-graph"></a><span data-ttu-id="5cb9e-103">Création d’un graphique de capture audio</span><span class="sxs-lookup"><span data-stu-id="5cb9e-103">Creating an Audio Capture Graph</span></span>

<span data-ttu-id="5cb9e-104">La première étape pour une application de capture audio consiste à créer un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-104">The first step for an audio capture application is to build a filter graph.</span></span> <span data-ttu-id="5cb9e-105">La configuration du graphique dépend du type de fichier que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-105">The configuration of the graph depends on the type of file that you want to create.</span></span>

-   <span data-ttu-id="5cb9e-106">Fichier AVI audio uniquement : filtre de capture audio vers un filtre [multiplex MUX](avi-mux-filter.md) et le filtre AVI MUX en [writer de fichier](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5cb9e-106">Audio-only AVI file: Audio Capture Filter to [AVI Mux](avi-mux-filter.md) filter, and AVI Mux to [File Writer](file-writer-filter.md) filter.</span></span>
-   <span data-ttu-id="5cb9e-107">Fichier WAV : filtre de capture audio de l' [exemple de filtre Wavdest](wavdest-filter-sample.md) au filtre de writer de fichier</span><span class="sxs-lookup"><span data-stu-id="5cb9e-107">WAV file: Audio Capture Filter to [WavDest Filter Sample](wavdest-filter-sample.md) to File Writer Filter</span></span>
-   <span data-ttu-id="5cb9e-108">Fichier Windows Media Audio (. WMA) : filtre de capture audio pour le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5cb9e-108">Windows Media Audio (.wma) file: Audio Capture Filter to [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

<span data-ttu-id="5cb9e-109">Le filtre WavDest est fourni en tant qu’exemple du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="5cb9e-109">The WavDest filter is provided as an SDK sample.</span></span> <span data-ttu-id="5cb9e-110">Pour l’utiliser, vous devez générer et inscrire le filtre.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-110">To use it, you must build and register the filter.</span></span>

<span data-ttu-id="5cb9e-111">Pour utiliser le filtre de l’enregistreur ASF, vous devez installer le kit de développement logiciel (SDK) Windows Media et obtenir une clé logicielle pour déverrouiller le filtre.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-111">To use the ASF Writer filter, you must install the Windows Media SDK and obtain a software key to unlock the filter.</span></span> <span data-ttu-id="5cb9e-112">Pour plus d’informations, consultez [utilisation de Windows Media dans DirectShow](using-windows-media-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="5cb9e-112">For more information, see [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).</span></span>

<span data-ttu-id="5cb9e-113">Vous pouvez générer le graphique de filtre à l’aide de l’objet de [Générateur de graphiques de capture](capture-graph-builder.md) , ou vous pouvez générer le graphique « manuellement ». autrement dit, l’application doit-elle ajouter et connecter chaque filtre par programmation.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-113">You can build the filter graph using the [Capture Graph Builder](capture-graph-builder.md) object, or you can build the graph "manually"; that is, have the application programmatically add and connect each filter.</span></span> <span data-ttu-id="5cb9e-114">Cet article décrit l’approche manuelle.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-114">This article describes the manual approach.</span></span> <span data-ttu-id="5cb9e-115">Pour plus d’informations sur l’utilisation du générateur de graphiques de capture, consultez [Video capture](video-capture.md).</span><span class="sxs-lookup"><span data-stu-id="5cb9e-115">For more information about using the Capture Graph Builder, see [Video Capture](video-capture.md).</span></span> <span data-ttu-id="5cb9e-116">La plupart des informations contenues dans cet article s’appliquent aux graphiques audio uniquement.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-116">Much of the information in that article applies to audio-only graphs.</span></span>

<span data-ttu-id="5cb9e-117">Ajout du périphérique de capture audio</span><span class="sxs-lookup"><span data-stu-id="5cb9e-117">Adding the Audio Capture Device</span></span>

<span data-ttu-id="5cb9e-118">Étant donné que le filtre de capture audio communique avec un périphérique matériel spécifique, vous ne pouvez pas simplement appeler **CoCreateInstance** pour créer le filtre.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-118">Because the Audio Capture Filter communicates with a specific hardware device, you cannot simply call **CoCreateInstance** to create the filter.</span></span> <span data-ttu-id="5cb9e-119">Utilisez plutôt l' [énumérateur de périphérique système](system-device-enumerator.md) pour énumérer tous les appareils dans la catégorie « sources de capture audio », qui est identifiée par l’identificateur de classe CLSID \_ AudioInputDeviceCategory.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-119">Instead, use the [System Device Enumerator](system-device-enumerator.md) to enumerate all of the devices in the "Audio Capture Sources" category, which is identified by the class identifier CLSID\_AudioInputDeviceCategory.</span></span>

<span data-ttu-id="5cb9e-120">L’énumérateur de périphérique système retourne la liste des monikers pour les appareils ; le nom convivial de chaque moniker correspond au nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-120">The System Device Enumerator returns a list of monikers for the devices; each moniker's friendly name corresponds to the name of the device.</span></span> <span data-ttu-id="5cb9e-121">Choisissez l’un des monikers retournés et utilisez-le pour créer une instance du filtre de capture audio pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-121">Choose one of the returned monikers and use it to create an instance of the Audio Capture Filter for that device.</span></span> <span data-ttu-id="5cb9e-122">Ajoutez le filtre au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-122">Add the filter to the filter graph.</span></span> <span data-ttu-id="5cb9e-123">L’appareil d’enregistrement audio préféré de l’utilisateur apparaît en premier dans la liste moniker.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-123">The user's preferred audio recording device appears first in the moniker list.</span></span> <span data-ttu-id="5cb9e-124">(L’utilisateur sélectionne un appareil par défaut en cliquant sur sons et multimédia dans le panneau de configuration.)</span><span class="sxs-lookup"><span data-stu-id="5cb9e-124">(The user selects a preferred device by clicking Sounds and Multimedia in Control Panel.)</span></span>

<span data-ttu-id="5cb9e-125">Pour plus d’informations, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="5cb9e-125">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="5cb9e-126">Pour spécifier l’entrée à partir de laquelle effectuer la capture, obtenez l’interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) à partir du filtre de capture audio et appelez la méthode **put \_ Enable** pour spécifier l’entrée.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-126">To specify which input to capture from, obtain the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface from the Audio Capture filter and call the **put\_Enable** method to specify the input.</span></span> <span data-ttu-id="5cb9e-127">Toutefois, une limitation de cette méthode est que différents périphériques matériels peuvent utiliser des chaînes différentes pour identifier leurs entrées.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-127">One limitation of this method, however, is that different hardware devices may use different strings to identify their inputs.</span></span> <span data-ttu-id="5cb9e-128">Par exemple, une carte peut utiliser le « microphone » pour identifier l’entrée microphone et une autre carte peut utiliser « MIC ».</span><span class="sxs-lookup"><span data-stu-id="5cb9e-128">For example, one card may use "Microphone" to identify the microphone input and another card may use "Mic".</span></span> <span data-ttu-id="5cb9e-129">Pour déterminer l’identificateur de chaîne pour une entrée donnée, utilisez les fonctions multimédias de Windows [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))et [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5cb9e-129">To determine the string identifier for a given input, use the Windows Multimedia functions [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85)), and [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span></span> <span data-ttu-id="5cb9e-130">Pour plus d’informations, consultez la rubrique MSDN consacrée aux [requêtes de périphérique](/windows/desktop/Multimedia/mixer-device-queries) .</span><span class="sxs-lookup"><span data-stu-id="5cb9e-130">See the MSDN topic [Mixer Device Queries](/windows/desktop/Multimedia/mixer-device-queries) for more information.</span></span>

<span data-ttu-id="5cb9e-131">Ajout du multiplexeur et du writer de fichier</span><span class="sxs-lookup"><span data-stu-id="5cb9e-131">Adding the Multiplexer and the File Writer</span></span>

<span data-ttu-id="5cb9e-132">Un graphique de capture audio doit contenir un multiplexeur et un writer de fichier.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-132">An audio capture graph must contain a multiplexer and a file writer.</span></span>

<span data-ttu-id="5cb9e-133">Un *multiplexeur* est un filtre qui associe un ou plusieurs flux en un seul flux avec un format particulier.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-133">A *multiplexer* is a filter that combines one or more streams into a single stream with a particular format.</span></span> <span data-ttu-id="5cb9e-134">Par exemple, le filtre multiplexeur AVI combine des flux audio et vidéo dans un flux AVI entrelacé.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-134">For example, the AVI Mux filter combines audio and video streams into an interleaved AVI stream.</span></span> <span data-ttu-id="5cb9e-135">Pour la capture audio, il n’y a généralement qu’un seul flux audio, mais les données audio doivent toujours être empaquetées dans un format qui peut être enregistré sur le disque, ce qui nécessite un multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-135">For audio capture, there is typically only a single audio stream, but the audio data must still be packaged into a format that can be saved to disk, which requires a multiplexer.</span></span> <span data-ttu-id="5cb9e-136">Le choix du multiplexeur dépend du format cible :</span><span class="sxs-lookup"><span data-stu-id="5cb9e-136">The choice of multiplexer depends on the target format:</span></span>

-   <span data-ttu-id="5cb9e-137">AVI : multiplexeur AVI</span><span class="sxs-lookup"><span data-stu-id="5cb9e-137">AVI: AVI Multiplexer</span></span>
-   <span data-ttu-id="5cb9e-138">WAV : WavDest</span><span class="sxs-lookup"><span data-stu-id="5cb9e-138">WAV: WavDest</span></span>
-   <span data-ttu-id="5cb9e-139">WMA : enregistreur ASF</span><span class="sxs-lookup"><span data-stu-id="5cb9e-139">WMA: ASF Writer</span></span>

<span data-ttu-id="5cb9e-140">Un *enregistreur de fichier* est un filtre qui écrit des données entrantes dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-140">A *file writer* is a filter that writes incoming data to a file.</span></span> <span data-ttu-id="5cb9e-141">Pour les fichiers AVI ou WAV, utilisez le [filtre du writer de fichier](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="5cb9e-141">For AVI or WAV files, use the [File Writer Filter](file-writer-filter.md).</span></span> <span data-ttu-id="5cb9e-142">Pour les fichiers WMA, le writer ASF agit à la fois en tant que multiplexeur et writer de fichier.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-142">For WMA files, the ASF Writer acts as both multiplexer and file writer.</span></span>

<span data-ttu-id="5cb9e-143">Après avoir créé les filtres et les avoir ajoutés au graphique, connectez la broche de sortie du filtre de capture audio à la broche d’entrée du multiplexeur et connectez la broche de sortie du multiplexeur à la broche d’entrée du générateur de filtre (en supposant que ces filtres soient distincts).</span><span class="sxs-lookup"><span data-stu-id="5cb9e-143">After you create the filters and add them to the graph, connect the Audio Capture Filter's output pin to the multiplexer's input pin, and connect the multiplexer's output pin to the filter writer's input pin (assuming these are separate filters).</span></span> <span data-ttu-id="5cb9e-144">Pour spécifier le nom de fichier, interrogez le writer de fichier de l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) et appelez la méthode [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .</span><span class="sxs-lookup"><span data-stu-id="5cb9e-144">To specify the file name, query the file writer for the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface and call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method.</span></span>

### <a name="example-code"></a><span data-ttu-id="5cb9e-145">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="5cb9e-145">Example Code</span></span>

<span data-ttu-id="5cb9e-146">L’exemple suivant montre comment générer un graphique de capture audio à l’aide du filtre WavDest.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-146">The following example shows how to build an audio capture graph using the WavDest filter.</span></span> <span data-ttu-id="5cb9e-147">Les mêmes principes s’appliquent aux autres types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-147">The same principles apply for the other file types.</span></span>


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



<span data-ttu-id="5cb9e-148">Cet exemple utilise la `AddFilterByCLSID` fonction décrite dans [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md)et la `ConnectFilters` fonction décrite dans [connecter deux filtres](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5cb9e-148">This example uses the `AddFilterByCLSID` function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the `ConnectFilters` function described in [Connect Two Filters](connect-two-filters.md).</span></span> <span data-ttu-id="5cb9e-149">Aucun de ces n’est une API DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5cb9e-149">Neither of these is a DirectShow API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cb9e-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5cb9e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cb9e-151">Capture audio</span><span class="sxs-lookup"><span data-stu-id="5cb9e-151">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 
