---
description: 'Fonction D3DXGetShaderConstantTableEx : obtient la table de constantes de nuanceur incorporée à l’intérieur d’un nuanceur.'
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: D3DXGetShaderConstantTableEx, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114428"
---
# <a name="d3dxgetshaderconstanttableex-function"></a><span data-ttu-id="41f08-103">D3DXGetShaderConstantTableEx fonction)</span><span class="sxs-lookup"><span data-stu-id="41f08-103">D3DXGetShaderConstantTableEx function</span></span>

<span data-ttu-id="41f08-104">Obtient la table de constantes de nuanceur incorporée à l’intérieur d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="41f08-104">Gets the shader-constant table embedded inside a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f08-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41f08-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="41f08-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41f08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41f08-107">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41f08-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f08-108">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="41f08-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="41f08-109">Pointeur vers le flux de fonction DWORD.</span><span class="sxs-lookup"><span data-stu-id="41f08-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="41f08-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="41f08-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41f08-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41f08-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41f08-112">Utilisez l' \_ indicateur D3DXCONSTTABLE LARGEADDRESSAWARE pour accéder à un espace d’adressage virtuel de 4 Go maximum (au lieu de 2 Go par défaut).</span><span class="sxs-lookup"><span data-stu-id="41f08-112">Use the D3DXCONSTTABLE\_LARGEADDRESSAWARE flag to access up to 4 GB of virtual address space (instead of the default of 2 GB).</span></span> <span data-ttu-id="41f08-113">Si vous n’avez pas besoin de l’espace d’adressage virtuel supplémentaire, utilisez [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="41f08-113">If you do not need the additional virtual address space, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span></span>

</dd> <dt>

 <span data-ttu-id="41f08-114">*ppConstantTable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="41f08-114">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41f08-115">Type : **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="41f08-115">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="41f08-116">Retourne l’interface de table constante (consultez [**ID3DXConstantTable**](id3dxconstanttable.md)) qui gère la table constante.</span><span class="sxs-lookup"><span data-stu-id="41f08-116">Returns the constant table interface (see [**ID3DXConstantTable**](id3dxconstanttable.md)) that manages the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41f08-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41f08-117">Return value</span></span>

<span data-ttu-id="41f08-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41f08-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41f08-119">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41f08-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="41f08-120">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="41f08-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f08-121">Notes </span><span class="sxs-lookup"><span data-stu-id="41f08-121">Remarks</span></span>

<span data-ttu-id="41f08-122">Une table constante est générée par [**D3DXCompileShader**](d3dxcompileshader.md) et incorporée dans le corps du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="41f08-122">A constant table is generated by [**D3DXCompileShader**](d3dxcompileshader.md) and embedded in the shader body.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f08-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41f08-123">Requirements</span></span>



| <span data-ttu-id="41f08-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41f08-124">Requirement</span></span> | <span data-ttu-id="41f08-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="41f08-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f08-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="41f08-126">Header</span></span><br/>  | <dl> <span data-ttu-id="41f08-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="41f08-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="41f08-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41f08-128">Library</span></span><br/> | <dl> <span data-ttu-id="41f08-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41f08-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="41f08-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41f08-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f08-131">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="41f08-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
