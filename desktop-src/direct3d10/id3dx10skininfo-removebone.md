---
description: Supprimer un segment.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: 'ID3DX10SkinInfo :: RemoveBone, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 49fd24c5661bbedb7fb839171fa4a835f07e446a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535177"
---
# <a name="id3dx10skininforemovebone-method"></a><span data-ttu-id="9ea20-103">ID3DX10SkinInfo :: RemoveBone, méthode</span><span class="sxs-lookup"><span data-stu-id="9ea20-103">ID3DX10SkinInfo::RemoveBone method</span></span>

<span data-ttu-id="9ea20-104">Supprimer un segment.</span><span class="sxs-lookup"><span data-stu-id="9ea20-104">Remove a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ea20-105">Syntax</span></span>


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="9ea20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ea20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ea20-107">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ea20-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ea20-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ea20-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ea20-109">Index qui spécifie le segment à supprimer.</span><span class="sxs-lookup"><span data-stu-id="9ea20-109">An index that specifies which bone to remove.</span></span> <span data-ttu-id="9ea20-110">Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="9ea20-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ea20-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ea20-111">Return value</span></span>

<span data-ttu-id="9ea20-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ea20-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ea20-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9ea20-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9ea20-114">Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="9ea20-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea20-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ea20-115">Requirements</span></span>



| <span data-ttu-id="9ea20-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ea20-116">Requirement</span></span> | <span data-ttu-id="9ea20-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ea20-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea20-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ea20-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9ea20-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ea20-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ea20-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ea20-120">Library</span></span><br/> | <dl> <span data-ttu-id="9ea20-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ea20-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ea20-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ea20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea20-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="9ea20-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="9ea20-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="9ea20-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
