---
description: 'ID3DXConstantTable :: SetFloatArray, méthode-définit un tableau de nombres à virgule flottante.'
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: 'ID3DXConstantTable :: SetFloatArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23c96cb2bfc8113fd167c8b57a21a46285b691a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115167"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="c61f0-103">ID3DXConstantTable :: SetFloatArray, méthode</span><span class="sxs-lookup"><span data-stu-id="c61f0-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="c61f0-104">Définit un tableau de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c61f0-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61f0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c61f0-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="c61f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c61f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61f0-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c61f0-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61f0-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c61f0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c61f0-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="c61f0-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="c61f0-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c61f0-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61f0-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c61f0-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c61f0-112">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="c61f0-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="c61f0-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c61f0-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c61f0-114">*PF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c61f0-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61f0-115">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c61f0-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c61f0-116">Tableau de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c61f0-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="c61f0-117">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c61f0-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61f0-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c61f0-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c61f0-119">Nombre de valeurs à virgule flottante dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="c61f0-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c61f0-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c61f0-120">Return value</span></span>

<span data-ttu-id="c61f0-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c61f0-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c61f0-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c61f0-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c61f0-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c61f0-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c61f0-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c61f0-124">Requirements</span></span>



| <span data-ttu-id="c61f0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c61f0-125">Requirement</span></span> | <span data-ttu-id="c61f0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c61f0-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c61f0-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c61f0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c61f0-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c61f0-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c61f0-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c61f0-129">Library</span></span><br/> | <dl> <span data-ttu-id="c61f0-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c61f0-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c61f0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c61f0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61f0-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="c61f0-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
