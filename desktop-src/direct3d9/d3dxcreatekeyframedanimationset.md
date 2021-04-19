---
description: Crée une interface de jeu d’animations à clé ID3DXKeyframedAnimationSet.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: D3DXCreateKeyframedAnimationSet, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538533"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a><span data-ttu-id="f2ddd-103">D3DXCreateKeyframedAnimationSet fonction)</span><span class="sxs-lookup"><span data-stu-id="f2ddd-103">D3DXCreateKeyframedAnimationSet function</span></span>

<span data-ttu-id="f2ddd-104">Crée une interface de jeu d’animations à clé [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="f2ddd-104">Creates a [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ddd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2ddd-105">Syntax</span></span>


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="f2ddd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2ddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ddd-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2ddd-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ddd-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2ddd-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2ddd-109">Pointeur vers le nom de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="f2ddd-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="f2ddd-110">*TicksPerSecond* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2ddd-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ddd-111">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2ddd-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2ddd-112">Nombre de battements d’image clé qui s’écoulent par seconde.</span><span class="sxs-lookup"><span data-stu-id="f2ddd-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="f2ddd-113">*Lecture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2ddd-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ddd-114">Type : **[ **D3DXPLAYBACK \_**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="f2ddd-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="f2ddd-115">Type de la boucle de lecture du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="f2ddd-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="f2ddd-116">Consultez [**\_ type D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="f2ddd-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2ddd-117">*NumAnimations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2ddd-117">*NumAnimations* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ddd-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2ddd-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2ddd-119">Nombre de jeux d’animations de mise à l’échelle, de rotation et de translation (SRT).</span><span class="sxs-lookup"><span data-stu-id="f2ddd-119">Number of scale, rotate, and translate (SRT) animation sets.</span></span>

</dd> <dt>

<span data-ttu-id="f2ddd-120">*NumCallbackKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2ddd-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ddd-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2ddd-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2ddd-122">Nombre de clés de rappel.</span><span class="sxs-lookup"><span data-stu-id="f2ddd-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="f2ddd-123">*pCallKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2ddd-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ddd-124">Type : **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2ddd-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="f2ddd-125">Pointeur vers une structure de [**\_ rappel D3DXKEY**](d3dxkey-callback.md) qui stocke les données de rappel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f2ddd-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="f2ddd-126">*ppAnimationSet* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f2ddd-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ddd-127">Type : **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2ddd-127">Type: **[**LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span></span>

<span data-ttu-id="f2ddd-128">Adresse d’un pointeur vers la clé [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) de l’interface de jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="f2ddd-128">Address of a pointer to the [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ddd-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2ddd-129">Return value</span></span>

<span data-ttu-id="f2ddd-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2ddd-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2ddd-131">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2ddd-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f2ddd-132">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f2ddd-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ddd-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2ddd-133">Requirements</span></span>



| <span data-ttu-id="f2ddd-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2ddd-134">Requirement</span></span> | <span data-ttu-id="f2ddd-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2ddd-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ddd-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2ddd-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f2ddd-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ddd-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f2ddd-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2ddd-138">Library</span></span><br/> | <dl> <span data-ttu-id="f2ddd-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2ddd-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2ddd-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2ddd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ddd-141">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="f2ddd-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
