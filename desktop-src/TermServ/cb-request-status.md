---
title: Énumération CB_REQUEST_STATUS (Cbclient. h)
description: Spécifie l’état d’une demande asynchrone.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- Énumération CB_REQUEST_STATUS Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317190"
---
# <a name="cb_request_status-enumeration"></a><span data-ttu-id="12940-104">Énumération de l’état de la \_ demande CB \_</span><span class="sxs-lookup"><span data-stu-id="12940-104">CB\_REQUEST\_STATUS enumeration</span></span>

<span data-ttu-id="12940-105">Spécifie l’état d’une demande asynchrone.</span><span class="sxs-lookup"><span data-stu-id="12940-105">Specifies the status of an asynchronous request.</span></span> <span data-ttu-id="12940-106">Cette énumération est utilisée avec la méthode [**IConnectionBrokerRequest :: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="12940-106">This enumeration is used with the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12940-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12940-107">Syntax</span></span>


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a><span data-ttu-id="12940-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="12940-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="12940-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**\_État CB \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="12940-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB\_STATUS\_INVALID**</span></span>
</dt> <dd>

<span data-ttu-id="12940-110">L’objet de requête n’est pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="12940-110">The request object is not initialized.</span></span>

</dd> <dt>

<span data-ttu-id="12940-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**État CB à l’origine de la \_ \_ \_ demande**</span><span class="sxs-lookup"><span data-stu-id="12940-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB\_STATUS\_INITIATING\_REQUEST**</span></span>
</dt> <dd>

<span data-ttu-id="12940-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="12940-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="12940-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_demande d’État CB \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="12940-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB\_STATUS\_REQUEST\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="12940-114">La demande est terminée.</span><span class="sxs-lookup"><span data-stu-id="12940-114">The request is complete.</span></span>

</dd> <dt>

<span data-ttu-id="12940-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**échec de la \_ demande d’État CB \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12940-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB\_STATUS\_REQUEST\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="12940-116">La demande a échoué.</span><span class="sxs-lookup"><span data-stu-id="12940-116">The request failed.</span></span>

</dd> <dt>

<span data-ttu-id="12940-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_demande d’État CB \_ \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="12940-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB\_STATUS\_REQUEST\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="12940-118">La demande a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="12940-118">The request was aborted.</span></span>

</dd> <dt>

<span data-ttu-id="12940-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**\_État CB \_ recherchant la \_ destination**</span><span class="sxs-lookup"><span data-stu-id="12940-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB\_STATUS\_FINDING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="12940-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="12940-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="12940-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**DESTINATION de chargement de l' \_ État CB \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12940-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB\_STATUS\_LOADING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="12940-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="12940-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="12940-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**État CB pour la \_ \_ \_ session \_ en ligne**</span><span class="sxs-lookup"><span data-stu-id="12940-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB\_STATUS\_BRINGING\_SESSION\_ONLINE**</span></span>
</dt> <dd>

<span data-ttu-id="12940-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="12940-124">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="12940-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_État CB \_ Redirigé \_ vers la \_ destination**</span><span class="sxs-lookup"><span data-stu-id="12940-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB\_STATUS\_REDIRECTING\_TO\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="12940-126">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="12940-126">Not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12940-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12940-127">Requirements</span></span>



| <span data-ttu-id="12940-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12940-128">Requirement</span></span> | <span data-ttu-id="12940-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="12940-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12940-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12940-130">Minimum supported client</span></span><br/> | <span data-ttu-id="12940-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="12940-131">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="12940-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12940-132">Minimum supported server</span></span><br/> | <span data-ttu-id="12940-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12940-133">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="12940-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="12940-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="12940-135"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="12940-135"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12940-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12940-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12940-137">**IConnectionBrokerRequest :: CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="12940-137">**IConnectionBrokerRequest::CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





