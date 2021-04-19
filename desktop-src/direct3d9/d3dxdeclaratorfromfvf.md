---
description: Retourne un déclarateur à partir d’un code de format de vertex flexible.
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: D3DXDeclaratorFromFVF, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106541252"
---
# <a name="d3dxdeclaratorfromfvf-function"></a><span data-ttu-id="b2d5b-103">D3DXDeclaratorFromFVF fonction)</span><span class="sxs-lookup"><span data-stu-id="b2d5b-103">D3DXDeclaratorFromFVF function</span></span>

<span data-ttu-id="b2d5b-104">Retourne un déclarateur à partir d’un code de format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="b2d5b-104">Returns a declarator from a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2d5b-105">Syntax</span></span>


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="b2d5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2d5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d5b-107">*Commission* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2d5b-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d5b-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2d5b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2d5b-109">Combinaison de [D3DFVF](d3dfvf.md) qui décrit le prix de la Commission à partir duquel générer le tableau de déclarateur retourné.</span><span class="sxs-lookup"><span data-stu-id="b2d5b-109">Combination of [D3DFVF](d3dfvf.md) that describes the FVF from which to generate the returned declarator array.</span></span>

</dd> <dt>

<span data-ttu-id="b2d5b-110">*Déclaration* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="b2d5b-110">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d5b-111">Type : **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="b2d5b-111">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="b2d5b-112">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) décrivant le format de vertex des vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="b2d5b-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="b2d5b-113">La limite supérieure de ce tableau déclarateur est [**la \_ \_ \_ taille maximale**](./max-fvf-decl-size.md)de la déclaration de la Commission de la Commission.</span><span class="sxs-lookup"><span data-stu-id="b2d5b-113">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d5b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2d5b-114">Return value</span></span>

<span data-ttu-id="b2d5b-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2d5b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2d5b-116">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2d5b-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2d5b-117">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DXERR \_ INVALIDMESH.</span><span class="sxs-lookup"><span data-stu-id="b2d5b-117">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2d5b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2d5b-118">Requirements</span></span>



| <span data-ttu-id="b2d5b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2d5b-119">Requirement</span></span> | <span data-ttu-id="b2d5b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2d5b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d5b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2d5b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b2d5b-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2d5b-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b2d5b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b2d5b-123">Library</span></span><br/> | <dl> <span data-ttu-id="b2d5b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2d5b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2d5b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2d5b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d5b-126">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="b2d5b-126">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="b2d5b-127">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="b2d5b-127">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
