---
description: Crée une copie d’un effet.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'ID3DXEffect :: CloneEffect, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527109"
---
# <a name="id3dxeffectcloneeffect-method"></a><span data-ttu-id="50c6b-103">ID3DXEffect :: CloneEffect, méthode</span><span class="sxs-lookup"><span data-stu-id="50c6b-103">ID3DXEffect::CloneEffect method</span></span>

<span data-ttu-id="50c6b-104">Crée une copie d’un effet.</span><span class="sxs-lookup"><span data-stu-id="50c6b-104">Creates a copy of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50c6b-105">Syntax</span></span>


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="50c6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50c6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50c6b-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50c6b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50c6b-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="50c6b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="50c6b-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à l’effet.</span><span class="sxs-lookup"><span data-stu-id="50c6b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> <dt>

<span data-ttu-id="50c6b-110">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="50c6b-110">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50c6b-111">Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="50c6b-111">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="50c6b-112">Pointeur vers une interface [**ID3DXEffect**](id3dxeffect.md) contenant l’effet cloné.</span><span class="sxs-lookup"><span data-stu-id="50c6b-112">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface, containing the cloned effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50c6b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50c6b-113">Return value</span></span>

<span data-ttu-id="50c6b-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50c6b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50c6b-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="50c6b-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="50c6b-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="50c6b-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="50c6b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="50c6b-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="50c6b-118">Cette fonction ne clone pas un effet si l’utilisateur spécifie que [D3DXFX \_ ne peut pas être \_ cloné](d3dxfx.md) pendant la création de l’effet.</span><span class="sxs-lookup"><span data-stu-id="50c6b-118">This function will not clone an effect if the user specifies [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md) during effect creation.</span></span>

 

<span data-ttu-id="50c6b-119">Pour mettre à jour des paramètres partagés et non partagés dans une technique active d’un effet cloné, consultez [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md).</span><span class="sxs-lookup"><span data-stu-id="50c6b-119">To update shared and non-shared parameters in an active technique of a cloned effect, see [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50c6b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50c6b-120">Requirements</span></span>



| <span data-ttu-id="50c6b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50c6b-121">Requirement</span></span> | <span data-ttu-id="50c6b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="50c6b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c6b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="50c6b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="50c6b-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="50c6b-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="50c6b-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50c6b-125">Library</span></span><br/> | <dl> <span data-ttu-id="50c6b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50c6b-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="50c6b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50c6b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c6b-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="50c6b-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
