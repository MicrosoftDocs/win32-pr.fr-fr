---
description: 'ID3DXConstantTable :: SetVectorArray, méthode-définit un tableau de vecteurs 4D.'
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
ms.openlocfilehash: fe93ef7a75cda743399133445a5f6efd34dd5ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115007"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="965e3-103">ID3DXConstantTable :: SetVectorArray, méthode</span><span class="sxs-lookup"><span data-stu-id="965e3-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="965e3-104">Définit un tableau de vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="965e3-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="965e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="965e3-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="965e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="965e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965e3-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="965e3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965e3-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="965e3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="965e3-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.</span><span class="sxs-lookup"><span data-stu-id="965e3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="965e3-110">*hConstant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="965e3-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965e3-111">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="965e3-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="965e3-112">Identificateur unique du tableau de constantes vectorielles.</span><span class="sxs-lookup"><span data-stu-id="965e3-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="965e3-113">Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="965e3-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="965e3-114">*pVector* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="965e3-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965e3-115">Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="965e3-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="965e3-116">Tableau de vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="965e3-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="965e3-117">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="965e3-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965e3-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="965e3-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="965e3-119">Nombre de vecteurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="965e3-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="965e3-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="965e3-120">Return value</span></span>

<span data-ttu-id="965e3-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="965e3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="965e3-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="965e3-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="965e3-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="965e3-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="965e3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="965e3-124">Requirements</span></span>



| <span data-ttu-id="965e3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="965e3-125">Requirement</span></span> | <span data-ttu-id="965e3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="965e3-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="965e3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="965e3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="965e3-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="965e3-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="965e3-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="965e3-129">Library</span></span><br/> | <dl> <span data-ttu-id="965e3-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="965e3-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="965e3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="965e3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965e3-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="965e3-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
