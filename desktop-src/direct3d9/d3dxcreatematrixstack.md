---
description: Crée une instance de l’interface ID3DXMATRIXStack.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: D3DXCreateMatrixStack, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537276"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a><span data-ttu-id="cb565-103">D3DXCreateMatrixStack, fonction (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cb565-103">D3DXCreateMatrixStack function (D3dx9math.h)</span></span>

<span data-ttu-id="cb565-104">Crée une instance de l’interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="cb565-104">Creates an instance of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb565-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb565-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="cb565-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb565-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="cb565-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb565-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb565-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb565-109">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="cb565-109">Not implemented.</span></span> <span data-ttu-id="cb565-110">Spécifiez zéro.</span><span class="sxs-lookup"><span data-stu-id="cb565-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="cb565-111">*ppStack* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cb565-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb565-112">Type : **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="cb565-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="cb565-113">Adresse d’un pointeur rempli avec un pointeur d’interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) si la fonction est réussie.</span><span class="sxs-lookup"><span data-stu-id="cb565-113">Address of a pointer filled with an [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface pointer if the function succeeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb565-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb565-114">Return value</span></span>

<span data-ttu-id="cb565-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb565-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb565-116">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb565-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cb565-117">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cb565-117">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb565-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb565-118">Requirements</span></span>



| <span data-ttu-id="cb565-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb565-119">Requirement</span></span> | <span data-ttu-id="cb565-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb565-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb565-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb565-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cb565-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb565-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cb565-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb565-123">Library</span></span><br/> | <dl> <span data-ttu-id="cb565-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb565-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb565-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb565-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb565-126">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="cb565-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
