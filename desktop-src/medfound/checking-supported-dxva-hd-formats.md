---
description: .
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Vérification des formats DXVA-HD pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7560d574cee5fca21ab8de78b01b87af1de5a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484121"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="13062-103">Vérification des formats DXVA-HD pris en charge</span><span class="sxs-lookup"><span data-stu-id="13062-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="13062-104">Vérification des formats d’entrée pris en charge</span><span class="sxs-lookup"><span data-stu-id="13062-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="13062-105">Pour obtenir la liste des formats d’entrée pris en charge par l’appareil haute définition (DXVA-HD) de Microsoft DirectX, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="13062-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="13062-106">Appelez [**IDXVAHD \_ Device :: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) pour accéder aux fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="13062-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="13062-107">Vérifiez le membre **InputFormatCount** de la structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="13062-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="13062-108">Ce membre donne le nombre de formats d’entrée pris en charge.</span><span class="sxs-lookup"><span data-stu-id="13062-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="13062-109">Allouez un tableau de valeurs **D3DFORMAT** , de taille **InputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="13062-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="13062-110">Transmettez ce tableau à la méthode [**IDXVAHD \_ Device :: GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) .</span><span class="sxs-lookup"><span data-stu-id="13062-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="13062-111">Les méthodes remplissent le tableau avec une liste de formats d’entrée.</span><span class="sxs-lookup"><span data-stu-id="13062-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="13062-112">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="13062-112">The following code shows these steps:</span></span>


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



## <a name="checking-supported-output-formats"></a><span data-ttu-id="13062-113">Vérification des formats de sortie pris en charge</span><span class="sxs-lookup"><span data-stu-id="13062-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="13062-114">Pour obtenir la liste des formats de sortie pris en charge par l’appareil DXVA-HD, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="13062-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="13062-115">Appelez [**IDXVAHD \_ Device :: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) pour accéder aux fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="13062-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="13062-116">Vérifiez le membre **OutputFormatCount** de la structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="13062-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="13062-117">Ce membre donne le nombre de formats d’entrée pris en charge.</span><span class="sxs-lookup"><span data-stu-id="13062-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="13062-118">Allouez un tableau de valeurs **D3DFORMAT** , de taille **OutputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="13062-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="13062-119">Transmettez ce tableau à la méthode [**IDXVAHD \_ Device :: GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) .</span><span class="sxs-lookup"><span data-stu-id="13062-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="13062-120">Les méthodes remplissent le tableau avec une liste de formats de sortie.</span><span class="sxs-lookup"><span data-stu-id="13062-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="13062-121">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="13062-121">The following code shows these steps:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="13062-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13062-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13062-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="13062-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



