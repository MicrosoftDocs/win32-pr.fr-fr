---
description: Demande asynchrone pour obtenir des informations sur les colonnes (champs) prises en charge par ce type de demande d’événements de frame.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestSupportedColumnsAsync\_IFrameEventsCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsRequest :: RequestSupportedColumnsAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8F8ED8F7-F764-4CC8-891B-F0582F6B1337
api_name:
- IFrameEventsRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 13d4c797e338f6b0901781760a39511a1f136174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746732"
---
# <a name="span-idvspixengineiframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dwordspaniframeeventsrequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="5df8b-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest :: RequestSupportedColumnsAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="5df8b-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="5df8b-104">Demande asynchrone pour obtenir des informations sur les colonnes (champs) prises en charge par ce type de demande d’événements de frame.</span><span class="sxs-lookup"><span data-stu-id="5df8b-104">An asynchronous request to get information about what columns (fields) this frame events request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df8b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5df8b-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IFrameEventsCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5df8b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5df8b-106">Parameters</span></span>

<span data-ttu-id="5df8b-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="5df8b-107">*requestCallback* </span></span>  
<span data-ttu-id="5df8b-108">Adresse du rappel utilisée pour notifier l’hôte de résultats.</span><span class="sxs-lookup"><span data-stu-id="5df8b-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="5df8b-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="5df8b-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5df8b-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5df8b-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5df8b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5df8b-111">Return value</span></span>

<span data-ttu-id="5df8b-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5df8b-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5df8b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df8b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5df8b-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5df8b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="5df8b-115">Header</span></span></p></td><td><span data-ttu-id="5df8b-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5df8b-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5df8b-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5df8b-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5df8b-118">**IFrameEventsRequest**</span><span class="sxs-lookup"><span data-stu-id="5df8b-118">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
