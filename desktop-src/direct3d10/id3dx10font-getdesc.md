---
description: Obtient une description de l’objet de police en cours.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'ID3DX10Font :: GetDesc, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523210"
---
# <a name="id3dx10fontgetdesc-method"></a><span data-ttu-id="cb43e-103">ID3DX10Font :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="cb43e-103">ID3DX10Font::GetDesc method</span></span>

<span data-ttu-id="cb43e-104">Obtient une description de l’objet de police en cours.</span><span class="sxs-lookup"><span data-stu-id="cb43e-104">Get a description of the current font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb43e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb43e-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="cb43e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb43e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb43e-107">*pDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb43e-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb43e-108">Type : description de la **[ **\_ police \_ d3dx10**](d3dx10-font-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb43e-108">Type: **[**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="cb43e-109">Pointeur vers une [**structure \_ \_ desc de police d3dx10**](d3dx10-font-desc.md) qui décrit l’objet font.</span><span class="sxs-lookup"><span data-stu-id="cb43e-109">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure that describes the font object.</span></span> <span data-ttu-id="cb43e-110">Si UNICODE est défini, un pointeur vers un D3DX10FONT \_ DESCW est retourné ; sinon, un pointeur vers un D3DX10FONT \_ DESCA est retourné.</span><span class="sxs-lookup"><span data-stu-id="cb43e-110">If UNICODE is defined, a pointer to a D3DX10FONT\_DESCW is returned; otherwise a pointer to a D3DX10FONT\_DESCA is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb43e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb43e-111">Return value</span></span>

<span data-ttu-id="cb43e-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb43e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb43e-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb43e-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cb43e-114">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cb43e-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb43e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cb43e-115">Remarks</span></span>

<span data-ttu-id="cb43e-116">Cette méthode décrit les objets de police Unicode si UNICODE est défini.</span><span class="sxs-lookup"><span data-stu-id="cb43e-116">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="cb43e-117">Sinon, GetDescA est appelé, ce qui retourne un pointeur vers la \_ structure D3DX10FONT DESCA.</span><span class="sxs-lookup"><span data-stu-id="cb43e-117">Otherwise GetDescA is called, which returns a pointer to the D3DX10FONT\_DESCA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb43e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb43e-118">Requirements</span></span>



| <span data-ttu-id="cb43e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb43e-119">Requirement</span></span> | <span data-ttu-id="cb43e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb43e-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb43e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb43e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cb43e-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb43e-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb43e-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb43e-123">Library</span></span><br/> | <dl> <span data-ttu-id="cb43e-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb43e-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb43e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb43e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb43e-126">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="cb43e-126">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="cb43e-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cb43e-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




