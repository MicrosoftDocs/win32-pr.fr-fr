---
description: Définit une valeur entière.
ms.assetid: b57d30b5-c2b5-469e-a267-24e6e712d645
title: 'ID3DXConstantTable :: setInt, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0aa0a213f9f4704a5d557db66aaf360f8baa727
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538519"
---
# <a name="id3dxconstanttablesetint-method"></a><span data-ttu-id="0b950-103">ID3DXConstantTable :: setInt, méthode</span><span class="sxs-lookup"><span data-stu-id="0b950-103">ID3DXConstantTable::SetInt method</span></span>

<span data-ttu-id="0b950-104">Définit une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="0b950-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b950-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b950-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] INT               n
);
```



## <a name="parameters"></a><span data-ttu-id="0b950-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b950-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b950-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b950-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0b950-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0b950-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="0b950-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0b950-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b950-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b950-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0b950-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0b950-112">Identificateur unique de la constante.</span><span class="sxs-lookup"><span data-stu-id="0b950-112">Unique identifier to the constant.</span></span> <span data-ttu-id="0b950-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0b950-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b950-114">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b950-114">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b950-115">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b950-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b950-116">Entier.</span><span class="sxs-lookup"><span data-stu-id="0b950-116">Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b950-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b950-117">Return value</span></span>

<span data-ttu-id="0b950-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b950-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b950-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b950-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0b950-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0b950-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b950-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b950-121">Requirements</span></span>



| <span data-ttu-id="0b950-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b950-122">Requirement</span></span> | <span data-ttu-id="0b950-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b950-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b950-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b950-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0b950-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b950-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0b950-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b950-126">Library</span></span><br/> | <dl> <span data-ttu-id="0b950-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b950-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0b950-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b950-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b950-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0b950-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
