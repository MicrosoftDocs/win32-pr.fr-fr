---
description: Demande asynchrone pour obtenir une liste des étapes utilisées pour le frame et l’événement spécifiés.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestSupportedStagesAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest :: RequestSupportedStagesAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C636FC40-0505-486B-B25D-9B424F5A584D
api_name:
- IPipeLineStagesRequest.RequestSupportedStagesAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0c3ebedee8dba4d7630d1bdff60bdaf479ea3561
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543441"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequestrequestsupportedstagesasync-method"></a><span data-ttu-id="c9370-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest :: RequestSupportedStagesAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="c9370-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest::RequestSupportedStagesAsync method</span></span>

<span data-ttu-id="c9370-104">Demande asynchrone pour obtenir une liste des étapes utilisées pour le frame et l’événement spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c9370-104">An asynchronous request to get a list of stages used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9370-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9370-105">Syntax</span></span>


```C++
HRESULT RequestSupportedStagesAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="c9370-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9370-106">Parameters</span></span>

<span data-ttu-id="c9370-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="c9370-107">*frameNumber* </span></span>  
<span data-ttu-id="c9370-108">Frame spécifié.</span><span class="sxs-lookup"><span data-stu-id="c9370-108">The specified frame.</span></span>

<span data-ttu-id="c9370-109">*1001* </span><span class="sxs-lookup"><span data-stu-id="c9370-109">*eventID* </span></span>  
<span data-ttu-id="c9370-110">Événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="c9370-110">The specified event.</span></span>

<span data-ttu-id="c9370-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="c9370-111">*requestCallback* </span></span>  
<span data-ttu-id="c9370-112">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="c9370-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="c9370-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="c9370-113">*requestCookie* </span></span>  
<span data-ttu-id="c9370-114">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="c9370-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="c9370-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="c9370-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="c9370-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c9370-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9370-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9370-117">Return value</span></span>

<span data-ttu-id="c9370-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c9370-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9370-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9370-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9370-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9370-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c9370-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9370-121">Header</span></span></p></td><td><span data-ttu-id="c9370-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c9370-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c9370-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9370-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c9370-124">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="c9370-124">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
