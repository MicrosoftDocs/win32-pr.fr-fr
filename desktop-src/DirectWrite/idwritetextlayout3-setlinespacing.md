---
title: Méthode IDWriteTextLayout3 SetLineSpacing
description: Définissez l’interligne. | Méthode IDWriteTextLayout3 SetLineSpacing
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Écriture directe de la méthode SetLineSpacing
- Méthode SetLineSpacing Write directe, interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, méthode SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531274"
---
# <a name="idwritetextlayout3setlinespacing-method"></a><span data-ttu-id="bfe85-107">IDWriteTextLayout3 :: SetLineSpacing, méthode</span><span class="sxs-lookup"><span data-stu-id="bfe85-107">IDWriteTextLayout3::SetLineSpacing method</span></span>

<span data-ttu-id="bfe85-108">Définissez l’interligne.</span><span class="sxs-lookup"><span data-stu-id="bfe85-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe85-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfe85-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="bfe85-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfe85-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfe85-111">*lineSpacingOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfe85-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfe85-112">Comment gérer l’espace entre les lignes.</span><span class="sxs-lookup"><span data-stu-id="bfe85-112">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfe85-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfe85-113">Return value</span></span>

<span data-ttu-id="bfe85-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bfe85-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bfe85-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bfe85-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe85-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfe85-116">Requirements</span></span>



| <span data-ttu-id="bfe85-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfe85-117">Requirement</span></span> | <span data-ttu-id="bfe85-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfe85-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe85-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfe85-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe85-120">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfe85-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bfe85-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfe85-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe85-122">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfe85-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bfe85-123">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfe85-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="bfe85-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="bfe85-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="bfe85-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bfe85-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="bfe85-126"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfe85-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bfe85-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bfe85-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfe85-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfe85-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bfe85-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfe85-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe85-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="bfe85-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





