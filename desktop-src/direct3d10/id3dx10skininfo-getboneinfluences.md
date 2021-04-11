---
description: Obtient la liste des vertex qu’un segment donné influence et une liste de la quantité d’influence que l’OS a sur chaque vertex.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'ID3DX10SkinInfo :: GetBoneInfluences, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211956"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a><span data-ttu-id="805a3-103">ID3DX10SkinInfo :: GetBoneInfluences, méthode</span><span class="sxs-lookup"><span data-stu-id="805a3-103">ID3DX10SkinInfo::GetBoneInfluences method</span></span>

<span data-ttu-id="805a3-104">Obtient la liste des vertex qu’un segment donné influence et une liste de la quantité d’influence que l’OS a sur chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="805a3-104">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="805a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="805a3-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a><span data-ttu-id="805a3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805a3-107">*BoneIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="805a3-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805a3-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="805a3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="805a3-109">Index qui spécifie un segment existant.</span><span class="sxs-lookup"><span data-stu-id="805a3-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="805a3-110">Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="805a3-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="805a3-111">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="805a3-111">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805a3-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="805a3-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="805a3-113">Décalage à partir du haut de la liste des vertex influencés par le segment.</span><span class="sxs-lookup"><span data-stu-id="805a3-113">An offset from the top of the bone's list of influenced vertices.</span></span> <span data-ttu-id="805a3-114">Elle doit être comprise entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span><span class="sxs-lookup"><span data-stu-id="805a3-114">This must be between 0 and the value returned by [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span></span>

</dd> <dt>

<span data-ttu-id="805a3-115">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="805a3-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805a3-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="805a3-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="805a3-117">Nombre d’index et de poids à récupérer.</span><span class="sxs-lookup"><span data-stu-id="805a3-117">The number of indices and weights to retrieve.</span></span> <span data-ttu-id="805a3-118">Doit être compris entre 0 et la valeur retournée par ID3DX10SkinInfo :: GetBoneInfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="805a3-118">Must be between 0 and the value returned by ID3DX10SkinInfo::GetBoneInfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="805a3-119">*pDestIndices* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="805a3-119">*pDestIndices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="805a3-120">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="805a3-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="805a3-121">Liste d’index dans la mémoire tampon de vertex, chacun représentant un vertex influencé par le segment.</span><span class="sxs-lookup"><span data-stu-id="805a3-121">A list of indices into the vertex buffer, each one representing a vertex influenced by the bone.</span></span> <span data-ttu-id="805a3-122">Ces valeurs correspondent aux valeurs de pDestWeights, de sorte que pDestIndices \[ i \] correspond à pDestWeights \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="805a3-122">These values correspond to the values in pDestWeights, such that pDestIndices\[i\] corresponds to pDestWeights\[i\].</span></span>

</dd> <dt>

<span data-ttu-id="805a3-123">*pDestWeights* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="805a3-123">*pDestWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="805a3-124">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="805a3-124">Type: **float\***</span></span>

<span data-ttu-id="805a3-125">Liste de la quantité d’influence du segment sur chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="805a3-125">A list of the amount of influence the bone has on each vertex.</span></span> <span data-ttu-id="805a3-126">Ces valeurs correspondent aux valeurs dans pDestIndices, de sorte que pDestWeights \[ i \] correspond à pDestIndices \[ i \] . f</span><span class="sxs-lookup"><span data-stu-id="805a3-126">These values correspond to the values in pDestIndices, such that pDestWeights\[i\] corresponds to pDestIndices\[i\].f</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="805a3-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="805a3-127">Return value</span></span>

<span data-ttu-id="805a3-128">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="805a3-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="805a3-129">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="805a3-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="805a3-130">Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG ou e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="805a3-130">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="805a3-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="805a3-131">Requirements</span></span>



| <span data-ttu-id="805a3-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="805a3-132">Requirement</span></span> | <span data-ttu-id="805a3-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="805a3-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="805a3-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="805a3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="805a3-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="805a3-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="805a3-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="805a3-136">Library</span></span><br/> | <dl> <span data-ttu-id="805a3-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="805a3-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805a3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="805a3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805a3-139">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="805a3-139">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="805a3-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="805a3-140">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
