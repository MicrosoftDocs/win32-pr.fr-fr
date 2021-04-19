---
description: Obtient un pointeur vers le tableau de constantes dans la table constante.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'ID3DXTextureShader :: GetConstantDesc, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529628"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a><span data-ttu-id="7c97e-103">ID3DXTextureShader :: GetConstantDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="7c97e-103">ID3DXTextureShader::GetConstantDesc method</span></span>

<span data-ttu-id="7c97e-104">Obtient un pointeur vers le tableau de constantes dans la table constante.</span><span class="sxs-lookup"><span data-stu-id="7c97e-104">Gets a pointer to the array of constants in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c97e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c97e-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="7c97e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c97e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c97e-107">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c97e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c97e-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7c97e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7c97e-109">Identificateur unique d’une constante.</span><span class="sxs-lookup"><span data-stu-id="7c97e-109">Unique identifier to a constant.</span></span> <span data-ttu-id="7c97e-110">Consultez [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="7c97e-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c97e-111">*pDesc* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7c97e-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c97e-112">Type : **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c97e-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="7c97e-113">Retourne un pointeur vers un tableau de descriptions.</span><span class="sxs-lookup"><span data-stu-id="7c97e-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="7c97e-114">Consultez [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="7c97e-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c97e-115">*pCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7c97e-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c97e-116">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c97e-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7c97e-117">L’entrée fournie doit correspondre à la taille maximale du tableau.</span><span class="sxs-lookup"><span data-stu-id="7c97e-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="7c97e-118">La sortie est le nombre d’éléments qui sont remplis dans le tableau lorsque la fonction retourne.</span><span class="sxs-lookup"><span data-stu-id="7c97e-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c97e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c97e-119">Return value</span></span>

<span data-ttu-id="7c97e-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c97e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c97e-121">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c97e-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c97e-122">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="7c97e-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c97e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7c97e-123">Remarks</span></span>

<span data-ttu-id="7c97e-124">Les échantillonneurs peuvent apparaître plusieurs fois dans une table constante. par conséquent, cette méthode peut retourner un tableau de descriptions, chacune avec un index de Registre différent.</span><span class="sxs-lookup"><span data-stu-id="7c97e-124">Samplers can appear more than once in a constant table, therefore, this method can return an array of descriptions each with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c97e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c97e-125">Requirements</span></span>



| <span data-ttu-id="7c97e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c97e-126">Requirement</span></span> | <span data-ttu-id="7c97e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c97e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c97e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c97e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7c97e-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c97e-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7c97e-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c97e-130">Library</span></span><br/> | <dl> <span data-ttu-id="7c97e-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c97e-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7c97e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c97e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c97e-133">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="7c97e-133">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> <dt>

[<span data-ttu-id="7c97e-134">**ID3DXTextureShader::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="7c97e-134">**ID3DXTextureShader::GetDesc**</span></span>](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
