---
description: Demande asynchrone pour obtenir des informations de synthèse sur un journal de graphisme.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISummaryRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517164"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span data-ttu-id="fd7ef-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="fd7ef-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest::RequestAsync method</span></span>

<span data-ttu-id="fd7ef-104">Demande asynchrone pour obtenir des informations de synthèse sur un journal de graphisme.</span><span class="sxs-lookup"><span data-stu-id="fd7ef-104">An asynchronous request to get summary information about a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd7ef-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fd7ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd7ef-106">Parameters</span></span>

<span data-ttu-id="fd7ef-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="fd7ef-107">*requestCallback* </span></span>  
<span data-ttu-id="fd7ef-108">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="fd7ef-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="fd7ef-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="fd7ef-109">*requestCookie* </span></span>  
<span data-ttu-id="fd7ef-110">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="fd7ef-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="fd7ef-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="fd7ef-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fd7ef-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="fd7ef-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd7ef-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd7ef-113">Return value</span></span>

<span data-ttu-id="fd7ef-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fd7ef-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd7ef-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd7ef-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7ef-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd7ef-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fd7ef-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd7ef-117">Header</span></span></p></td><td><span data-ttu-id="fd7ef-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fd7ef-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fd7ef-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd7ef-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fd7ef-120">**ISummaryRequest**</span><span class="sxs-lookup"><span data-stu-id="fd7ef-120">**ISummaryRequest**</span></span>](/windows/desktop/direct3dtools/isummaryrequest)

 

 
