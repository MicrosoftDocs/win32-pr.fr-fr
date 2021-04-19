---
title: D3D12DecomposeSubresource, fonction (D3dx12.h)
description: Affiche la tranche MIP, le segment de tableau et la tranche de plan correspondant à l’index de sous-ressource spécifié.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource fonction)
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545263"
---
# <a name="d3d12decomposesubresource-function"></a><span data-ttu-id="82ec1-104">D3D12DecomposeSubresource fonction)</span><span class="sxs-lookup"><span data-stu-id="82ec1-104">D3D12DecomposeSubresource function</span></span>

<span data-ttu-id="82ec1-105">Affiche la tranche MIP, le segment de tableau et la tranche de plan correspondant à l’index de sous-ressource spécifié.</span><span class="sxs-lookup"><span data-stu-id="82ec1-105">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ec1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82ec1-106">Syntax</span></span>


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a><span data-ttu-id="82ec1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82ec1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ec1-108">*Sous-ressource*</span><span class="sxs-lookup"><span data-stu-id="82ec1-108">*Subresource*</span></span> 
</dt> <dd>

<span data-ttu-id="82ec1-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="82ec1-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="82ec1-110">Index de la sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="82ec1-110">The index of the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="82ec1-111">*Miplevels a*</span><span class="sxs-lookup"><span data-stu-id="82ec1-111">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="82ec1-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="82ec1-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="82ec1-113">Nombre maximal de niveaux de mipmap dans la sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="82ec1-113">The maximum number of mipmap levels in the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="82ec1-114">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="82ec1-114">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="82ec1-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="82ec1-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="82ec1-116">Nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="82ec1-116">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="82ec1-117">*MipSlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="82ec1-117">*MipSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="82ec1-118">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="82ec1-118">Type: **T**</span></span>

<span data-ttu-id="82ec1-119">Génère une sortie de la tranche MIP qui correspond à l’index de sous-ressource donné.</span><span class="sxs-lookup"><span data-stu-id="82ec1-119">Outputs the mip slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="82ec1-120">*ArraySlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="82ec1-120">*ArraySlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="82ec1-121">Type : **U**</span><span class="sxs-lookup"><span data-stu-id="82ec1-121">Type: **U**</span></span>

<span data-ttu-id="82ec1-122">Génère la sortie de la tranche de tableau qui correspond à l’index de sous-ressource donné.</span><span class="sxs-lookup"><span data-stu-id="82ec1-122">Outputs the array slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="82ec1-123">*PlaneSlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="82ec1-123">*PlaneSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="82ec1-124">Type : **V**</span><span class="sxs-lookup"><span data-stu-id="82ec1-124">Type: **V**</span></span>

<span data-ttu-id="82ec1-125">Génère la sortie de la tranche de plan qui correspond à l’index de sous-ressource donné.</span><span class="sxs-lookup"><span data-stu-id="82ec1-125">Outputs the plane slice that corresponds to the given subresource index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ec1-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82ec1-126">Return value</span></span>

<span data-ttu-id="82ec1-127">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="82ec1-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82ec1-128">Notes</span><span class="sxs-lookup"><span data-stu-id="82ec1-128">Remarks</span></span>

<span data-ttu-id="82ec1-129">Cette fonction détermine quelle tranche MIP, tranche de tableau et tranche de plan correspondent à un index de sous-ressources donné.</span><span class="sxs-lookup"><span data-stu-id="82ec1-129">This function determines which mip slice, array slice, and plane slice correspond to a given subresource index.</span></span> <span data-ttu-id="82ec1-130">Il s’agit d’un utilitaire utile, bien qu’il soit spécifique à C++.</span><span class="sxs-lookup"><span data-stu-id="82ec1-130">This is a useful utility, though it is C++ specific.</span></span>

<span data-ttu-id="82ec1-131">Cette fonction est déclarée comme suit, avec des paramètres de type C++ pour les types **T**, **U** et **V**:</span><span class="sxs-lookup"><span data-stu-id="82ec1-131">This function is declared as follows, with C++ templatized parameters for types **T**, **U**, and **V**:</span></span>


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a><span data-ttu-id="82ec1-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82ec1-132">Requirements</span></span>



| <span data-ttu-id="82ec1-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82ec1-133">Requirement</span></span> | <span data-ttu-id="82ec1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="82ec1-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82ec1-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="82ec1-135">Header</span></span><br/>  | <dl> <span data-ttu-id="82ec1-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="82ec1-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="82ec1-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="82ec1-137">Library</span></span><br/> | <dl> <span data-ttu-id="82ec1-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82ec1-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="82ec1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="82ec1-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="82ec1-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82ec1-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ec1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82ec1-141">See also</span></span>

[<span data-ttu-id="82ec1-142">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="82ec1-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)

[<span data-ttu-id="82ec1-143">Sous-ressources</span><span class="sxs-lookup"><span data-stu-id="82ec1-143">Subresources</span></span>](subresources.md)
