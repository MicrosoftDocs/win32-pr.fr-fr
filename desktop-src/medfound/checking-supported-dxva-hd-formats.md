---
description: Vérification des formats DXVA-HD pris en charge
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Vérification des formats DXVA-HD pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07d47043ed200d256e2bef8fa2c9ab6717f3b82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525833"
---
# <a name="checking-supported-dxva-hd-formats"></a>Vérification des formats DXVA-HD pris en charge

## <a name="checking-supported-input-formats"></a>Vérification des formats d’entrée pris en charge

Pour obtenir la liste des formats d’entrée pris en charge par l’appareil haute définition (DXVA-HD) de Microsoft DirectX, procédez comme suit :

1.  Appelez [**IDXVAHD \_ Device :: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) pour accéder aux fonctionnalités de l’appareil.
2.  Vérifiez le membre **InputFormatCount** de la structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . Ce membre donne le nombre de formats d’entrée pris en charge.
3.  Allouez un tableau de valeurs **D3DFORMAT** , de taille **InputFormatCount**.
4.  Transmettez ce tableau à la méthode [**IDXVAHD \_ Device :: GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) . Les méthodes remplissent le tableau avec une liste de formats d’entrée.

Le code suivant illustre ces étapes :


```C++
// Checks whether a DXVA-HD device supports a specified input format.

HRESULT CheckInputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[ caps.InputFormatCount ];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorInputFormats(
        caps.InputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.InputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.InputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="checking-supported-output-formats"></a>Vérification des formats de sortie pris en charge

Pour obtenir la liste des formats de sortie pris en charge par l’appareil DXVA-HD, procédez comme suit :

1.  Appelez [**IDXVAHD \_ Device :: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) pour accéder aux fonctionnalités de l’appareil.
2.  Vérifiez le membre **OutputFormatCount** de la structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . Ce membre donne le nombre de formats d’entrée pris en charge.
3.  Allouez un tableau de valeurs **D3DFORMAT** , de taille **OutputFormatCount**.
4.  Transmettez ce tableau à la méthode [**IDXVAHD \_ Device :: GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) . Les méthodes remplissent le tableau avec une liste de formats de sortie.

Le code suivant illustre ces étapes :


```C++
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



