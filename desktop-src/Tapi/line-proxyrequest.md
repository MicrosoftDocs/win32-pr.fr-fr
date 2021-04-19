---
description: Le message PROXYREQUEST de ligne TAPI \_ envoie une requête à un gestionnaire de fonctions proxy inscrit.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Message LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542577"
---
# <a name="line_proxyrequest-message"></a><span data-ttu-id="71c62-103">\_Message PROXYREQUEST de ligne</span><span class="sxs-lookup"><span data-stu-id="71c62-103">LINE\_PROXYREQUEST message</span></span>

<span data-ttu-id="71c62-104">Le message **\_ PROXYREQUEST de ligne** TAPI envoie une requête à un gestionnaire de fonctions proxy inscrit.</span><span class="sxs-lookup"><span data-stu-id="71c62-104">The TAPI **LINE\_PROXYREQUEST** message delivers a request to a registered proxy function handler.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="71c62-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71c62-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71c62-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="71c62-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="71c62-107">Handle de l’application sur le périphérique de ligne sur lequel l’état de l’agent a changé.</span><span class="sxs-lookup"><span data-stu-id="71c62-107">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="71c62-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="71c62-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="71c62-109">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="71c62-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="71c62-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="71c62-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="71c62-111">Pointeur vers une structure [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) contenant la demande à traiter par l’application du gestionnaire de proxy.</span><span class="sxs-lookup"><span data-stu-id="71c62-111">Pointer to a [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) structure containing the request to be processed by the proxy handler application.</span></span>

</dd> <dt>

<span data-ttu-id="71c62-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="71c62-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="71c62-113">Réservé.</span><span class="sxs-lookup"><span data-stu-id="71c62-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="71c62-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="71c62-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="71c62-115">Réservé.</span><span class="sxs-lookup"><span data-stu-id="71c62-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71c62-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71c62-116">Return value</span></span>

<span data-ttu-id="71c62-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="71c62-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71c62-118">Notes</span><span class="sxs-lookup"><span data-stu-id="71c62-118">Remarks</span></span>

<span data-ttu-id="71c62-119">Le message de **ligne \_ PROXYREQUEST** est envoyé uniquement à la première application inscrite pour gérer les demandes de proxy du type remis.</span><span class="sxs-lookup"><span data-stu-id="71c62-119">The **LINE\_PROXYREQUEST** message is sent only to the first application that registered to handle proxy requests of the type being delivered.</span></span>

<span data-ttu-id="71c62-120">L’application doit traiter la requête contenue dans la mémoire tampon du proxy et appeler [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) pour retourner des données ou fournir des résultats.</span><span class="sxs-lookup"><span data-stu-id="71c62-120">The application should process the request contained in the proxy buffer and call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) to return data or deliver results.</span></span> <span data-ttu-id="71c62-121">Le traitement de la requête doit être effectué dans le contexte de la fonction de rappel TAPI de l’application uniquement si elle peut être exécutée immédiatement, sans attendre la réponse d’une autre entité.</span><span class="sxs-lookup"><span data-stu-id="71c62-121">Processing of the request should be done within the context of the application's TAPI callback function only if it can be performed immediately, without waiting for response from any other entity.</span></span> <span data-ttu-id="71c62-122">Si l’application doit communiquer avec d’autres entités (par exemple, un fournisseur de services pour gérer les ACD basés sur PBX, ou tout autre service système qui peut entraîner un blocage), la demande doit être mise en file d’attente dans l’application et la fonction de rappel s’est arrêtée pour éviter de retarder la réception de messages TAPI supplémentaires par l’application.</span><span class="sxs-lookup"><span data-stu-id="71c62-122">If the application needs to communicate with other entities (for example, a service provider to handle PBX-based ACD, or any other system service which might result in blocking), then the request should be queued within the application and the callback function exited to avoid delaying the receipt of further TAPI messages by the application.</span></span>

<span data-ttu-id="71c62-123">Au moment où la **ligne \_ PROXYREQUEST** est remise au gestionnaire proxy, TAPI a déjà retourné un résultat de fonction *dwRequestID* positif à l’application d’origine et a débloqué le thread appelant pour poursuivre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="71c62-123">At the time the **LINE\_PROXYREQUEST** is delivered to the proxy handler, TAPI has already returned a positive *dwRequestID* function result to the original application and unblocked the calling thread to continue execution.</span></span> <span data-ttu-id="71c62-124">L’application attend un message de [**\_ réponse de ligne**](line-reply.md) , qui est généré automatiquement lorsque l’application de gestionnaire proxy appelle [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="71c62-124">The application is awaiting a [**LINE\_REPLY**](line-reply.md) message, which is automatically generated when the proxy handler application calls [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span>

<span data-ttu-id="71c62-125">L’application ne libère pas la mémoire vers laquelle pointe *lpProxyRequest*.</span><span class="sxs-lookup"><span data-stu-id="71c62-125">The application shall not free the memory pointed to by *lpProxyRequest*.</span></span> <span data-ttu-id="71c62-126">L’interface TAPI libère de la mémoire pendant l’exécution de [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="71c62-126">TAPI frees the memory during the execution of [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span> <span data-ttu-id="71c62-127">L’application peut appeler [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactement une fois pour chaque message de **\_ PROXYREQUEST de ligne** .</span><span class="sxs-lookup"><span data-stu-id="71c62-127">The application can call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactly once for each **LINE\_PROXYREQUEST** message.</span></span>

<span data-ttu-id="71c62-128">Si l’application reçoit un message de [**\_ fermeture de ligne**](line-close.md) alors qu’elle a des requêtes proxy en attente, elle doit appeler [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) pour chaque demande en attente, en transmettant une valeur *dwResult* appropriée (telle que LINEERR \_ OPERATIONFAILED).</span><span class="sxs-lookup"><span data-stu-id="71c62-128">If the application receives a [**LINE\_CLOSE**](line-close.md) message while it has pending proxy requests, it should call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) for each pending request, passing in an appropriate *dwResult* value (such as LINEERR\_OPERATIONFAILED).</span></span>

## <a name="requirements"></a><span data-ttu-id="71c62-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71c62-129">Requirements</span></span>



| <span data-ttu-id="71c62-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71c62-130">Requirement</span></span> | <span data-ttu-id="71c62-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="71c62-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71c62-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="71c62-132">TAPI version</span></span><br/> | <span data-ttu-id="71c62-133">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="71c62-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="71c62-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="71c62-134">Header</span></span><br/>       | <dl> <span data-ttu-id="71c62-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="71c62-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c62-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71c62-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c62-137">**fermeture de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="71c62-137">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="71c62-138">**réponse de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="71c62-138">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="71c62-139">**LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="71c62-139">**LINEPROXYREQUEST**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[<span data-ttu-id="71c62-140">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="71c62-140">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




