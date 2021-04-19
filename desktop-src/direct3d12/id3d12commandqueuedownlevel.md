---
title: Interface ID3D12CommandQueueDownlevel
description: Fournit un mécanisme présent spécifique à Windows 7.
keywords:
- Interface ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531520"
---
# <a name="id3d12commandqueuedownlevel-interface"></a><span data-ttu-id="5a511-104">Interface ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="5a511-104">ID3D12CommandQueueDownlevel interface</span></span>

<span data-ttu-id="5a511-105">Cette interface est accessible via **QueryInterface** à partir d’une [file d’attente de commandes Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) lors de l’utilisation [de Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="5a511-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 command queue](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="5a511-106">Il fournit un mécanisme présent spécifique à Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a511-106">It provides a Windows-7-specific present mechanism.</span></span>

### <a name="methods"></a><span data-ttu-id="5a511-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a511-107">Methods</span></span>

<span data-ttu-id="5a511-108">L’interface **ID3D12CommandQueueDownlevel** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5a511-108">The **ID3D12CommandQueueDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="5a511-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="5a511-109">Method</span></span> | <span data-ttu-id="5a511-110">Description</span><span class="sxs-lookup"><span data-stu-id="5a511-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="5a511-111">**Présent**</span><span class="sxs-lookup"><span data-stu-id="5a511-111">**Present**</span></span>](id3d12commandqueuedownlevel-present.md) | <span data-ttu-id="5a511-112">Copie le contenu d’une ressource D3D12 Texture2D dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5a511-112">Copies contents from a D3D12 Texture2D resource into a window.</span></span> |

## <a name="requirements"></a><span data-ttu-id="5a511-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a511-113">Requirements</span></span>

| <span data-ttu-id="5a511-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a511-114">Requirement</span></span> | <span data-ttu-id="5a511-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a511-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="5a511-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a511-116">Header</span></span> | <span data-ttu-id="5a511-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="5a511-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="5a511-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5a511-118">DLL</span></span>    | <span data-ttu-id="5a511-119">D3D12.dll (Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="5a511-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5a511-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a511-120">See also</span></span>
* [<span data-ttu-id="5a511-121">Interfaces Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="5a511-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="5a511-122">Informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="5a511-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="5a511-123">Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="5a511-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
