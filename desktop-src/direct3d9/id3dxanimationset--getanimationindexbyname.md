---
description: Obtient l’index d’une animation, en fonction de son nom.
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: 'ID3DXAnimationSet :: GetAnimationIndexByName, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4d3e5fb39ebcfa5ce906d1f90c2c5c10bdd4b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522342"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a><span data-ttu-id="3308f-103">ID3DXAnimationSet :: GetAnimationIndexByName, méthode</span><span class="sxs-lookup"><span data-stu-id="3308f-103">ID3DXAnimationSet::GetAnimationIndexByName method</span></span>

<span data-ttu-id="3308f-104">Obtient l’index d’une animation, en fonction de son nom.</span><span class="sxs-lookup"><span data-stu-id="3308f-104">Gets the index of an animation, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3308f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3308f-105">Syntax</span></span>


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a><span data-ttu-id="3308f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3308f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3308f-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3308f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3308f-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3308f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3308f-109">Nom de l’animation.</span><span class="sxs-lookup"><span data-stu-id="3308f-109">Name of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="3308f-110">*pIndex* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3308f-110">*pIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3308f-111">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3308f-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3308f-112">Pointeur vers l’index d’animation.</span><span class="sxs-lookup"><span data-stu-id="3308f-112">Pointer to the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3308f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3308f-113">Return value</span></span>

<span data-ttu-id="3308f-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3308f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3308f-115">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="3308f-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="3308f-116">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3308f-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="3308f-117">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="3308f-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3308f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3308f-118">Requirements</span></span>



| <span data-ttu-id="3308f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3308f-119">Requirement</span></span> | <span data-ttu-id="3308f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3308f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3308f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3308f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3308f-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3308f-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3308f-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3308f-123">Library</span></span><br/> | <dl> <span data-ttu-id="3308f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3308f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3308f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3308f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3308f-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="3308f-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
