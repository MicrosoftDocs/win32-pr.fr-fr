---
description: Vérification des formats DXVA-HD pris en charge
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Vérification des formats DXVA-HD pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07d47043ed200d256e2bef8fa2c9ab6717f3b82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090007"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="04f91-103">Vérification des formats DXVA-HD pris en charge</span><span class="sxs-lookup"><span data-stu-id="04f91-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="04f91-104">Vérification des formats d’entrée pris en charge</span><span class="sxs-lookup"><span data-stu-id="04f91-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="04f91-105">Pour obtenir la liste des formats d’entrée pris en charge par l’appareil haute définition (DXVA-HD) de Microsoft DirectX, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="04f91-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="04f91-106">Appelez [**IDXVAHD \_ Device :: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) pour accéder aux fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="04f91-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="04f91-107">Vérifiez le membre **InputFormatCount** de la structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="04f91-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="04f91-108">Ce membre donne le nombre de formats d’entrée pris en charge.</span><span class="sxs-lookup"><span data-stu-id="04f91-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="04f91-109">Allouez un tableau de valeurs **D3DFORMAT** , de taille **InputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="04f91-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="04f91-110">Transmettez ce tableau à la méthode [**IDXVAHD \_ Device :: GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) .</span><span class="sxs-lookup"><span data-stu-id="04f91-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="04f91-111">Les méthodes remplissent le tableau avec une liste de formats d’entrée.</span><span class="sxs-lookup"><span data-stu-id="04f91-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="04f91-112">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="04f91-112">The following code shows these steps:</span></span>


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



## <a name="checking-supported-output-formats"></a><span data-ttu-id="04f91-113">Vérification des formats de sortie pris en charge</span><span class="sxs-lookup"><span data-stu-id="04f91-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="04f91-114">Pour obtenir la liste des formats de sortie pris en charge par l’appareil DXVA-HD, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="04f91-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="04f91-115">Appelez [**IDXVAHD \_ Device :: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) pour accéder aux fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="04f91-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="04f91-116">Vérifiez le membre **OutputFormatCount** de la structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="04f91-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="04f91-117">Ce membre donne le nombre de formats d’entrée pris en charge.</span><span class="sxs-lookup"><span data-stu-id="04f91-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="04f91-118">Allouez un tableau de valeurs **D3DFORMAT** , de taille **OutputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="04f91-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="04f91-119">Transmettez ce tableau à la méthode [**IDXVAHD \_ Device :: GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) .</span><span class="sxs-lookup"><span data-stu-id="04f91-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="04f91-120">Les méthodes remplissent le tableau avec une liste de formats de sortie.</span><span class="sxs-lookup"><span data-stu-id="04f91-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="04f91-121">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="04f91-121">The following code shows these steps:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="04f91-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04f91-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04f91-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="04f91-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



