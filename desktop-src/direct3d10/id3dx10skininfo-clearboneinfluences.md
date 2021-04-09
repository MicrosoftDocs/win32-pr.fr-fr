---
description: Désactivez la liste des vertex d’un os qu’elle influence.
ms.assetid: 1ba6f43a-1f85-4057-b0ed-247cc38d4932
title: 'ID3DX10SkinInfo :: ClearBoneInfluences, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.ClearBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6f161ba400b684b12d6b0a091abb1fa452d476b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953860"
---
# <a name="id3dx10skininfoclearboneinfluences-method"></a><span data-ttu-id="4ce14-103">ID3DX10SkinInfo :: ClearBoneInfluences, méthode</span><span class="sxs-lookup"><span data-stu-id="4ce14-103">ID3DX10SkinInfo::ClearBoneInfluences method</span></span>

<span data-ttu-id="4ce14-104">Désactivez la liste des vertex d’un os qu’elle influence.</span><span class="sxs-lookup"><span data-stu-id="4ce14-104">Clear a bone's list of vertices that it influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce14-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ce14-105">Syntax</span></span>


```C++
HRESULT ClearBoneInfluences(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4ce14-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ce14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce14-107">*BoneIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ce14-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce14-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ce14-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ce14-109">Index qui spécifie un segment existant.</span><span class="sxs-lookup"><span data-stu-id="4ce14-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="4ce14-110">Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="4ce14-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce14-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ce14-111">Return value</span></span>

<span data-ttu-id="4ce14-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ce14-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ce14-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4ce14-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4ce14-114">Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="4ce14-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ce14-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ce14-115">Requirements</span></span>



| <span data-ttu-id="4ce14-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ce14-116">Requirement</span></span> | <span data-ttu-id="4ce14-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ce14-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce14-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ce14-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4ce14-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ce14-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ce14-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ce14-120">Library</span></span><br/> | <dl> <span data-ttu-id="4ce14-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ce14-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ce14-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ce14-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce14-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="4ce14-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="4ce14-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="4ce14-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
