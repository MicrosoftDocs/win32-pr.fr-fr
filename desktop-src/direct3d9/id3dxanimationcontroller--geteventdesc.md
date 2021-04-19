---
description: Obtient une description d’un événement d’animation spécifié.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'ID3DXAnimationController :: GetEventDesc, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531370"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a><span data-ttu-id="64d18-103">ID3DXAnimationController :: GetEventDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="64d18-103">ID3DXAnimationController::GetEventDesc method</span></span>

<span data-ttu-id="64d18-104">Obtient une description d’un événement d’animation spécifié.</span><span class="sxs-lookup"><span data-stu-id="64d18-104">Gets a description of a specified animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d18-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64d18-105">Syntax</span></span>


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="64d18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64d18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d18-107">*hEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64d18-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d18-108">Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="64d18-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="64d18-109">Handle d’événement vers un événement d’animation à décrire.</span><span class="sxs-lookup"><span data-stu-id="64d18-109">Event handle to an animation event to describe.</span></span>

</dd> <dt>

<span data-ttu-id="64d18-110">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64d18-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64d18-111">Type : **[ **LPD3DXEVENT \_ desc**](d3dxevent-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="64d18-111">Type: **[**LPD3DXEVENT\_DESC**](d3dxevent-desc.md)**</span></span>

<span data-ttu-id="64d18-112">Pointeur vers une structure [**D3DXEVENT \_ desc**](d3dxevent-desc.md) qui contient une description de l’événement d’animation.</span><span class="sxs-lookup"><span data-stu-id="64d18-112">Pointer to a [**D3DXEVENT\_DESC**](d3dxevent-desc.md) structure that contains a description of the animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d18-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64d18-113">Return value</span></span>

<span data-ttu-id="64d18-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64d18-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64d18-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64d18-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="64d18-116">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="64d18-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d18-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64d18-117">Requirements</span></span>



| <span data-ttu-id="64d18-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64d18-118">Requirement</span></span> | <span data-ttu-id="64d18-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="64d18-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64d18-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="64d18-120">Header</span></span><br/>  | <dl> <span data-ttu-id="64d18-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="64d18-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="64d18-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64d18-122">Library</span></span><br/> | <dl> <span data-ttu-id="64d18-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64d18-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64d18-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d18-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="64d18-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




