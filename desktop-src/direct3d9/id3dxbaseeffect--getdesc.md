---
description: Obtient la description de l’effet.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'ID3DXBaseEffect :: GetDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545314"
---
# <a name="id3dxbaseeffectgetdesc-method"></a><span data-ttu-id="a43a8-103">ID3DXBaseEffect :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="a43a8-103">ID3DXBaseEffect::GetDesc method</span></span>

<span data-ttu-id="a43a8-104">Obtient la description de l’effet.</span><span class="sxs-lookup"><span data-stu-id="a43a8-104">Gets the effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a43a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a43a8-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a43a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a43a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a43a8-107">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a43a8-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a43a8-108">Type : **[ **D3DXEFFECT \_ desc**](d3dxeffect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a43a8-108">Type: **[**D3DXEFFECT\_DESC**](d3dxeffect-desc.md)\***</span></span>

<span data-ttu-id="a43a8-109">Retourne une description de l’effet.</span><span class="sxs-lookup"><span data-stu-id="a43a8-109">Returns a description of the effect.</span></span> <span data-ttu-id="a43a8-110">Consultez [**D3DXEFFECT \_ desc**](d3dxeffect-desc.md).</span><span class="sxs-lookup"><span data-stu-id="a43a8-110">See [**D3DXEFFECT\_DESC**](d3dxeffect-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a43a8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a43a8-111">Return value</span></span>

<span data-ttu-id="a43a8-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a43a8-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a43a8-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a43a8-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a43a8-114">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a43a8-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a43a8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a43a8-115">Requirements</span></span>



| <span data-ttu-id="a43a8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a43a8-116">Requirement</span></span> | <span data-ttu-id="a43a8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a43a8-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a43a8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="a43a8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a43a8-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a43a8-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a43a8-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a43a8-120">Library</span></span><br/> | <dl> <span data-ttu-id="a43a8-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a43a8-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a43a8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a43a8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43a8-123">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a43a8-123">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




