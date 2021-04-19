---
description: Prise en charge de DXVA 2,0 dans Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Prise en charge de DXVA 2,0 dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce144c24a1aeeda6281ddb423757f3e339903440
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522887"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Prise en charge de DXVA 2,0 dans Media Foundation

Cette rubrique explique comment prendre en charge DirectX Video Acceleration (DXVA) 2,0 dans une transformation de Media Foundation (MFT) à l’aide de Microsoft Direct3D 9, mais décrit la communication entre le décodeur et le convertisseur vidéo, qui est pris en charge par le chargeur de topologie. Cette rubrique ne décrit pas comment implémenter le décodage DXVA.

Dans le reste de cette rubrique, le *décodeur* de terme fait référence à la table MFT du décodeur, qui reçoit la vidéo compressée et génère des sorties vidéo non compressées. L' *appareil décodeur* terme fait référence à un accélérateur vidéo matériel implémenté par le pilote Graphics.

> [!TIP]
> Pour plus d’informations sur le décodage vidéo de Microsoft Direct3D 11, consultez [prise en charge du décodage vidéo Direct3D 11 dans Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Les applications du Windows Store doivent utiliser Direct3D 11.

 

Voici les étapes de base qu’un décodeur doit effectuer pour prendre en charge DXVA 2,0 dans Media Foundation :

1.  Ouvrez un handle vers l’appareil Direct3D 9.
2.  Recherchez une configuration de décodeur DXVA.
3.  Allouez des tampons non compressés.
4.  Décodez les frames.

Ces étapes sont décrites plus en détail dans le reste de cette rubrique.

## <a name="opening-a-direct3d-device-handle"></a>Ouverture d’un handle de périphérique Direct3D

La table MFT utilise le gestionnaire de périphériques Microsoft Direct3D pour obtenir un descripteur de l’appareil Direct3D 9. Pour ouvrir le descripteur de l’appareil, procédez comme suit :

1.  Exposez l’attribut [ \_ prenant en \_ \_ charge Direct3D sa](mf-sa-d3d-aware-attribute.md) avec la valeur **true**. Le chargeur de topologie interroge cet attribut en appelant [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). L’affectation de la **valeur true** à l’attribut indique au chargeur de topologie que la table MFT prend en charge DXVA.
2.  Lorsque la négociation de format commence, le chargeur de topologie appelle [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de l' [**ensemble de messages MFT du \_ \_ \_ \_ Gestionnaire D3D**](mft-message-set-d3d-manager.md) . Le paramètre *ulParam* est un pointeur **IUnknown** vers le gestionnaire de périphériques Direct3D du convertisseur vidéo. Interrogez ce pointeur sur l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Appelez [**IDirect3DDeviceManager9 :: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) pour obtenir un handle sur le périphérique Direct3D du convertisseur.
4.  Appelez [**IDirect3DDeviceManager9 :: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) et transmettez le descripteur de l’appareil. Cette méthode retourne un pointeur vers l’interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Mettez en cache les pointeurs et le handle d’appareil.

## <a name="finding-a-decoder-configuration"></a>Recherche d’une configuration de décodeur

La table MFT doit trouver une configuration compatible pour le périphérique décodeur DXVA. Effectuez les étapes suivantes à l’intérieur de la méthode [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , après avoir validé le type d’entrée :

1.  Appelez [**IDirectXVideoDecoderService :: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Cette méthode retourne un tableau de GUID d’appareil de décodage.
2.  Parcourez le tableau de GUID de décodeur pour trouver ceux que le décodeur prend en charge. Par exemple, pour un décodeur MPEG-2, vous devez rechercher **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** ou DXVA2 ModeMPEG2 **\_ \_ VLD**.

3.  Lorsque vous trouvez un GUID d’appareil décodeur candidat, transmettez le GUID à la méthode [**IDirectXVideoDecoderService :: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Cette méthode retourne un tableau de formats de cible de rendu, spécifiés en tant que valeurs **D3DFORMAT** .
4.  Parcourez les formats des cibles de rendu et recherchez un format pris en charge par le décodeur.
5.  Appelez [**IDirectXVideoDecoderService :: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Transmettez le même GUID de périphérique décodeur, ainsi qu’une structure [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) qui décrit le format de sortie proposé. La méthode retourne un tableau de structures [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Chaque structure décrit une configuration possible pour l’appareil décodeur. Recherchez une configuration prise en charge par le décodeur.
6.  Stockez le format et la configuration de la cible de rendu.

Dans la méthode [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , retourne un format vidéo non compressé, en fonction du format de cible de rendu proposé.

Dans la méthode [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , vérifiez le type de média par rapport au format de la cible de rendu.

### <a name="fallback-to-software-decoding"></a>Revenir au décodage logiciel

Si la MFT ne trouve pas de configuration DXVA (par exemple, si le pilote Graphics n’a pas les bonnes fonctionnalités), il doit retourner le code d’erreur **MF \_ E \_ \_ \_ type D3D non pris en charge** à partir des méthodes [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) et [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . Le chargeur de topologie répond en envoyant le message de [**l' \_ ensemble de messages MFT du \_ \_ \_ Gestionnaire D3D**](mft-message-set-d3d-manager.md) avec la valeur **null** pour le paramètre *ulParam* . La table MFT doit libérer son pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Le chargeur de topologie renégocie ensuite le type de média et la table MFT peut utiliser le décodage logiciel.

## <a name="allocating-uncompressed-buffers"></a>Allocation de mémoires tampons non compressées

Dans DXVA 2,0, le décodeur est chargé d’allouer des surfaces Direct3D à utiliser comme mémoires tampons vidéo non compressées. Le décodeur doit allouer 3 surfaces pour le EVR à utiliser pour l’entrelacement. Ce nombre est fixe, car Media Foundation ne permet pas au EVR de spécifier le nombre de surfaces nécessaires au pilote Graphics pour l’entrelacement. Trois surfaces doivent être suffisantes pour n’importe quel pilote.

Dans la méthode [**IMFTransform :: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , définissez le **flux de sortie MFT fournit l’indicateur \_ \_ \_ \_ Samples** dans la structure d' [**informations du \_ \_ flux \_ de sortie MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Cet indicateur signale à la session multimédia que la table MFT alloue ses propres exemples de sortie.

Pour créer les surfaces, appelez [**IDirectXVideoAccelerationService :: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface). (L’interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) hérite de cette méthode de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).) Vous pouvez le faire dans [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype), après avoir trouvé le format de la cible du rendu.

Pour chaque surface, appelez [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) pour créer un échantillon de support destiné à accueillir l’aire. La méthode retourne un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .

## <a name="decoding"></a>Décodage

Pour créer l’appareil de décodage, appelez [**IDirectXVideoDecoderService :: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). La méthode retourne un pointeur vers l’interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) de l’appareil décodeur.

Le décodage doit se produire à l’intérieur de la méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Sur chaque frame, appelez [**IDirect3DDeviceManager9 :: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) pour tester le handle de l’appareil. Si l’appareil a changé, la méthode retourne **DXVA2 \_ E \_ New \_ Video \_ Device**. Si cela se produit, procédez comme suit :

1.  Fermez le handle d’appareil en appelant [**IDirect3DDeviceManager9 :: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Libérez les pointeurs [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) et [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Ouvrez un nouveau descripteur d’appareil.
4.  Négociez une nouvelle configuration de décodeur, comme décrit dans la section « recherche d’une configuration de décodeur », plus haut dans cette page.
5.  Créez un appareil de décodage.

En supposant que le descripteur de l’appareil est valide, le processus de décodage fonctionne comme suit :

1.  Obtient une surface disponible qui n’est pas en cours d’utilisation. (Initialement, toutes les surfaces sont disponibles.)
2.  Interrogez l’exemple de support pour l’interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .
3.  Appelez [**IMFTrackedSample :: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) et fournissez un pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , implémentée par le décodeur. Quand le convertisseur vidéo libère l’exemple, le rappel du décodeur est appelé.
4.  Appelez [**IDirectXVideoDecoder :: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
5.  Effectuez les opérations suivantes une ou plusieurs fois :
    1.  Appelez [**IDirectXVideoDecoder :: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) pour obtenir une mémoire tampon de décodeur DXVA.
    2.  Remplir la mémoire tampon.
    3.  Appelez [**IDirectXVideoDecoder :: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
    4.  Appelez [**IDirectXVideoDecoder :: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) pour effectuer les opérations de décodage sur le frame.

DXVA 2,0 utilise les mêmes structures de données que DXVA 1,0 pour les opérations de décodage. Pour l’ensemble initial de profils DXVA (pour H. 261, H. 263 et MPEG-2), ces structures de données sont décrites dans la [spécification DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Au sein de chaque paire d’appels [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , vous pouvez appeler [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) plusieurs fois, mais une seule fois pour chaque type de mémoire tampon DXVA. Si vous l’appelez deux fois avec le même type de mémoire tampon, vous allez remplacer les données.

Utilisez le rappel à partir de la méthode [**SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (étape 3) pour effectuer le suivi des exemples qui sont actuellement disponibles et qui sont en cours d’utilisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 
