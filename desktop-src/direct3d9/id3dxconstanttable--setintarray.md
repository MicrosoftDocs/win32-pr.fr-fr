---
description: Définit un tableau d’entiers.
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
ms.openlocfilehash: 9f89de7d784ce355570d369606bfa67ddd6f5acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522595"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="2abbf-103">ID3DXConstantTable :: SetIntArray, méthode</span><span class="sxs-lookup"><span data-stu-id="2abbf-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="2abbf-104">Définit un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="2abbf-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2abbf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2abbf-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="2abbf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2abbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2abbf-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2abbf-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2abbf-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2abbf-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2abbf-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="2abbf-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="2abbf-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2abbf-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2abbf-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2abbf-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2abbf-112">Identificateur unique du tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="2abbf-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="2abbf-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2abbf-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2abbf-114">*PN* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2abbf-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2abbf-115">Type : **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2abbf-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2abbf-116">Tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="2abbf-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="2abbf-117">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2abbf-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2abbf-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2abbf-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2abbf-119">Nombre d’entiers dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2abbf-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2abbf-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2abbf-120">Return value</span></span>

<span data-ttu-id="2abbf-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2abbf-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2abbf-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2abbf-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2abbf-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2abbf-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abbf-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2abbf-124">Requirements</span></span>



| <span data-ttu-id="2abbf-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2abbf-125">Requirement</span></span> | <span data-ttu-id="2abbf-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2abbf-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abbf-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2abbf-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2abbf-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2abbf-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2abbf-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2abbf-129">Library</span></span><br/> | <dl> <span data-ttu-id="2abbf-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2abbf-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2abbf-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2abbf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abbf-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2abbf-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
