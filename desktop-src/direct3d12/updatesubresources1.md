---
title: Updatesubresources par, fonction (D3dx12. h)
description: Met à jour les sous-ressources, tous les tableaux de sous-ressources doivent être remplis, en général en appelant ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- Updatesubresources par fonction)
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525302"
---
# <a name="updatesubresources-function"></a><span data-ttu-id="0bced-104">Updatesubresources par fonction)</span><span class="sxs-lookup"><span data-stu-id="0bced-104">UpdateSubresources function</span></span>

<span data-ttu-id="0bced-105">Met à jour les sous-ressources, tous les tableaux de sous-ressources doivent être remplis, en général en appelant [**ID3D12Device :: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="0bced-105">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span>

## <a name="syntax"></a><span data-ttu-id="0bced-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bced-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="0bced-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bced-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bced-108">*pCmdList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-109">Type : **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="0bced-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="0bced-110">La liste de commandes, en tant que pointeur vers un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="0bced-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="0bced-111">*pDestinationResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-112">Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="0bced-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="0bced-113">La ressource de destination, en tant que pointeur vers un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="0bced-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="0bced-114">*pIntermediate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-115">Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="0bced-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="0bced-116">Ressource intermédiaire, en tant que pointeur vers un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="0bced-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="0bced-117">*FirstSubresource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-117">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0bced-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0bced-119">Index de la première sous-ressource dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="0bced-119">The index of the first subresource in the resource.</span></span> <span data-ttu-id="0bced-120">La plage de valeurs valides est comprise entre 0 et des sous- \_ ressources D3D12 req \_ .</span><span class="sxs-lookup"><span data-stu-id="0bced-120">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="0bced-121">*NumSubresources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-121">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-122">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0bced-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0bced-123">Nombre de sous-ressources dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="0bced-123">The number of subresources in the resource.</span></span> <span data-ttu-id="0bced-124">La plage de valeurs valides est comprise entre 0 et (D3D12 \_ req \_ Resources- *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="0bced-124">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="0bced-125">*RequiredSize*</span><span class="sxs-lookup"><span data-stu-id="0bced-125">*RequiredSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0bced-126">Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0bced-126">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0bced-127">Taille requise, en octets, de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0bced-127">The required size, in bytes, for the update.</span></span>

</dd> <dt>

<span data-ttu-id="0bced-128">*pLayouts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-128">*pLayouts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-129">Type : **const [**D3D12 a \_ placé l' \_ \_ encombrement**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) \*** des sous-ressources</span><span class="sxs-lookup"><span data-stu-id="0bced-129">Type: **const [**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)\***</span></span>

<span data-ttu-id="0bced-130">Pointeur vers un tableau (de longueur *NumSubresources*) de pointeurs vers les structures qui contiennent la description et le placement des sous-ressources de la ressource.</span><span class="sxs-lookup"><span data-stu-id="0bced-130">Pointer to an array (of length *NumSubresources*) of pointers to the structures that contains the description and placement of the resource's subresources.</span></span>

</dd> <dt>

<span data-ttu-id="0bced-131">*pNumRows* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-131">*pNumRows* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-132">Type : **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="0bced-132">Type: **const [**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="0bced-133">Pointeur vers un tableau (de longueur *NumSubresources*) de Uints contenant le nombre de lignes pour chaque sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="0bced-133">Pointer to an array (of length *NumSubresources*) of UINTS containing the number of rows for each subresource.</span></span>

</dd> <dt>

<span data-ttu-id="0bced-134">*pRowSizesInBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-134">*pRowSizesInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-135">Type : **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="0bced-135">Type: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="0bced-136">Pointeur vers un tableau (de longueur *NumSubresources*) de uint qui contient la taille, en octets, de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="0bced-136">Pointer to an array (of length *NumSubresources*) of UINTS containing the size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="0bced-137">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bced-137">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bced-138">Type : **const [**D3D12 les \_ \_ données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \*** de sous-ressource</span><span class="sxs-lookup"><span data-stu-id="0bced-138">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="0bced-139">Pointeur vers un tableau (de longueur *NumSubresources*) de pointeurs vers des structures de données de sous- [**\_ \_ ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenant les descriptions des données de sous-ressources utilisées pour la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0bced-139">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bced-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bced-140">Return value</span></span>

<span data-ttu-id="0bced-141">Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0bced-141">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0bced-142">Taille en octets de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0bced-142">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bced-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bced-143">Requirements</span></span>



| <span data-ttu-id="0bced-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bced-144">Requirement</span></span> | <span data-ttu-id="0bced-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bced-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bced-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bced-146">Header</span></span><br/>  | <dl> <span data-ttu-id="0bced-147"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bced-147"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="0bced-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bced-148">Library</span></span><br/> | <dl> <span data-ttu-id="0bced-149"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bced-149"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="0bced-150">DLL</span><span class="sxs-lookup"><span data-stu-id="0bced-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="0bced-151"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bced-151"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bced-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bced-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bced-153">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="0bced-153">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0bced-154">Sous-ressources</span><span class="sxs-lookup"><span data-stu-id="0bced-154">Subresources</span></span>](subresources.md)
</dt> </dl>

 

