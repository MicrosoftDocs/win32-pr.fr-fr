---
description: Crée un objet Sprite associé à un appareil particulier. Les objets Sprit sont utilisés pour dessiner des images 2D à l’écran.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: D3DXCreateSprite, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522961"
---
# <a name="d3dxcreatesprite-function"></a><span data-ttu-id="dcdac-104">D3DXCreateSprite fonction)</span><span class="sxs-lookup"><span data-stu-id="dcdac-104">D3DXCreateSprite function</span></span>

<span data-ttu-id="dcdac-105">Crée un objet Sprite associé à un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="dcdac-105">Creates a sprite object which is associated with a particular device.</span></span> <span data-ttu-id="dcdac-106">Les objets Sprit sont utilisés pour dessiner des images 2D à l’écran.</span><span class="sxs-lookup"><span data-stu-id="dcdac-106">Sprite objects are used to draw 2D images to the screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcdac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcdac-107">Syntax</span></span>


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="dcdac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcdac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcdac-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcdac-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcdac-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="dcdac-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="dcdac-111">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’appareil à associer au Sprite.</span><span class="sxs-lookup"><span data-stu-id="dcdac-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="dcdac-112">*ppSprite* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dcdac-112">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcdac-113">Type : **[ **LPD3DXSPRITE**](id3dxsprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="dcdac-113">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)\***</span></span>

<span data-ttu-id="dcdac-114">Adresse d’un pointeur vers une interface [**ID3DXSprite**](id3dxsprite.md) .</span><span class="sxs-lookup"><span data-stu-id="dcdac-114">Address of a pointer to an [**ID3DXSprite**](id3dxsprite.md) interface.</span></span> <span data-ttu-id="dcdac-115">Cette interface permet à l’utilisateur d’accéder aux fonctions Sprite.</span><span class="sxs-lookup"><span data-stu-id="dcdac-115">This interface allows the user to access sprite functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcdac-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcdac-116">Return value</span></span>

<span data-ttu-id="dcdac-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcdac-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcdac-118">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcdac-118">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dcdac-119">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dcdac-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcdac-120">Notes</span><span class="sxs-lookup"><span data-stu-id="dcdac-120">Remarks</span></span>

<span data-ttu-id="dcdac-121">Cette interface peut être utilisée pour dessiner deux images dimensionnelles dans l’espace à l’écran de l’appareil associé.</span><span class="sxs-lookup"><span data-stu-id="dcdac-121">This interface can be used to draw two dimensional images in screen space of the associated device.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcdac-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcdac-122">Requirements</span></span>



| <span data-ttu-id="dcdac-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcdac-123">Requirement</span></span> | <span data-ttu-id="dcdac-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcdac-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcdac-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcdac-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dcdac-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcdac-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="dcdac-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dcdac-127">Library</span></span><br/> | <dl> <span data-ttu-id="dcdac-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcdac-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dcdac-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcdac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcdac-130">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="dcdac-130">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
