---
description: Désassemblez un effet.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: D3DXDisassembleEffect, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524859"
---
# <a name="d3dxdisassembleeffect-function"></a><span data-ttu-id="3d91b-103">D3DXDisassembleEffect fonction)</span><span class="sxs-lookup"><span data-stu-id="3d91b-103">D3DXDisassembleEffect function</span></span>

<span data-ttu-id="3d91b-104">Désassemblez un effet.</span><span class="sxs-lookup"><span data-stu-id="3d91b-104">Disassemble an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d91b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d91b-105">Syntax</span></span>


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="3d91b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d91b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d91b-107">*pEffect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d91b-107">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d91b-108">Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="3d91b-108">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)**</span></span>

<span data-ttu-id="3d91b-109">Pointeur vers une interface [**ID3DXEffect**](id3dxeffect.md) qui contient l’effet.</span><span class="sxs-lookup"><span data-stu-id="3d91b-109">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface that contains the effect.</span></span>

</dd> <dt>

<span data-ttu-id="3d91b-110">*EnableColorCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d91b-110">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d91b-111">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d91b-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d91b-112">Activez le codage en couleurs pour faciliter la lecture du code machine.</span><span class="sxs-lookup"><span data-stu-id="3d91b-112">Enable color coding to make the disassembly easier to read.</span></span>

</dd> <dt>

<span data-ttu-id="3d91b-113">*ppDisassembly* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3d91b-113">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d91b-114">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d91b-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3d91b-115">Retourne une mémoire tampon contenant le nuanceur désassemblé.</span><span class="sxs-lookup"><span data-stu-id="3d91b-115">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="3d91b-116">Consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3d91b-116">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d91b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d91b-117">Return value</span></span>

<span data-ttu-id="3d91b-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d91b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d91b-119">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3d91b-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3d91b-120">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3d91b-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d91b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d91b-121">Requirements</span></span>



| <span data-ttu-id="3d91b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d91b-122">Requirement</span></span> | <span data-ttu-id="3d91b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d91b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d91b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d91b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3d91b-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d91b-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3d91b-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3d91b-126">Library</span></span><br/> | <dl> <span data-ttu-id="3d91b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d91b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3d91b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d91b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d91b-129">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="3d91b-129">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
