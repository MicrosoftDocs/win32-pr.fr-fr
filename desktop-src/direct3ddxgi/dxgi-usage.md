---
description: Indicateurs pour les options de création de surface et de ressource.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525874"
---
# <a name="dxgi_usage"></a><span data-ttu-id="69f7e-103">utilisation de DXGI \_</span><span class="sxs-lookup"><span data-stu-id="69f7e-103">DXGI\_USAGE</span></span>

<span data-ttu-id="69f7e-104">Indicateurs pour les options de création de surface et de ressource.</span><span class="sxs-lookup"><span data-stu-id="69f7e-104">Flags for surface and resource creation options.</span></span>



| <span data-ttu-id="69f7e-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="69f7e-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="69f7e-106">Description</span><span class="sxs-lookup"><span data-stu-id="69f7e-106">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <span data-ttu-id="69f7e-107"><dt>**Dxgi \_ \_ \_ Mémoire tampon d’arrière-plan d’utilisation**</dt> <dt>1L <<  (2 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="69f7e-107"><dt>**DXGI\_USAGE\_BACK\_BUFFER**</dt> <dt>1L << (2 + 4)</dt></span></span> </dl>                             | <span data-ttu-id="69f7e-108">La surface ou la ressource est utilisée comme mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="69f7e-108">The surface or resource is used as a back buffer.</span></span> <span data-ttu-id="69f7e-109">Vous n’avez pas besoin de transmettre la **\_ \_ \_ mémoire tampon d’arrière-plan d’utilisation dxgi** quand vous créez une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="69f7e-109">You don’t need to pass **DXGI\_USAGE\_BACK\_BUFFER** when you create a swap chain.</span></span> <span data-ttu-id="69f7e-110">Toutefois, vous pouvez déterminer si une ressource appartient à une chaîne de permutation quand vous appelez [**IDXGIResource :: GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) et obtenir une **\_ \_ \_ mémoire tampon d’arrière-plan d’utilisation dxgi**.</span><span class="sxs-lookup"><span data-stu-id="69f7e-110">But you can determine whether a resource belongs to a swap chain when you call [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) and get **DXGI\_USAGE\_BACK\_BUFFER**.</span></span><br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <span data-ttu-id="69f7e-111"><dt>**Dxgi \_ UTILISATION \_ ignorée \_ le \_**</dt> <dt> <<  1L présent (5 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="69f7e-111"><dt>**DXGI\_USAGE\_DISCARD\_ON\_PRESENT**</dt> <dt>1L << (5 + 4)</dt></span></span> </dl>       | <span data-ttu-id="69f7e-112">Cet indicateur est destiné à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="69f7e-112">This flag is for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <span data-ttu-id="69f7e-113"><dt>**Dxgi \_ <<  \_ lecture \_ seule 1L de l’utilisation**</dt> <dt>(4 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="69f7e-113"><dt>**DXGI\_USAGE\_READ\_ONLY**</dt> <dt>1L << (4 + 4)</dt></span></span> </dl>                                   | <span data-ttu-id="69f7e-114">Utilisez l’aire ou la ressource pour la lecture uniquement.</span><span class="sxs-lookup"><span data-stu-id="69f7e-114">Use the surface or resource for reading only.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <span data-ttu-id="69f7e-115"><dt>**Dxgi \_ \_ \_ \_ Sortie de la cible de rendu de l’utilisation**</dt> <dt>1L <<  (1 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="69f7e-115"><dt>**DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT**</dt> <dt>1L << (1 + 4)</dt></span></span> </dl> | <span data-ttu-id="69f7e-116">Utilisez la surface ou la ressource en tant que cible de rendu de sortie.</span><span class="sxs-lookup"><span data-stu-id="69f7e-116">Use the surface or resource as an output render target.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <span data-ttu-id="69f7e-117"><dt>**Dxgi \_ <<  \_ \_ d’entrée du nuanceur d’utilisation**</dt> <dt>1L (0 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="69f7e-117"><dt>**DXGI\_USAGE\_SHADER\_INPUT**</dt> <dt>1L << (0 + 4)</dt></span></span> </dl>                          | <span data-ttu-id="69f7e-118">Utilisez la surface ou la ressource comme entrée d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="69f7e-118">Use the surface or resource as an input to a shader.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <span data-ttu-id="69f7e-119"><dt>**Dxgi \_ 1L \_ partagé d’utilisation**</dt> <dt> <<  (3 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="69f7e-119"><dt>**DXGI\_USAGE\_SHARED**</dt> <dt>1L << (3 + 4)</dt></span></span> </dl>                                             | <span data-ttu-id="69f7e-120">Partager l’aire ou la ressource.</span><span class="sxs-lookup"><span data-stu-id="69f7e-120">Share the surface or resource.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <span data-ttu-id="69f7e-121"><dt>**Dxgi \_ Utilisation non \_ triée \_ de l’accès**</dt> <dt>1L <<  (6 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="69f7e-121"><dt>**DXGI\_USAGE\_UNORDERED\_ACCESS**</dt> <dt>1L << (6 + 4)</dt></span></span> </dl>              | <span data-ttu-id="69f7e-122">Utilisez l’aire ou la ressource pour un accès non ordonné.</span><span class="sxs-lookup"><span data-stu-id="69f7e-122">Use the surface or resource for unordered access.</span></span><br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="69f7e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="69f7e-123">Remarks</span></span>

<span data-ttu-id="69f7e-124">Chaque indicateur est défini comme un entier non signé.</span><span class="sxs-lookup"><span data-stu-id="69f7e-124">Each flag is defined as an unsigned integer.</span></span>

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

<span data-ttu-id="69f7e-125">Ces options d’indicateur sont utilisées dans un appel à la méthode [**IDXGIFactory :: CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2 :: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2 :: CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)ou [**IDXGIFactory2 :: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) pour décrire les options d’accès à l’utilisation de la surface et de l’UC pour la mémoire tampon d’arrière-plan d’une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="69f7e-125">These flag options are used in a call to the [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow), or [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method to describe the surface usage and CPU access options for the back buffer of a swap chain.</span></span> <span data-ttu-id="69f7e-126">Vous ne pouvez pas utiliser les valeurs **\_ \_ Shared dxgi Shared**, **dxgi \_ usage \_ ignore \_ on \_ present** et **dxgi \_ usage \_ Read \_ only** comme entrée pour créer une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="69f7e-126">You can't use the **DXGI\_USAGE\_SHARED**, **DXGI\_USAGE\_DISCARD\_ON\_PRESENT**, and **DXGI\_USAGE\_READ\_ONLY** values as input to create a swap chain.</span></span> <span data-ttu-id="69f7e-127">Toutefois, DXGI peut définir **le \_ \_ rejet \_ de l' \_ utilisation de dxgi en présence** et **\_ l’utilisation de dxgi \_ \_ uniquement** pour certaines des mémoires tampons d’arrière-plan de la chaîne de permutation au nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="69f7e-127">However, DXGI can set **DXGI\_USAGE\_DISCARD\_ON\_PRESENT** and **DXGI\_USAGE\_READ\_ONLY** for some of the swap chain's back buffers on the application's behalf.</span></span> <span data-ttu-id="69f7e-128">Vous pouvez appeler la méthode [**IDXGIResource :: GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) pour récupérer l’utilisation de ces mémoires tampons d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="69f7e-128">You can call the [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) method to retrieve the usage of these back buffers.</span></span> <span data-ttu-id="69f7e-129">La chaîne de permutation ne prend en charge que la valeur None de l’accès de l' **\_ UC \_ \_ dxgi** dans la partie du **\_ \_ \_ champ d’accès UC dxgi** de l' **\_ utilisation de dxgi**.</span><span class="sxs-lookup"><span data-stu-id="69f7e-129">Swap chain's only support the **DXGI\_CPU\_ACCESS\_NONE** value in the **DXGI\_CPU\_ACCESS\_FIELD** part of **DXGI\_USAGE**.</span></span>

<span data-ttu-id="69f7e-130">Ces options d’indicateur sont également utilisées par la méthode [**IDXGIDevice :: CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .</span><span class="sxs-lookup"><span data-stu-id="69f7e-130">These flag options are also used by the [**IDXGIDevice::CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="69f7e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69f7e-131">Requirements</span></span>



| <span data-ttu-id="69f7e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69f7e-132">Requirement</span></span> | <span data-ttu-id="69f7e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="69f7e-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="69f7e-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="69f7e-134">Header</span></span><br/> | <dl> <span data-ttu-id="69f7e-135"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="69f7e-135"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f7e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69f7e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f7e-137">Constantes DXGI</span><span class="sxs-lookup"><span data-stu-id="69f7e-137">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




