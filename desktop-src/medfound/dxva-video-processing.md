---
description: Le traitement vidéo DXVA encapsule les fonctions du matériel graphique dédié au traitement d’images vidéo non compressées. Les services de traitement vidéo incluent l’entrelacement et le mixage vidéo.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Traitement vidéo DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220884"
---
# <a name="dxva-video-processing"></a>Traitement vidéo DXVA

Le traitement vidéo DXVA encapsule les fonctions du matériel graphique dédié au traitement d’images vidéo non compressées. Les services de traitement vidéo incluent l’entrelacement et le mixage vidéo.

Cette rubrique contient les sections suivantes :

-   [Vue d'ensemble](#overview)
-   [Création d’un périphérique de traitement vidéo](#creating-a-video-processing-device)
    -   [Obtient le pointeur IDirectXVideoProcessorService](#get-the-idirectxvideoprocessorservice-pointer)
    -   [Énumérer les appareils de traitement vidéo](#enumerate-the-video-processing-devices)
    -   [Énumérer les formats de Render-Target](#enumerate-render-target-formats)
    -   [Interroger les fonctionnalités de l’appareil](#query-the-device-capabilities)
    -   [Créer l’appareil](#create-the-device)
-   [Blit de traitement vidéo](#video-process-blit)
    -   [Paramètres blit](#blit-parameters)
    -   [Exemples d’entrée](#input-samples)
-   [Composition de l’image](#image-composition)
    -   [Exemple 1 : cadre](#example-1-letterboxing)
    -   [Exemple 2 : étirer des images de sous-flux](#example-2-stretching-substream-images)
    -   [Exemple 3 : hauteurs de flux incompatibles](#example-3-mismatched-stream-heights)
    -   [Exemple 4 : rectangle cible plus petit que la surface de destination](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [Exemple 5 : rectangles sources](#example-5-source-rectangles)
    -   [Exemple 6 : rectangles de destination d’intersection](#example-6-intersecting-destination-rectangles)
    -   [Exemple 7 : vidéo sur l’étirement et le rognage](#example-7-stretching-and-cropping-video)
-   [Ordre de l’exemple d’entrée](#input-sample-order)
    -   [Exemple 1](#example-1-letterboxing)
    -   [Exemple 2](#example-2-stretching-substream-images)
    -   [Exemple 3](#example-3-mismatched-stream-heights)
    -   [Exemple 4](#example-4-target-rectangle-smaller-than-destination-surface)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Le matériel graphique peut utiliser l’unité de traitement graphique (GPU) pour traiter les images vidéo non compressées. Un périphérique de *traitement vidéo* est un composant logiciel qui encapsule ces fonctions. Les applications peuvent utiliser un appareil de traitement vidéo pour exécuter des fonctions telles que :

-   Désentrelacement et inversement
-   Mixage de sous-flux vidéo sur l’image vidéo principale
-   Réglage des couleurs (ProcAmp) et filtrage d’images
-   Mise à l'échelle de l’image
-   Conversion de l’espace colorimétrique
-   Fusion alpha

Le diagramme suivant montre les étapes du pipeline de traitement vidéo. Le diagramme n’est pas destiné à illustrer une implémentation réelle. Par exemple, le pilote Graphics peut combiner plusieurs étapes en une seule opération. Toutes ces opérations peuvent être effectuées dans un seul appel à l’appareil de traitement vidéo. Certaines étapes présentées ici, telles que le filtrage du bruit et du détail, peuvent ne pas être prises en charge par le pilote.

![Diagramme montrant les étapes du traitement vidéo DXVA.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

L’entrée du pipeline de traitement vidéo inclut toujours un flux vidéo *principal* , qui contient les données d’image principales. Le flux vidéo principal détermine la fréquence d’images de la vidéo de sortie. Chaque image de la vidéo de sortie est calculée par rapport aux données d’entrée du flux vidéo principal. Les pixels du flux principal sont toujours opaques, sans données alpha par pixel. Le flux vidéo principal peut être progressif ou entrelacé.

Le pipeline de traitement vidéo peut éventuellement recevoir jusqu’à 15 sous-flux vidéo. Un sous-flux contient des données d’image auxiliaire, telles que des sous-titres ou des sous-images de DVD. Ces images sont affichées sur le flux vidéo principal et ne sont généralement pas censées être affichées par elles-mêmes. Les images de sous-flux peuvent contenir des données alpha par pixel et sont toujours des images progressives. L’appareil de traitement vidéo alpha-fusionne les images de sous-flux avec la trame désentrelacée actuelle du flux vidéo principal.

Dans le reste de cette rubrique, le terme *image* est utilisé pour les données d’entrée sur un appareil de traitement vidéo. Une image peut se composer d’une trame progressive, d’un champ unique ou de deux champs entrelacés. La sortie est toujours un frame désentrelacé.

Un pilote vidéo peut implémenter plusieurs périphériques de traitement vidéo pour fournir différents jeux de fonctionnalités de traitement vidéo. Les appareils sont identifiés par un GUID. Les GUID suivants sont prédéfinis :

-   **DXVA2 \_ VideoProcBobDevice**. Cet appareil effectue une désentrelacement Bob.
-   **DXVA2 \_ VideoProcProgressiveDevice**. Ce périphérique est utilisé si la vidéo contient uniquement des images progressives, sans Frame entrelacé. (Un contenu vidéo contient un mélange d’images progressives et entrelacées. L’appareil progressif ne peut pas être utilisé pour ce type de contenu vidéo « mixte », car une étape de désentrelacement est requise pour les images entrelacées.)

Chaque pilote graphique qui prend en charge le traitement vidéo DXVA doit implémenter au moins ces deux appareils. Le pilote Graphics peut également fournir d’autres périphériques, identifiés par des GUID spécifiques au pilote. Par exemple, un pilote peut implémenter un algorithme de désentrelacement propriétaire qui produit une sortie de qualité supérieure à celle de Bob. Certains algorithmes de désentrelacement peuvent nécessiter des images de référence vers l’avant ou vers l’arrière à partir du flux principal. Dans ce cas, l’appelant doit fournir ces images au pilote dans l’ordre approprié, comme décrit plus loin dans cette section.

Un périphérique logiciel de référence est également fourni. L’appareil logiciel est optimisé pour une qualité supérieure à la vitesse et peut ne pas être adapté au traitement vidéo en temps réel. Le périphérique logiciel de référence utilise la valeur GUID DXVA2 \_ VideoProcSoftwareDevice.

## <a name="creating-a-video-processing-device"></a>Création d’un périphérique de traitement vidéo

Avant d’utiliser le traitement vidéo DXVA, l’application doit créer un périphérique de traitement vidéo. Voici un bref aperçu des étapes qui sont expliquées plus en détail dans le reste de cette section :

1.  Obtient un pointeur vers l’interface [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .
2.  Créez une description du format vidéo pour le flux vidéo principal. Utilisez cette description pour obtenir la liste des périphériques de traitement vidéo qui prennent en charge le format vidéo. Les appareils sont identifiés par un GUID.
3.  Pour un appareil particulier, obtenir la liste des formats de cible de rendu pris en charge par l’appareil. Les formats sont retournés sous la forme d’une liste de valeurs **D3DFORMAT** . Si vous envisagez de mélanger des sous-flux, récupérez également la liste des formats de sous-flux pris en charge.
4.  Interroger les fonctionnalités de chaque appareil.
5.  Créez le périphérique de traitement vidéo.

Parfois, vous pouvez omettre certaines de ces étapes. Par exemple, au lieu d’obtenir la liste des formats de cible de rendu, vous pouvez simplement essayer de créer le périphérique de traitement vidéo avec votre format préféré et voir s’il a été correctement exécuté. Un format courant, tel que D3DFMT \_ X8R8G8B8, est susceptible d’être correctement exécuté.

Le reste de cette section décrit ces étapes en détail.

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a>Obtient le pointeur IDirectXVideoProcessorService

L’interface [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) est obtenue à partir de l’appareil Direct3D. Il existe deux façons d’obtenir un pointeur vers cette interface :

-   À partir d’un appareil Direct3D.
-   À partir de la [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md).

Si vous avez un pointeur vers un appareil Direct3D, vous pouvez obtenir un pointeur [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) en appelant la fonction [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) . Transmettez un pointeur vers l’interface **IDirect3DDevice9** de l’appareil et spécifiez **IID \_ IDirectXVideoProcessorService** pour le paramètre *riid* , comme indiqué dans le code suivant :


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



dans certains cas, un objet crée le périphérique Direct3D, puis le partage avec d’autres objets via le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md). Dans ce cas, vous pouvez appeler [**IDirect3DDeviceManager9 :: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) sur le gestionnaire de périphériques pour accéder au pointeur [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , comme illustré dans le code suivant :


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a>Énumérer les appareils de traitement vidéo

Pour obtenir la liste des périphériques de traitement vidéo, remplissez une structure [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) avec le format du flux vidéo principal, puis transmettez cette structure à la méthode [**IDirectXVideoProcessorService :: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) . La méthode retourne un tableau de GUID, un pour chaque périphérique de traitement vidéo qui peut être utilisé avec ce format vidéo.

Prenons l’exemple d’une application qui affiche un flux vidéo au format YUY2, à l’aide de la définition BT. 709 de couleur YUV, avec une fréquence d’images de 29,97 images par seconde. Supposons que le contenu vidéo se compose uniquement d’images progressives. Le fragment de code suivant montre comment remplir la description de format et récupérer les GUID d’appareil :


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



Le code de cet exemple provient de l’exemple du kit de développement logiciel (SDK) [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) .

Dans cet exemple, le tableau *pGuids* est alloué par la méthode [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , de sorte que l’application doit libérer le tableau en appelant [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree). Les étapes restantes peuvent être effectuées à l’aide de l’un des GUID d’appareil retournés par cette méthode.

### <a name="enumerate-render-target-formats"></a>Énumérer les formats de Render-Target

Pour obtenir la liste des formats de cible de rendu pris en charge par l’appareil, transmettez le GUID de l’appareil et la structure [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) à la méthode [**IDirectXVideoProcessorService :: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , comme illustré dans le code suivant :


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



La méthode retourne un tableau de valeurs **D3DFORMAT** . Dans cet exemple, où le type d’entrée est YUY2, une liste type de formats peut être D3DFMT \_ X8R8G8B8 (32 bits RGB) et D3DMFT \_ YUY2 (format d’entrée). Toutefois, la liste exacte dépend du pilote.

La liste des formats disponibles pour les sous-flux peut varier en fonction du format de la cible de rendu et du format d’entrée. Pour obtenir la liste des formats de sous-flux, transmettez le GUID de l’appareil, la structure du format et le format de la cible de rendu à la méthode [**IDirectXVideoProcessorService :: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , comme indiqué dans le code suivant :


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



Cette méthode retourne un autre tableau de valeurs **D3DFORMAT** . Les formats de sous-flux types sont AYUV et AI44.

### <a name="query-the-device-capabilities"></a>Interroger les fonctionnalités de l’appareil

Pour obtenir les fonctionnalités d’un appareil particulier, transmettez le GUID de l’appareil, la structure du format et un format de cible de rendu à la méthode [**IDirectXVideoProcessorService :: GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) . La méthode remplit une structure de structure [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) avec les fonctionnalités de l’appareil.


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a>Créer l’appareil

Pour créer le périphérique de traitement vidéo, appelez [**IDirectXVideoProcessorService :: CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor). L’entrée de cette méthode est le GUID de l’appareil, la description du format, le format de la cible de rendu et le nombre maximal de sous-flux que vous envisagez de mélanger. La méthode retourne un pointeur vers l’interface [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , qui représente le périphérique de traitement vidéo.


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a>Blit de traitement vidéo

L’opération principale de traitement vidéo est le *blit de traitement vidéo*. (Un *blit* est une opération qui combine deux ou plusieurs bitmaps en une seule bitmap. Un blit de traitement vidéo combine des images d’entrée pour créer un frame de sortie.) Pour effectuer un blit de traitement vidéo, appelez [**IDirectXVideoProcessor :: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Cette méthode passe un ensemble d’exemples de vidéos à l’appareil de traitement vidéo. En réponse, le périphérique de traitement vidéo traite les images d’entrée et génère une trame de sortie. Le traitement peut inclure la désentrelacement, la conversion de l’espace colorimétrique et le mixage de sous-flux. La sortie est écrite dans une surface de destination fournie par l’appelant.

La méthode [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) accepte les paramètres suivants :

-   *pRT* pointe vers une surface cible de rendu **IDirect3DSurface9** qui recevra la trame vidéo traitée.
-   *pBltParams* pointe vers une structure [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) qui spécifie les paramètres de la blit.
-   *pSamples* est l’adresse d’un tableau de [**structures \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Ces structures contiennent les exemples d’entrée pour la blit.
-   *Échantillons* donne la taille du tableau *pSamples* .
-   Le paramètre *reserved* est réservé et doit avoir la valeur **null**.

Dans le tableau *pSamples* , l’appelant doit fournir les exemples d’entrée suivants :

-   Image actuelle du flux vidéo principal.
-   Les images de référence avant et arrière, si elles sont requises par l’algorithme de désentrelacement.
-   Zéro, une ou plusieurs images de sous-flux, jusqu’à un maximum de 15 sous-flux.

Le pilote s’attend à ce que ce tableau soit dans un ordre particulier, comme décrit dans l' [exemple d’ordre d’entrée](#input-sample-order).

### <a name="blit-parameters"></a>Paramètres blit

La structure [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contient des paramètres généraux pour la blit. Les paramètres les plus importants sont stockés dans les membres suivants de la structure :

-   **TargetFrame** est l’heure de présentation du frame de sortie. Pour le contenu progressif, cette heure doit être égale à l’heure de début de l’image actuelle du flux vidéo principal. Cette heure est spécifiée dans le membre **Start** de la [**structure \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) pour cet exemple d’entrée.

    Pour le contenu entrelacé, un frame avec deux champs entrelacés produit deux trames de sortie désentrelacées. Sur le premier frame de sortie, l’heure de la présentation doit être égale à l’heure de début de l’image actuelle dans le flux vidéo principal, tout comme du contenu progressif. Sur le deuxième frame de sortie, l’heure de début doit être égale au point médian entre l’heure de début de l’image actuelle dans le flux vidéo principal et l’heure de début de l’image suivante dans le flux. Par exemple, si la vidéo d’entrée est de 25 images par seconde (50 champs par seconde), les trames de sortie auront les horodatages indiqués dans le tableau suivant. Les horodatages sont affichés en unités de nanosecondes de 100.

    

    | Image d’entrée | **TargetFrame** (1) | **TargetFrame** (2) |
    |---------------|---------------------|---------------------|
    | 0             | 0                   | 200000              |
    | 400000        | 0                   | 600000              |
    | 800000        | 800000              | 1000000             |
    | 1,2 million       | 1,2 million             | 1,4 million             |

    

     

    Si le contenu entrelacé se compose de champs uniques plutôt que de champs entrelacés, les temps de sortie correspondent toujours aux temps d’entrée, comme avec le contenu progressif.

-   **TargetRect** définit une zone rectangulaire dans la surface de destination. La blit écrira la sortie dans cette région. Plus précisément, chaque pixel dans **TargetRect** sera modifié, et aucun pixel en dehors de **TargetRect** ne sera modifié. Le rectangle cible définit le rectangle englobant pour tous les flux vidéo d’entrée. Le positionnement des flux individuels dans ce rectangle est contrôlé par le paramètre *pSamples* de [**IDirectXVideoProcessor :: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).
-   **BackgroundColor** donne la couleur de l’arrière-plan où aucune image vidéo ne s’affiche. Par exemple, lorsqu’une image vidéo 16 x 9 s’affiche dans une zone de 4 x 3 (cadre), les régions letterboxed sont affichées avec la couleur d’arrière-plan. La couleur d’arrière-plan ne s’applique qu’à l’intérieur du rectangle cible (**TargetRect**). Tous les pixels en dehors de **TargetRect** ne sont pas modifiés.
-   **DestFormat** décrit l’espace colorimétrique de la vidéo de sortie (par exemple, si ITU-R BT. 709 ou BT. 601 Color est utilisé). Ces informations peuvent affecter la façon dont l’image s’affiche. Pour plus d’informations, consultez [informations sur les couleurs étendues](extended-color-information.md).

D’autres paramètres sont décrits dans la page de référence de la structure [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .

### <a name="input-samples"></a>Exemples d’entrée

Le paramètre *pSamples* de [**IDirectXVideoProcessor :: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) pointe vers un tableau de [**structures \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Chacune de ces structures contient des informations sur un exemple d’entrée et un pointeur vers la surface Direct3D contenant l’exemple. Chaque échantillon est l’un des éléments suivants :

-   Image actuelle du flux principal.
-   Image de référence vers l’avant ou vers l’arrière à partir du flux principal, utilisée pour l’entrelacement.
-   Image de sous-flux.

L’ordre exact dans lequel les exemples doivent apparaître dans le tableau est décrit plus loin dans la section [exemple d’ordre d’entrée](#input-sample-order).

Vous pouvez fournir jusqu’à 15 images sous-flux, même si la plupart des applications vidéo n’ont besoin que d’un seul sous-flux. Le nombre de sous-flux peut changer à chaque appel à [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Les images de sous-flux sont indiquées en affectant au membre **SampleFormat. SampleFormat** de la structure [**\_ VIDEOSAMPLE DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) la valeur DXVA2 \_ SampleSubStream. Pour le flux vidéo principal, ce membre décrit l’entrelacement de la vidéo d’entrée. Pour plus d’informations, consultez [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) , énumération.

Pour le flux vidéo principal, les membres de **début** et de **fin** de la structure [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) fournissent les heures de début et de fin de l’exemple d’entrée. Pour les images sous-flux, définissez ces valeurs sur zéro, car l’heure de présentation est toujours calculée à partir du flux principal. L’application est chargée de suivre le moment où chaque image de sous-flux doit être présentée et de la soumettre à [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) au moment opportun.

Deux rectangles définissent la façon dont la vidéo source est positionnée pour chaque flux :

-   Le membre **SrcRect** de la [**structure \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) spécifie le *rectangle source*, une zone rectangulaire de l’image source qui s’affichera dans le frame de sortie composite. Pour rogner l’image, définissez cette valeur sur une valeur inférieure à la taille du cadre. Sinon, affectez-lui une valeur égale à la taille du frame.
-   Le membre **au dstrect** de la même structure spécifie le *rectangle de destination*, une zone rectangulaire de la surface de destination dans laquelle le cadre vidéo apparaît.

Le pilote BLITS les pixels du rectangle source dans le rectangle de destination. Les deux rectangles peuvent avoir des tailles ou des proportions différentes ; le pilote met à l’échelle l’image en fonction des besoins. En outre, chaque flux d’entrée peut utiliser un facteur d’échelle différent. En fait, la mise à l’échelle peut être nécessaire pour produire les proportions correctes dans le frame de sortie. Le pilote ne prend pas en compte le rapport hauteur des pixels de la source. par conséquent, si l’image source utilise des pixels non carrés, c’est à l’application de calculer le rectangle de destination approprié.

Les formats de sous-flux préférés sont AYUV et AI44. Ce dernier est un format de palette de 16 couleurs. Les entrées de palette sont spécifiées dans le membre **PAL** de la structure [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . (Si votre format vidéo source est initialement exprimé comme un type de média Media Foundation, les entrées de palette sont stockées dans l’attribut de la [**\_ \_ palette MF MT**](mf-mt-palette-attribute.md) .) Pour les formats qui ne sont pas des palettes, désactivez ce tableau à zéro.

## <a name="image-composition"></a>Composition de l’image

Chaque opération blit est définie par les trois rectangles suivants :

-   Le rectangle *cible* (**TargetRect**) définit la région dans la surface de destination où la sortie apparaît. L’image de sortie est découpée sur ce rectangle.
-   Le rectangle de *destination* pour chaque flux (**au dstrect**) définit l’emplacement où le flux d’entrée apparaît dans l’image composite.
-   Le rectangle *source* pour chaque flux (**SrcRect**) définit la partie de l’image source qui apparaît.

Les rectangles cible et de destination sont spécifiés par rapport à la surface de destination. Le rectangle source est spécifié par rapport à l’image source. Tous les rectangles sont spécifiés en pixels.

![Diagramme montrant les rectangles source, de destination et cible](images/dxva-vp-rects.gif)

L’appareil de traitement vidéo alpha fusionne les images d’entrée, à l’aide de l’une des sources de données alpha suivantes :

-   Données alpha par pixel issues de sous-flux.
-   Valeur alpha planaire pour chaque flux vidéo, spécifiée dans le membre **PlanarAlpha** de la structure [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .
-   Valeur alpha planaire de l’image composite, spécifiée dans le membre **alpha** de la [**structure \_ VideoProcessBltParams DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) . Cette valeur est utilisée pour fusionner la totalité de l’image composite avec la couleur d’arrière-plan.

Cette section fournit une série d’exemples qui illustrent la façon dont le périphérique de traitement vidéo crée l’image de sortie.

### <a name="example-1-letterboxing"></a>Exemple 1 : cadre

Cet exemple montre comment mettre en bandes l’image source en définissant le rectangle de destination sur une valeur inférieure à celle du rectangle cible. Le flux vidéo principal de cet exemple est une image 720 × 480 et est destiné à être affiché à un proportions de 16:9. La surface de destination est 640 × 480 pixels (proportions 4:3). Pour obtenir les proportions correctes, le rectangle de destination doit être 640 × 360. Par souci de simplicité, cet exemple n’inclut pas de sous-flux. Le diagramme suivant montre les rectangles source et de destination.

![Diagramme montrant cadre.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

Le diagramme ci-dessus montre les rectangles suivants :

-   Rectangle cible : {0, 0, 640, 480}
-   Vidéo principale :

    -   Rectangle source : {0, 0, 720, 480}
    -   Rectangle de destination : {0, 60, 640, 420}

Le pilote désentrelace la vidéo, réduit le frame désentrelacé à 640 × 360 et blit le frame dans le rectangle de destination. Le rectangle cible est plus grand que le rectangle de destination, de sorte que le pilote utilise la couleur d’arrière-plan pour remplir les barres horizontales au-dessus et en dessous du cadre. La couleur d’arrière-plan est spécifiée dans la structure [**\_ VideoProcessBltParams DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .

### <a name="example-2-stretching-substream-images"></a>Exemple 2 : étirer des images de sous-flux

Les images de sous-flux peuvent s’étendre au-delà de l’image vidéo principale. Dans la vidéo DVD, par exemple, le flux vidéo principal peut avoir un proportions de 4:3, tandis que le sous-flux est 16:9. Dans cet exemple, les deux flux vidéo ont les mêmes dimensions sources (720 × 480), mais le sous-flux est destiné à être affiché à un proportions de 16:9. Pour obtenir ces proportions, l’image de sous-flux est étirée horizontalement. Les rectangles source et de destination sont présentés dans le diagramme suivant.

![Diagramme montrant l’étirement d’image sous-flux.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

Le diagramme ci-dessus montre les rectangles suivants :

-   Rectangle cible : {0, 0, 854, 480}
-   Vidéo principale :

    -   Rectangle source : {0, 0, 720, 480}
    -   Rectangle de destination : {0, 107, 474, 480}

-   Sous-flux
    -   Rectangle source : {0, 0, 720, 480}
    -   Rectangle de destination : {0, 0, 854, 480}

Ces valeurs préservent la hauteur de l’image et ajustent les deux images horizontalement. Dans les régions où les deux images apparaissent, elles sont mélangées en alpha. Lorsque l’image de sous-flux se termine au-delà de la vidéo à l’origine, le sous-flux est fusionné alpha avec la couleur d’arrière-plan. Cette couche alpha fusionne les couleurs modifiées dans le côté droit du diagramme.

### <a name="example-3-mismatched-stream-heights"></a>Exemple 3 : hauteurs de flux incompatibles

Dans l’exemple précédent, le sous-flux et le flux principal sont de la même hauteur. les Flux peuvent également avoir des hauteurs incompatibles, comme illustré dans cet exemple. Les zones du rectangle cible où aucune vidéo ne s’affiche sont dessinées à l’aide de la couleur d’arrière-plan (noir dans cet exemple). Les rectangles source et de destination sont présentés dans le diagramme suivant.

![Diagramme montrant des hauteurs de flux incompatibles,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

Le diagramme ci-dessus montre les rectangles suivants :

-   Rectangle cible : {0, 0, 150, 85}
-   Vidéo principale :
    -   Rectangle source : {0, 0, 150, 50}
    -   Rectangle de destination : {0, 17, 150, 67}
-   Sous-flux
    -   Rectangle source : {0, 0, 100, 85}
    -   Rectangle de destination : {25, 0, 125, 85}

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a>Exemple 4 : rectangle cible plus petit que la surface de destination

Cet exemple montre un cas où le rectangle cible est plus petit que la surface de destination.

![Diagramme montrant un blit dans un rectangle de destination.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

Le diagramme ci-dessus montre les rectangles suivants :

-   Surface de destination : {0, 0, 300, 200}
-   Rectangle cible : {0, 0, 150, 85}
-   Vidéo principale :
    -   Rectangle source : {0, 0, 150, 50}
    -   Rectangle de destination : {0, 17, 150, 67}
-   Sous-flux
    -   Rectangle source : {0, 0, 100, 85}
    -   Rectangle de destination : {25, 0, 125, 85}

Les pixels en dehors du rectangle cible ne sont pas modifiés, donc la couleur d’arrière-plan apparaît uniquement dans le rectangle cible. La zone en pointillés indique des parties de la surface de destination qui ne sont pas affectées par la blit.

### <a name="example-5-source-rectangles"></a>Exemple 5 : rectangles sources

Si vous spécifiez un rectangle source plus petit que l’image source, le pilote blit uniquement cette partie de l’image. Dans cet exemple, les rectangles sources spécifient le quadrant inférieur droit du flux vidéo principal et le quadrant inférieur gauche du sous-flux (indiqué par les marques de hachage dans le diagramme). Les rectangles de destination ont la même taille que les rectangles sources, donc la vidéo n’est pas étirée. Les rectangles source et de destination sont présentés dans le diagramme suivant.

![Diagramme montrant un blit de deux rectangles sources.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

Le diagramme ci-dessus montre les rectangles suivants :

-   Rectangle cible : {0, 0, 720, 576}
-   Vidéo principale :
    -   Taille de la surface source : {0, 0, 720, 480}
    -   Rectangle source : {360, 240, 720, 480}
    -   Rectangle de destination : {0, 0, 360, 240}
-   Sous-flux
    -   Taille de la surface source : {0, 0, 640, 576}
    -   Rectangle source : {0, 288, 320, 576}
    -   Rectangle de destination : {400, 0, 720, 288}

### <a name="example-6-intersecting-destination-rectangles"></a>Exemple 6 : rectangles de destination d’intersection

Cet exemple est similaire à l’exemple précédent, mais les rectangles de destination se croisent. Les dimensions de surface sont les mêmes que dans l’exemple précédent, mais les rectangles source et de destination ne le sont pas. Là encore, la vidéo est rognée, mais pas étirée. Les rectangles source et de destination sont présentés dans le diagramme suivant.

![Diagramme montrant l’intersection des rectangles de destination.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

Le diagramme ci-dessus montre les rectangles suivants :

-   Rectangle cible : {0, 0, 720, 576}
-   Vidéo principale :
    -   Taille de la surface source : {0, 0, 720, 480}
    -   Rectangle source : {260, 92, 720, 480}
    -   Rectangle de destination : {0, 0, 460, 388}
-   Sous-flux
    -   Taille de la surface source : {0, 0, 640, 576}
    -   Rectangle source : {0, 0, 460, 388}
    -   Rectangle de destination : {260, 188, 720, 576}

### <a name="example-7-stretching-and-cropping-video"></a>Exemple 7 : vidéo sur l’étirement et le rognage

Dans cet exemple, la vidéo est étirée et rognée. Une région 180 × 120 de chaque flux est étirée pour couvrir une zone 360 × 240 dans le rectangle de destination.

![Diagramme montrant l’étirement et le rognage.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

Le diagramme ci-dessus montre les rectangles suivants :

-   Rectangle cible : {0, 0, 720, 480}
-   Vidéo principale :
    -   Taille de la surface source : {0, 0, 360, 240}
    -   Rectangle source : {180, 120, 360, 240}
    -   Rectangle de destination : {0, 0, 360, 240}
-   Sous-flux
    -   Taille de la surface source : {0, 0, 360, 240}
    -   Rectangle source : {0, 0, 180, 120}
    -   Rectangle de destination : {360, 240, 720, 480}

## <a name="input-sample-order"></a>Ordre de l’exemple d’entrée

Le paramètre *pSamples* de la méthode [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) est un pointeur vers un tableau d’exemples d’entrée. Les exemples du flux vidéo principal apparaissent en premier, suivis d’images sous-flux dans l’ordre de plan. Les exemples doivent être placés dans le tableau dans l’ordre suivant :

-   Les exemples du flux vidéo principal apparaissent en premier dans le tableau, dans l’ordre temporel. Selon le mode de désentrelacement, le pilote peut nécessiter un ou plusieurs exemples de référence à partir du flux vidéo principal. Les membres **NumForwardRefSamples** et **NumBackwardRefSamples** de la [**structure \_ VideoProcessorCaps DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) spécifient le nombre d’exemples de référence ascendante et descendante nécessaires. L’appelant doit fournir ces exemples de référence même si le contenu vidéo est progressif et ne nécessite pas de désentrelacement. (Cela peut se produire lorsque des trames progressifs sont attribuées à un appareil de désentrelacement, par exemple lorsque la source contient une combinaison de trames entrelacées et progressives.)
-   Après les exemples du flux vidéo principal, le tableau peut contenir jusqu’à 15 exemples de sous-flux, organisés en ordre de plan, de bas en haut. Les sous-flux sont toujours progressifs et ne nécessitent pas d’images de référence.

À tout moment, le flux vidéo principal peut basculer entre le contenu entrelacé et le contenu progressif, et le nombre de sous-flux peut changer.

Le membre **SampleFormat. SampleFormat** de la [**structure \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indique le type d’image. Pour les images sous-flux, définissez cette valeur sur DXVA2 \_ SampleSubStream. Pour les images progressives, la valeur est DXVA2 \_ SampleProgressiveFrame. Pour les images entrelacées, la valeur dépend de la disposition des champs.

Si le pilote requiert des exemples de référence avant et arrière, le nombre complet d’exemples peut ne pas être disponible au début de la séquence vidéo. Dans ce cas, incluez des entrées pour celles-ci dans le tableau *pSamples* , mais Marquez les exemples manquants comme ayant le type DXVA2 \_ SampleUnknown.

Les membres de **début** et de **fin** de la structure [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) fournissent l’emplacement temporel de chaque échantillon. Ces valeurs sont utilisées uniquement pour les exemples du flux vidéo principal. Pour les images sous-flux, définissez les deux membres sur zéro.

Les exemples suivants peuvent vous aider à clarifier ces exigences.

### <a name="example-1"></a>Exemple 1

Le cas le plus simple se produit lorsqu’il n’y a aucun sous-flux et que l’algorithme de désentrelacement ne requiert pas d’exemples de référence (**NumForwardRefSamples** et **NumBackwardRefSamples** sont tous deux nuls). Bob désentrelacement est un exemple de ce type d’algorithme. Dans ce cas, le tableau *pSamples* doit contenir une seule surface d’entrée, comme indiqué dans le tableau suivant.



| Index           | Type de surface        | Emplacement temporel |
|-----------------|---------------------|-------------------|
| *pSamples* \[ entre\] | Image entrelacée. | *T*               |



 

La valeur d’heure *T* est supposée être l’heure de début de la trame vidéo actuelle.

### <a name="example-2"></a>Exemple 2

Dans cet exemple, l’application mélange deux sous-flux avec le flux principal. L’algorithme de désentrelacement ne requiert pas d’exemples de référence. Le tableau suivant montre comment ces exemples sont organisés dans le tableau *pSamples* .



| Index           | Type de surface       | Emplacement temporel | Ordre de plan |
|-----------------|--------------------|-------------------|---------|
| *pSamples* \[ entre\] | Image entrelacée | *T*               | 0       |
| *pSamples* \[ 1,0\] | Sous-flux          | 0                 | 1       |
| *pSamples* \[ 2\] | Sous-flux          | 0                 | 2       |



 

### <a name="example-3"></a>Exemple 3

Supposons à présent que l’algorithme de désentrelacement nécessite un exemple de référence arrière et un exemple de référence avant. En outre, deux images de sous-flux sont fournies, pour un total de cinq surfaces. Le classement correct est indiqué dans le tableau suivant.



| Index           | Type de surface                   | Emplacement temporel | Ordre de plan        |
|-----------------|--------------------------------|-------------------|----------------|
| *pSamples* \[ entre\] | Image entrelacée (référence) | *T* − 1            | Non applicable |
| *pSamples* \[ 1,0\] | Image entrelacée             | *T*               | 0              |
| *pSamples* \[ 2\] | Image entrelacée (référence) | *T* + 1            | Non applicable |
| *pSamples* \[ 1,3\] | Sous-flux                      | 0                 | 1              |
| *pSamples* \[ 4\] | Sous-flux                      | 0                 | 2              |



 

L’heure *t* − 1 est l’heure de début de l’image avant le frame actuel, et *t* + 1 est l’heure de début du cadre suivant.

Si le flux vidéo bascule vers du contenu progressif, en utilisant le même mode de désentrelacement, l’application doit fournir le même nombre d’exemples, comme indiqué dans le tableau suivant.



| Index           | Type de surface                    | Emplacement temporel | Ordre de plan        |
|-----------------|---------------------------------|-------------------|----------------|
| *pSamples* \[ entre\] | Image progressive (référence) | *T* − 1            | Non applicable |
| *pSamples* \[ 1,0\] | Image progressive             | *T*               | 0              |
| *pSamples* \[ 2\] | Image progressive (référence) | *T* + 1            | Non applicable |
| *pSamples* \[ 1,3\] | Sous-flux                       | 0                 | 1              |
| *pSamples* \[ 4\] | Sous-flux                       | 0                 | 2              |



 

### <a name="example-4"></a>Exemple 4

Au début d’une séquence vidéo, les exemples de référence ascendante et descendante peuvent ne pas être disponibles. Dans ce cas, les entrées des exemples manquants sont incluses dans le tableau *pSamples* , avec l’exemple de type DXVA2 \_ SampleUnknown.

En supposant que le mode de désentrelacement a besoin d’un exemple de référence ascendante et descendante, les trois premiers appels à [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) auront les séquences d’entrées affichées dans les trois tables suivantes.



| Index           | Type de surface                   | Emplacement temporel |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ entre\] | Unknown                        | 0                 |
| *pSamples* \[ 1,0\] | Unknown                        | 0                 |
| *pSamples* \[ 2\] | Image entrelacée (référence) | *T* + 1            |



 



| Index           | Type de surface                   | Emplacement temporel |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ entre\] | Unknown                        | 0                 |
| *pSamples* \[ 1,0\] | Image entrelacée             | *T*               |
| *pSamples* \[ 2\] | Image entrelacée (référence) | *T* + 1            |



 



| Index           | Type de surface                   | Emplacement temporel |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ entre\] | Image entrelacée             | *T* − 1            |
| *pSamples* \[ 1,0\] | Image entrelacée             | *T*               |
| *pSamples* \[ 2\] | Image entrelacée (référence) | *T* + 1            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[\_Exemple DXVA2 VideoProc](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
