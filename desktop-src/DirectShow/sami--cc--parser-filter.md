---
description: Filtre de l’analyseur SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Filtre de l’analyseur SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0449bccd41a09fca952b5d84552ef919055526
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522039"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="89f11-103">Filtre de l’analyseur SAMI (CC)</span><span class="sxs-lookup"><span data-stu-id="89f11-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="89f11-104">Analyse les données de sous-titrage des fichiers SAMI (Synchronized Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="89f11-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="89f11-105">SAMI est un format de texte similaire à HTML et est utilisé pour l’encodage des légendes basées sur le temps.</span><span class="sxs-lookup"><span data-stu-id="89f11-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="89f11-106">Ce filtre convertit les données SAMI en un flux de texte.</span><span class="sxs-lookup"><span data-stu-id="89f11-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="89f11-107">Chaque échantillon du flux contient une entrée de légende, ainsi que des informations de format.</span><span class="sxs-lookup"><span data-stu-id="89f11-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="89f11-108">Les horodatages des échantillons sont générés à partir des informations d’heure dans le fichier SAMI.</span><span class="sxs-lookup"><span data-stu-id="89f11-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="89f11-109">Ce filtre est conçu pour être utilisé avec le filtre de [convertisseur de commande de script interne](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="89f11-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="89f11-110">Le convertisseur de commande de script interne reçoit les exemples de texte et les envoie à l’application, sous la forme de notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="89f11-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="89f11-111">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="89f11-111">For more information, see the Remarks section.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89f11-112">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="89f11-112">Filter Interfaces</span></span>                        | <span data-ttu-id="89f11-113">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="89f11-113">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="89f11-114">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="89f11-115">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="89f11-115">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="89f11-116">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="89f11-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="89f11-117">[**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="89f11-117">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="89f11-118">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="89f11-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="89f11-119">\_Texte de MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="89f11-119">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="89f11-120">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="89f11-120">Output Pin Interfaces</span></span>                    | <span data-ttu-id="89f11-121">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="89f11-121">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="89f11-122">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="89f11-122">Filter CLSID</span></span>                             | <span data-ttu-id="89f11-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="89f11-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="89f11-124">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="89f11-124">Property Page CLSID</span></span>                      | <span data-ttu-id="89f11-125">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="89f11-125">No property page</span></span>                                                                                         |
| <span data-ttu-id="89f11-126">Exécutable</span><span class="sxs-lookup"><span data-stu-id="89f11-126">Executable</span></span>                               | <span data-ttu-id="89f11-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="89f11-127">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="89f11-128">Mérite</span><span class="sxs-lookup"><span data-stu-id="89f11-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="89f11-129">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="89f11-129">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="89f11-130">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="89f11-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="89f11-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="89f11-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="89f11-132">Notes</span><span class="sxs-lookup"><span data-stu-id="89f11-132">Remarks</span></span>

<span data-ttu-id="89f11-133">Voici un fichier SAMI simple :</span><span class="sxs-lookup"><span data-stu-id="89f11-133">The following is a simple SAMI file:</span></span>


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



<span data-ttu-id="89f11-134">La balise **style** définit deux paramètres de langue, anglais (. ENCC) et français (. FRCC).</span><span class="sxs-lookup"><span data-stu-id="89f11-134">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="89f11-135">Il définit également deux styles, \# normal et \# GREENTEXT.</span><span class="sxs-lookup"><span data-stu-id="89f11-135">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="89f11-136">Chaque balise de **synchronisation** définit l’heure de début d’une légende, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="89f11-136">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="89f11-137">Les balises **P** contiennent le texte de légende, tandis que l’attribut de **classe** spécifie le paramètre de langue auquel la légende s’applique.</span><span class="sxs-lookup"><span data-stu-id="89f11-137">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="89f11-138">Pour chaque langue et chaque style, le filtre crée un flux logique.</span><span class="sxs-lookup"><span data-stu-id="89f11-138">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="89f11-139">À tout moment, un seul flux de langage et un seul flux de style sont activés.</span><span class="sxs-lookup"><span data-stu-id="89f11-139">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="89f11-140">Quand le filtre génère un exemple, il sélectionne la légende de la langue active et applique le style actuel.</span><span class="sxs-lookup"><span data-stu-id="89f11-140">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="89f11-141">Par défaut, la première langue et le style déclarés dans le fichier sont activés.</span><span class="sxs-lookup"><span data-stu-id="89f11-141">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="89f11-142">Une application peut utiliser la méthode [**IAMStreamSelect :: Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) pour activer un autre flux.</span><span class="sxs-lookup"><span data-stu-id="89f11-142">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="89f11-143">Avec les paramètres par défaut, la première légende de l’exemple de fichier produit la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="89f11-143">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="89f11-144">Si la sortie est envoyée vers le convertisseur de commande de script interne, ce filtre envoie une notification d’événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="89f11-144">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="89f11-145">Le deuxième paramètre d’événement est un BSTR avec le texte de légende.</span><span class="sxs-lookup"><span data-stu-id="89f11-145">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="89f11-146">L’application peut récupérer l’événement et afficher la légende.</span><span class="sxs-lookup"><span data-stu-id="89f11-146">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="89f11-147">L’exemple suivant montre comment restituer un fichier SAMI, récupérer des informations de flux, activer des flux et afficher le texte de légende.</span><span class="sxs-lookup"><span data-stu-id="89f11-147">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="89f11-148">L’exemple suppose que le fichier SAMI précédent est enregistré en tant que C : \\ sami \_ test \_ file. sami.</span><span class="sxs-lookup"><span data-stu-id="89f11-148">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="89f11-149">Par souci de concision, cet exemple utilise des index de flux codés en dur lorsqu’il appelle la méthode **IAMStreamSelect :: Enable** .</span><span class="sxs-lookup"><span data-stu-id="89f11-149">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="89f11-150">Il effectue également une vérification des erreurs minimale.</span><span class="sxs-lookup"><span data-stu-id="89f11-150">It also performs minimal error checking.</span></span>


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



<span data-ttu-id="89f11-151">Ce filtre utilise l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) pour extraire des échantillons du filtre source.</span><span class="sxs-lookup"><span data-stu-id="89f11-151">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="89f11-152">Par conséquent, il ne prend pas en charge l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sur sa broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="89f11-152">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89f11-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89f11-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f11-154">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="89f11-154">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



