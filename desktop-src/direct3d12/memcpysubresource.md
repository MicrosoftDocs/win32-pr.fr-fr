---
title: MemcpySubresource, fonction (D3dx12. h)
description: Copie une sous-ressource ligne par ligne.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- MemcpySubresource fonction)
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545296"
---
# <a name="memcpysubresource-function"></a><span data-ttu-id="f618a-104">MemcpySubresource fonction)</span><span class="sxs-lookup"><span data-stu-id="f618a-104">MemcpySubresource function</span></span>

<span data-ttu-id="f618a-105">Copie une sous-ressource ligne par ligne.</span><span class="sxs-lookup"><span data-stu-id="f618a-105">Copies a subresource row by row.</span></span>

## <a name="syntax"></a><span data-ttu-id="f618a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f618a-106">Syntax</span></span>


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a><span data-ttu-id="f618a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f618a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f618a-108">*pDEST* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f618a-108">*pDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f618a-109">Type : **const [**D3D12 \_ MEMCPY \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***</span><span class="sxs-lookup"><span data-stu-id="f618a-109">Type: **const [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)\***</span></span>

<span data-ttu-id="f618a-110">Pointeur vers une structure [**de \_ \_ dest D3D12 MEMCPY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) qui décrit la destination de l’opération de copie de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f618a-110">A pointer to a [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) structure that describes the destination of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="f618a-111">*pSrc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f618a-111">*pSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f618a-112">Type : **const [**D3D12 les \_ \_ données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \*** de sous-ressource</span><span class="sxs-lookup"><span data-stu-id="f618a-112">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="f618a-113">Pointeur vers une structure [**de \_ \_ données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) de sous-ressource D3D12 qui décrit la source de l’opération de copie de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f618a-113">A pointer to a [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structure that describes the source of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="f618a-114">*RowSizeInBytes*</span><span class="sxs-lookup"><span data-stu-id="f618a-114">*RowSizeInBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="f618a-115">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f618a-115">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f618a-116">Taille, en octets, de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="f618a-116">The size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="f618a-117">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="f618a-117">*NumRows*</span></span> 
</dt> <dd>

<span data-ttu-id="f618a-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f618a-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f618a-119">Nombre de lignes.</span><span class="sxs-lookup"><span data-stu-id="f618a-119">The number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="f618a-120">*NumSlices*</span><span class="sxs-lookup"><span data-stu-id="f618a-120">*NumSlices*</span></span> 
</dt> <dd>

<span data-ttu-id="f618a-121">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f618a-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f618a-122">Nombre de secteurs.</span><span class="sxs-lookup"><span data-stu-id="f618a-122">The number of slices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f618a-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f618a-123">Return value</span></span>

<span data-ttu-id="f618a-124">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f618a-124">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f618a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f618a-125">Remarks</span></span>

<span data-ttu-id="f618a-126">Prenez également en compte les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f618a-126">Also consider the following methods:</span></span>

-   [<span data-ttu-id="f618a-127">**ID3D12Resource::WriteToSubresource**</span><span class="sxs-lookup"><span data-stu-id="f618a-127">**ID3D12Resource::WriteToSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [<span data-ttu-id="f618a-128">**ID3D12Resource::ReadFromSubresource**</span><span class="sxs-lookup"><span data-stu-id="f618a-128">**ID3D12Resource::ReadFromSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [<span data-ttu-id="f618a-129">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="f618a-129">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a><span data-ttu-id="f618a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f618a-130">Requirements</span></span>



| <span data-ttu-id="f618a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f618a-131">Requirement</span></span> | <span data-ttu-id="f618a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f618a-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f618a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="f618a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="f618a-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f618a-134"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f618a-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f618a-135">Library</span></span><br/> | <dl> <span data-ttu-id="f618a-136"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f618a-136"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f618a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f618a-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="f618a-138"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f618a-138"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f618a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f618a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f618a-140">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="f618a-140">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f618a-141">Sous-ressources</span><span class="sxs-lookup"><span data-stu-id="f618a-141">Subresources</span></span>](subresources.md)
</dt> </dl>

 

