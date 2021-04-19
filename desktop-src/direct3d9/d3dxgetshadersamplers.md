---
description: Obtenir les noms d’échantillonneur référencés dans un nuanceur.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: D3DXGetShaderSamplers, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532186"
---
# <a name="d3dxgetshadersamplers-function"></a><span data-ttu-id="157e0-103">D3DXGetShaderSamplers fonction)</span><span class="sxs-lookup"><span data-stu-id="157e0-103">D3DXGetShaderSamplers function</span></span>

<span data-ttu-id="157e0-104">Obtenir les noms d’échantillonneur référencés dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="157e0-104">Get the sampler names referenced in a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="157e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="157e0-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="157e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="157e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="157e0-107">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="157e0-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="157e0-108">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="157e0-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="157e0-109">Pointeur vers le flux de fonction de nuanceur DWORD.</span><span class="sxs-lookup"><span data-stu-id="157e0-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="157e0-110">*pSamplers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="157e0-110">*pSamplers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="157e0-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="157e0-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="157e0-112">Pointeur vers un tableau de LPCSTRs.</span><span class="sxs-lookup"><span data-stu-id="157e0-112">Pointer to an array of LPCSTRs.</span></span> <span data-ttu-id="157e0-113">La fonction remplit ce tableau avec des pointeurs vers les noms d’échantillonneurs contenus dans *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="157e0-113">The function will fill this array with pointers to the sampler names contained within *pFunction*.</span></span> <span data-ttu-id="157e0-114">La taille de tableau maximale est le nombre maximal de registres d’échantillonnage (16 pour vs \_ 3 \_ 0 et PS \_ 3 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="157e0-114">The maximum array size is the maximum number of sampler registers (16 for vs\_3\_0 and ps\_3\_0).</span></span>

<span data-ttu-id="157e0-115">Pour déterminer le nombre d’échantillonneurs utilisés, consultez *pCount* après avoir appelé **D3DXGetShaderSamplers** avec pSamplers = **null**.</span><span class="sxs-lookup"><span data-stu-id="157e0-115">To find the number of samplers used, check *pCount* after calling **D3DXGetShaderSamplers** with pSamplers = **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="157e0-116">*pCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="157e0-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="157e0-117">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="157e0-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="157e0-118">Retourne le nombre d’échantillonneurs référencés par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="157e0-118">Returns the number of samplers referenced by the shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="157e0-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="157e0-119">Return value</span></span>

<span data-ttu-id="157e0-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="157e0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="157e0-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="157e0-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="157e0-122">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="157e0-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="157e0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="157e0-123">Requirements</span></span>



| <span data-ttu-id="157e0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="157e0-124">Requirement</span></span> | <span data-ttu-id="157e0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="157e0-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="157e0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="157e0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="157e0-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="157e0-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="157e0-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="157e0-128">Library</span></span><br/> | <dl> <span data-ttu-id="157e0-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="157e0-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="157e0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="157e0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="157e0-131">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="157e0-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
