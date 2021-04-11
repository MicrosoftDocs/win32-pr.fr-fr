---
description: Mémoire tampon de surface DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Mémoire tampon de surface DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111787"
---
# <a name="directx-surface-buffer"></a>Mémoire tampon de surface DirectX

L’objet de mémoire tampon de surface DirectX est un tampon de média qui gère une surface Direct3D. Pour créer une instance de cet objet, appelez [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) et transmettez un pointeur vers la surface DirectX. La mémoire tampon de surface DirectX expose les interfaces suivantes :

-   [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Il existe plusieurs façons d’accéder à la mémoire de surface à partir de l’objet buffer :

-   Recommandé : appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la mémoire tampon. Utilisez le **\_ \_ service de mémoire tampon** de l’identificateur de service Mr. La méthode retourne un pointeur vers la surface Direct3D sous-jacente.
-   Appelez [**IMF2DBuffer :: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d). Cette méthode appelle **IDirect3DSurface9 :: LockRect** directement sur l’aire de conception. La méthode [**IMF2DBuffer :: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) appelle **UnlockRect** sur l’aire de conception.
-   Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). En général, cela n’est pas recommandé, car il force l’objet à copier la mémoire à partir de la surface Direct3D, puis de revenir en arrière. La méthode [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) est plus efficace.

[**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) et [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) peuvent échouer si la surface sous-jacente n’est pas verrouillable. La mémoire tampon de surface DirectX implémente ces deux méthodes principalement pour les composants qui ne sont pas conçus pour fonctionner avec les surfaces Direct3D.

Le convertisseur vidéo amélioré (EVR) crée des mémoires tampons de surface DirectX quand le décodeur n’est pas configuré pour l’accélération vidéo DirectX (DXVA). Pour plus d’informations, consultez [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).

### <a name="obtaining-the-direct3d-surface"></a>Obtention de la surface Direct3D

Pour obtenir une surface Direct3D à partir d’un exemple de vidéo, procédez comme suit :

1.  Appelez [**IMFSample :: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) avec une valeur d’index égale à zéro.
2.  Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) et spécifiez l’identificateur de service de **\_ mémoire \_ tampon Mr** .

Le code suivant illustre ces étapes :


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de média](media-buffers.md)
</dt> <dt>

[Exemples vidéo](video-samples.md)
</dt> </dl>

 

 



