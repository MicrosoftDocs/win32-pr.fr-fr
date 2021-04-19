---
title: Interface ID3D12DeviceDownlevel
description: Fournit une requête de statistiques de mémoire spécifique à Windows 7.
keywords:
- Interface ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525854"
---
# <a name="id3d12devicedownlevel-interface"></a><span data-ttu-id="95fbc-104">Interface ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="95fbc-104">ID3D12DeviceDownlevel interface</span></span>

<span data-ttu-id="95fbc-105">Cette interface est accessible via **QueryInterface** sur un [appareil Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) lors de l’utilisation de [Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="95fbc-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="95fbc-106">Il fournit une requête de statistiques de mémoire spécifique à Windows 7.</span><span class="sxs-lookup"><span data-stu-id="95fbc-106">It provides a Windows-7-specific memory statistics query.</span></span>

### <a name="methods"></a><span data-ttu-id="95fbc-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="95fbc-107">Methods</span></span>

<span data-ttu-id="95fbc-108">L’interface **ID3D12DeviceDownlevel** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="95fbc-108">The **ID3D12DeviceDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="95fbc-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="95fbc-109">Method</span></span> | <span data-ttu-id="95fbc-110">Description</span><span class="sxs-lookup"><span data-stu-id="95fbc-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="95fbc-111">**QueryVideoMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="95fbc-111">**QueryVideoMemoryInfo**</span></span>](id3d12devicedownlevel-queryvideomemoryinfo.md) | <span data-ttu-id="95fbc-112">Fournit des statistiques de mémoire sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="95fbc-112">Provides memory statistics on Windows 7.</span></span> |

## <a name="requirements"></a><span data-ttu-id="95fbc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95fbc-113">Requirements</span></span>

| <span data-ttu-id="95fbc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95fbc-114">Requirement</span></span> | <span data-ttu-id="95fbc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="95fbc-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="95fbc-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="95fbc-116">Header</span></span> | <span data-ttu-id="95fbc-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="95fbc-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="95fbc-118">DLL</span><span class="sxs-lookup"><span data-stu-id="95fbc-118">DLL</span></span>    | <span data-ttu-id="95fbc-119">D3D12.dll (Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="95fbc-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="95fbc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95fbc-120">See also</span></span>
* [<span data-ttu-id="95fbc-121">Interfaces Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="95fbc-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="95fbc-122">Informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="95fbc-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="95fbc-123">Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="95fbc-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
