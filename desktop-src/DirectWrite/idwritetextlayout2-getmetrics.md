---
title: Méthode IDWriteTextLayout2 GetMetrics
description: Récupère les métriques globales de la chaîne mise en forme.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Écriture directe de la méthode GetMetrics
- Méthode GetMetrics Write directe, interface IDWriteTextLayout2
- Écriture directe de l’interface IDWriteTextLayout2, méthode GetMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106533571"
---
# <a name="idwritetextlayout2getmetrics-method"></a><span data-ttu-id="f25ee-106">IDWriteTextLayout2 :: GetMetrics, méthode</span><span class="sxs-lookup"><span data-stu-id="f25ee-106">IDWriteTextLayout2::GetMetrics method</span></span>

<span data-ttu-id="f25ee-107">Récupère les métriques globales de la chaîne mise en forme.</span><span class="sxs-lookup"><span data-stu-id="f25ee-107">Retrieves overall metrics for the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f25ee-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f25ee-108">Syntax</span></span>


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f25ee-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f25ee-109">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="f25ee-110">*textMetrics* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f25ee-110">*textMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f25ee-111">Type : \**[**DWRITE \_ texte \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _ _</span><span class="sxs-lookup"><span data-stu-id="f25ee-111">Type: \**[**DWRITE\_TEXT\_METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\** _</span></span>

<span data-ttu-id="f25ee-112">Lorsque cette méthode est retournée, contient les distances mesurées du texte et du contenu associé après avoir été mis en forme.</span><span class="sxs-lookup"><span data-stu-id="f25ee-112">When this method returns, contains the measured distances of text and associated content after being formatted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f25ee-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f25ee-113">Return value</span></span>

<span data-ttu-id="f25ee-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f25ee-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f25ee-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f25ee-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f25ee-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f25ee-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f25ee-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f25ee-117">Requirements</span></span>



| <span data-ttu-id="f25ee-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f25ee-118">Requirement</span></span> | <span data-ttu-id="f25ee-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f25ee-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f25ee-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f25ee-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f25ee-121">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f25ee-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="f25ee-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f25ee-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f25ee-123">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f25ee-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f25ee-124">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f25ee-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="f25ee-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="f25ee-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="f25ee-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f25ee-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f25ee-127"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f25ee-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f25ee-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f25ee-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f25ee-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f25ee-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f25ee-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f25ee-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f25ee-131">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="f25ee-131">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





