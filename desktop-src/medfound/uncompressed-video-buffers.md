---
description: Mémoires tampons vidéo non compressées
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Mémoires tampons vidéo non compressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529767"
---
# <a name="uncompressed-video-buffers"></a>Mémoires tampons vidéo non compressées

Cet article explique comment utiliser des mémoires tampons de média qui contiennent des images vidéo non compressées. Par ordre de préférence, les options suivantes sont disponibles. Chaque mémoire tampon de média ne prend pas en charge chaque option.

1.  Utilisez la surface Direct3D sous-jacente. (S’applique uniquement aux images vidéo stockées dans des surfaces Direct3D.)
2.  Utilisez l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
3.  Utilisez l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .

## <a name="use-the-underlying-direct3d-surface"></a>Utiliser la surface Direct3D sous-jacente

L’image vidéo peut être stockée à l’intérieur d’une surface Direct3D. Si c’est le cas, vous pouvez obtenir un pointeur vers la surface en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ou [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sur l’objet de mémoire tampon du média. Utilisez le service de mémoire tampon de l’identificateur de service MR \_ \_ . Cette approche est recommandée lorsque le composant qui accède à la trame vidéo est conçu pour utiliser Direct3D. Par exemple, un décodeur vidéo qui prend en charge l’accélération vidéo DirectX doit utiliser cette approche.

Le code suivant montre comment obtenir le pointeur **IDirect3DSurface9** à partir d’une mémoire tampon de média.


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



Les objets suivants prennent en charge le service de **\_ mémoire \_ tampon Mr** :

-   [Mémoire tampon de surface DirectX](directx-surface-buffer.md)
-   [Exemples vidéo](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a>Utiliser l’interface IMF2DBuffer

Si la trame vidéo n’est pas stockée dans une surface Direct3D, ou si le composant n’est pas conçu pour utiliser Direct3D, la méthode recommandée suivante pour accéder à la vidéo est d’interroger la mémoire tampon pour l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Cette interface est conçue spécifiquement pour les données d’image. Pour obtenir un pointeur vers cette interface, appelez **QueryInterface** sur la mémoire tampon du média. Les objets de mémoire tampon de média n’exposent pas tous cette interface. Toutefois, si une mémoire tampon de support expose l’interface **IMF2DBuffer** , vous devez utiliser cette interface pour accéder aux données, si possible, au lieu d’utiliser [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer). Vous pouvez toujours utiliser l’interface **IMFMediaBuffer** , mais elle peut être moins efficace.

1.  Appelez **QueryInterface** sur la mémoire tampon du média pour accéder à l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
2.  Appelez [**IMF2DBuffer :: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) pour accéder à la mémoire de la mémoire tampon. Cette méthode retourne un pointeur vers le premier octet de la ligne supérieure de pixels. Elle retourne également l’image Stride, qui est le nombre d’octets à partir du début d’une ligne de pixels jusqu’au début de la ligne suivante. La mémoire tampon peut contenir des octets de remplissage après chaque ligne de pixels. par conséquent, le Stride peut être plus large que la largeur de l’image en octets. La valeur Stride peut également être négative si l’image est orientée vers le bas en mémoire. Pour plus d’informations, consultez l' [image Stride](image-stride.md).
3.  Veillez à ce que la mémoire tampon soit verrouillée uniquement lorsque vous avez besoin d’accéder à la mémoire. Déverrouillez la mémoire tampon en appelant [**IMF2DBuffer :: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).

Chaque mémoire tampon de média n’implémente pas l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Si la mémoire tampon du média n’implémente pas cette interface (autrement dit, l’objet buffer retourne E \_ nointerface à l’étape 1), vous devez utiliser l’interface d’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , décrite ci-dessous.

## <a name="use-the-imfmediabuffer-interface"></a>Utiliser l’interface IMFMediaBuffer

Si une mémoire tampon de support n’expose pas l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , utilisez l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . La sémantique générale de cette interface est décrite dans la rubrique [utilisation des mémoires tampons de média](working-with-media-buffers.md).

1.  Appelez **QueryInterface** sur la mémoire tampon du média pour accéder à l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
2.  Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour accéder à la mémoire tampon. Cette méthode retourne un pointeur vers la mémoire tampon. Lorsque la méthode **Lock** est utilisée, le Stride est toujours le Stride minimal pour le format vidéo en question, sans octets de remplissage supplémentaires.
3.  Veillez à ce que la mémoire tampon soit verrouillée uniquement lorsque vous avez besoin d’accéder à la mémoire. Déverrouillez la mémoire tampon en appelant [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Vous devez toujours éviter d’appeler [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) si la mémoire tampon expose [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), parce que la méthode **Lock** peut forcer l’objet de mémoire tampon à la trame vidéo dans un bloc de mémoire contigu, puis de nouveau. En revanche, si la mémoire tampon ne prend pas en charge **IMF2DBuffer**, **IMFMediaBuffer :: Lock** n’entraînera probablement pas de copie.

Calculez la valeur Stride minimale à partir du type de média comme suit :

-   La valeur Stride minimale peut être stockée dans l’attribut [**\_ \_ Stride MT default \_ Stride**](mf-mt-default-stride-attribute.md) .
-   Si l' **attribut \_ \_ Stride MT default \_ Stride** n’est pas défini, appelez la fonction [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) pour calculer le Stride pour les formats vidéo les plus courants.
-   Si la fonction [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) ne reconnaît pas le format, vous devez calculer la Stride en fonction de la définition du format. Dans ce cas, il n’y a pas de règle générale ; vous devez connaître les détails de la définition de format.

Le code suivant montre comment obtenir le Stride par défaut pour les formats vidéo les plus courants.


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



Selon votre application, vous pouvez savoir à l’avance si une mémoire tampon de média donnée prend en charge [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (par exemple, si vous avez créé la mémoire tampon). Dans le cas contraire, vous devez être prêt à utiliser l’une ou l’autre des deux interfaces de tampon.

L’exemple suivant montre une classe d’assistance qui masque certains de ces détails. Cette classe possède une méthode LockBuffer qui appelle [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) ou [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) et retourne un pointeur vers le début de la première ligne de pixels. (Ce comportement correspond à la méthode **Lock2D** .) La méthode LockBuffer prend le Stride par défaut comme paramètre d’entrée et retourne le Stride réel en tant que paramètre de sortie.


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[STRIDE d’image](image-stride.md)
</dt> <dt>

[Mémoires tampons de média](media-buffers.md)
</dt> </dl>

 

 



