---
description: Demande asynchrone pour lancer une action (par exemple, capturer un frame) dans le moteur.
MS-HAID: vspixengine.IRunActionRequest\_RequestAsync\_REFGUID\_IUnknown\_ptr\_IRunActionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IRunActionRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4A4DF4BE-383D-4B36-9195-61720C3B4D97
api_name:
- IRunActionRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 179abf44231d122ca82527fc5739b876395c327b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109742"
---
# <a name="span-idvspixengineirunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dwordspanirunactionrequestrequestasync-method"></a><span data-ttu-id="f5357-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest :: RequestAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="f5357-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest::RequestAsync method</span></span>

<span data-ttu-id="f5357-104">Demande asynchrone pour lancer une action (par exemple, capturer un frame) dans le moteur.</span><span class="sxs-lookup"><span data-stu-id="f5357-104">An asynchronous request to initiate an action (for example, capture a frame) in the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5357-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5357-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   REFGUID              action,
   IUnknown *           actionPayload,
   IRunActionCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f5357-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5357-106">Parameters</span></span>

<span data-ttu-id="f5357-107">*transactionnel* </span><span class="sxs-lookup"><span data-stu-id="f5357-107">*action* </span></span>  
<span data-ttu-id="f5357-108">Action spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f5357-108">The specified action.</span></span>

<span data-ttu-id="f5357-109">*actionPayload* </span><span class="sxs-lookup"><span data-stu-id="f5357-109">*actionPayload* </span></span>  
<span data-ttu-id="f5357-110">Charge utile de l’action spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f5357-110">The payload of the specified action.</span></span>

<span data-ttu-id="f5357-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="f5357-111">*requestCallback* </span></span>  
<span data-ttu-id="f5357-112">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="f5357-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="f5357-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="f5357-113">*requestCookie* </span></span>  
<span data-ttu-id="f5357-114">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="f5357-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="f5357-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="f5357-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f5357-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="f5357-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5357-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5357-117">Return value</span></span>

<span data-ttu-id="f5357-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5357-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5357-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5357-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5357-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5357-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f5357-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5357-121">Header</span></span></p></td><td><span data-ttu-id="f5357-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f5357-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f5357-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5357-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f5357-124">**IRunActionRequest**</span><span class="sxs-lookup"><span data-stu-id="f5357-124">**IRunActionRequest**</span></span>](/windows/desktop/direct3dtools/irunactionrequest)

 

 
