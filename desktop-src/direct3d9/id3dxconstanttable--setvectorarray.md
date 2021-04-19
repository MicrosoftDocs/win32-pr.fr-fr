---
description: Définit un tableau de vecteurs 4D.
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: 'ID3DXConstantTable :: SetVectorArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6c68621a3f97251cdd88836792bf55980f28311
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532451"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="516c5-103">ID3DXConstantTable :: SetVectorArray, méthode</span><span class="sxs-lookup"><span data-stu-id="516c5-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="516c5-104">Définit un tableau de vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="516c5-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="516c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="516c5-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="516c5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="516c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516c5-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="516c5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516c5-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="516c5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="516c5-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="516c5-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="516c5-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="516c5-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516c5-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="516c5-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="516c5-112">Identificateur unique du tableau de constantes vectorielles.</span><span class="sxs-lookup"><span data-stu-id="516c5-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="516c5-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="516c5-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="516c5-114">*pVector* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="516c5-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516c5-115">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="516c5-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="516c5-116">Tableau de vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="516c5-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="516c5-117">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="516c5-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516c5-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="516c5-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="516c5-119">Nombre de vecteurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="516c5-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516c5-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="516c5-120">Return value</span></span>

<span data-ttu-id="516c5-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="516c5-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="516c5-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="516c5-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="516c5-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="516c5-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="516c5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="516c5-124">Requirements</span></span>



| <span data-ttu-id="516c5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="516c5-125">Requirement</span></span> | <span data-ttu-id="516c5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="516c5-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="516c5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="516c5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="516c5-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="516c5-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="516c5-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="516c5-129">Library</span></span><br/> | <dl> <span data-ttu-id="516c5-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="516c5-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="516c5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="516c5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516c5-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="516c5-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
