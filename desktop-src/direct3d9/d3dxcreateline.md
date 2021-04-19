---
description: Utilise un système de coordonnées droitier pour créer une ligne.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: D3DXCreateLine, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538742"
---
# <a name="d3dxcreateline-function"></a><span data-ttu-id="93712-103">D3DXCreateLine fonction)</span><span class="sxs-lookup"><span data-stu-id="93712-103">D3DXCreateLine function</span></span>

<span data-ttu-id="93712-104">Utilise un système de coordonnées droitier pour créer une ligne.</span><span class="sxs-lookup"><span data-stu-id="93712-104">Uses a left-handed coordinate system to create a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="93712-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93712-105">Syntax</span></span>


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a><span data-ttu-id="93712-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93712-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93712-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93712-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93712-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="93712-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="93712-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la maille Box créée.</span><span class="sxs-lookup"><span data-stu-id="93712-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="93712-110">*ppLine* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="93712-110">*ppLine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93712-111">Type : **[ **LPD3DXLINE**](id3dxline.md)\***</span><span class="sxs-lookup"><span data-stu-id="93712-111">Type: **[**LPD3DXLINE**](id3dxline.md)\***</span></span>

<span data-ttu-id="93712-112">Pointeur vers une interface [**ID3DXLine**](id3dxline.md) .</span><span class="sxs-lookup"><span data-stu-id="93712-112">Pointer to an [**ID3DXLine**](id3dxline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93712-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93712-113">Return value</span></span>

<span data-ttu-id="93712-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93712-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93712-115">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93712-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="93712-116">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="93712-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="93712-117">Notes</span><span class="sxs-lookup"><span data-stu-id="93712-117">Remarks</span></span>

<span data-ttu-id="93712-118">Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.</span><span class="sxs-lookup"><span data-stu-id="93712-118">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) Flexible Vertex Format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="93712-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93712-119">Requirements</span></span>



| <span data-ttu-id="93712-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93712-120">Requirement</span></span> | <span data-ttu-id="93712-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="93712-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93712-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="93712-122">Header</span></span><br/>  | <dl> <span data-ttu-id="93712-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="93712-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="93712-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="93712-124">Library</span></span><br/> | <dl> <span data-ttu-id="93712-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93712-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93712-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93712-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93712-127">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="93712-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
