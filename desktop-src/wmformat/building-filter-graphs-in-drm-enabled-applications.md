---
title: Création de graphiques de filtre dans les applications DRM-Enabled
description: Création de graphiques de filtre dans les applications DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Media Format SDK, création de graphiques de filtres
- Windows Media Format SDK, DirectShow
- Kit de développement logiciel (SDK) Windows Media format, applications compatibles DRM
- ASF (Advanced Systems Format), création de graphiques de filtres
- ASF (format des systèmes avancés), création de graphiques de filtres
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), applications compatibles DRM
- ASF (Advanced Systems Format), applications compatibles DRM
- DirectShow, création de graphiques de filtres
- DirectShow, applications compatibles DRM
- gestion des droits numériques (DRM), DirectShow
- DRM (gestion des droits numériques), DirectShow
- gestion des droits numériques (DRM), création de graphiques de filtres
- DRM (gestion des droits numériques), création de graphiques de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314330"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a><span data-ttu-id="1acb4-118">Création de graphiques de filtre dans les applications DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="1acb4-118">Building Filter Graphs in DRM-Enabled Applications</span></span>

<span data-ttu-id="1acb4-119">Si votre application DirectShow prend en charge la lecture des fichiers protégés par DRM, vous ne devez généralement pas utiliser **RenderFile** pour créer le graphique de filtre, car il n’existe aucun moyen de spécifier les droits DRM que vous demandez avant l’ouverture du fichier.</span><span class="sxs-lookup"><span data-stu-id="1acb4-119">If your DirectShow application supports playback of DRM-protected files, then you generally should not use **RenderFile** to create the filter graph because there is no way to specify which DRM rights you are requesting before the file is opened.</span></span> <span data-ttu-id="1acb4-120">Par défaut, le lecteur ASF WM demande uniquement des droits de lecture.</span><span class="sxs-lookup"><span data-stu-id="1acb4-120">The WM ASF Reader by default asks for only playback rights.</span></span> <span data-ttu-id="1acb4-121">Le filtre n’est pas ajouté au graphique et n’est donc pas détectable par les applications, jusqu’à ce qu’un fichier soit ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="1acb4-121">The filter is not added to the graph, and is therefore not discoverable by applications, until a file is successfully opened.</span></span>

<span data-ttu-id="1acb4-122">Pour créer un graphique de lecture compatible DRM à l’aide du [lecteur ASF WM](wm-asf-reader-filter.md), vous devez instancier le filtre à l’aide de **CoCreateInstance**, l’ajouter au graphique de filtre à l’aide de **IGraphBuilder :: AddFilter**, le configurer, puis restituer ses broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="1acb4-122">To build a DRM-enabled playback graph using the [WM ASF Reader](wm-asf-reader-filter.md), you must instantiate the filter using **CoCreateInstance**, add it to the filter graph using **IGraphBuilder::AddFilter**, configure it, and then render its output pins.</span></span> <span data-ttu-id="1acb4-123">Cette technique est illustrée dans l’exemple PlayWndASF.</span><span class="sxs-lookup"><span data-stu-id="1acb4-123">This technique is demonstrated in the PlayWndASF sample.</span></span> <span data-ttu-id="1acb4-124">Lorsque vous générez le graphique de cette manière, vous disposez déjà du pointeur **IBaseFilter** qui peut être utilisé pour appeler **QueryService** afin d’obtenir **IWMDRMWriter**.</span><span class="sxs-lookup"><span data-stu-id="1acb4-124">When you build the graph in this way, you already have the **IBaseFilter** pointer that can be used to call **QueryService** to obtain **IWMDRMWriter**.</span></span> <span data-ttu-id="1acb4-125">Toutefois, cette interface n’est pas disponible tant que l’objet lecteur du kit de développement logiciel (SDK) de format Windows Media n’est pas créé en interne par le lecteur ASF WM.</span><span class="sxs-lookup"><span data-stu-id="1acb4-125">However, this interface is not available until the Windows Media Format SDK reader object is created internally by the WM ASF Reader.</span></span> <span data-ttu-id="1acb4-126">La première opportunité pour laquelle l’application doit définir les droits DRM est dans son WMT \_ aucun \_ Gestionnaire d' \_ événements (par exemple), comme indiqué dans cet extrait de code :</span><span class="sxs-lookup"><span data-stu-id="1acb4-126">The first opportunity the application has to set DRM rights is in its WMT\_NO\_RIGHTS\_EX event handler, as shown in this code snippet:</span></span>


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a><span data-ttu-id="1acb4-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1acb4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1acb4-128">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="1acb4-128">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="1acb4-129">**Liste des attributs DRM**</span><span class="sxs-lookup"><span data-stu-id="1acb4-129">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="1acb4-130">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="1acb4-130">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="1acb4-131">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="1acb4-131">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="1acb4-132">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="1acb4-132">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[<span data-ttu-id="1acb4-133">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="1acb4-133">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




