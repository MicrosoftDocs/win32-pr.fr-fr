---
description: Définit la description de la piste.
ms.assetid: bc3324b3-ca23-4035-958d-9763a70071f2
title: 'ID3DXAnimationController :: SetTrackDesc, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1aca9385f1e9bc9439b9fe4b3dc1acddda94e395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529255"
---
# <a name="id3dxanimationcontrollersettrackdesc-method"></a><span data-ttu-id="f5d3a-103">ID3DXAnimationController :: SetTrackDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="f5d3a-103">ID3DXAnimationController::SetTrackDesc method</span></span>

<span data-ttu-id="f5d3a-104">Définit la description de la piste.</span><span class="sxs-lookup"><span data-stu-id="f5d3a-104">Sets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d3a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5d3a-105">Syntax</span></span>


```C++
HRESULT SetTrackDesc(
  [in] UINT             Track,
  [in] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="f5d3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5d3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d3a-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5d3a-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d3a-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5d3a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f5d3a-109">Identificateur de la piste à modifier.</span><span class="sxs-lookup"><span data-stu-id="f5d3a-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="f5d3a-110">*pDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5d3a-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d3a-111">Type : **[ **LPD3DXTRACK \_ desc**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="f5d3a-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="f5d3a-112">Description de la piste.</span><span class="sxs-lookup"><span data-stu-id="f5d3a-112">Description of the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d3a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5d3a-113">Return value</span></span>

<span data-ttu-id="f5d3a-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f5d3a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f5d3a-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f5d3a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f5d3a-116">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f5d3a-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d3a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5d3a-117">Requirements</span></span>



| <span data-ttu-id="f5d3a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5d3a-118">Requirement</span></span> | <span data-ttu-id="f5d3a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5d3a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d3a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5d3a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f5d3a-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d3a-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f5d3a-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5d3a-122">Library</span></span><br/> | <dl> <span data-ttu-id="f5d3a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5d3a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f5d3a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5d3a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d3a-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f5d3a-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
