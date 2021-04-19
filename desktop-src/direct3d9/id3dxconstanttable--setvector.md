---
description: Définit un vecteur 4D.
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
ms.openlocfilehash: ace1e7b12b67173eb5b9d9a5fc5e56a8b360f2b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545287"
---
# <a name="id3dxconstanttablesetvector-method"></a><span data-ttu-id="0c30f-103">ID3DXConstantTable :: SetVector, méthode</span><span class="sxs-lookup"><span data-stu-id="0c30f-103">ID3DXConstantTable::SetVector method</span></span>

<span data-ttu-id="0c30f-104">Définit un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="0c30f-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c30f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c30f-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="0c30f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c30f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c30f-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c30f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c30f-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0c30f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0c30f-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="0c30f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0c30f-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c30f-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c30f-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0c30f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0c30f-112">Identificateur unique de la constante Vector.</span><span class="sxs-lookup"><span data-stu-id="0c30f-112">Unique identifier to the vector constant.</span></span> <span data-ttu-id="0c30f-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0c30f-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c30f-114">*pVector* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c30f-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c30f-115">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="0c30f-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="0c30f-116">Pointeur vers un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="0c30f-116">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c30f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c30f-117">Return value</span></span>

<span data-ttu-id="0c30f-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c30f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c30f-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c30f-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0c30f-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0c30f-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c30f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c30f-121">Requirements</span></span>



| <span data-ttu-id="0c30f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c30f-122">Requirement</span></span> | <span data-ttu-id="0c30f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c30f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c30f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c30f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0c30f-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c30f-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0c30f-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c30f-126">Library</span></span><br/> | <dl> <span data-ttu-id="0c30f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c30f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0c30f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c30f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c30f-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0c30f-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
