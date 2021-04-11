---
title: Méthode IDWriteTextLayout3 GetLineSpacing
description: Obtient les informations d’interligne.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Écriture directe de la méthode GetLineSpacing
- Méthode GetLineSpacing Write directe, interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, méthode GetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942362"
---
# <a name="idwritetextlayout3getlinespacing-method"></a><span data-ttu-id="22879-106">IDWriteTextLayout3 :: GetLineSpacing, méthode</span><span class="sxs-lookup"><span data-stu-id="22879-106">IDWriteTextLayout3::GetLineSpacing method</span></span>

<span data-ttu-id="22879-107">Obtient les informations d’interligne.</span><span class="sxs-lookup"><span data-stu-id="22879-107">Gets line spacing information.</span></span>

## <a name="syntax"></a><span data-ttu-id="22879-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22879-108">Syntax</span></span>


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="22879-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22879-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22879-110">*lineSpacingOptions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="22879-110">*lineSpacingOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22879-111">Comment gérer l’espace entre les lignes.</span><span class="sxs-lookup"><span data-stu-id="22879-111">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22879-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22879-112">Return value</span></span>

<span data-ttu-id="22879-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="22879-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22879-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22879-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="22879-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22879-115">Requirements</span></span>



| <span data-ttu-id="22879-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22879-116">Requirement</span></span> | <span data-ttu-id="22879-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="22879-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22879-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22879-118">Minimum supported client</span></span><br/> | <span data-ttu-id="22879-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22879-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="22879-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22879-120">Minimum supported server</span></span><br/> | <span data-ttu-id="22879-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22879-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="22879-122">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22879-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="22879-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="22879-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="22879-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22879-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="22879-125"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22879-125"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="22879-126">DLL</span><span class="sxs-lookup"><span data-stu-id="22879-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22879-127"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22879-127"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22879-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22879-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22879-129">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="22879-129">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





