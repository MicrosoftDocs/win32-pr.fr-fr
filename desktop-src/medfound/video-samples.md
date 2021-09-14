---
description: Exemples vidéo
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Exemples vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313597"
---
# <a name="video-samples"></a>Exemples vidéo

L’exemple d’objet vidéo est une implémentation spécialisée de l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pour une utilisation avec le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR). Pour créer une instance de cet objet, appelez la fonction [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) . La fonction prend un pointeur vers une surface Direct3D et retourne un pointeur vers l’interface **IMFSample** . Les types d’objets suivants doivent allouer des exemples à l’aide de cette fonction :

-   Présentateur EVR personnalisé. Un présentateur alloue des échantillons vidéo et les envoie à la méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) de mixer. Pour plus d’informations, consultez [Comment écrire un présentateur EVR](how-to-write-an-evr-presenter.md).

-   Décodeurs vidéo qui prennent en charge l’accélération vidéo. Pour plus d’informations, consultez [prise en charge de DXVA 2,0 dans Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

L’exemple d’objet Video implémente les interfaces suivantes :

-   [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Si le paramètre *pUnkSurface* de [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) est non **null**, l’exemple de vidéo qui en résulte contient une seule mémoire tampon de média qui encapsule la surface Direct3D. Cet objet de mémoire tampon a des fonctionnalités limitées :

-   La méthode [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) de la mémoire tampon retourne E \_ NOTIMPL.

-   La mémoire tampon n’implémente pas l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .

La seule façon d’accéder à la surface à partir de la mémoire tampon consiste à appeler [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)à l’aide de l’identificateur de service \_ service de mémoire tampon Mr \_ .

Si le paramètre *pUnkSurface* est **null**, l’exemple de vidéo est créé avec des tampons de média nuls. Pour ajouter un tampon à l’exemple, procédez comme suit :

1.  Créez une surface Direct3D.

2.  Créez une mémoire tampon de surface en appelant [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer). Pour plus d’informations, consultez [DirectX surface buffer](directx-surface-buffer.md).

3.  Ajoutez la mémoire tampon à l’exemple en appelant [**IMFSample :: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Utilisez cette approche si vous avez besoin que la mémoire de surface soit accessible par le biais de l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de média](media-buffers.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> </dl>

 

 
