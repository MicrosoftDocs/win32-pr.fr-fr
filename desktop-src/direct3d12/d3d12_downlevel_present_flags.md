---
title: Énumération D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Indicateurs passés à la méthode ID3D12CommandQueueDownlevel ::P retournée.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532422"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a><span data-ttu-id="b06da-103">Énumération d’indicateurs D3D12 de \_ bas niveau \_ présente \_</span><span class="sxs-lookup"><span data-stu-id="b06da-103">D3D12\_DOWNLEVEL\_PRESENT\_FLAGS enumeration</span></span>

<span data-ttu-id="b06da-104">Indicateurs passés à la fonction [**ID3D12CommandQueueDownlevel ::P renvoyée**](id3d12commandqueuedownlevel-present.md) pour modifier le comportement.</span><span class="sxs-lookup"><span data-stu-id="b06da-104">Flags passed to the [**ID3D12CommandQueueDownlevel::Present**](id3d12commandqueuedownlevel-present.md) function to modify behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="b06da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b06da-105">Syntax</span></span>

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a><span data-ttu-id="b06da-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b06da-106">Constants</span></span>

<span data-ttu-id="b06da-107">**Indicateur de D3D12 de \_ niveau inférieur \_ absent \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b06da-107">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_NONE**</span></span>

<span data-ttu-id="b06da-108">Aucune option sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="b06da-108">No options selected.</span></span>

<span data-ttu-id="b06da-109">**\_ \_ Indicateur de présence de niveau inférieur D3D12 \_ \_ wait \_ pour \_ vblank**</span><span class="sxs-lookup"><span data-stu-id="b06da-109">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_WAIT\_FOR\_VBLANK**</span></span>

<span data-ttu-id="b06da-110">L’opération **actuelle** n’est pas effectuée tant qu’un Vsync n’a pas eu lieu depuis la dernière **Présentation** de Ed.</span><span class="sxs-lookup"><span data-stu-id="b06da-110">The **Present** operation won't be done until a VSync has occurred since the last time you **Present** ed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b06da-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b06da-111">Requirements</span></span>

| <span data-ttu-id="b06da-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b06da-112">Requirement</span></span> | <span data-ttu-id="b06da-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b06da-113">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="b06da-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="b06da-114">Header</span></span> | <span data-ttu-id="b06da-115">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="b06da-115">d3d12downlevel.h</span></span> |
| <span data-ttu-id="b06da-116">DLL</span><span class="sxs-lookup"><span data-stu-id="b06da-116">DLL</span></span>    | <span data-ttu-id="b06da-117">D3D12.dll (Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="b06da-117">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b06da-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b06da-118">See also</span></span>
* [<span data-ttu-id="b06da-119">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="b06da-119">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="b06da-120">Énumérations Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="b06da-120">Direct3D 12 On Windows 7 enumerations</span></span>](direct3d-12on7-enumerations.md)
* [<span data-ttu-id="b06da-121">Informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="b06da-121">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="b06da-122">Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="b06da-122">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
