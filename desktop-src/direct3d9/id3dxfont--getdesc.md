---
description: Obtient une description de l’objet de police en cours. GetDescW et GetDescA sont identiques à cette méthode, sauf qu’un pointeur est retourné à une \_ structure D3DXFONT DESCW ou D3DXFONT \_ DESCA, respectivement.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'ID3DXFont :: GetDesc, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529251"
---
# <a name="id3dxfontgetdesc-method"></a><span data-ttu-id="c8179-104">ID3DXFont :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="c8179-104">ID3DXFont::GetDesc method</span></span>

<span data-ttu-id="c8179-105">Obtient une description de l’objet de police en cours.</span><span class="sxs-lookup"><span data-stu-id="c8179-105">Gets a description of the current font object.</span></span> <span data-ttu-id="c8179-106">GetDescW et GetDescA sont identiques à cette méthode, sauf qu’un pointeur est retourné à une structure [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) ou **D3DXFONT \_ DESCA** , respectivement.</span><span class="sxs-lookup"><span data-stu-id="c8179-106">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8179-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8179-107">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="c8179-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8179-109">*pDesc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c8179-109">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8179-110">Type : **[ **D3DXFONT \_ desc**](d3dxfont-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8179-110">Type: **[**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="c8179-111">Pointeur vers une structure [**D3DXFONT \_ desc**](d3dxfont-desc.md) qui décrit l’objet font.</span><span class="sxs-lookup"><span data-stu-id="c8179-111">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure that describes the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8179-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8179-112">Return value</span></span>

<span data-ttu-id="c8179-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8179-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8179-114">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c8179-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c8179-115">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c8179-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8179-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c8179-116">Remarks</span></span>

<span data-ttu-id="c8179-117">Cette méthode décrit les objets de police Unicode si UNICODE est défini.</span><span class="sxs-lookup"><span data-stu-id="c8179-117">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="c8179-118">Sinon, GetDescA est appelé, ce qui retourne un pointeur vers la structure [**D3DXFONT \_ DESCA**](d3dxfont-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="c8179-118">Otherwise GetDescA is called, which returns a pointer to the [**D3DXFONT\_DESCA**](d3dxfont-desc.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8179-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8179-119">Requirements</span></span>



| <span data-ttu-id="c8179-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8179-120">Requirement</span></span> | <span data-ttu-id="c8179-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8179-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8179-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8179-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c8179-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8179-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c8179-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c8179-124">Library</span></span><br/> | <dl> <span data-ttu-id="c8179-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8179-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8179-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8179-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8179-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="c8179-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




