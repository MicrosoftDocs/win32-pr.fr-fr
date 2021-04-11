---
description: Préparez un appareil pour dessiner des sprites.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'ID3DX10Sprite :: Begin, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211854"
---
# <a name="id3dx10spritebegin-method"></a><span data-ttu-id="58c4f-103">ID3DX10Sprite :: Begin, méthode</span><span class="sxs-lookup"><span data-stu-id="58c4f-103">ID3DX10Sprite::Begin method</span></span>

<span data-ttu-id="58c4f-104">Préparez un appareil pour dessiner des sprites.</span><span class="sxs-lookup"><span data-stu-id="58c4f-104">Prepare a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c4f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58c4f-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a><span data-ttu-id="58c4f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58c4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c4f-107">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58c4f-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c4f-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58c4f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58c4f-109">Indicateurs qui contrôlent la façon dont les sprites seront dessinés.</span><span class="sxs-lookup"><span data-stu-id="58c4f-109">Flags that control how the sprites will be drawn.</span></span> <span data-ttu-id="58c4f-110">Consultez [**\_ \_ indicateur Sprite d3dx10**](d3dx10-sprite-flag.md).</span><span class="sxs-lookup"><span data-stu-id="58c4f-110">See [**D3DX10\_SPRITE\_FLAG**](d3dx10-sprite-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c4f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58c4f-111">Return value</span></span>

<span data-ttu-id="58c4f-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58c4f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58c4f-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58c4f-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="58c4f-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="58c4f-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="58c4f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="58c4f-115">Remarks</span></span>

<span data-ttu-id="58c4f-116">Chaque appel à Begin doit être mis en correspondance avec un appel à [**ID3DX10Sprite :: end**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="58c4f-116">Every call to Begin must be matched with a call to [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58c4f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58c4f-117">Requirements</span></span>



| <span data-ttu-id="58c4f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58c4f-118">Requirement</span></span> | <span data-ttu-id="58c4f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="58c4f-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58c4f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="58c4f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="58c4f-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="58c4f-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="58c4f-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58c4f-122">Library</span></span><br/> | <dl> <span data-ttu-id="58c4f-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58c4f-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58c4f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58c4f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c4f-125">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="58c4f-125">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="58c4f-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="58c4f-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
