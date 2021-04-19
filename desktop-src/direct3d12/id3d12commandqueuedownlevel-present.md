---
title: ID3D12CommandQueueDownlevel ::P méthode reenvoyé
description: Copie le contenu d’une ressource Direct3D 12 Texture2D dans une fenêtre. | ID3D12CommandQueueDownlevel ::P méthode reenvoyé
keywords:
- Present (méthode)
- Méthode présente, interface ID3D12CommandQueueDownlevel
- Interface ID3D12CommandQueueDownlevel, méthode présente
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522972"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a><span data-ttu-id="62ea6-107">ID3D12CommandQueueDownlevel ::P méthode reenvoyé</span><span class="sxs-lookup"><span data-stu-id="62ea6-107">ID3D12CommandQueueDownlevel::Present method</span></span>

<span data-ttu-id="62ea6-108">Copie le contenu d’une ressource Direct3D 12 Texture2D dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="62ea6-108">Copies contents from a Direct3D 12 Texture2D resource into a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ea6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62ea6-109">Syntax</span></span>

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a><span data-ttu-id="62ea6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62ea6-110">Parameters</span></span>

`pOpenCommandList`

<span data-ttu-id="62ea6-111">Type : **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="62ea6-111">Type: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="62ea6-112">Une liste de commandes ouverte, dans laquelle Direct3D 12 met en file d’attente une commande présente, puis ferme et envoie pour vous.</span><span class="sxs-lookup"><span data-stu-id="62ea6-112">An open command list, which Direct3D 12 enqueues a Present command onto, and then closes and submits for you.</span></span>

`pSourceTex2D`

<span data-ttu-id="62ea6-113">Type : **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="62ea6-113">Type: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="62ea6-114">Ressource contenant le contenu que vous souhaitez afficher, avec la [**\_ dimension D3D12 \_ ressource \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)dimension et un format qui est l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="62ea6-114">A resource containing your desired contents to display, with dimension [**D3D12\_RESOURCE\_DIMENSION\_TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), and a format that is one of the following.</span></span>

* <span data-ttu-id="62ea6-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span><span class="sxs-lookup"><span data-stu-id="62ea6-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span></span>
* <span data-ttu-id="62ea6-116">DXGI_FORMAT_R10G10B10A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="62ea6-116">DXGI_FORMAT_R10G10B10A2_UNORM</span></span>
* <span data-ttu-id="62ea6-117">DXGI_FORMAT_R8G8B8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="62ea6-117">DXGI_FORMAT_R8G8B8A8_UNORM</span></span>
* <span data-ttu-id="62ea6-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="62ea6-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span></span>
* <span data-ttu-id="62ea6-119">DXGI_FORMAT_B8G8R8X8_UNORM</span><span class="sxs-lookup"><span data-stu-id="62ea6-119">DXGI_FORMAT_B8G8R8X8_UNORM</span></span>
* <span data-ttu-id="62ea6-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="62ea6-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span></span>
* <span data-ttu-id="62ea6-121">DXGI_FORMAT_B8G8R8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="62ea6-121">DXGI_FORMAT_B8G8R8A8_UNORM</span></span>
* <span data-ttu-id="62ea6-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="62ea6-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span></span>

`hWindow`

<span data-ttu-id="62ea6-123">Type : **[HWND](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62ea6-123">Type: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62ea6-124">Handle de la fenêtre dans laquelle le contenu doit être affiché.</span><span class="sxs-lookup"><span data-stu-id="62ea6-124">The handle to the window where the contents should be displayed.</span></span>

`Flags`

<span data-ttu-id="62ea6-125">Type : **[ \_ indicateurs de \_ présence \_ de niveau inférieur D3D12](d3d12_downlevel_present_flags.md)**</span><span class="sxs-lookup"><span data-stu-id="62ea6-125">Type: **[D3D12\_DOWNLEVEL\_PRESENT\_FLAGS](d3d12_downlevel_present_flags.md)**</span></span>

<span data-ttu-id="62ea6-126">Indicateurs permettant de modifier l’opération **présente** .</span><span class="sxs-lookup"><span data-stu-id="62ea6-126">Flags to modify the **Present** operation.</span></span>

## <a name="return-value"></a><span data-ttu-id="62ea6-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62ea6-127">Return value</span></span>

<span data-ttu-id="62ea6-128">Retourne **S_OK** en cas de réussite, ou un HRESULT qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="62ea6-128">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ea6-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62ea6-129">Requirements</span></span>

| <span data-ttu-id="62ea6-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62ea6-130">Requirement</span></span> | <span data-ttu-id="62ea6-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="62ea6-131">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="62ea6-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="62ea6-132">Header</span></span> | <span data-ttu-id="62ea6-133">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="62ea6-133">d3d12downlevel.h</span></span> |
| <span data-ttu-id="62ea6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="62ea6-134">DLL</span></span>    | <span data-ttu-id="62ea6-135">D3D12.dll (Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="62ea6-135">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="62ea6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62ea6-136">See also</span></span>
* [<span data-ttu-id="62ea6-137">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="62ea6-137">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="62ea6-138">Interfaces Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="62ea6-138">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="62ea6-139">Informations de référence sur Direct3D 12 sur Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="62ea6-139">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="62ea6-140">Direct3D 12 sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="62ea6-140">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
