---
description: Cette rubrique explique comment créer une topologie pour la lecture audio ou vidéo.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Création de topologies de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514368"
---
# <a name="creating-playback-topologies"></a>Création de topologies de lecture

Cette rubrique explique comment créer une topologie pour la lecture audio ou vidéo. Pour la lecture de base, vous pouvez créer une topologie partielle, dans laquelle les nœuds sources sont connectés directement aux nœuds de sortie. Vous n’avez pas besoin d’insérer de nœuds pour les transformations intermédiaires, telles que les décodeurs ou les convertisseurs de couleurs. La session multimédia utilise le chargeur de topologie pour résoudre la topologie, et le chargeur de topologie insère les transformations qui sont requises.

-   [Création de la topologie](#creating-the-topology)
-   [Connexion de flux à des récepteurs multimédias](#connecting-streams-to-media-sinks)
-   [Création du récepteur multimédia](#creating-the-media-sink)
-   [Next Steps](#next-steps)
-   [Rubriques connexes](#related-topics)

## <a name="creating-the-topology"></a>Création de la topologie

Voici les étapes générales pour créer une topologie de lecture partielle à partir d’une source de média :

1.  Créez la source du média. Dans la plupart des cas, vous utiliserez le programme de résolution source pour créer la source du média. Pour plus d’informations, consultez la page programme de [résolution source](source-resolver.md).
2.  Obtient le descripteur de présentation de la source du média.
3.  Créez une topologie vide.
4.  Utilisez le descripteur de présentation pour énumérer les descripteurs de flux. Pour chaque descripteur de flux :
    1.  Obtient le type de média principal du flux, tel que l’audio ou la vidéo.
    2.  Vérifiez si le flux est actuellement sélectionné. (Si vous le souhaitez, vous pouvez sélectionner ou désélectionner un flux, en fonction du type de média.)
    3.  Si le flux est sélectionné, créez un objet d’activation pour le récepteur multimédia, en fonction du type de média du flux.
    4.  Ajoutez un nœud source pour le flux et un nœud de sortie pour le récepteur multimédia.
    5.  Connectez le nœud source au nœud de sortie.

Pour faciliter ce processus, l’exemple de code de cette rubrique est organisé en plusieurs fonctions. La fonction de niveau supérieur est nommée `CreatePlaybackTopology` . Il accepte trois paramètres :

-   Pointeur vers une interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.
-   Pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) du descripteur de présentation. Pour ce faire, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Pour les sources avec plusieurs présentations, les descripteurs de présentation pour les présentations suivantes sont fournis dans l’événement [MENewPresentation](menewpresentation.md) .
-   Handle d’une fenêtre d’application. Si la source a un flux vidéo, la vidéo s’affiche dans cette fenêtre.

La fonction retourne un pointeur vers une topologie de lecture partielle dans le paramètre *ppTopology* .


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



Cette fonction effectue les étapes suivantes :

1.  Appelez [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) pour créer la topologie. Au départ, la topologie ne contient aucun nœud.
2.  Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) pour connaître le nombre de flux dans la présentation.
3.  Pour chaque flux, appelez la fonction définie par l’application `AddBranchToPartialTopology` dans une branche de la topologie. Cette fonction est présentée dans la section suivante.

## <a name="connecting-streams-to-media-sinks"></a>Connexion de flux à des récepteurs multimédias

Pour chaque flux sélectionné, ajoutez un nœud source et un nœud de sortie, puis connectez les deux nœuds. Le nœud source représente le flux. Le nœud de sortie représente soit le [convertisseur de vidéo amélioré](enhanced-video-renderer.md) (EVR), soit le [convertisseur audio de streaming](streaming-audio-renderer.md) (SAR).

La `AddBranchToPartialTopology` fonction, illustrée dans l’exemple suivant, accepte les paramètres suivants :

-   Pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topologie.
-   Pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.
-   Pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) du descripteur de présentation.
-   Index de base zéro du flux.
-   Handle de la fenêtre vidéo. Ce descripteur est utilisé uniquement pour le flux vidéo.


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



La fonction effectue les opérations suivantes :

1.  Appelle [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) et passe l’index de flux. Cette méthode retourne un pointeur vers le descripteur de flux pour ce flux, ainsi qu’une valeur booléenne indiquant si le flux est sélectionné.
2.  Si le flux n’est pas sélectionné, la fonction se termine et retourne S \_ OK, car l’application n’a pas besoin de créer une branche de topologie pour un flux, sauf si elle est sélectionnée.
3.  Si le flux est sélectionné, la fonction termine la branche de topologie comme suit :
    1.  Crée un objet d’activation pour le récepteur, en appelant la fonction CreateMediaSinkActivate définie par l’application. Cette fonction est présentée dans la section suivante.
    2.  Ajoute un nœud source à la topologie. Le code pour cette étape est présenté dans la rubrique [création de nœuds sources](creating-source-nodes.md).
    3.  Ajoute un nœud de sortie à la topologie. Le code pour cette étape est présenté dans la rubrique [création de nœuds de sortie](creating-output-nodes.md).
    4.  Connecte les deux nœuds en appelant [**IMFTopologyNode :: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) sur le nœud source. En connectant les nœuds, l’application indique que le nœud en amont doit fournir des données au nœud en aval. Un nœud source a une sortie et un nœud de sortie a une entrée, donc les deux index de flux sont nuls.

Des applications plus avancées peuvent sélectionner ou désélectionner des flux, au lieu d’utiliser la configuration par défaut de la source. Une source peut avoir plusieurs flux, et l’une d’elles peut être sélectionnée par défaut. Le descripteur de présentation de la source du média possède un ensemble de sélections de flux par défaut. Dans un fichier vidéo simple avec un flux audio et un flux vidéo uniques, la source du média sélectionne généralement les deux flux par défaut. Toutefois, un fichier peut avoir plusieurs flux audio pour différentes langues, ou plusieurs flux vidéo encodés à des vitesses de transmission différentes. Dans ce cas, certains flux sont désélectionnés par défaut. L’application peut modifier la sélection en appelant [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) et [**IMFPresentationDescriptor ::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) sur le descripteur de présentation.

## <a name="creating-the-media-sink"></a>Création du récepteur multimédia

La fonction Next crée un objet d’activation pour le récepteur multimédia EVR ou SAR.


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



Cette fonction effectue les étapes suivantes :

1.  Appelle [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sur le descripteur de flux. Cette méthode retourne un pointeur d’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

2.  Appelle [**IMFMediaTypeHandler :: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Cette méthode retourne le GUID du type principal pour le flux.

3.  Si le type de flux est audio, la fonction appelle [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) pour créer l’objet d’activation du convertisseur audio. Si le type de flux est vidéo, la fonction appelle [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer l’objet d’activation du convertisseur vidéo. Ces deux fonctions retournent un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Ce pointeur est utilisé pour initialiser le nœud de sortie du récepteur, comme indiqué précédemment.

Pour tout autre type de flux, cet exemple retourne un code d’erreur. Vous pouvez également désélectionner simplement le flux.

## <a name="next-steps"></a>Étapes suivantes

Pour lire un fichier multimédias à la fois, en file d’attente sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). La session multimédia utilise le chargeur de topologie pour résoudre la topologie. Pour obtenir un exemple complet, consultez [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment lire des fichiers multimédias non protégés](how-to-play-unprotected-media-files.md)
</dt> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Topologies](topologies.md)
</dt> </dl>

 

 



