---
title: Méthode IDWriteTextFormat2 SetLineSpacing
description: Définissez l’interligne. | Méthode IDWriteTextFormat2 SetLineSpacing
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- Écriture directe de la méthode SetLineSpacing
- Méthode SetLineSpacing Write directe, interface IDWriteTextFormat2
- Écriture directe de l’interface IDWriteTextFormat2, méthode SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211614"
---
# <a name="idwritetextformat2setlinespacing-method"></a><span data-ttu-id="666af-107">IDWriteTextFormat2 :: SetLineSpacing, méthode</span><span class="sxs-lookup"><span data-stu-id="666af-107">IDWriteTextFormat2::SetLineSpacing method</span></span>

<span data-ttu-id="666af-108">Définissez l’interligne.</span><span class="sxs-lookup"><span data-stu-id="666af-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="666af-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="666af-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="666af-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="666af-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="666af-111">*lineSpacingOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="666af-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="666af-112">Type : **const [**DWRITE \_ ligne \_ Spacing**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \***</span><span class="sxs-lookup"><span data-stu-id="666af-112">Type: **const [**DWRITE\_LINE\_SPACING**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)\***</span></span>

<span data-ttu-id="666af-113">Comment gérer l’espace entre les lignes.</span><span class="sxs-lookup"><span data-stu-id="666af-113">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="666af-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="666af-114">Return value</span></span>

<span data-ttu-id="666af-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="666af-115">Type: **HRESULT**</span></span>

<span data-ttu-id="666af-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="666af-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="666af-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="666af-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="666af-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="666af-118">Requirements</span></span>



| <span data-ttu-id="666af-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="666af-119">Requirement</span></span> | <span data-ttu-id="666af-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="666af-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="666af-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="666af-121">Minimum supported client</span></span><br/> | <span data-ttu-id="666af-122">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="666af-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="666af-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="666af-123">Minimum supported server</span></span><br/> | <span data-ttu-id="666af-124">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="666af-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="666af-125">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="666af-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="666af-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="666af-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="666af-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="666af-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="666af-128"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="666af-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="666af-129">DLL</span><span class="sxs-lookup"><span data-stu-id="666af-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="666af-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="666af-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="666af-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="666af-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="666af-132">**IDWriteTextFormat2**</span><span class="sxs-lookup"><span data-stu-id="666af-132">**IDWriteTextFormat2**</span></span>](idwritetextformat2.md)
</dt> </dl>

 

 





