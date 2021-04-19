---
description: Obtient le nom d’une animation, en fonction de son index.
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: 'ID3DXAnimationSet :: GetAnimationNameByIndex, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 820b21fa69fd7007bdd1971e83ea44368dce5cc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527283"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a><span data-ttu-id="f99c0-103">ID3DXAnimationSet :: GetAnimationNameByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="f99c0-103">ID3DXAnimationSet::GetAnimationNameByIndex method</span></span>

<span data-ttu-id="f99c0-104">Obtient le nom d’une animation, en fonction de son index.</span><span class="sxs-lookup"><span data-stu-id="f99c0-104">Gets the name of an animation, given its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f99c0-105">Syntax</span></span>


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="f99c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f99c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f99c0-107">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f99c0-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99c0-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f99c0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f99c0-109">Index de l’animation.</span><span class="sxs-lookup"><span data-stu-id="f99c0-109">Index of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="f99c0-110">*ppName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f99c0-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f99c0-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f99c0-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f99c0-112">Adresse d’un pointeur vers une chaîne qui reçoit le nom de l’animation.</span><span class="sxs-lookup"><span data-stu-id="f99c0-112">Address of a pointer to a string that receives the animation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f99c0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f99c0-113">Return value</span></span>

<span data-ttu-id="f99c0-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f99c0-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f99c0-115">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="f99c0-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="f99c0-116">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f99c0-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="f99c0-117">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="f99c0-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f99c0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f99c0-118">Requirements</span></span>



| <span data-ttu-id="f99c0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f99c0-119">Requirement</span></span> | <span data-ttu-id="f99c0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f99c0-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f99c0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f99c0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f99c0-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f99c0-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f99c0-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f99c0-123">Library</span></span><br/> | <dl> <span data-ttu-id="f99c0-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f99c0-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f99c0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f99c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99c0-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="f99c0-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
