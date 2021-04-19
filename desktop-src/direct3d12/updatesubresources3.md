---
title: Fonction Updatesubresources par (allocation de pile) (D3dx12. h)
description: Met à jour les sous-ressources avec une implémentation d’allocation de pile.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525869"
---
# <a name="updatesubresources-stack-allocating-function"></a><span data-ttu-id="71e71-104">Updatesubresources par (allocation de pile) (fonction)</span><span class="sxs-lookup"><span data-stu-id="71e71-104">UpdateSubresources (stack-allocating) function</span></span>

<span data-ttu-id="71e71-105">Met à jour les sous-ressources avec une implémentation d’allocation de pile.</span><span class="sxs-lookup"><span data-stu-id="71e71-105">Updates subresources with a stack-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e71-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71e71-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="71e71-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71e71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e71-108">*pCmdList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71e71-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e71-109">Type : **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="71e71-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="71e71-110">La liste de commandes, en tant que pointeur vers un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="71e71-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="71e71-111">*pDestinationResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71e71-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e71-112">Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="71e71-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="71e71-113">La ressource de destination, en tant que pointeur vers un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="71e71-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="71e71-114">*pIntermediate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71e71-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e71-115">Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="71e71-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="71e71-116">Ressource intermédiaire, en tant que pointeur vers un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="71e71-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="71e71-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="71e71-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="71e71-118">Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="71e71-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="71e71-119">Offset, en octets, de la ressource intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="71e71-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="71e71-120">*FirstSubresource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71e71-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e71-121">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="71e71-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="71e71-122">Index de la première sous-ressource dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="71e71-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="71e71-123">Les valeurs valides sont comprises entre 0 et *MaxSubresources*.</span><span class="sxs-lookup"><span data-stu-id="71e71-123">Valid values range from 0 to *MaxSubresources*.</span></span>

</dd> <dt>

<span data-ttu-id="71e71-124">*NumSubresources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71e71-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e71-125">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="71e71-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="71e71-126">Nombre de sous-ressources dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="71e71-126">The number of subresources in the resource.</span></span> <span data-ttu-id="71e71-127">Les valeurs valides sont comprises entre 1 et (*MaxSubresources*  -  *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="71e71-127">Valid values range from 1 to (*MaxSubresources* - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="71e71-128">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71e71-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e71-129">Type : données de sous- **[ **\_ ressource \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="71e71-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="71e71-130">Pointeur vers un tableau (de longueur *NumSubresources*) de pointeurs vers des structures de données de sous- [**\_ \_ ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenant les descriptions des données de sous-ressources utilisées pour la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71e71-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e71-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71e71-131">Return value</span></span>

<span data-ttu-id="71e71-132">Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="71e71-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="71e71-133">Taille en octets de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="71e71-133">The size, in bytes, of the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="71e71-134">Notes</span><span class="sxs-lookup"><span data-stu-id="71e71-134">Remarks</span></span>

<span data-ttu-id="71e71-135">La déclaration de cette fonction commence par : `template <UINT MaxSubresources>`</span><span class="sxs-lookup"><span data-stu-id="71e71-135">The declaration of this function begins with: `template <UINT MaxSubresources>`</span></span>

## <a name="requirements"></a><span data-ttu-id="71e71-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71e71-136">Requirements</span></span>



| <span data-ttu-id="71e71-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71e71-137">Requirement</span></span> | <span data-ttu-id="71e71-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="71e71-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="71e71-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="71e71-139">Header</span></span><br/>  | <dl> <span data-ttu-id="71e71-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="71e71-140"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="71e71-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71e71-141">Library</span></span><br/> | <dl> <span data-ttu-id="71e71-142"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71e71-142"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="71e71-143">DLL</span><span class="sxs-lookup"><span data-stu-id="71e71-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="71e71-144"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71e71-144"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e71-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71e71-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e71-146">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="71e71-146">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="71e71-147">Sous-ressources</span><span class="sxs-lookup"><span data-stu-id="71e71-147">Subresources</span></span>](subresources.md)
</dt> </dl>

 

