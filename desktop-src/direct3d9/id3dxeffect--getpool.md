---
description: Obtient un pointeur vers le pool de paramètres partagés.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'ID3DXEffect :: GetPool, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953812"
---
# <a name="id3dxeffectgetpool-method"></a><span data-ttu-id="b45de-103">ID3DXEffect :: GetPool, méthode</span><span class="sxs-lookup"><span data-stu-id="b45de-103">ID3DXEffect::GetPool method</span></span>

<span data-ttu-id="b45de-104">Obtient un pointeur vers le pool de paramètres partagés.</span><span class="sxs-lookup"><span data-stu-id="b45de-104">Gets a pointer to the pool of shared parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b45de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b45de-105">Syntax</span></span>


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="b45de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b45de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b45de-107">*ppPool* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b45de-107">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b45de-108">Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="b45de-108">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="b45de-109">Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="b45de-109">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b45de-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b45de-110">Return value</span></span>

<span data-ttu-id="b45de-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b45de-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b45de-112">Cette méthode retourne toujours la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b45de-112">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b45de-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b45de-113">Remarks</span></span>

<span data-ttu-id="b45de-114">Les pools contiennent des paramètres partagés entre les effets.</span><span class="sxs-lookup"><span data-stu-id="b45de-114">Pools contain shared parameters between effects.</span></span> <span data-ttu-id="b45de-115">Consultez [clonage et partage (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="b45de-115">See [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b45de-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b45de-116">Requirements</span></span>



| <span data-ttu-id="b45de-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b45de-117">Requirement</span></span> | <span data-ttu-id="b45de-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b45de-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45de-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="b45de-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b45de-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b45de-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b45de-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b45de-121">Library</span></span><br/> | <dl> <span data-ttu-id="b45de-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b45de-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b45de-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b45de-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b45de-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="b45de-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




