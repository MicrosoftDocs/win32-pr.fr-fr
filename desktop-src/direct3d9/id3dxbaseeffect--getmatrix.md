---
description: Obtient une matrice nontransposed.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'ID3DXBaseEffect :: GetMatrix, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525096"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a><span data-ttu-id="fc2ee-103">ID3DXBaseEffect :: GetMatrix, méthode</span><span class="sxs-lookup"><span data-stu-id="fc2ee-103">ID3DXBaseEffect::GetMatrix method</span></span>

<span data-ttu-id="fc2ee-104">Obtient une matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="fc2ee-104">Gets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc2ee-105">Syntax</span></span>


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="fc2ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc2ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc2ee-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc2ee-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc2ee-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fc2ee-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fc2ee-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="fc2ee-109">Unique identifier.</span></span> <span data-ttu-id="fc2ee-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fc2ee-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc2ee-111">*pMatrix* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fc2ee-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc2ee-112">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc2ee-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc2ee-113">Retourne une matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="fc2ee-113">Returns a nontransposed matrix.</span></span> <span data-ttu-id="fc2ee-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="fc2ee-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc2ee-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc2ee-115">Return value</span></span>

<span data-ttu-id="fc2ee-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc2ee-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc2ee-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc2ee-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fc2ee-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fc2ee-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc2ee-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fc2ee-119">Remarks</span></span>

<span data-ttu-id="fc2ee-120">Une matrice nontransposed contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="fc2ee-120">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="fc2ee-121">Si la matrice de destination est plus grande que la matrice source, seuls les composants supérieurs gauches de la matrice de destination seront remplis et les composants restants seront définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="fc2ee-121">If the destination matrix is larger than the source matrix, only the upper-left components of the destination matrix will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2ee-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc2ee-122">Requirements</span></span>



| <span data-ttu-id="fc2ee-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc2ee-123">Requirement</span></span> | <span data-ttu-id="fc2ee-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc2ee-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2ee-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc2ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fc2ee-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ee-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fc2ee-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc2ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="fc2ee-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ee-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fc2ee-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc2ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2ee-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fc2ee-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fc2ee-131">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="fc2ee-131">**SetMatrix**</span></span>](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




