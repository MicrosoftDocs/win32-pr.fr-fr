---
description: Recherche l’index qui indique où un vertex donné figure dans la liste des vertex influencés d’un segment donné.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'ID3DX10SkinInfo :: FindBoneInfluenceIndex, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211855"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a><span data-ttu-id="d4fc5-103">ID3DX10SkinInfo :: FindBoneInfluenceIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="d4fc5-103">ID3DX10SkinInfo::FindBoneInfluenceIndex method</span></span>

<span data-ttu-id="d4fc5-104">Recherche l’index qui indique où un vertex donné figure dans la liste des vertex influencés d’un segment donné.</span><span class="sxs-lookup"><span data-stu-id="d4fc5-104">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4fc5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4fc5-105">Syntax</span></span>


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="d4fc5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4fc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4fc5-107">*BoneIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4fc5-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4fc5-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4fc5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4fc5-109">Index qui spécifie un segment existant.</span><span class="sxs-lookup"><span data-stu-id="d4fc5-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="d4fc5-110">Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="d4fc5-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4fc5-111">*VertexIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4fc5-111">*VertexIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4fc5-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4fc5-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4fc5-113">Index du vertex dans la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="d4fc5-113">The index of the vertex in the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d4fc5-114">*pInfluenceIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4fc5-114">*pInfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4fc5-115">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4fc5-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d4fc5-116">Index du vertex dans la liste des segments influencés.</span><span class="sxs-lookup"><span data-stu-id="d4fc5-116">The index of the vertex in the bone's list of influenced vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4fc5-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4fc5-117">Return value</span></span>

<span data-ttu-id="d4fc5-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4fc5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4fc5-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4fc5-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4fc5-120">Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d4fc5-120">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4fc5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4fc5-121">Requirements</span></span>



| <span data-ttu-id="d4fc5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4fc5-122">Requirement</span></span> | <span data-ttu-id="d4fc5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4fc5-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4fc5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4fc5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d4fc5-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4fc5-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4fc5-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4fc5-126">Library</span></span><br/> | <dl> <span data-ttu-id="d4fc5-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4fc5-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4fc5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4fc5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4fc5-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="d4fc5-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="d4fc5-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d4fc5-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
