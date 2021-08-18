---
description: Cette rubrique décrit comment prendre en charge Microsoft Direct3D 11 dans un décodeur de Microsoft Media Foundation.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Prise en charge du décodage vidéo Direct3D 11 dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95a1d1bc1dd9987fe59fe807e56aa9af1ea4ad597b72c077906483d623e11e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972881"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Prise en charge du décodage vidéo Direct3D 11 dans Media Foundation

Cette rubrique décrit comment prendre en charge Microsoft Direct3D 11 dans un décodeur de Microsoft Media Foundation. Plus précisément, il décrit la communication entre le décodeur et le convertisseur vidéo. Cette rubrique ne décrit pas comment implémenter les opérations de décodage.

-   [Vue d'ensemble](#overview)
-   [Ouvrir un handle d’appareil](#open-a-device-handle)
-   [Rechercher une configuration de décodeur](#find-a-decoder-configuration)
-   [Revenir au décodage logiciel](#fallback-to-software-decoding)
-   [Allocation de mémoires tampons non compressées](#allocating-uncompressed-buffers)
-   [Décodage](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Dans le reste de cette rubrique, les termes suivants sont utilisés :

-   **Décodeur logiciel**. Le décodeur logiciel est la Media Foundation transformation (MFT) qui reçoit des échantillons vidéo compressés et génère des trames vidéo non compressées.
-   **Appareil de décodage**. L’appareil décodeur est l’accélérateur vidéo et est implémenté par le pilote Graphics. L’appareil décodeur effectue des opérations de décodage accélérées.
-   **Pipeline**. Le pipeline héberge le décodeur logiciel et fournit des mémoires tampons vers et depuis le décodeur logiciel. Selon l’application, le pipeline peut être la [session multimédia](media-session.md), le [lecteur source](source-reader.md)ou le code d’application qui appelle directement la table MFT.

Pour effectuer le décodage à l’aide de Direct3D 11, le décodeur logiciel doit avoir un pointeur vers un appareil Direct3D 11. L’appareil Direct3D 11 est créé en externe dans le décodeur logiciel. Dans un scénario de [session multimédia](media-session.md) , le convertisseur vidéo crée l’appareil Direct3D 11. Dans un scénario de [lecteur source](source-reader.md) , l’application crée généralement l’appareil Direct3D 11.

Le Gestionnaire de périphériques DXGI est utilisé pour partager le Direct3D 11 entre les composants. L’Gestionnaire de périphériques DXGI expose l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Le pipeline définit le pointeur **IMFDXGIDeviceManager** sur le décodeur logiciel en envoyant le message de l' [**ensemble de messages MFT du \_ \_ \_ \_ Gestionnaire D3D**](mft-message-set-d3d-manager.md) .

Le diagramme suivant montre la relation entre le décodeur logiciel, Direct3D 11 et le pipeline.

![diagramme qui montre le décodeur logiciel et le gestionnaire d’appareils DXGI.](images/d3d11video01.png)

Voici les étapes de base qu’un décodeur logiciel doit effectuer pour prendre en charge Direct3D 11 dans Media Foundation :

1.  Ouvrez un handle vers l’appareil Direct3D 11.
2.  Rechercher une configuration de décodeur.
3.  Allouez des tampons non compressés.
4.  Décodez les frames.

Ces étapes sont décrites plus en détail dans le reste de cette rubrique.

## <a name="open-a-device-handle"></a>Ouvrir un handle d’appareil

La table MFT du décodeur utilise DXGI Device Manager pour obtenir un descripteur de l’appareil Direct3D 11. Pour ouvrir le descripteur de l’appareil, procédez comme suit :

1.  La table MFT du décodeur doit exposer l’attribut [ \_ prenant en \_ \_ charge MF sa d3d11](mf-sa-d3d11-aware.md) avec la valeur **true**.
2.  Le chargeur de topologie interroge cet attribut en appelant [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). La valeur **true** indique que la table MFT prend en charge Direct3D 11.
3.  Le chargeur de topologie appelle [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de l' [**ensemble de messages MFT du \_ \_ \_ \_ Gestionnaire D3D**](mft-message-set-d3d-manager.md) . Le paramètre *ulParam* est un pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) vers le gestionnaire de périphériques DXGI. Interrogez ce pointeur sur l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .
4.  Appelez [**IMFDXGIDeviceManager :: OpenDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) pour obtenir un descripteur de l’appareil Direct3D 11.
5.  Pour obtenir un pointeur vers l’appareil Direct3D 11, appelez [**IMFDXGIDeviceManager :: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Transmettez le descripteur de l’appareil et la valeur **IID \_ ID3D11Device**. La méthode retourne un pointeur vers l’interface [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) .
6.  Pour obtenir un pointeur vers l’accélérateur vidéo, appelez à nouveau [**IMFDXGIDeviceManager :: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) . Cette fois-ci, transmettez le descripteur de l’appareil et la valeur **IID \_ ID3D11VideoDevice**. La méthode retourne un pointeur vers l’interface [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) .
7.  Appelez [**ID3D11Device :: GetImmediateContext**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) pour accéder à un pointeur [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) .
8.  Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) pour accéder à un pointeur [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) .
9.  Il est recommandé d’utiliser la protection multithreads sur le contexte de l’appareil pour éviter des problèmes d’interblocage qui peuvent parfois se produire quand vous appelez [**ID3D11VideoContext :: GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) ou [**ID3D11VideoContext :: ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer). Pour définir la protection multithread, appelez d’abord [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) pour accéder à un pointeur [**ID3D10Multithread**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) . Appelez ensuite [**ID3D10Multithread :: SetMultithreadProtected**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected), en passant **true** pour *bMTProtect*.

## <a name="find-a-decoder-configuration"></a>Rechercher une configuration de décodeur

Pour effectuer le décodage, le décodeur logiciel doit trouver une configuration compatible qui est prise en charge par l’appareil décodeur, y compris un format de cible de rendu. Cette étape se produit à l’intérieur de la méthode [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , comme suit.

1.  Validez le type de média d’entrée. Si le type est rejeté, ignorez les étapes restantes et retournez un code d’erreur.
2.  Appelez [**ID3D11VideoDevice :: GetVideoDecoderProfileCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) pour connaître le nombre de profils pris en charge.
3.  Appelez [**ID3D11VideoDevice :: GetVideoDecoderProfile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) pour énumérer les profils et récupérer les GUID de profil.
4.  Recherchez un GUID de profil qui correspond au format vidéo et aux fonctionnalités du décodeur logiciel. Par exemple, un décodeur MPEG-2 recherche le **profil de \_ décodage d3d11 \_ \_ MPEG2 \_ MOCOMP**, le profil de **\_ décodage d3d11 MPEG2 \_ \_ \_ IDCT** et le **profil de \_ décodeur d3d11 \_ \_ MPEG2 \_ VLD**.
5.  Si un GUID de décodeur approprié est trouvé, vérifiez le format de sortie en appelant la méthode [**ID3D11VideoDevice :: CheckVideoDecoderFormat**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) . Transmettez le GUID du décodeur et une valeur de **\_ format de dxgi** qui spécifie le format de la cible de rendu.
6.  Recherchez ensuite une configuration appropriée pour le décodeur.
    1.  Appelez [**ID3D11VideoDevice :: GetVideoDecoderConfigCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) pour connaître le nombre de configurations du décodeur. Transmettez le même GUID de périphérique décodeur, ainsi qu’une structure [**\_ \_ \_ desc décodeur vidéo d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) qui décrit le format de cible de rendu proposé.
    2.  Appelez [**ID3D11VideoDevice :: GetVideoDecoderConfig**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) pour énumérer les configurations du décodeur.

Dans la méthode [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , retourne un format vidéo non compressé basé sur le format de cible de rendu proposé.

Dans la méthode [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , vérifiez le type de média par rapport au format de la cible de rendu.

## <a name="fallback-to-software-decoding"></a>Revenir au décodage logiciel

Il se peut que la MFT ne trouve pas de configuration. Par exemple, le pilote Graphics peut ne pas prendre en charge les fonctionnalités appropriées. Dans ce cas, la MFT doit revenir au décodage logiciel, comme suit.

1.  Les méthodes [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) et [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) doivent retourner un **\_ \_ \_ \_ type D3D non pris en charge MF E**.
2.  En réponse, le chargeur de topologie envoie le message de [**l' \_ ensemble de messages MFT du \_ \_ \_ Gestionnaire D3D**](mft-message-set-d3d-manager.md) avec la valeur **null** pour le paramètre *ulParam* .
3.  La table MFT libère son pointeur vers l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .
4.  Le chargeur de topologie renégocie le type de média.

À ce stade, la table MFT peut utiliser le décodage logiciel.

## <a name="allocating-uncompressed-buffers"></a>Allocation de mémoires tampons non compressées

Le décodeur est chargé d’allouer les textures Direct3D 11 à utiliser comme tampons vidéo non compressés. L’attribut de [ \_ \_ nombre minimal d' \_ \_ échantillons \_ de sortie MF sa](mf-sa-minimum-output-sample-count.md) dans les attributs de flux de sortie (voir [**IMFTransform :: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) est utilisé pour déterminer le nombre de surfaces que le décodeur doit allouer pour le convertisseur vidéo à utiliser pour l’entrelacement. Un décodeur doit utiliser cette valeur pour la limiter à des limites supérieures et inférieures raisonnables, par exemple 3-32. Pour obtenir du contenu progressif, consultez [MF \_ sa \_ minimum \_ Output \_ Sample \_ Count \_ progressif](mf-sa-minimum-output-sample-count-progressive.md).

Dans la méthode [**IMFTransform :: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , définissez le **flux de sortie MFT fournit l’indicateur \_ \_ \_ \_ Samples** dans la structure d' [**informations du \_ \_ flux \_ de sortie MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) . Cet indicateur signale à la session multimédia que la table MFT alloue ses propres exemples de sortie. Pour allouer les exemples de sortie, la table MFT effectue les étapes suivantes :

1.  Créez un tableau de texture 2D en appelant [**ID3D11Device :: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d). Dans la structure [**d3d11 \_ TEXTURE2D \_ desc**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) , définissez **arraySize** égal au nombre de surfaces dont le décodeur a besoin. notamment :
    -   Surfaces pour les frames de référence.
    -   Surfaces pour l’entrelacement (trois surfaces).
    -   Surfaces dont le décodeur a besoin pour la mise en mémoire tampon.

    Les indicateurs de liaison (**BindFlags**) doivent inclure l’indicateur de **\_ \_ décodeur de liaison d3d11** et tous les indicateurs de liaison définis par le biais de l’attribut [ \_ \_ \_ BindFlags MF d3d11](mf-sa-d3d11-bindflags.md) dans les attributs de flux de sortie.
2.  Pour chaque surface dans le tableau de texture, appelez [**ID3D11VideoDevice :: CreateVideoDecoderOutputView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) pour créer une vue de sortie du décodeur vidéo. Pendant le décodage, ces affichages de sortie sont transmis à la méthode [**ID3D11VideoContext ::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) .
3.  Pour chaque surface dans le tableau de textures, créez un exemple de support comme suit :
    1.  Créez une mémoire tampon de média DXGI en appelant la fonction [**MFCreateDXGISurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) . Transmettez le pointeur [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) et le décalage pour chaque élément dans le tableau de texture. La fonction retourne un pointeur [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
    2.  Créez un exemple de support vide en appelant la fonction [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) . Affectez la valeur **null** au paramètre *pUnkSurface* . La fonction retourne un pointeur [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .
    3.  Appelez [**IMFSample :: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) pour ajouter la mémoire tampon du média à l’exemple.

Vous devez détruire toutes les textures que vous créez en même temps, au lieu de détruire uniquement certains et de continuer à utiliser le rappel.

## <a name="decoding"></a>Décodage

Pour créer l’appareil de décodage, appelez [**ID3D11VideoDevice :: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder). La méthode retourne un pointeur vers l’interface [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) . Le décodage doit se produire à l’intérieur de la méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Sur chaque frame, appelez [**IMFDXGIDeviceManager :: TestDevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) pour tester la disponibilité du DXGI. Si l’appareil a changé, le décodeur logiciel doit recréer le périphérique décodeur, comme suit :

1.  Fermez le handle d’appareil en appelant [**IMFDXGIDeviceManager :: CloseDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle).
2.  Libérer toutes les ressources associées à l’appareil Direct3D 11 précédent, y compris les interfaces [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder), [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext), [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)et [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) .
3.  Ouvrez un nouveau descripteur d’appareil.
4.  Négociez une nouvelle configuration de décodeur, comme décrit précédemment dans [Rechercher une configuration de décodeur](#find-a-decoder-configuration). Cette étape est nécessaire, car les fonctionnalités de l’appareil peuvent avoir changé.
5.  Créez un appareil de décodage.

En supposant que le descripteur de l’appareil est valide, le processus de décodage fonctionne comme suit :

1.  Obtient une surface disponible qui n’est pas en cours d’utilisation. Initialement, toutes les surfaces sont disponibles.
2.  Interrogez l’exemple de support pour l’interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Appelez [**IMFTrackedSample :: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) et fournissez un pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . (Le décodeur logiciel doit implémenter cette interface.) Quand le convertisseur vidéo libère l’exemple, le rappel est appelé. Utilisez ce rappel pour suivre les exemples actuellement disponibles et ceux qui sont en cours d’utilisation.
4.  Appelez [**ID3D11VideoContext ::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe). Transmettez les pointeurs vers l’interface [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) pour l’appareil de décodage et l’interface [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) pour la vue de sortie.
5.  Effectuez les opérations suivantes une ou plusieurs fois :
    1.  Appelez [**ID3D11VideoContext :: GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) pour obtenir une mémoire tampon.
    2.  Remplir la mémoire tampon.
    3.  Appelez [**ID3D11VideoContext :: ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer).
    4.  Appelez [**ID3D11VideoContext :: SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers). Cette méthode indique à l’appareil décodeur d’effectuer les opérations de décodage sur le frame.
6.  Appelez [**ID3D11VideoContext ::D ecoderendframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) pour signaler la fin du décodage du frame actuel.

Direct3D 11 utilise les mêmes structures de données que DXVA 2,0 pour les opérations de décodage. Pour l’ensemble initial de profils DXVA (pour H. 261, H. 263 et MPEG-2), ces structures de données sont décrites dans la [spécification DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Au sein de chaque paire d’appels [**DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) et [**SubmitDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) , vous pouvez appeler [**GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) plusieurs fois, mais une seule fois pour chaque type de mémoire tampon. Si vous utilisez le même type de mémoire tampon à deux reprises sans appeler **SubmitDecoderBuffer**, vous allez remplacer les données dans la mémoire tampon.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D 11](direct3d-11-video-apis.md)
</dt> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
