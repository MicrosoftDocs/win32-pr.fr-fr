---
title: D3D12CalcSubresource, fonction (D3dx12. h)
description: Calcule un index de sous-ressource pour une texture.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource fonction)
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538491"
---
# <a name="d3d12calcsubresource-function"></a><span data-ttu-id="ec85a-104">D3D12CalcSubresource fonction)</span><span class="sxs-lookup"><span data-stu-id="ec85a-104">D3D12CalcSubresource function</span></span>

<span data-ttu-id="ec85a-105">Calcule un index de sous-ressource pour une texture.</span><span class="sxs-lookup"><span data-stu-id="ec85a-105">Calculates a subresource index for a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec85a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec85a-106">Syntax</span></span>


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="ec85a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec85a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec85a-108">*MipSlice*</span><span class="sxs-lookup"><span data-stu-id="ec85a-108">*MipSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="ec85a-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ec85a-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ec85a-110">Index de base zéro pour le niveau de mipmap à traiter ; 0 indique le premier niveau de mipmap, le plus détaillé.</span><span class="sxs-lookup"><span data-stu-id="ec85a-110">The zero-based index for the mipmap level to address; 0 indicates the first, most detailed mipmap level.</span></span>

</dd> <dt>

<span data-ttu-id="ec85a-111">*ArraySlice*</span><span class="sxs-lookup"><span data-stu-id="ec85a-111">*ArraySlice*</span></span> 
</dt> <dd>

<span data-ttu-id="ec85a-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ec85a-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ec85a-113">Index de base zéro pour le niveau de tableau à traiter ; Utilisez toujours 0 pour les textures de volume (3D).</span><span class="sxs-lookup"><span data-stu-id="ec85a-113">The zero-based index for the array level to address; always use 0 for volume (3D) textures.</span></span>

</dd> <dt>

<span data-ttu-id="ec85a-114">*PlaneSlice*</span><span class="sxs-lookup"><span data-stu-id="ec85a-114">*PlaneSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="ec85a-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ec85a-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ec85a-116">Index de base zéro pour le niveau de plan à traiter.</span><span class="sxs-lookup"><span data-stu-id="ec85a-116">The zero-based index for the plane level to address.</span></span>

</dd> <dt>

<span data-ttu-id="ec85a-117">*Miplevels a*</span><span class="sxs-lookup"><span data-stu-id="ec85a-117">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="ec85a-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ec85a-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ec85a-119">Nombre de niveaux de mipmap dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="ec85a-119">The number of mipmap levels in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ec85a-120">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="ec85a-120">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="ec85a-121">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ec85a-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ec85a-122">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ec85a-122">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec85a-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec85a-123">Return value</span></span>

<span data-ttu-id="ec85a-124">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ec85a-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ec85a-125">Index qui est égal à MipSlice + (ArraySlice \* miplevels a).</span><span class="sxs-lookup"><span data-stu-id="ec85a-125">The index which equals MipSlice + (ArraySlice \* MipLevels).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec85a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="ec85a-126">Remarks</span></span>

<span data-ttu-id="ec85a-127">Une mémoire tampon est une ressource non structurée et est donc définie comme contenant une seule sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="ec85a-127">A buffer is an unstructured resource and is therefore defined as containing a single subresource.</span></span> <span data-ttu-id="ec85a-128">Les API qui prennent des mémoires tampons n’ont pas besoin d’un index de sous-ressources.</span><span class="sxs-lookup"><span data-stu-id="ec85a-128">APIs that take buffers do not need a subresource index.</span></span> <span data-ttu-id="ec85a-129">Une texture en revanche est très structurée.</span><span class="sxs-lookup"><span data-stu-id="ec85a-129">A texture on the other hand is highly structured.</span></span> <span data-ttu-id="ec85a-130">Chaque objet texture peut contenir une ou plusieurs sous-ressources en fonction de la taille du tableau et du nombre de niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="ec85a-130">Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.</span></span>

<span data-ttu-id="ec85a-131">Pour les textures de volume (3D), toutes les tranches d’un niveau de mipmap donné sont un index de sous-ressource unique.</span><span class="sxs-lookup"><span data-stu-id="ec85a-131">For volume (3D) textures, all slices for a given mipmap level are a single subresource index.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec85a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec85a-132">Requirements</span></span>



| <span data-ttu-id="ec85a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec85a-133">Requirement</span></span> | <span data-ttu-id="ec85a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec85a-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ec85a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec85a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ec85a-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec85a-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ec85a-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ec85a-137">Library</span></span><br/> | <dl> <span data-ttu-id="ec85a-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec85a-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ec85a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ec85a-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="ec85a-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec85a-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec85a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec85a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec85a-142">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="ec85a-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ec85a-143">Sous-ressources</span><span class="sxs-lookup"><span data-stu-id="ec85a-143">Subresources</span></span>](subresources.md)
</dt> </dl>

 

