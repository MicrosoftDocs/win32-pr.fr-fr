---
description: Le message de demande de ligne TAPI \_ est envoyé pour signaler l’arrivée d’une nouvelle demande à partir d’une autre application.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Message LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539615"
---
# <a name="line_request-message"></a><span data-ttu-id="29f91-103">Message de demande de ligne \_</span><span class="sxs-lookup"><span data-stu-id="29f91-103">LINE\_REQUEST message</span></span>

<span data-ttu-id="29f91-104">Le message **de \_ demande de ligne** TAPI est envoyé pour signaler l’arrivée d’une nouvelle demande à partir d’une autre application.</span><span class="sxs-lookup"><span data-stu-id="29f91-104">The TAPI **LINE\_REQUEST** message is sent to report the arrival of a new request from another application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="29f91-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29f91-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29f91-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="29f91-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="29f91-107">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="29f91-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="29f91-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="29f91-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="29f91-109">Instance d’inscription de l’application spécifiée sur [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span><span class="sxs-lookup"><span data-stu-id="29f91-109">The registration instance of the application specified on [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span></span>

</dd> <dt>

<span data-ttu-id="29f91-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="29f91-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="29f91-111">Mode de requête de la demande nouvellement en attente.</span><span class="sxs-lookup"><span data-stu-id="29f91-111">The request mode of the newly pending request.</span></span> <span data-ttu-id="29f91-112">Ce paramètre utilise les [**\_ constantes LINEREQUESTMODE**](linerequestmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="29f91-112">This parameter uses the [**LINEREQUESTMODE\_ constants**](linerequestmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="29f91-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="29f91-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="29f91-114">Les conditions de ce paramètre sont, si *dwParam1* est défini sur LINEREQUESTMODE \_ Drop, *dwParam2* contient le *HWND* de l’application qui demande la suppression.</span><span class="sxs-lookup"><span data-stu-id="29f91-114">The conditions for this parameter are, if *dwParam1* is set to LINEREQUESTMODE\_DROP, *dwParam2* contains the *hWnd* of the application requesting the drop.</span></span> <span data-ttu-id="29f91-115">Dans le cas contraire, *dwParam2* n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="29f91-115">Otherwise, *dwParam2* is unused.</span></span>

</dd> <dt>

<span data-ttu-id="29f91-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="29f91-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="29f91-117">Si *dwParam1* a la valeur LINEREQUESTMODE \_ Drop, le mot de poids faible de *dwParam3* contient le *wRequestID* tel que spécifié par l’application qui a demandé la suppression.</span><span class="sxs-lookup"><span data-stu-id="29f91-117">If *dwParam1* is set to LINEREQUESTMODE\_DROP, the low-order word of *dwParam3* contains the *wRequestID* as specified by the application that requested the drop.</span></span> <span data-ttu-id="29f91-118">Dans le cas contraire, *dwParam3* n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="29f91-118">Otherwise, *dwParam3* is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29f91-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29f91-119">Return value</span></span>

<span data-ttu-id="29f91-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="29f91-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29f91-121">Notes</span><span class="sxs-lookup"><span data-stu-id="29f91-121">Remarks</span></span>

<span data-ttu-id="29f91-122">Le message de **\_ demande de ligne** est envoyé à l’application dont la priorité est la plus élevée et qui est inscrite pour le mode de requête correspondant.</span><span class="sxs-lookup"><span data-stu-id="29f91-122">The **LINE\_REQUEST** message is sent to the highest priority application that has registered for the corresponding request mode.</span></span> <span data-ttu-id="29f91-123">Ce message indique l’arrivée d’une demande de téléphonie assistée du mode de demande spécifié.</span><span class="sxs-lookup"><span data-stu-id="29f91-123">This message indicates the arrival of an Assisted Telephony request of the specified request mode.</span></span> <span data-ttu-id="29f91-124">Si *dwParam1* est LINEREQUESTMODE \_ MAKECALL, l’application peut appeler [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) en utilisant le mode de demande correspondant pour recevoir la demande.</span><span class="sxs-lookup"><span data-stu-id="29f91-124">If *dwParam1* is LINEREQUESTMODE\_MAKECALL, the application can invoke [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) using the corresponding request mode to receive the request.</span></span> <span data-ttu-id="29f91-125">Si *dwParam1* est LINEREQUESTMODE \_ Drop, le message contient toutes les données requises par le destinataire de la demande pour effectuer la demande.</span><span class="sxs-lookup"><span data-stu-id="29f91-125">If *dwParam1* is LINEREQUESTMODE\_DROP, the message contains all of the data the request recipient requires to perform the request.</span></span>

## <a name="requirements"></a><span data-ttu-id="29f91-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29f91-126">Requirements</span></span>



| <span data-ttu-id="29f91-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29f91-127">Requirement</span></span> | <span data-ttu-id="29f91-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="29f91-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="29f91-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="29f91-129">TAPI version</span></span><br/> | <span data-ttu-id="29f91-130">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="29f91-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="29f91-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="29f91-131">Header</span></span><br/>       | <dl> <span data-ttu-id="29f91-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="29f91-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29f91-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29f91-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f91-134">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="29f91-134">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[<span data-ttu-id="29f91-135">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="29f91-135">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[<span data-ttu-id="29f91-136">**tapiRequestMakeCall**</span><span class="sxs-lookup"><span data-stu-id="29f91-136">**tapiRequestMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




