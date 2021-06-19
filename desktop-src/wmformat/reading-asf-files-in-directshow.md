---
title: Lecture de fichiers ASF dans DirectShow (kit de développement logiciel (SDK) Windows Media format 11)
description: La lecture des fichiers ASF est gérée par le filtre de lecteur ASF WM. En savoir plus sur la lecture de fichiers ASF dans DirectShow dans le kit de développement logiciel (SDK) Windows Media format 11.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, lire des fichiers ASF
- Kit de développement logiciel (SDK) Windows Media format, filtre de lecteur ASF WM
- Windows Media Format SDK, interface IMediaSeeking
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
- ASF (Advanced Systems Format), filtre de lecteur ASF WM
- ASF (format des systèmes avancés), filtre de lecteur ASF WM
- ASF (Advanced Systems Format), interface IMediaSeeking
- ASF (format des systèmes avancés), interface IMediaSeeking
- DirectShow, lire des fichiers ASF
- DirectShow, filtre de lecteur ASF WM
- DirectShow, interface IMediaSeeking
- Filtre de lecteur ASF WM
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaab64798011eb21edbe43f49438db99d0bae6b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404322"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="d376e-121">Lecture de fichiers ASF dans DirectShow (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="d376e-121">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="d376e-122">La lecture des fichiers ASF est gérée par le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d376e-122">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="d376e-123">Lorsque le lecteur ASF WM lit un fichier, il crée automatiquement une broche de sortie pour chaque flux, y compris les flux Web, les flux de commandes de script et tout autre type de flux arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d376e-123">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="d376e-124">Dans le cas de plusieurs fichiers à vitesse de transmission, les codes confidentiels sont créés uniquement pour les flux actuellement sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d376e-124">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="d376e-125">Le lecteur ASF WM prend en charge l’interface DirectShow **IMediaSeeking** , qui permet aux applications d’effectuer une recherche temporelle dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="d376e-125">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="d376e-126">Toutefois, la lecture à des vitesses autres que 1,0 (comme spécifié dans **IMediaSeeking ::** sesente) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d376e-126">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="d376e-127">Le filtre expose également plusieurs interfaces du kit de développement logiciel (SDK) du format Windows Media, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d376e-127">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="d376e-128">Interface</span><span class="sxs-lookup"><span data-stu-id="d376e-128">Interface</span></span>                                        | <span data-ttu-id="d376e-129">Exposition</span><span class="sxs-lookup"><span data-stu-id="d376e-129">How exposed</span></span>                            | <span data-ttu-id="d376e-130">Commentaires</span><span class="sxs-lookup"><span data-stu-id="d376e-130">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d376e-131">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="d376e-131">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="d376e-132">Via **IServiceProvider** sur le filtre</span><span class="sxs-lookup"><span data-stu-id="d376e-132">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="d376e-133">Fourni pour les applications qui doivent lire du contenu protégé par des Rights Management numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="d376e-133">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="d376e-134">Cette interface peut également être utilisée pour obtenir directement d’autres interfaces sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="d376e-134">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="d376e-135">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="d376e-135">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="d376e-136">**QueryInterface** sur le filtre</span><span class="sxs-lookup"><span data-stu-id="d376e-136">**QueryInterface** on filter</span></span>           | <span data-ttu-id="d376e-137">Fourni pour permettre aux applications de lire les attributs de fichier et de contenu, ainsi que les informations de marqueur et de script et les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d376e-137">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="d376e-138">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="d376e-138">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="d376e-139">**QueryInterface** sur le filtre</span><span class="sxs-lookup"><span data-stu-id="d376e-139">**QueryInterface** on filter</span></span>           | <span data-ttu-id="d376e-140">Partiellement implémenté sur le filtre afin que les applications puissent accéder aux méthodes d’information sur l’objet WM Reader.</span><span class="sxs-lookup"><span data-stu-id="d376e-140">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="d376e-141">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="d376e-141">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="d376e-142">**QueryInterface** sur le filtre</span><span class="sxs-lookup"><span data-stu-id="d376e-142">**QueryInterface** on filter</span></span>           | <span data-ttu-id="d376e-143">Partiellement implémenté sur le filtre afin que les applications puissent accéder aux méthodes d’information sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="d376e-143">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="d376e-144">Le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) a été mis à disposition pour la première fois dans DirectShow 8,0.</span><span class="sxs-lookup"><span data-stu-id="d376e-144">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="d376e-145">La version du filtre fourni avec DirectShow 8,1 et 9,0 prend en charge la version 7. *x* du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d376e-145">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="d376e-146">La version la plus récente du filtre, avec les autres composants QASF, est fournie avec et prend en charge le kit de développement logiciel (SDK) Windows Media Format 9 Series, ainsi que les versions ultérieures, et remplace le filtre dans DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="d376e-146">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="d376e-147">Si vous installez le kit de développement logiciel (SDK) Windows Media format après l’installation de DirectX 8. *x* ou 9. *x* SDK, vous remplacerez la version DirectX de qasf.dll par la version 9 Series.</span><span class="sxs-lookup"><span data-stu-id="d376e-147">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="d376e-148">Cela ne doit pas poser de problèmes, sauf dans un scénario où cela entraînerait un comportement différent dans la méthode DirectShow **IGraphBuilder :: RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="d376e-148">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="d376e-149">La version du kit de développement logiciel (SDK) de Windows Media Format 9 du lecteur ASF WM est le filtre source par défaut pour les extensions de nom de fichier. ASF,. wmv et. WMA.</span><span class="sxs-lookup"><span data-stu-id="d376e-149">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="d376e-150">Cela signifie que le lecteur ASF WM est automatiquement créé et ajouté au graphique de filtre par le gestionnaire de graphique de filtre dans des méthodes telles que **IGraphBuilder :: RenderFile** ou **IGraphBuilder :: AddSourceFilter** lorsqu’un fichier de ce type est spécifié.</span><span class="sxs-lookup"><span data-stu-id="d376e-150">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="d376e-151">Dans DirectX 9,0 et versions antérieures, et Windows XP Service Pack 1 et versions antérieures, la méthode **RenderFile** utilise l’ancien filtre source Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d376e-151">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="d376e-152">Ce comportement a été maintenu pour garantir la compatibilité descendante avec les applications qui utilisaient le lecteur Windows Media 6,4.</span><span class="sxs-lookup"><span data-stu-id="d376e-152">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="d376e-153">Pour plus d’informations sur le filtre de source Windows Media hérité, consultez la documentation du kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d376e-153">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="d376e-154">Pour lire un fichier ASF avec du contenu Windows Media à l’aide du lecteur ASF WM, les trois étapes principales sont la création d’une instance du gestionnaire de graphes de filtre, l’appel de **IGraphBuilder :: RenderFile** pour créer le graphique, puis l’appel de **IMediaControl :: Run** pour lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="d376e-154">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="d376e-155">L’exemple de code suivant est un programme complet qui lit un fichier ASF à l’aide de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d376e-155">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="d376e-156">Pour exécuter cet exemple, vous devez avoir installé le kit de développement logiciel (SDK) DirectX et votre environnement de build doit être configuré conformément aux instructions de la rubrique de la documentation du kit de développement logiciel (SDK) DirectShow « configuration de l’environnement de génération ».</span><span class="sxs-lookup"><span data-stu-id="d376e-156">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="d376e-157">En outre, vous devez spécifier un fichier sur votre ordinateur dans l’appel à **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="d376e-157">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


```C++
#include <dshow.h>
#include <stdio.h>

void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}

```



<span data-ttu-id="d376e-158">Notez que le code de l’application pour cet exemple simple ne référence jamais spécifiquement le lecteur ASF WM.</span><span class="sxs-lookup"><span data-stu-id="d376e-158">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="d376e-159">Ce filtre est créé, connecté, exécuté et finalement libéré par le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="d376e-159">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="d376e-160">Toutefois, dans de nombreux scénarios, vous souhaiterez peut-être configurer le lecteur ASF WM avant de commencer la lecture.</span><span class="sxs-lookup"><span data-stu-id="d376e-160">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




