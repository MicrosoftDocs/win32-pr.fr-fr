---
description: 'ID3DXConstantTable :: SetIntArray, méthode-définit un tableau d’entiers.'
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: 'ID3DXConstantTable :: SetIntArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f674bc730398c386856314a7e7305f33f3e7fa1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115107"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="71dff-103">ID3DXConstantTable :: SetIntArray, méthode</span><span class="sxs-lookup"><span data-stu-id="71dff-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="71dff-104">Définit un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="71dff-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="71dff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71dff-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="71dff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71dff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71dff-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71dff-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71dff-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="71dff-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="71dff-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="71dff-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="71dff-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71dff-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71dff-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="71dff-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="71dff-112">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="71dff-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="71dff-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="71dff-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="71dff-114">*PN* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71dff-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71dff-115">Type : **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="71dff-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="71dff-116">Tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="71dff-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="71dff-117">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71dff-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71dff-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71dff-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71dff-119">Nombre d’entiers dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="71dff-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71dff-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71dff-120">Return value</span></span>

<span data-ttu-id="71dff-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71dff-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71dff-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="71dff-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="71dff-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="71dff-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="71dff-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71dff-124">Requirements</span></span>



| <span data-ttu-id="71dff-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71dff-125">Requirement</span></span> | <span data-ttu-id="71dff-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="71dff-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71dff-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="71dff-127">Header</span></span><br/>  | <dl> <span data-ttu-id="71dff-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="71dff-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="71dff-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71dff-129">Library</span></span><br/> | <dl> <span data-ttu-id="71dff-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71dff-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="71dff-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71dff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71dff-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="71dff-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
