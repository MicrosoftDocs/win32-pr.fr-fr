---
description: Génère une déclaration de vertex de sortie à partir de la déclaration d’entrée. La déclaration de sortie est destinée à être utilisée par les fonctions de pavage de maillage.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: D3DXGenerateOutputDecl, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520321"
---
# <a name="d3dxgenerateoutputdecl-function"></a><span data-ttu-id="d52dd-104">D3DXGenerateOutputDecl fonction)</span><span class="sxs-lookup"><span data-stu-id="d52dd-104">D3DXGenerateOutputDecl function</span></span>

<span data-ttu-id="d52dd-105">Génère une déclaration de vertex de sortie à partir de la déclaration d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d52dd-105">Generates an output vertex declaration from the input declaration.</span></span> <span data-ttu-id="d52dd-106">La déclaration de sortie est destinée à être utilisée par les fonctions de pavage de maillage.</span><span class="sxs-lookup"><span data-stu-id="d52dd-106">The output declaration is intended for use by the mesh tessellation functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52dd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d52dd-107">Syntax</span></span>


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="d52dd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d52dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d52dd-109">*pOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d52dd-109">*pOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d52dd-110">Type : **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span><span class="sxs-lookup"><span data-stu-id="d52dd-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="d52dd-111">Pointeur vers la déclaration de vertex de sortie.</span><span class="sxs-lookup"><span data-stu-id="d52dd-111">Pointer to the output vertex declaration.</span></span> <span data-ttu-id="d52dd-112">Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="d52dd-112">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="d52dd-113">*pInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d52dd-113">*pInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d52dd-114">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="d52dd-114">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="d52dd-115">Pointeur vers la déclaration de vertex d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d52dd-115">Pointer to the input vertex declaration.</span></span> <span data-ttu-id="d52dd-116">Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="d52dd-116">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d52dd-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d52dd-117">Return value</span></span>

<span data-ttu-id="d52dd-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d52dd-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d52dd-119">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d52dd-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d52dd-120">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d52dd-120">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d52dd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d52dd-121">Requirements</span></span>



| <span data-ttu-id="d52dd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d52dd-122">Requirement</span></span> | <span data-ttu-id="d52dd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d52dd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d52dd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d52dd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d52dd-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d52dd-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d52dd-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d52dd-126">Library</span></span><br/> | <dl> <span data-ttu-id="d52dd-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d52dd-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d52dd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d52dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52dd-129">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="d52dd-129">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




