---
description: Définit un tableau de valeurs booléennes.
ms.assetid: 323ad654-81e3-4986-a667-8333dd44a2d1
title: 'ID3DXConstantTable :: SetBoolArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d573a2c44b54809ec259a0ceb5abab02ef37df34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527110"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="7cd8d-103">ID3DXConstantTable :: SetBoolArray, méthode</span><span class="sxs-lookup"><span data-stu-id="7cd8d-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="7cd8d-104">Définit un tableau de valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="7cd8d-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd8d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cd8d-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="7cd8d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cd8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd8d-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cd8d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd8d-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7cd8d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7cd8d-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="7cd8d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="7cd8d-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cd8d-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd8d-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7cd8d-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7cd8d-112">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="7cd8d-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="7cd8d-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7cd8d-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cd8d-114">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cd8d-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd8d-115">Type : **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7cd8d-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7cd8d-116">Tableau de valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="7cd8d-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="7cd8d-117">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cd8d-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd8d-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cd8d-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cd8d-119">Nombre de valeurs booléennes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="7cd8d-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd8d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cd8d-120">Return value</span></span>

<span data-ttu-id="7cd8d-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7cd8d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7cd8d-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7cd8d-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7cd8d-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7cd8d-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd8d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cd8d-124">Requirements</span></span>



| <span data-ttu-id="7cd8d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cd8d-125">Requirement</span></span> | <span data-ttu-id="7cd8d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cd8d-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd8d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cd8d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7cd8d-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cd8d-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7cd8d-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7cd8d-129">Library</span></span><br/> | <dl> <span data-ttu-id="7cd8d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cd8d-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7cd8d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cd8d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd8d-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="7cd8d-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
