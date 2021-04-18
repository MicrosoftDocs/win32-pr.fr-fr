---
description: Obtient la sémantique pour tous les éléments de sortie du nuanceur.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: D3DXGetShaderOutputSemantics, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530903"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a><span data-ttu-id="8c0f8-103">D3DXGetShaderOutputSemantics fonction)</span><span class="sxs-lookup"><span data-stu-id="8c0f8-103">D3DXGetShaderOutputSemantics function</span></span>

<span data-ttu-id="8c0f8-104">Obtient la sémantique pour tous les éléments de sortie du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-104">Get the semantics for all shader output elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0f8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c0f8-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="8c0f8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c0f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0f8-107">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c0f8-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f8-108">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c0f8-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8c0f8-109">Pointeur vers le flux de fonction de nuanceur DWORD.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f8-110">*pSemantics* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c0f8-110">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f8-111">Type : **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c0f8-111">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="8c0f8-112">Pointeur vers un tableau de structures [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="8c0f8-112">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="8c0f8-113">La fonction remplit ce tableau avec la sémantique pour chaque élément de sortie référencé par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-113">The function will fill this array with the semantics for each output element referenced by the shader.</span></span> <span data-ttu-id="8c0f8-114">Ce tableau est supposé contenir au moins des éléments MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-114">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="8c0f8-115">Toutefois, l’appel de **D3DXGetShaderOutputSemantics** avec PSemantics = **null** retourne le nombre d’éléments nécessaires pour pCount.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-115">However, calling **D3DXGetShaderOutputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f8-116">*pCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8c0f8-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f8-117">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c0f8-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8c0f8-118">Retourne le nombre d’éléments dans pSemantics.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-118">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c0f8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c0f8-119">Return value</span></span>

<span data-ttu-id="8c0f8-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c0f8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c0f8-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8c0f8-122">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8c0f8-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0f8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c0f8-123">Requirements</span></span>



| <span data-ttu-id="8c0f8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c0f8-124">Requirement</span></span> | <span data-ttu-id="8c0f8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c0f8-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0f8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c0f8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8c0f8-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f8-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8c0f8-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c0f8-128">Library</span></span><br/> | <dl> <span data-ttu-id="8c0f8-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f8-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8c0f8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c0f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0f8-131">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8c0f8-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
