---
title: Interface INapEnforcementClientConnection (NapEnforcementClient. h)
description: Autoriser la gestion des connexions clientes. | Interface INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- NAP de l’interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, Description
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211432"
---
# <a name="inapenforcementclientconnection-interface"></a><span data-ttu-id="331bc-106">Interface INapEnforcementClientConnection</span><span class="sxs-lookup"><span data-stu-id="331bc-106">INapEnforcementClientConnection interface</span></span>

> [!Note]  
> <span data-ttu-id="331bc-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="331bc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="331bc-108">**INapEnforcementClientConnection** fournit des méthodes qui permettent la gestion des connexions clientes.</span><span class="sxs-lookup"><span data-stu-id="331bc-108">The **INapEnforcementClientConnection** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="331bc-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) hérite de toutes les méthodes de cette interface et doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="331bc-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="331bc-110">Membres</span><span class="sxs-lookup"><span data-stu-id="331bc-110">Members</span></span>

<span data-ttu-id="331bc-111">L’interface **INapEnforcementClientConnection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="331bc-111">The **INapEnforcementClientConnection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="331bc-112">**INapEnforcementClientConnection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="331bc-112">**INapEnforcementClientConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="331bc-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="331bc-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="331bc-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="331bc-114">Methods</span></span>

<span data-ttu-id="331bc-115">L’interface **INapEnforcementClientConnection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="331bc-115">The **INapEnforcementClientConnection** interface has these methods.</span></span>



