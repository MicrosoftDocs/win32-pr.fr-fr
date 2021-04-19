---
description: Écriture d’un fichier Windows Media dans DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Écriture d’un fichier Windows Media dans DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537174"
---
# <a name="writing-a-windows-media-file-in-des"></a><span data-ttu-id="62bc2-103">Écriture d’un fichier Windows Media dans DES</span><span class="sxs-lookup"><span data-stu-id="62bc2-103">Writing a Windows Media File in DES</span></span>

<span data-ttu-id="62bc2-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="62bc2-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="62bc2-105">Cette section décrit comment écrire un fichier Windows Media à l’aide des [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="62bc2-105">This section describes how to write a Windows Media file using [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62bc2-106">N’utilisez pas le moteur de rendu intelligent pour écrire des fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="62bc2-106">Do not use the Smart Render Engine to write Windows Media files.</span></span> <span data-ttu-id="62bc2-107">Utilisez toujours le moteur de rendu de base (CLSID \_ RenderEngine).</span><span class="sxs-lookup"><span data-stu-id="62bc2-107">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

 

<span data-ttu-id="62bc2-108">Pour écrire un fichier Windows Media, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="62bc2-108">To write a Windows Media file, do the following:</span></span>

1.  <span data-ttu-id="62bc2-109">Appelez **SetSite** sur le moteur de rendu, avec un pointeur vers votre fournisseur de clés.</span><span class="sxs-lookup"><span data-stu-id="62bc2-109">Call **SetSite** on the render engine, with a pointer to your key provider.</span></span>
2.  <span data-ttu-id="62bc2-110">Créez le composant frontal du graphique.</span><span class="sxs-lookup"><span data-stu-id="62bc2-110">Build the front end of the graph.</span></span> <span data-ttu-id="62bc2-111">(Consultez [rendu d’un projet](rendering-a-project.md).)</span><span class="sxs-lookup"><span data-stu-id="62bc2-111">(See [Rendering a Project](rendering-a-project.md).)</span></span>
3.  <span data-ttu-id="62bc2-112">Créez le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) et ajoutez-le au graphique.</span><span class="sxs-lookup"><span data-stu-id="62bc2-112">Create the [WM ASF Writer](wm-asf-writer-filter.md) filter and add it to the graph.</span></span>
4.  <span data-ttu-id="62bc2-113">Utilisez l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) sur le filtre du writer WM ASF pour définir le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="62bc2-113">Use the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface on the WM ASF Writer filter to set the file name.</span></span>
5.  <span data-ttu-id="62bc2-114">Configurez l’enregistreur ASF WM pour utiliser un profil Windows Media.</span><span class="sxs-lookup"><span data-stu-id="62bc2-114">Configure the WM ASF Writer to use a Windows Media profile.</span></span> <span data-ttu-id="62bc2-115">Chaque profil a un nombre prédéfini de flux.</span><span class="sxs-lookup"><span data-stu-id="62bc2-115">Each profile has a predefined number of streams.</span></span> <span data-ttu-id="62bc2-116">Vous devez choisir un profil qui correspond aux groupes de votre projet.</span><span class="sxs-lookup"><span data-stu-id="62bc2-116">You must choose a profile that matches the groups in your project.</span></span>

    <span data-ttu-id="62bc2-117">L’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contient différentes méthodes pour définir le profil.</span><span class="sxs-lookup"><span data-stu-id="62bc2-117">The [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface contains a few different methods for setting the profile.</span></span> <span data-ttu-id="62bc2-118">Par exemple, la méthode **ConfigureFilterUsingProfileGuid** spécifie un profil système comme GUID.</span><span class="sxs-lookup"><span data-stu-id="62bc2-118">For example, the **ConfigureFilterUsingProfileGuid** method specifies a system profile as a GUID.</span></span> <span data-ttu-id="62bc2-119">Vous pouvez utiliser les méthodes de format Windows Media pour récupérer un pointeur **IWMProfile** , puis appeler [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span><span class="sxs-lookup"><span data-stu-id="62bc2-119">Or, you can use Windows Media Format methods to get an **IWMProfile** pointer and then call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span></span> <span data-ttu-id="62bc2-120">Pour plus d’informations, consultez [configuration de l’enregistreur ASF](configuring-the-asf-writer.md).</span><span class="sxs-lookup"><span data-stu-id="62bc2-120">For more information, see [Configuring the ASF Writer](configuring-the-asf-writer.md).</span></span>

6.  <span data-ttu-id="62bc2-121">Connectez le serveur frontal à l’enregistreur ASF.</span><span class="sxs-lookup"><span data-stu-id="62bc2-121">Connect the front end to the ASF Writer.</span></span> <span data-ttu-id="62bc2-122">La partie frontale du graphique contient une broche de sortie pour chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="62bc2-122">The front end of the graph contains one output pin for each group.</span></span> <span data-ttu-id="62bc2-123">En supposant que vous avez spécifié un profil compatible, l’enregistreur ASF doit avoir un ensemble de broches d’entrée correspondant.</span><span class="sxs-lookup"><span data-stu-id="62bc2-123">Assuming that you specified a compatible profile, the ASF Writer should have a matching set of input pins.</span></span> <span data-ttu-id="62bc2-124">Connectez chaque broche de sortie à la broche d’entrée correspondante.</span><span class="sxs-lookup"><span data-stu-id="62bc2-124">Connect each output pin to the corresponding input pin.</span></span> <span data-ttu-id="62bc2-125">Le moyen le plus simple consiste à utiliser la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) .</span><span class="sxs-lookup"><span data-stu-id="62bc2-125">The easiest way to do this is using the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="62bc2-126">Tout d’abord, créez une nouvelle instance du [Générateur de graphiques de capture](capture-graph-builder.md) et initialisez-la avec un pointeur vers le gestionnaire de graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="62bc2-126">First, create a new instance of the [Capture Graph Builder](capture-graph-builder.md) and initialize it with a pointer to the Filter Graph Manager:</span></span>

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    <span data-ttu-id="62bc2-127">Ensuite, récupérez la broche de sortie pour chaque groupe en appelant la méthode [**IRenderEngine :: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="62bc2-127">Next, retrieve the output pin for each group by calling the [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) method.</span></span> <span data-ttu-id="62bc2-128">Appelez **RenderStream** pour connecter le pin à l’enregistreur ASF :</span><span class="sxs-lookup"><span data-stu-id="62bc2-128">Call **RenderStream** to connect the pin to the ASF Writer:</span></span>

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a><span data-ttu-id="62bc2-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62bc2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62bc2-130">Utilisation de Windows Media avec les services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="62bc2-130">Using Windows Media With DirectShow Editing Services</span></span>](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



