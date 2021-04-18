---
description: 'Création d’une chronologie : exemple de code'
ms.assetid: efe6e8d7-2465-4374-8c99-a410091f8d46
title: 'Création d’une chronologie : exemple de code'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877bd79b055171dfa5bd12cff0ae257d60e76a16
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512875"
---
# <a name="creating-a-timeline-example-code"></a>Création d’une chronologie : exemple de code

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

L’exemple de code suivant montre comment créer et afficher un aperçu d’une chronologie dans les [services de modification DirectShow](directshow-editing-services.md).

> [!Note]  
> Par souci de concision, l’exemple de code n’effectue aucune vérification des erreurs. Dans une application réelle, vous devez vérifier les valeurs de retour des appels de méthode pour vous assurer qu’aucun n’a échoué.

 


```C++
#include <dshow.h>
#include <qedit.h>

// Preview a timeline.
void PreviewTL(IAMTimeline *pTL, IRenderEngine *pRender) 
{
    IGraphBuilder   *pGraph = NULL;
    IMediaControl   *pControl = NULL;
    IMediaEvent     *pEvent = NULL;

    // Build the graph.
    pRender->SetTimelineObject(pTL);
    pRender->ConnectFrontEnd( );
    pRender->RenderOutputPins( );

    // Run the graph.
    pRender->GetFilterGraph(&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
    pControl->Run();

    long evCode;
    pEvent->WaitForCompletion(INFINITE, &evCode);
    pControl->Stop();

    // Clean up.
    pEvent->Release();
    pControl->Release();
    pGraph->Release();
}

void main( void )
{
    // Start by making an empty timeline.

    IAMTimeline    *pTL = NULL;
    CoInitialize(NULL);
    CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);

    // GROUP: Add a video group to the timeline. 

    IAMTimelineGroup    *pGroup = NULL;
    IAMTimelineObj      *pGroupObj = NULL;
    pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
    pGroupObj->QueryInterface(IID_IAMTimelineGroup, (void **)&pGroup);

    // Set the group media type. This example sets the type to "video" and
    // lets DES pick the default settings. For a more detailed example,
    // see "Setting the Group Media Type."
    AM_MEDIA_TYPE mtGroup;  
    ZeroMemory(&mtGroup, sizeof(AM_MEDIA_TYPE));
    mtGroup.majortype = MEDIATYPE_Video;
    pGroup->SetMediaType(&mtGroup);
    pTL->AddGroup(pGroupObj);
    pGroupObj->Release();

    // TRACK: Add a track to the group. 

    IAMTimelineObj      *pTrackObj;
    IAMTimelineTrack    *pTrack;
    IAMTimelineComp     *pComp = NULL;

    pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
    pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
    pComp->VTrackInsBefore(pTrackObj, 0);
    pTrackObj->QueryInterface(IID_IAMTimelineTrack, (void **)&pTrack);

    pTrackObj->Release();
    pComp->Release();    
    pGroup->Release();

    // SOURCE: Add a source to the track.

    IAMTimelineSrc *pSource = NULL;
    IAMTimelineObj *pSourceObj;
    pTL->CreateEmptyNode(&pSourceObj, TIMELINE_MAJOR_TYPE_SOURCE);
    pSourceObj->QueryInterface(IID_IAMTimelineSrc, (void **)&pSource);

    // Set the times and the file name.
    pSourceObj->SetStartStop(0, 50000000);
    BSTR bstrFile = SysAllocString(OLESTR("C:\\example.avi"));
    pSource->SetMediaName(bstrFile); 
    SysFreeString(bstrFile);
    pSource->SetMediaTimes(40000000, 140000000);
    pTrack->SrcAdd(pSourceObj);

    pSourceObj->Release();
    pSource->Release();
    pTrack->Release();

    // Preview the timeline.
    IRenderEngine *pRenderEngine = NULL;
    CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
        IID_IRenderEngine, (void**) &pRenderEngine);
    PreviewTL(pTL, pRenderEngine);

    // Clean up.
    pRenderEngine->ScrapIt();
    pRenderEngine->Release();
    pTL->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Construction d’une chronologie](constructing-a-timeline.md)
</dt> </dl>

 

 