| <span data-ttu-id="331bc-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="331bc-116">Method</span></span>                                                                                                                           | <span data-ttu-id="331bc-117">Description</span><span class="sxs-lookup"><span data-stu-id="331bc-117">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="331bc-118">**INapEnforcementClientConnection :: GetConnectionID,**</span><span class="sxs-lookup"><span data-stu-id="331bc-118">**INapEnforcementClientConnection::GetConnectionId**</span></span>](inapenforcementclientconnection-getconnectionid-method.md)               | <span data-ttu-id="331bc-119">Obtient l’ID de connexion du client.</span><span class="sxs-lookup"><span data-stu-id="331bc-119">Gets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="331bc-120">**INapEnforcementClientConnection::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="331bc-120">**INapEnforcementClientConnection::GetCorrelationId**</span></span>](inapenforcementclientconnection-getcorrelationid-method.md)             | <span data-ttu-id="331bc-121">Obtient l’ID utilisé pour corréler les demandes SoH et les réponses SoH.</span><span class="sxs-lookup"><span data-stu-id="331bc-121">Gets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="331bc-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="331bc-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-getenforcerprivatedata-method.md) | <span data-ttu-id="331bc-123">Utilisé par l’application pour recevoir des données privées.</span><span class="sxs-lookup"><span data-stu-id="331bc-123">Used by the enforcer to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="331bc-124">**INapEnforcementClientConnection :: GetFlags**</span><span class="sxs-lookup"><span data-stu-id="331bc-124">**INapEnforcementClientConnection::GetFlags**</span></span>](inapenforcementclientconnection-getflags-method.md)                             | <span data-ttu-id="331bc-125">Obtient la valeur de l’indicateur qui différencie les réponses premières des réponses en raison des SoHRequests mises en cache par les enforceurs.</span><span class="sxs-lookup"><span data-stu-id="331bc-125">Gets the value of the flag that differentiates first-time responses from responses due to SoHRequests cached by the enforcers.</span></span><br/> |
| [<span data-ttu-id="331bc-126">**INapEnforcementClientConnection::GetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="331bc-126">**INapEnforcementClientConnection::GetIsolationInfo**</span></span>](inapenforcementclientconnection-getisolationinfo-method.md)             | <span data-ttu-id="331bc-127">Utilisé pour récupérer les informations d’isolation du client.</span><span class="sxs-lookup"><span data-stu-id="331bc-127">Used get the isolation information of the client.</span></span><br/>                                                                              |
| [<span data-ttu-id="331bc-128">**INapEnforcementClientConnection::GetMaxSize**</span><span class="sxs-lookup"><span data-stu-id="331bc-128">**INapEnforcementClientConnection::GetMaxSize**</span></span>](inapenforcementclientconnection-getmaxsize-method.md)                         | <span data-ttu-id="331bc-129">Obtient la taille maximale du paquet SoH pour ce client.</span><span class="sxs-lookup"><span data-stu-id="331bc-129">Gets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="331bc-130">**INapEnforcementClientConnection::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="331bc-130">**INapEnforcementClientConnection::GetPrivateData**</span></span>](inapenforcementclientconnection-getprivatedata-method.md)                 | <span data-ttu-id="331bc-131">Utilisé par NapAgent pour accéder aux données privées.</span><span class="sxs-lookup"><span data-stu-id="331bc-131">Used by the NapAgent to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="331bc-132">**INapEnforcementClientConnection::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="331bc-132">**INapEnforcementClientConnection::GetSoHRequest**</span></span>](inapenforcementclientconnection-getsohrequest-method.md)                   | <span data-ttu-id="331bc-133">Obtient la demande de déclaration d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="331bc-133">Gets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="331bc-134">**INapEnforcementClientConnection::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="331bc-134">**INapEnforcementClientConnection::GetSoHResponse**</span></span>](inapenforcementclientconnection-getsohresponse-method.md)                 | <span data-ttu-id="331bc-135">Obtient le SoH-Response reçu par le client de mise en œuvre.</span><span class="sxs-lookup"><span data-stu-id="331bc-135">Gets the SoH-Response received by the enforcement client.</span></span><br/>                                                                      |
| [<span data-ttu-id="331bc-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="331bc-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span></span>](inapenforcementclientconnection-getstringcorrelationid-method.md) | <span data-ttu-id="331bc-137">Obtient la version de chaîne de l’ID de corrélation.</span><span class="sxs-lookup"><span data-stu-id="331bc-137">Gets the string version of the CorrelationId.</span></span> <span data-ttu-id="331bc-138">Principalement utilisé à des fins de journalisation.</span><span class="sxs-lookup"><span data-stu-id="331bc-138">Used primarily for logging purposes.</span></span><br/>                                             |
| [<span data-ttu-id="331bc-139">**INapEnforcementClientConnection :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="331bc-139">**INapEnforcementClientConnection::Initialize**</span></span>](inapenforcementclientconnection-initialize-method.md)                         | <span data-ttu-id="331bc-140">Initialise la connexion.</span><span class="sxs-lookup"><span data-stu-id="331bc-140">Initializes the connection.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="331bc-141">**INapEnforcementClientConnection::SetConnectionId**</span><span class="sxs-lookup"><span data-stu-id="331bc-141">**INapEnforcementClientConnection::SetConnectionId**</span></span>](inapenforcementclientconnection-setconnectionid-method.md)               | <span data-ttu-id="331bc-142">Définit l’ID de connexion du client.</span><span class="sxs-lookup"><span data-stu-id="331bc-142">Sets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="331bc-143">**INapEnforcementClientConnection::SetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="331bc-143">**INapEnforcementClientConnection::SetCorrelationId**</span></span>](inapenforcementclientconnection-setcorrelationid-method.md)             | <span data-ttu-id="331bc-144">Définit l’ID utilisé pour corréler les demandes SoH et les réponses SoH.</span><span class="sxs-lookup"><span data-stu-id="331bc-144">Sets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="331bc-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="331bc-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-setenforcerprivatedata-method.md) | <span data-ttu-id="331bc-146">Utilisé par l’application pour définir des données privées.</span><span class="sxs-lookup"><span data-stu-id="331bc-146">Used by the enforcer to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="331bc-147">**INapEnforcementClientConnection::SetFlags**</span><span class="sxs-lookup"><span data-stu-id="331bc-147">**INapEnforcementClientConnection::SetFlags**</span></span>](inapenforcementclientconnection-setflags-method.md)                             | <span data-ttu-id="331bc-148">Définit l’indicateur qui différencie les réponses de première heure des réponses en raison des SoHRequests mises en cache par les enforceurs.</span><span class="sxs-lookup"><span data-stu-id="331bc-148">Sets the flag that differentiates first-time responses from responses due to SoHRequests cached by enforcers.</span></span><br/>                  |
| [<span data-ttu-id="331bc-149">**INapEnforcementClientConnection::SetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="331bc-149">**INapEnforcementClientConnection::SetIsolationInfo**</span></span>](inapenforcementclientconnection-setisolationinfo-method.md)             | <span data-ttu-id="331bc-150">Utilisé par NapAgent pour définir les informations d’isolation du client.</span><span class="sxs-lookup"><span data-stu-id="331bc-150">Used by the NapAgent to set the isolation information of the client.</span></span><br/>                                                           |
| [<span data-ttu-id="331bc-151">**INapEnforcementClientConnection::SetMaxSize**</span><span class="sxs-lookup"><span data-stu-id="331bc-151">**INapEnforcementClientConnection::SetMaxSize**</span></span>](inapenforcementclientconnection-setmaxsize-method.md)                         | <span data-ttu-id="331bc-152">Définit la taille maximale du paquet SoH pour ce client.</span><span class="sxs-lookup"><span data-stu-id="331bc-152">Sets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="331bc-153">**INapEnforcementClientConnection::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="331bc-153">**INapEnforcementClientConnection::SetPrivateData**</span></span>](inapenforcementclientconnection-setprivatedata-method.md)                 | <span data-ttu-id="331bc-154">Utilisé par NapAgent pour définir les données privées.</span><span class="sxs-lookup"><span data-stu-id="331bc-154">Used by the NapAgent to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="331bc-155">**INapEnforcementClientConnection::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="331bc-155">**INapEnforcementClientConnection::SetSoHRequest**</span></span>](inapenforcementclientconnection-setsohrequest-method.md)                   | <span data-ttu-id="331bc-156">Définit la demande de déclaration d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="331bc-156">Sets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="331bc-157">**INapEnforcementClientConnection::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="331bc-157">**INapEnforcementClientConnection::SetSoHResponse**</span></span>](inapenforcementclientconnection-setsohresponse-method.md)                 | <span data-ttu-id="331bc-158">Définit le SoH-Response et est utilisé par le client de mise en œuvre lors de la réception d’un paquet.</span><span class="sxs-lookup"><span data-stu-id="331bc-158">Sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span><br/>                                             |



 

## <a name="requirements"></a><span data-ttu-id="331bc-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="331bc-159">Requirements</span></span>



| <span data-ttu-id="331bc-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="331bc-160">Requirement</span></span> | <span data-ttu-id="331bc-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="331bc-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331bc-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="331bc-162">Minimum supported client</span></span><br/> | <span data-ttu-id="331bc-163">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="331bc-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="331bc-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="331bc-164">Minimum supported server</span></span><br/> | <span data-ttu-id="331bc-165">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="331bc-165">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="331bc-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="331bc-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="331bc-167"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="331bc-167"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="331bc-168">MIDL</span><span class="sxs-lookup"><span data-stu-id="331bc-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="331bc-169"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="331bc-169"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="331bc-170">DLL</span><span class="sxs-lookup"><span data-stu-id="331bc-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="331bc-171"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="331bc-171"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="331bc-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="331bc-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331bc-173">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="331bc-173">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="331bc-174">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="331bc-174">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

