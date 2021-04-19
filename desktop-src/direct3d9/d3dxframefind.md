---
description: Recherche le frame enfant d’un frame racine.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: D3DXFrameFind, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522354"
---
# <a name="d3dxframefind-function"></a><span data-ttu-id="9230e-103">D3DXFrameFind fonction)</span><span class="sxs-lookup"><span data-stu-id="9230e-103">D3DXFrameFind function</span></span>

<span data-ttu-id="9230e-104">Recherche le frame enfant d’un frame racine.</span><span class="sxs-lookup"><span data-stu-id="9230e-104">Finds the child frame of a root frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="9230e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9230e-105">Syntax</span></span>


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a><span data-ttu-id="9230e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9230e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9230e-107">*pFrameRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9230e-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9230e-108">Type : **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="9230e-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="9230e-109">Pointeur vers le frame racine.</span><span class="sxs-lookup"><span data-stu-id="9230e-109">Pointer to the root frame.</span></span> <span data-ttu-id="9230e-110">Consultez [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="9230e-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9230e-111">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9230e-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9230e-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9230e-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9230e-113">Nom du Frame enfant à rechercher.</span><span class="sxs-lookup"><span data-stu-id="9230e-113">Name of the child frame to find.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9230e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9230e-114">Return value</span></span>

<span data-ttu-id="9230e-115">Type : **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="9230e-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="9230e-116">Retourne le frame enfant s’il est trouvé, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9230e-116">Returns the child frame if it is found, or **NULL** otherwise.</span></span> <span data-ttu-id="9230e-117">Consultez [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="9230e-117">See [**D3DXFRAME**](d3dxframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9230e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9230e-118">Requirements</span></span>



| <span data-ttu-id="9230e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9230e-119">Requirement</span></span> | <span data-ttu-id="9230e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9230e-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9230e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9230e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9230e-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9230e-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9230e-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9230e-123">Library</span></span><br/> | <dl> <span data-ttu-id="9230e-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9230e-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9230e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9230e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9230e-126">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="9230e-126">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
