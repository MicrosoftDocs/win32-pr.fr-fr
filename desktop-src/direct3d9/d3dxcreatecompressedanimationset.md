---
description: Crée une interface de jeu d’animations à clé ID3DXCompressedAnimationSet qui stocke les données d’image clé dans un format compressé.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: D3DXCreateCompressedAnimationSet, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953878"
---
# <a name="d3dxcreatecompressedanimationset-function"></a><span data-ttu-id="664eb-103">D3DXCreateCompressedAnimationSet fonction)</span><span class="sxs-lookup"><span data-stu-id="664eb-103">D3DXCreateCompressedAnimationSet function</span></span>

<span data-ttu-id="664eb-104">Crée une interface de jeu d’animations à clé [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) qui stocke les données d’image clé dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="664eb-104">Creates a [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) key framed animation set interface that stores key frame data in a compressed format.</span></span>

## <a name="syntax"></a><span data-ttu-id="664eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="664eb-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="664eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="664eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="664eb-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="664eb-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="664eb-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="664eb-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="664eb-109">Pointeur vers le nom de l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="664eb-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="664eb-110">*TicksPerSecond* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="664eb-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="664eb-111">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="664eb-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="664eb-112">Nombre de battements d’image clé qui s’écoulent par seconde.</span><span class="sxs-lookup"><span data-stu-id="664eb-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="664eb-113">*Lecture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="664eb-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="664eb-114">Type : **[ **D3DXPLAYBACK \_**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="664eb-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="664eb-115">Type de la boucle de lecture du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="664eb-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="664eb-116">Consultez [**\_ type D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="664eb-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="664eb-117">*pCompressedData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="664eb-117">*pCompressedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="664eb-118">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="664eb-118">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="664eb-119">Pointeur vers la mémoire tampon [**ID3DXBuffer**](id3dxbuffer.md) qui stocke l’animation définie en tant que données compressées.</span><span class="sxs-lookup"><span data-stu-id="664eb-119">Pointer to the [**ID3DXBuffer**](id3dxbuffer.md) buffer that stores the animation set as compressed data.</span></span>

</dd> <dt>

<span data-ttu-id="664eb-120">*NumCallbackKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="664eb-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="664eb-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="664eb-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="664eb-122">Nombre de clés de rappel.</span><span class="sxs-lookup"><span data-stu-id="664eb-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="664eb-123">*pCallKeys* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="664eb-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="664eb-124">Type : **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="664eb-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="664eb-125">Pointeur vers une structure de [**\_ rappel D3DXKEY**](d3dxkey-callback.md) qui stocke les données de rappel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="664eb-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="664eb-126">*ppAnimationSet* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="664eb-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="664eb-127">Type : **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="664eb-127">Type: **[**LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span></span>

<span data-ttu-id="664eb-128">Adresse d’un pointeur vers l’interface [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) qui stocke les données du jeu d’animations des clés dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="664eb-128">Address of a pointer to the [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) interface that stores key framed animation set data in a compressed format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="664eb-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="664eb-129">Return value</span></span>

<span data-ttu-id="664eb-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="664eb-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="664eb-131">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="664eb-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="664eb-132">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="664eb-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="664eb-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="664eb-133">Requirements</span></span>



| <span data-ttu-id="664eb-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="664eb-134">Requirement</span></span> | <span data-ttu-id="664eb-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="664eb-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="664eb-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="664eb-136">Header</span></span><br/>  | <dl> <span data-ttu-id="664eb-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="664eb-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="664eb-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="664eb-138">Library</span></span><br/> | <dl> <span data-ttu-id="664eb-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="664eb-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="664eb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="664eb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="664eb-141">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="664eb-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
