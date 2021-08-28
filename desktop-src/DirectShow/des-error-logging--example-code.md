---
description: 'Journal DES Erreurs DES : exemple de code'
ms.assetid: e734daed-9230-4376-839f-7e09da7bc275
title: 'Journal DES Erreurs DES : exemple de code'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2919e8214a247be77c5d706bbbf5a043751791b26ecb59f95e2e1bc69ce9f070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952958"
---
# <a name="des-error-logging-example-code"></a>Journal DES Erreurs DES : exemple de code

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

l’exemple de code suivant présente une application console complète qui charge et affiche un aperçu d’un DirectShow fichier de projet XML de [Services d’édition](directshow-editing-services.md) , à l’aide de la classe de journalisation des erreurs décrite dans cette section. (Voir [journalisation des erreurs](logging-errors.md).) Le nom du fichier projet est codé en dur dans l’application.

Pour rendre le code plus concis, l’application console utilise des pointeurs intelligents ATL, ce qui évite d’avoir à appeler **QueryInterface** et **Release**. Si vous préférez, vous pouvez modifier l’exemple d’application en [chargeant et en prévisualisation d’un Project](loading-and-previewing-a-project.md). Ajoutez simplement le code présenté dans la section précédente.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Journalisation des erreurs](logging-errors.md)
</dt> </dl>

 

 



