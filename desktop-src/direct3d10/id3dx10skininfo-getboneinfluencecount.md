---
description: Obtient le nombre de vertex qu’un segment donné influence.
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: 'ID3DX10SkinInfo :: GetBoneInfluenceCount, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531542"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a><span data-ttu-id="b5d52-103">ID3DX10SkinInfo :: GetBoneInfluenceCount, méthode</span><span class="sxs-lookup"><span data-stu-id="b5d52-103">ID3DX10SkinInfo::GetBoneInfluenceCount method</span></span>

<span data-ttu-id="b5d52-104">Obtient le nombre de vertex qu’un segment donné influence.</span><span class="sxs-lookup"><span data-stu-id="b5d52-104">Get the number of vertices that a given bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d52-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5d52-105">Syntax</span></span>


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b5d52-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5d52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d52-107">*BoneIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5d52-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d52-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5d52-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5d52-109">Index qui spécifie un segment existant.</span><span class="sxs-lookup"><span data-stu-id="b5d52-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="b5d52-110">Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="b5d52-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d52-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5d52-111">Return value</span></span>

<span data-ttu-id="b5d52-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5d52-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5d52-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5d52-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b5d52-114">Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="b5d52-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d52-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5d52-115">Requirements</span></span>



| <span data-ttu-id="b5d52-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5d52-116">Requirement</span></span> | <span data-ttu-id="b5d52-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5d52-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d52-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5d52-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b5d52-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d52-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5d52-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5d52-120">Library</span></span><br/> | <dl> <span data-ttu-id="b5d52-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5d52-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d52-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5d52-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d52-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="b5d52-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="b5d52-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="b5d52-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
