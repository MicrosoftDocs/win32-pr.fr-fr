---
title: 'ID3D12DeviceDownlevel :: QueryVideoMemoryInfo, méthode'
description: 'Copie le contenu d’une ressource Direct3D 12 Texture2D dans une fenêtre. | ID3D12DeviceDownlevel :: QueryVideoMemoryInfo, méthode'
keywords:
- Méthode QueryVideoMemoryInfo
- Méthode QueryVideoMemoryInfo, interface ID3D12DeviceDownlevel
- Interface ID3D12DeviceDownlevel, méthode QueryVideoMemoryInfo
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539902"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a><span data-ttu-id="227f7-107">ID3D12DeviceDownlevel :: QueryVideoMemoryInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="227f7-107">ID3D12DeviceDownlevel::QueryVideoMemoryInfo method</span></span>

<span data-ttu-id="227f7-108">Fournit des statistiques de mémoire sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="227f7-108">Provides memory statistics on Windows 7.</span></span> <span data-ttu-id="227f7-109">Cette méthode est équivalente à [IDXGIAdapter3 :: QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), qui n’est pas disponible sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="227f7-109">This method is equivalent to [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), which is not available on Windows 7.</span></span>

## <a name="syntax"></a><span data-ttu-id="227f7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="227f7-110">Syntax</span></span>

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a><span data-ttu-id="227f7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="227f7-111">Parameters</span></span>

`NodeIndex`

<span data-ttu-id="227f7-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="227f7-112">Type: **UINT**</span></span>

<span data-ttu-id="227f7-113">Spécifie la carte physique de l’appareil pour laquelle les informations de mémoire vidéo sont interrogées.</span><span class="sxs-lookup"><span data-stu-id="227f7-113">Specifies the device's physical adapter for which the video memory information is queried.</span></span> <span data-ttu-id="227f7-114">Pour une opération à processeur unique, affectez-lui la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="227f7-114">For single-GPU operation, set this to zero.</span></span> <span data-ttu-id="227f7-115">S’il existe plusieurs nœuds GPU, définissez cette valeur sur l’index du nœud (la carte physique de l’appareil) pour lequel les informations de mémoire vidéo sont interrogées.</span><span class="sxs-lookup"><span data-stu-id="227f7-115">If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.</span></span> <span data-ttu-id="227f7-116">Consultez [systèmes à plusieurs adaptateurs](multi-engine.md).</span><span class="sxs-lookup"><span data-stu-id="227f7-116">See [Multi-adapter systems](multi-engine.md).</span></span>

`MemorySegmentGroup`

<span data-ttu-id="227f7-117">Type : **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span><span class="sxs-lookup"><span data-stu-id="227f7-117">Type: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span></span>

<span data-ttu-id="227f7-118">Spécifie un **DXGI_MEMORY_SEGMENT_GROUP** qui identifie le groupe comme local ou non local.</span><span class="sxs-lookup"><span data-stu-id="227f7-118">Specifies a **DXGI_MEMORY_SEGMENT_GROUP** that identifies the group as local or non-local.</span></span>

`pVideoMemoryInfo`

<span data-ttu-id="227f7-119">Type : **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span><span class="sxs-lookup"><span data-stu-id="227f7-119">Type: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span></span>

<span data-ttu-id="227f7-120">Remplit une structure **DXGI_QUERY_VIDEO_MEMORY_INFO** avec les valeurs actuelles.</span><span class="sxs-lookup"><span data-stu-id="227f7-120">Fills in a **DXGI_QUERY_VIDEO_MEMORY_INFO** structure with the current values.</span></span>

## <a name="return-value"></a><span data-ttu-id="227f7-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="227f7-121">Return value</span></span>

<span data-ttu-id="227f7-122">Retourne **S_OK** en cas de réussite, ou un HRESULT qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="227f7-122">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="227f7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="227f7-123">Requirements</span></span>

| <span data-ttu-id="227f7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="227f7-124">Requirement</span></span> | <span data-ttu-id="227f7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="227f7-125">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="227f7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="227f7-126">Header</span></span> | <span data-ttu-id="227f7-127">d3d12downlevel. h et dxgi1_4. h</span><span class="sxs-lookup"><span data-stu-id="227f7-127">d3d12downlevel.h and dxgi1_4.h</span></span> |
| <span data-ttu-id="227f7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="227f7-128">DLL</span></span>    | <span data-ttu-id="227f7-129">D3D12.dll (Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="227f7-129">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="227f7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="227f7-130">See also</span></span>
* [<span data-ttu-id="227f7-131">ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="227f7-131">ID3D12DeviceDownlevel</span></span>](id3d12devicedownlevel.md)
* [<span data-ttu-id="227f7-132">Interfaces Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="227f7-132">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="227f7-133">Informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="227f7-133">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="227f7-134">Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="227f7-134">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
