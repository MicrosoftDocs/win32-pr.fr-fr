---
description: Définit une matrice non transposée.
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
ms.openlocfilehash: 39a5aed1d6321cf0599d212222fd967ee512e20e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530849"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="127e2-103">ID3DXBaseEffect :: SetMatrix, méthode</span><span class="sxs-lookup"><span data-stu-id="127e2-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="127e2-104">Définit une matrice non transposée.</span><span class="sxs-lookup"><span data-stu-id="127e2-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="127e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="127e2-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="127e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="127e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="127e2-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="127e2-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="127e2-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="127e2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="127e2-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="127e2-109">Unique identifier.</span></span> <span data-ttu-id="127e2-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="127e2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="127e2-111">*pMatrix* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="127e2-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="127e2-112">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="127e2-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="127e2-113">Pointeur vers une matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="127e2-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="127e2-114">Consultez [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="127e2-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="127e2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="127e2-115">Return value</span></span>

<span data-ttu-id="127e2-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="127e2-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="127e2-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="127e2-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="127e2-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="127e2-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="127e2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="127e2-119">Remarks</span></span>

<span data-ttu-id="127e2-120">Une matrice non transposée contient des données de lignes principales.</span><span class="sxs-lookup"><span data-stu-id="127e2-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="127e2-121">En d’autres termes, chaque vecteur est contenu dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="127e2-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="127e2-122">Si la matrice de destination est plus petite que la matrice source, les composants supplémentaires de la matrice source seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="127e2-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="127e2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="127e2-123">Requirements</span></span>



| <span data-ttu-id="127e2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="127e2-124">Requirement</span></span> | <span data-ttu-id="127e2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="127e2-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="127e2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="127e2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="127e2-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="127e2-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="127e2-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="127e2-128">Library</span></span><br/> | <dl> <span data-ttu-id="127e2-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="127e2-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="127e2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="127e2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127e2-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="127e2-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="127e2-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="127e2-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




