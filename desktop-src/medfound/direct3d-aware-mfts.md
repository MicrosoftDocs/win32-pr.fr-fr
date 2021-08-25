---
description: Cette rubrique explique comment implémenter une table de Media Foundation pour la vidéo.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae3bc071ee707505fd7412cba6f0a5aa397fd4c3f623225da28cc5490bf3323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958735"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware MFTs

Cette rubrique explique comment implémenter une table de Media Foundation *pour la vidéo* .

Une table MFT vidéo est considérée comme *compatible Direct3D* si elle peut traiter des exemples qui contiennent des surfaces Direct3D. La prise en charge de Direct3D dans une table MFT vidéo est généralement nécessaire pour activer le décodage accéléré par le matériel, à l’aide de l’accélération vidéo DirectX (DXVA).

Cette rubrique décrit les étapes nécessaires à la prise en charge de Direct3D MFT. Cette rubrique ne couvre pas la mécanique du décodage DXVA. Pour plus d’informations sur DXVA, consultez [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md).

> [!IMPORTANT]
> à compter de Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) peut être utilisé à la place de [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). pour les applications Windows store, vous devez utiliser **IMFDXGIDeviceManager** et Microsoft Direct3D 11. Pour plus d’informations, consultez les [API vidéo Direct3D 11](direct3d-11-video-apis.md).

 

1.  Implémentez la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Cette méthode retourne un pointeur vers un magasin d’attributs.
2.  La table MFT doit définir la valeur de l’attribut [**\_ prenant en \_ \_ charge Direct3D sa**](mf-sa-d3d-aware-attribute.md) sur **true** dans son propre magasin d’attributs. à compter de Windows 8, si vous utilisez Direct3D 11, utilisez [MF \_ SA \_ D3D11 \_ ](mf-sa-d3d11-aware.md).
3.  Au cours de la négociation de format, si l’attribut compatible avec la prise en [**\_ \_ \_ charge Direct3D MF**](mf-sa-d3d-aware-attribute.md) (ou [MF \_ sa \_ d3d11 \_](mf-sa-d3d11-aware.md) avec l’utilisation de Direct3D 11) a la **valeur true**, le client peut envoyer le message du [**\_ \_ \_ \_ Gestionnaire D3D du jeu de messages MFT**](mft-message-set-d3d-manager.md) à la MFT. Le paramètre d’événement *ulParam* est un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . à partir de Windows 8, vous pouvez utiliser [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) au lieu de **IDirect3DDeviceManager9**. Le client n’est pas obligé d’envoyer ce message.
4.  La table MFT appelle [**IDirect3DDeviceManager9 :: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) pour effectuer une requête sur le service DXVA dont elle a besoin. à compter de Windows 8, si [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) a été utilisé, la MFT appelle [**IMFDXGIDeviceManager :: GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). En général, un décodeur interroge pour [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)et un processeur vidéo interroge [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice).
5.  En supposant que l’étape précédente est réussie, les méthodes [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) et [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) doivent retourner des formats compatibles DXVA.
6.  Le client configure les types de média sur la table MFT. Si un type de média n’est pas compatible avec DXVA, le MFT doit retourner le code d’erreur **MF \_ E \_ \_ \_ type D3D non pris en charge**.
7.  À ce stade, il existe deux options, selon que le client trouve un format DXVA approprié.
    -   Si le client configure correctement un format DXVA, il peut commencer le traitement. À ce stade, la MFT peut utiliser DXVA pour le traitement ou revenir au traitement logiciel.
    -   Sinon, si le client ne trouve pas de format DXVA acceptable, le client peut envoyer un autre message du [**\_ \_ \_ \_ Gestionnaire D3D de l’ensemble de messages MFT**](mft-message-set-d3d-manager.md) , ce qui affecte la **valeur null** à *ulParam* . La table MFT doit libérer le pointeur [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) (le pointeur [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) , si **IMFDXGIDeviceManager** a été utilisé) et toutes les autres interfaces DXVA, et revenir au traitement logiciel. À ce stade, la MFT ne doit pas utiliser le traitement DXVA.

Une table MFT prenant en charge Direct3D doit être préparée pour gérer les exemples qui contiennent une surface Direct3D. L’exemple contient exactement un seul tampon de média. Pour récupérer la surface Direct3D à partir de la mémoire tampon, appelez la fonction [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) et spécifiez le service de **\_ mémoire \_ tampon Mr** . Pour plus d’informations, consultez [DirectX surface buffer](directx-surface-buffer.md).

Une table MFT qui utilise DXVA doit allouer ses propres exemples de sortie, comme suit :

1.  Dans la méthode [**IMFTransform :: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) , le **flux de \_ sortie MFT fournit des \_ \_ \_ exemples** d’indicateurs.
2.  Créez un pool de surfaces DXVA, comme décrit dans la spécification DXVA.
3.  Créez des exemples de supports en appelant [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface).

La table MFT doit toujours prendre en charge le traitement logiciel comme secours, car le traitement DXVA peut ne pas être disponible pour plusieurs raisons :

-   Le GPU ne prend peut-être pas en charge DXVA.
-   Le client peut ne pas utiliser Direct3D.
-   Les profils DXVA ne sont pas définis pour chaque format vidéo.

Une table MFT prenant en charge Direct3D doit avoir un seul flux de sortie. Il ne peut pas avoir plusieurs sorties.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> </dl>

 

 



