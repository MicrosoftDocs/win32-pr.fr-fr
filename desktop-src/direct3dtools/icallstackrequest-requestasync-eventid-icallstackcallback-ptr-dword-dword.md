---
description: Requête asynchrone pour obtenir les adresses RVA de la pile des appels (adresses virtuelles relatives) de l’événement spécifié.
MS-HAID: vspixengine.ICallStackRequest\_RequestAsync\_EventID\_ICallStackCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ICallStackRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1951716F-5382-41EE-90BB-A9053DB38A78
api_name:
- ICallStackRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cad4007a8bc3d0e7b7c9cf1efc7218ce09813a5a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200761"
---
# <a name="span-idvspixengineicallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dwordspanicallstackrequestrequestasync-method"></a><span data-ttu-id="0209e-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="0209e-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest::RequestAsync method</span></span>

<span data-ttu-id="0209e-104">Requête asynchrone pour obtenir les adresses RVA de la pile des appels (adresses virtuelles relatives) de l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="0209e-104">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="0209e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0209e-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID              eventID,
   ICallStackCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="0209e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0209e-106">Parameters</span></span>

<span data-ttu-id="0209e-107">*1001* </span><span class="sxs-lookup"><span data-stu-id="0209e-107">*eventID* </span></span>  
<span data-ttu-id="0209e-108">Événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="0209e-108">The specified event.</span></span>

<span data-ttu-id="0209e-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="0209e-109">*requestCallback* </span></span>  
<span data-ttu-id="0209e-110">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="0209e-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="0209e-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="0209e-111">*requestCookie* </span></span>  
<span data-ttu-id="0209e-112">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="0209e-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="0209e-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="0209e-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="0209e-114">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="0209e-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="0209e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0209e-115">Return value</span></span>

<span data-ttu-id="0209e-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0209e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0209e-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0209e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0209e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0209e-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0209e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0209e-119">Header</span></span></p></td><td><span data-ttu-id="0209e-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0209e-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0209e-121"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0209e-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0209e-122">**ICallStackRequest**</span><span class="sxs-lookup"><span data-stu-id="0209e-122">**ICallStackRequest**</span></span>](/windows/desktop/direct3dtools/icallstackrequest)

 

 
