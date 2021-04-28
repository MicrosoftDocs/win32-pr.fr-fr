---
description: 'ID3DXBaseEffect :: SetMatrix, méthode-définit une matrice non transposée.'
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'ID3DXBaseEffect :: SetMatrix, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7af7dc0daa3dcd29e7b15c4fe435b9626ea41746
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097497"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="1f2e9-103">ID3DXBaseEffect :: SetMatrix, méthode</span><span class="sxs-lookup"><span data-stu-id="1f2e9-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="1f2e9-104">Définit une matrice non transposée.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f2e9-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="1f2e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f2e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f2e9-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f2e9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f2e9-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1f2e9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1f2e9-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-109">Unique identifier.</span></span> <span data-ttu-id="1f2e9-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1f2e9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f2e9-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f2e9-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f2e9-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f2e9-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1f2e9-113">Pointeur vers une matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="1f2e9-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="1f2e9-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f2e9-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f2e9-115">Return value</span></span>

<span data-ttu-id="1f2e9-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f2e9-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f2e9-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1f2e9-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f2e9-119">Notes </span><span class="sxs-lookup"><span data-stu-id="1f2e9-119">Remarks</span></span>

<span data-ttu-id="1f2e9-120">Une matrice non transposée contient des données de lignes principales.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="1f2e9-121">En d’autres termes, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="1f2e9-122">Si la matrice de destination est plus petite que la matrice source, les composants supplémentaires de la matrice source seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="1f2e9-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2e9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f2e9-123">Requirements</span></span>



| <span data-ttu-id="1f2e9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f2e9-124">Requirement</span></span> | <span data-ttu-id="1f2e9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f2e9-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2e9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f2e9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1f2e9-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f2e9-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1f2e9-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f2e9-128">Library</span></span><br/> | <dl> <span data-ttu-id="1f2e9-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f2e9-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1f2e9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f2e9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2e9-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="1f2e9-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="1f2e9-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="1f2e9-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




