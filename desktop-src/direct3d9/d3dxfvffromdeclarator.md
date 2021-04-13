---
description: Retourne un code de format de vertex flexible (Commission) à partir d’un déclarateur.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: D3DXFVFFromDeclarator, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322913"
---
# <a name="d3dxfvffromdeclarator-function"></a><span data-ttu-id="ad710-103">D3DXFVFFromDeclarator fonction)</span><span class="sxs-lookup"><span data-stu-id="ad710-103">D3DXFVFFromDeclarator function</span></span>

<span data-ttu-id="ad710-104">Retourne un code de format de vertex flexible (Commission) à partir d’un déclarateur.</span><span class="sxs-lookup"><span data-stu-id="ad710-104">Returns a flexible vertex format (FVF) code from a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad710-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad710-105">Syntax</span></span>


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a><span data-ttu-id="ad710-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad710-107">*pDeclaration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad710-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad710-108">Type : **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad710-108">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="ad710-109">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le code de la Commission.</span><span class="sxs-lookup"><span data-stu-id="ad710-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the FVF code.</span></span>

</dd> <dt>

<span data-ttu-id="ad710-110">*pFVF* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ad710-110">*pFVF* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad710-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad710-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad710-112">Pointeur vers une valeur DWORD représentant la combinaison retournée de [D3DFVF](d3dfvf.md) qui décrit le format de vertex retourné par le déclarateur.</span><span class="sxs-lookup"><span data-stu-id="ad710-112">Pointer to a DWORD value, representing the returned combination of [D3DFVF](d3dfvf.md) that describes the vertex format returned from the declarator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad710-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad710-113">Return value</span></span>

<span data-ttu-id="ad710-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad710-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad710-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad710-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ad710-116">Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ad710-116">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad710-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ad710-117">Remarks</span></span>

<span data-ttu-id="ad710-118">Cette fonction échoue pour tout déclarateur qui ne correspond pas directement à un prix de la Commission.</span><span class="sxs-lookup"><span data-stu-id="ad710-118">This function will fail for any declarator that does not map directly to an FVF.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad710-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad710-119">Requirements</span></span>



| <span data-ttu-id="ad710-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad710-120">Requirement</span></span> | <span data-ttu-id="ad710-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad710-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad710-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad710-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ad710-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad710-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ad710-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad710-124">Library</span></span><br/> | <dl> <span data-ttu-id="ad710-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad710-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad710-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad710-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad710-127">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="ad710-127">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="ad710-128">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="ad710-128">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
