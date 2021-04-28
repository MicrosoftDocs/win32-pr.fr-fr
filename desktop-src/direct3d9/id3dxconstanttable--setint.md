---
description: 'ID3DXConstantTable :: setInt, méthode-définit une valeur entière.'
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
ms.openlocfilehash: f218a0cd1a0e1858f24ec8cbccb4848c37121086
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115127"
---
# <a name="id3dxconstanttablesetint-method"></a><span data-ttu-id="1e3fa-103">ID3DXConstantTable :: setInt, méthode</span><span class="sxs-lookup"><span data-stu-id="1e3fa-103">ID3DXConstantTable::SetInt method</span></span>

<span data-ttu-id="1e3fa-104">Définit une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="1e3fa-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e3fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e3fa-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] INT               n
);
```



## <a name="parameters"></a><span data-ttu-id="1e3fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e3fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e3fa-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e3fa-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3fa-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1e3fa-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1e3fa-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="1e3fa-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="1e3fa-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e3fa-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3fa-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1e3fa-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1e3fa-112">Identificateur unique de la constante.</span><span class="sxs-lookup"><span data-stu-id="1e3fa-112">Unique identifier to the constant.</span></span> <span data-ttu-id="1e3fa-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1e3fa-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e3fa-114">*n* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e3fa-114">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3fa-115">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e3fa-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e3fa-116">Entier.</span><span class="sxs-lookup"><span data-stu-id="1e3fa-116">Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e3fa-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1e3fa-117">Return value</span></span>

<span data-ttu-id="1e3fa-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e3fa-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e3fa-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e3fa-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e3fa-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1e3fa-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e3fa-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e3fa-121">Requirements</span></span>



| <span data-ttu-id="1e3fa-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e3fa-122">Requirement</span></span> | <span data-ttu-id="1e3fa-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e3fa-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e3fa-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e3fa-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1e3fa-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e3fa-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1e3fa-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e3fa-126">Library</span></span><br/> | <dl> <span data-ttu-id="1e3fa-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e3fa-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1e3fa-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e3fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e3fa-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="1e3fa-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
