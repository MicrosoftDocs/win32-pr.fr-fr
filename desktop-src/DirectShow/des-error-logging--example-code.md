---
description: 'Journal DES Erreurs DES : exemple de code'
ms.assetid: e734daed-9230-4376-839f-7e09da7bc275
title: 'Journal DES Erreurs DES : exemple de code'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9e0d47535e1d4035669a0e672a30fb2520c676
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522780"
---
# <a name="des-error-logging-example-code"></a><span data-ttu-id="933e5-103">Journal DES Erreurs DES : exemple de code</span><span class="sxs-lookup"><span data-stu-id="933e5-103">DES Error Logging: Example Code</span></span>

<span data-ttu-id="933e5-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="933e5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="933e5-105">L’exemple de code suivant présente une application console complète qui charge et affiche un aperçu du fichier de projet XML des [services de modification DirectShow](directshow-editing-services.md) , à l’aide de la classe de journalisation des erreurs décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="933e5-105">The following sample code presents a complete console application that loads and previews a [DirectShow Editing Services](directshow-editing-services.md) XML project file, using the error logging class described in this section.</span></span> <span data-ttu-id="933e5-106">(Voir [journalisation des erreurs](logging-errors.md).) Le nom du fichier projet est codé en dur dans l’application.</span><span class="sxs-lookup"><span data-stu-id="933e5-106">(See [Logging Errors](logging-errors.md).) The name of the project file is hard-coded into the application.</span></span>

<span data-ttu-id="933e5-107">Pour rendre le code plus concis, l’application console utilise des pointeurs intelligents ATL, ce qui évite d’avoir à appeler **QueryInterface** et **Release**.</span><span class="sxs-lookup"><span data-stu-id="933e5-107">To make the code shorter, the console application uses ATL smart pointers, which removes the need to call **QueryInterface** and **Release**.</span></span> <span data-ttu-id="933e5-108">Si vous préférez, vous pouvez modifier l’exemple d’application lors [du chargement et de l’aperçu d’un projet](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="933e5-108">If you prefer, you can modify the sample application in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span> <span data-ttu-id="933e5-109">Ajoutez simplement le code présenté dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="933e5-109">Simply add the code shown in the previous section.</span></span>


```C++
#include <atlbase.h>
#include <dshow.h>
#include <qedit.h>
#include <stdio.h>

// Declare error logging class.
class CErrReporter;

// (The implementation of CErrReporter was given previously.)

void __cdecl main(void)
{
    HRESULT hr = CoInitialize(NULL);

    if (FAILED(hr))
    {
        // Error handling is omitted for clarity.
    }

    { // Scope for smart pointers.

    CComPtr<IAMTimeline>   pTL;
    CComPtr<IRenderEngine> pRenderEngine; 
    CComPtr<IXml2Dex>      pXML; 
    CComPtr<IGraphBuilder> pGraph;

    hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
                IID_IAMTimeline, (void**) &pTL);
    hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
                IID_IXml2Dex, (void**) &pXML);
    hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
                IID_IRenderEngine, (void**) &pRenderEngine);

    // Set the error log.
    CComQIPtr<IAMSetErrorLog, &IID_IAMSetErrorLog> pSetLog(pTL);
    if (pSetLog)
    {
        IAMErrorLog *pLog = new CErrReporter;    
        pSetLog->put_ErrorLog(pLog);
    }
   
    // Load and preview the project.
    CComBSTR bstrFile(OLESTR("C:\\example.xtl"));
    hr = pXML->ReadXMLFile(pTL, bstrFile); 
    if (SUCCEEDED(hr))
    {
        hr = pRenderEngine->SetTimelineObject(pTL);
        hr = pRenderEngine->ConnectFrontEnd( );
        hr = pRenderEngine->RenderOutputPins( );
        hr = pRenderEngine->GetFilterGraph(&pGraph);

        CComQIPtr<IMediaControl, &IID_IMediaControl> pControl(pGraph);
        CComQIPtr<IMediaEvent, &IID_IMediaEvent> pEvent(pGraph);
        pControl->Run();

        long evCode;
        hr = pEvent->WaitForCompletion(INFINITE, &evCode);
        pControl->Stop();
    }
    // Clean up.
    pRenderEngine->ScrapIt();
    }
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="933e5-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="933e5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="933e5-111">Journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="933e5-111">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



