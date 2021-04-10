---
description: Obtient la description de la piste.
ms.assetid: 7663a26f-5ad3-4a17-a502-c0dcfa730db2
title: 'ID3DXAnimationController :: GetTrackDesc, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 940b43ede480766155d09ebe51dfb55eba114c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762157"
---
# <a name="id3dxanimationcontrollergettrackdesc-method"></a><span data-ttu-id="f7414-103">ID3DXAnimationController :: GetTrackDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="f7414-103">ID3DXAnimationController::GetTrackDesc method</span></span>

<span data-ttu-id="f7414-104">Obtient la description de la piste.</span><span class="sxs-lookup"><span data-stu-id="f7414-104">Gets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7414-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7414-105">Syntax</span></span>


```C++
HRESULT GetTrackDesc(
  [in]  UINT             Track,
  [out] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="f7414-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7414-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7414-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7414-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7414-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7414-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7414-109">Identificateur de suivi.</span><span class="sxs-lookup"><span data-stu-id="f7414-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f7414-110">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f7414-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7414-111">Type : **[ **LPD3DXTRACK \_ desc**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="f7414-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="f7414-112">Pointeur vers la description de la piste.</span><span class="sxs-lookup"><span data-stu-id="f7414-112">Pointer to the track description.</span></span> <span data-ttu-id="f7414-113">Consultez [**D3DXTRACK \_ desc**](d3dxtrack-desc.md).</span><span class="sxs-lookup"><span data-stu-id="f7414-113">See [**D3DXTRACK\_DESC**](d3dxtrack-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7414-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7414-114">Return value</span></span>

<span data-ttu-id="f7414-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7414-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7414-116">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f7414-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f7414-117">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f7414-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7414-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7414-118">Requirements</span></span>



| <span data-ttu-id="f7414-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7414-119">Requirement</span></span> | <span data-ttu-id="f7414-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7414-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7414-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7414-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f7414-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7414-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f7414-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f7414-123">Library</span></span><br/> | <dl> <span data-ttu-id="f7414-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7414-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7414-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7414-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7414-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f7414-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
