---
description: 'ID3DXConstantTable :: SetVector, méthode-définit un vecteur 4D.'
ms.assetid: d5849a8b-b372-4ad0-8773-8c9c4bac3799
title: 'ID3DXConstantTable :: SetVector, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d7c464cebb050b9fd54c27656505e6f2221fe4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115017"
---
# <a name="id3dxconstanttablesetvector-method"></a><span data-ttu-id="b39b6-103">ID3DXConstantTable :: SetVector, méthode</span><span class="sxs-lookup"><span data-stu-id="b39b6-103">ID3DXConstantTable::SetVector method</span></span>

<span data-ttu-id="b39b6-104">Définit un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="b39b6-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b39b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b39b6-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="b39b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b39b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b39b6-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b39b6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b39b6-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b39b6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b39b6-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="b39b6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="b39b6-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b39b6-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b39b6-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b39b6-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b39b6-112">Identificateur unique de la constante Vector.</span><span class="sxs-lookup"><span data-stu-id="b39b6-112">Unique identifier to the vector constant.</span></span> <span data-ttu-id="b39b6-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b39b6-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b39b6-114">*pVector* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b39b6-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b39b6-115">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b39b6-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="b39b6-116">Pointeur vers un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="b39b6-116">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b39b6-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b39b6-117">Return value</span></span>

<span data-ttu-id="b39b6-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b39b6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b39b6-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b39b6-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b39b6-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b39b6-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b39b6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b39b6-121">Requirements</span></span>



| <span data-ttu-id="b39b6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b39b6-122">Requirement</span></span> | <span data-ttu-id="b39b6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b39b6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b39b6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b39b6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b39b6-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b39b6-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b39b6-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b39b6-126">Library</span></span><br/> | <dl> <span data-ttu-id="b39b6-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b39b6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b39b6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b39b6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b39b6-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b39b6-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
