---
title: Comment se procurer le niveau de fonctionnalité de l’appareil
description: Cette rubrique montre comment obtenir le niveau de fonctionnalité le plus élevé pris en charge par un appareil.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840585"
---
# <a name="how-to-get-the-device-feature-level"></a><span data-ttu-id="2ba93-103">Procédure : obtention du niveau de fonctionnalité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="2ba93-103">How To: Get the Device Feature Level</span></span>

<span data-ttu-id="2ba93-104">Cette rubrique montre comment obtenir le niveau de [fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) le plus élevé pris en charge par un [appareil](overviews-direct3d-11-devices-intro.md).</span><span class="sxs-lookup"><span data-stu-id="2ba93-104">This topics shows how to get the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a [device](overviews-direct3d-11-devices-intro.md).</span></span> <span data-ttu-id="2ba93-105">Les périphériques Direct3D 11 prennent en charge un ensemble fixe de niveaux de fonctionnalités qui sont définis dans l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="2ba93-105">Direct3D 11 devices support a fixed set of feature levels that are defined in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span> <span data-ttu-id="2ba93-106">Lorsque vous connaissez le [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) le plus élevé pris en charge par un appareil, vous pouvez exécuter des chemins de code appropriés pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2ba93-106">When you know the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a device, you can run code paths that are appropriate for that device.</span></span>

<span data-ttu-id="2ba93-107">**Pour accéder au niveau de fonctionnalité de l’appareil**</span><span class="sxs-lookup"><span data-stu-id="2ba93-107">**To get the device feature level**</span></span>

1.  <span data-ttu-id="2ba93-108">Appelez la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou les fonctions [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) tout en spécifiant une **valeur null** pour le paramètre *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="2ba93-108">Call either the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) functions while specifying **NULL** for the *ppDevice* parameter.</span></span> <span data-ttu-id="2ba93-109">Vous pouvez effectuer cette opération avant la création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2ba93-109">You can do this before device creation.</span></span>

    <span data-ttu-id="2ba93-110">\- ou -</span><span class="sxs-lookup"><span data-stu-id="2ba93-110">\- or -</span></span>

    <span data-ttu-id="2ba93-111">Appelez [**ID3D11Device :: GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) après la création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2ba93-111">Call [**ID3D11Device::GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) after device creation.</span></span>

2.  <span data-ttu-id="2ba93-112">Examinez la valeur de l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) retournée à partir de la dernière étape pour déterminer le niveau de fonctionnalité pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2ba93-112">Examine the value of the returned [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration from the last step to determine the supported feature level.</span></span>

<span data-ttu-id="2ba93-113">L’exemple de code suivant montre comment déterminer le niveau de fonctionnalité le plus élevé pris en charge en appelant la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) .</span><span class="sxs-lookup"><span data-stu-id="2ba93-113">The following code example demonstrates how to determine the highest supported feature level by calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function.</span></span> <span data-ttu-id="2ba93-114">**D3D11CreateDevice** stocke le niveau de fonctionnalité le plus élevé pris en charge dans la variable FeatureLevel.</span><span class="sxs-lookup"><span data-stu-id="2ba93-114">**D3D11CreateDevice** stores the highest supported feature level in the FeatureLevel variable.</span></span> <span data-ttu-id="2ba93-115">Vous pouvez utiliser ce code pour examiner la valeur du type énuméré de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) retourné par **D3D11CreateDevice** .</span><span class="sxs-lookup"><span data-stu-id="2ba93-115">You can use this code to examine the value of the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumerated type that **D3D11CreateDevice** returns.</span></span> <span data-ttu-id="2ba93-116">Notez que ce code répertorie tous les niveaux de fonctionnalité explicitement (pour Direct3D 11,1 et Direct3D 11,2).</span><span class="sxs-lookup"><span data-stu-id="2ba93-116">Note that this code lists all feature levels explicitly (for Direct3D 11.1 and Direct3D 11.2).</span></span>

> [!Note]  
> <span data-ttu-id="2ba93-117">Si le runtime Direct3D 11,1 est présent sur l’ordinateur et que *pFeatureLevels* a la valeur **null**, cette fonction ne crée pas un appareil de [**niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="2ba93-117">If the Direct3D 11.1 runtime is present on the computer and *pFeatureLevels* is set to **NULL**, this function won't create a [**D3D\_FEATURE\_LEVEL\_11\_1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) device.</span></span> <span data-ttu-id="2ba93-118">Pour créer un appareil de **\_ niveau de fonctionnalité D3D \_ \_ 11 \_ 1** , vous devez fournir explicitement un tableau de **\_ \_ niveau de fonctionnalité D3D** qui comprend le **niveau de \_ fonctionnalité D3D \_ \_ 11 \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="2ba93-118">To create a **D3D\_FEATURE\_LEVEL\_11\_1** device, you must explicitly provide a **D3D\_FEATURE\_LEVEL** array that includes **D3D\_FEATURE\_LEVEL\_11\_1**.</span></span> <span data-ttu-id="2ba93-119">Si vous fournissez un tableau de **\_ \_ niveau de fonctionnalité D3D** qui contient le **niveau de \_ fonctionnalité D3D \_ \_ 11 \_ 1** sur un ordinateur sur lequel le runtime Direct3D 11,1 n’est pas installé, cette fonction échoue immédiatement avec E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="2ba93-119">If you provide a **D3D\_FEATURE\_LEVEL** array that contains **D3D\_FEATURE\_LEVEL\_11\_1** on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E\_INVALIDARG.</span></span>

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



<span data-ttu-id="2ba93-120">La section de [référence 10Level9](d3d11-graphics-reference-10level9.md) répertorie les différences entre la façon dont les différentes méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportent à différents niveaux de fonctionnalités 10Level9.</span><span class="sxs-lookup"><span data-stu-id="2ba93-120">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ba93-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ba93-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ba93-122">Direct3D 11 sur du matériel de niveau inférieur</span><span class="sxs-lookup"><span data-stu-id="2ba93-122">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[<span data-ttu-id="2ba93-123">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2ba93-123">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




