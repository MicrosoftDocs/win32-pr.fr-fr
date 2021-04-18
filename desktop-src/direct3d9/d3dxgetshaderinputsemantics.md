---
description: Obtient la sémantique pour les entrées du nuanceur. Utilisez cette méthode pour déterminer le format de vertex d’entrée.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: D3DXGetShaderInputSemantics, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522955"
---
# <a name="d3dxgetshaderinputsemantics-function"></a><span data-ttu-id="0d35b-104">D3DXGetShaderInputSemantics fonction)</span><span class="sxs-lookup"><span data-stu-id="0d35b-104">D3DXGetShaderInputSemantics function</span></span>

<span data-ttu-id="0d35b-105">Obtient la sémantique pour les entrées du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0d35b-105">Gets the semantics for the shader inputs.</span></span> <span data-ttu-id="0d35b-106">Utilisez cette méthode pour déterminer le format de vertex d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0d35b-106">Use this method to determine the input vertex format.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d35b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d35b-107">Syntax</span></span>


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="0d35b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d35b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d35b-109">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d35b-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d35b-110">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0d35b-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0d35b-111">Pointeur vers le flux de fonction de nuanceur DWORD.</span><span class="sxs-lookup"><span data-stu-id="0d35b-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="0d35b-112">*pSemantics* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d35b-112">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d35b-113">Type : **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d35b-113">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="0d35b-114">Pointeur vers un tableau de structures [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="0d35b-114">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="0d35b-115">La fonction remplit ce tableau avec la sémantique de chaque élément d’entrée référencé par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0d35b-115">The function will fill this array with the semantics for each input element referenced by the shader.</span></span> <span data-ttu-id="0d35b-116">Ce tableau est supposé contenir au moins des éléments MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="0d35b-116">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="0d35b-117">Toutefois, l’appel de **D3DXGetShaderInputSemantics** avec PSemantics = **null** retourne le nombre d’éléments nécessaires pour pCount.</span><span class="sxs-lookup"><span data-stu-id="0d35b-117">However, calling **D3DXGetShaderInputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="0d35b-118">*pCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d35b-118">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d35b-119">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d35b-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0d35b-120">Retourne le nombre d’éléments dans pSemantics.</span><span class="sxs-lookup"><span data-stu-id="0d35b-120">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d35b-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d35b-121">Return value</span></span>

<span data-ttu-id="0d35b-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d35b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d35b-123">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d35b-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0d35b-124">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0d35b-124">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d35b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0d35b-125">Remarks</span></span>

<span data-ttu-id="0d35b-126">Utilisez **D3DXGetShaderInputSemantics** pour retourner une liste des sémantiques d’entrée requises par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0d35b-126">Use **D3DXGetShaderInputSemantics** to return a list of input semantics required by the shader.</span></span> <span data-ttu-id="0d35b-127">Il s’agit de la façon de déterminer le format de vertex d’entrée pour un nuanceur HLSL (High-Level Shader Language).</span><span class="sxs-lookup"><span data-stu-id="0d35b-127">This is the way to find out what the input vertex format is for a high-level shader language (HLSL) shader.</span></span> <span data-ttu-id="0d35b-128">Si le nuanceur a des entrées supplémentaires pour lesquelles votre déclaration de vertex est manquante, vous pouvez créer un flux de vertex supplémentaire avec un Stride de 0 qui contient les composants manquants avec des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="0d35b-128">If the shader has additional inputs that your vertex declaration is missing, you could create an extra vertex stream that has a stride of 0 that has the missing components with default values.</span></span> <span data-ttu-id="0d35b-129">Par exemple, cette technique peut être utilisée pour fournir la couleur de vertex par défaut pour les modèles qui ne le spécifient pas.</span><span class="sxs-lookup"><span data-stu-id="0d35b-129">For instance, this technique could be used to provide default vertex color for models that do not specify it.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d35b-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d35b-130">Requirements</span></span>



| <span data-ttu-id="0d35b-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d35b-131">Requirement</span></span> | <span data-ttu-id="0d35b-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d35b-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d35b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d35b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0d35b-134"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d35b-134"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0d35b-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d35b-135">Library</span></span><br/> | <dl> <span data-ttu-id="0d35b-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d35b-136"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0d35b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d35b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d35b-138">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0d35b-138">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
