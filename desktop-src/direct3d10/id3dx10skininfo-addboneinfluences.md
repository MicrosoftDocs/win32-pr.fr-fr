---
description: Activez un segment existant pour influencer un groupe de vertex et définissez l’influence du segment sur chaque vertex.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'ID3DX10SkinInfo :: AddBoneInfluences, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211778"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a><span data-ttu-id="e53e5-103">ID3DX10SkinInfo :: AddBoneInfluences, méthode</span><span class="sxs-lookup"><span data-stu-id="e53e5-103">ID3DX10SkinInfo::AddBoneInfluences method</span></span>

<span data-ttu-id="e53e5-104">Activez un segment existant pour influencer un groupe de vertex et définissez l’influence du segment sur chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="e53e5-104">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e53e5-105">Syntax</span></span>


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="e53e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e53e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e53e5-107">*BoneIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e53e5-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e53e5-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e53e5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e53e5-109">Index qui spécifie un segment existant.</span><span class="sxs-lookup"><span data-stu-id="e53e5-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="e53e5-110">Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="e53e5-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="e53e5-111">*InfluenceCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e53e5-111">*InfluenceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e53e5-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e53e5-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e53e5-113">Nombre de vertex à ajouter à l’influence du segment.</span><span class="sxs-lookup"><span data-stu-id="e53e5-113">Number of vertices to add to the bone's influence.</span></span>

</dd> <dt>

<span data-ttu-id="e53e5-114">*pIndices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e53e5-114">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e53e5-115">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e53e5-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e53e5-116">Pointeur vers un tableau d’index de vertex.</span><span class="sxs-lookup"><span data-stu-id="e53e5-116">Pointer to an array of vertex indices.</span></span> <span data-ttu-id="e53e5-117">Chaque membre de ce tableau a un membre correspondant dans pWeights, de sorte que pIndices \[ i \] correspond à pWeights \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="e53e5-117">Each member of this array has a corresponding member in pWeights, such that pIndices\[i\] corresponds to pWeights\[i\].</span></span> <span data-ttu-id="e53e5-118">La valeur correspondante dans pWeights \[ i \] détermine la quantité d’influence que BoneIndex aura sur le vertex indexé par pIndices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="e53e5-118">The corresponding value in pWeights\[i\] determines how much influence BoneIndex will have on the vertex indexed by pIndices\[i\].</span></span> <span data-ttu-id="e53e5-119">La taille du tableau pIndices doit être supérieure ou égale à InfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="e53e5-119">The size of the pIndices array must be equal to or greater than InfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="e53e5-120">*pWeights* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e53e5-120">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e53e5-121">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="e53e5-121">Type: **float\***</span></span>

<span data-ttu-id="e53e5-122">Pointeur vers un tableau de poids osseux.</span><span class="sxs-lookup"><span data-stu-id="e53e5-122">Pointer to an array of bone weights.</span></span> <span data-ttu-id="e53e5-123">Chaque membre de ce tableau a un membre correspondant dans pIndices, de sorte que pWeights \[ i \] correspond à pIndices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="e53e5-123">Each member of this array has a corresponding member in pIndices, such that pWeights\[i\] corresponds to pIndices\[i\].</span></span> <span data-ttu-id="e53e5-124">Chaque valeur de pWeights est comprise entre 0 et 1 et définit la quantité d’influence du segment sur chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="e53e5-124">Each value in pWeights is between 0 and 1 and defines the amount of influence the bone has over each vertex.</span></span> <span data-ttu-id="e53e5-125">La taille de pWeights doit être supérieure ou égale à InfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="e53e5-125">The size of pWeights must be equal to or greater than InfluenceCount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e53e5-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e53e5-126">Return value</span></span>

<span data-ttu-id="e53e5-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e53e5-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e53e5-128">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e53e5-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e53e5-129">Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG ou e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e53e5-129">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53e5-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e53e5-130">Requirements</span></span>



| <span data-ttu-id="e53e5-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e53e5-131">Requirement</span></span> | <span data-ttu-id="e53e5-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e53e5-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e53e5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="e53e5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e53e5-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e53e5-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e53e5-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e53e5-135">Library</span></span><br/> | <dl> <span data-ttu-id="e53e5-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e53e5-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e53e5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e53e5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53e5-138">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="e53e5-138">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="e53e5-139">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e53e5-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
