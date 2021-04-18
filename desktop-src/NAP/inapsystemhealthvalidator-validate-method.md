---
title: INapSystemHealthValidator Validate, méthode (NapSystemHealthValidator. h)
description: Le système NAP pour valider les SoHRequest reçus d’un client.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Valider la méthode NAP
- Valider la méthode NAP, interface INapSystemHealthValidator
- INapSystemHealthValidator interface NAP, Validate, méthode
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512793"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a><span data-ttu-id="96e5a-106">INapSystemHealthValidator :: Validate, méthode</span><span class="sxs-lookup"><span data-stu-id="96e5a-106">INapSystemHealthValidator::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="96e5a-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="96e5a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="96e5a-108">La méthode **INapSystemHealthValidator :: Validate** est définie par le développeur SHV et appelée par le système NAP pour valider les [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) reçues d’un client.</span><span class="sxs-lookup"><span data-stu-id="96e5a-108">The **INapSystemHealthValidator::Validate** method is defined by the SHV developer and called by the NAP system to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e5a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96e5a-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a><span data-ttu-id="96e5a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96e5a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e5a-111">*demande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96e5a-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e5a-112">Pointeur COM vers un objet [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) qui identifie l’objet de demande de validation.</span><span class="sxs-lookup"><span data-stu-id="96e5a-112">A COM pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that identifies the validation request object.</span></span>

</dd> <dt>

<span data-ttu-id="96e5a-113">*hintTimeOutInMsec* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96e5a-113">*hintTimeOutInMsec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e5a-114">Durée, en millisecondes, du délai d’attente de communication.</span><span class="sxs-lookup"><span data-stu-id="96e5a-114">The duration, in milliseconds, of the communication timeout period.</span></span> <span data-ttu-id="96e5a-115">Le programme de validation d’intégrité système (SHV) doit répondre dans ce laps de temps. dans le cas contraire, la réponse est supprimée.</span><span class="sxs-lookup"><span data-stu-id="96e5a-115">The System Health Validator (SHV) should respond within this amount of time; otherwise the response is dropped.</span></span>

> [!Note]  
> <span data-ttu-id="96e5a-116">Le délai d’expiration par défaut pour tous les validateurs d’intégrité est de 2000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="96e5a-116">The default timeout for all SHVs is 2000 milliseconds.</span></span> <span data-ttu-id="96e5a-117">L’utilisation d’une valeur autre que la valeur par défaut modifie le délai d’expiration pour tous les validateurs d’intégrité inscrits.</span><span class="sxs-lookup"><span data-stu-id="96e5a-117">Using a value other than the default will change the timeout for all registered SHVs.</span></span>

 

</dd> <dt>

<span data-ttu-id="96e5a-118">*rappel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96e5a-118">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96e5a-119">Pointeur vers l’objet de rappel [**INapServerCallback**](inapservercallback.md).</span><span class="sxs-lookup"><span data-stu-id="96e5a-119">A pointer to the callback object [**INapServerCallback**](inapservercallback.md).</span></span> <span data-ttu-id="96e5a-120">Ce pointeur de rappel est utilisé par les validateurs d’intégrité du système lorsqu’ils retournent **E \_ en attente** à partir de l’appel à **INapSystemHealthValidator :: Validate**.</span><span class="sxs-lookup"><span data-stu-id="96e5a-120">This callback pointer is used by the SHVs when they return **E\_PENDING** from the call to **INapSystemHealthValidator::Validate**.</span></span> <span data-ttu-id="96e5a-121">Utilisé pour la validation asynchrone.</span><span class="sxs-lookup"><span data-stu-id="96e5a-121">This is used for asynchronous validation.</span></span> <span data-ttu-id="96e5a-122">Les validateurs d’intégrité du système sont censés répondre dans le temps *hintTimeOutInMsec* , sinon la réponse sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="96e5a-122">The SHVs are expected to respond within the *hintTimeOutInMsec* time or else the response will be dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e5a-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96e5a-123">Return value</span></span>

<span data-ttu-id="96e5a-124">Si un autre code d’erreur est retourné, le système suppose que l’échec de serverComponent s’est produit et que le mappage approprié est effectué pour réussir ou échouer.</span><span class="sxs-lookup"><span data-stu-id="96e5a-124">If any other error code is returned, then the system assumes serverComponent failure has occurred, and the appropriate mapping is done to pass/fail.</span></span>



| <span data-ttu-id="96e5a-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="96e5a-125">Return code</span></span>                                                                                                | <span data-ttu-id="96e5a-126">Description</span><span class="sxs-lookup"><span data-stu-id="96e5a-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96e5a-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96e5a-127"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="96e5a-128">Indique que le validateur a défini un SoHResponse sur l’objet « Request ».</span><span class="sxs-lookup"><span data-stu-id="96e5a-128">Indicates that the validator has set an SoHResponse on the 'request' object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="96e5a-129"><dt>**E \_ en attente**</dt></span><span class="sxs-lookup"><span data-stu-id="96e5a-129"><dt>**E\_PENDING**</dt></span></span> </dl>                  | <span data-ttu-id="96e5a-130">Indique que OnComplete () sera appelé sur un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="96e5a-130">Indicates that OnComplete() will be called on a separate thread.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="96e5a-131"><dt>**\_serveur RPC \_ S \_ non disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="96e5a-131"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="96e5a-132">Indique que le processus du programme de validation d’intégrité système (SHV) s’est terminé sans que le NapServer libère réellement une référence à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="96e5a-132">Indicates that the System Health Validator (SHV) process terminated without the NapServer actually releasing a reference to it.</span></span> <span data-ttu-id="96e5a-133">Le NapServer essaiera de recréer une nouvelle référence au VALIDateur de validation et de réexécuter l’appel Validate une seule fois.</span><span class="sxs-lookup"><span data-stu-id="96e5a-133">The NapServer will try to re-create a new reference to the SHV and will reexecute the Validate call once.</span></span> <span data-ttu-id="96e5a-134">Si la création de l’objet ou de la validation réexécutée échoue, le SHV est supprimé de la liste des validateurs chargés.</span><span class="sxs-lookup"><span data-stu-id="96e5a-134">If the creation of the object or the re-executed Validate fails, the SHV is removed from the list of loaded SHVs.</span></span> <span data-ttu-id="96e5a-135">Le seul moyen de rechargement de ce VALIDateur consiste à annuler l’inscription et à réinscrire le SHV, ou lors du redémarrage de NapServer</span><span class="sxs-lookup"><span data-stu-id="96e5a-135">The only way this SHV can now be reloaded is to unregister and reregister the SHV again, or when the NapServer restarts</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96e5a-136">Notes</span><span class="sxs-lookup"><span data-stu-id="96e5a-136">Remarks</span></span>

<span data-ttu-id="96e5a-137">Pour permettre la prise en charge de la détection d’intrusion, les validateurs d’intégrité système seront invités à valider l’ordinateur client, que le client ait envoyé un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destiné à l’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="96e5a-137">In order to support intrusion detection, SHVs will be asked to validate the client machine regardless of whether the client sent an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) intended for the SHV.</span></span>

<span data-ttu-id="96e5a-138">Le SHV doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="96e5a-138">The SHV must do the following:</span></span>

-   <span data-ttu-id="96e5a-139">Récupérez le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à partir de la *demande* en appelant la [**demande. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="96e5a-139">Retrieve the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) from *request* by calling [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span></span>
-   <span data-ttu-id="96e5a-140">Si le paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) est NULL :</span><span class="sxs-lookup"><span data-stu-id="96e5a-140">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is null:</span></span>
    -   <span data-ttu-id="96e5a-141">Si le SHV est un système de détection d’intrusion, renseignez un paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) avec le [**code d’erreur NAP**](nap-error-constants.md) approprié en fonction de la raison pour laquelle l’ordinateur client est malveillant.</span><span class="sxs-lookup"><span data-stu-id="96e5a-141">If the SHV is an intrusion detection system, populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the appropriate [**NAP error code**](nap-error-constants.md) as to why the client machine is malicious.</span></span>
    -   <span data-ttu-id="96e5a-142">Tous les autres programmes de validation d’intégrité système doivent remplir un paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) avec un code d’erreur de [**déclaration d' \_ \_ \_ intégrité réseau manquante NAP**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="96e5a-142">All other SHVs should populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with an error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>
-   <span data-ttu-id="96e5a-143">Si *napSystemGenerated* a la **valeur true** à partir de l’appel à la [**requête. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), le SHV doit s’attendre à un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) avec les 3 TLVs suivants : [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span><span class="sxs-lookup"><span data-stu-id="96e5a-143">If *napSystemGenerated* is **TRUE** from the call to [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), the SHV should expect an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the following 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span></span> <span data-ttu-id="96e5a-144">Ce **SoHRequest** est généré par le NapAgent pour le compte de l’agent d’intégrité système (SHA), car une erreur s’est produite lors de la récupération d’un paquet de demande à partir de l’agent Sha.</span><span class="sxs-lookup"><span data-stu-id="96e5a-144">This **SoHRequest** is generated by the NapAgent on behalf of the System Health Agent (SHA) since there was an error in retrieving a request packet from the SHA.</span></span>
-   <span data-ttu-id="96e5a-145">Validez le paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="96e5a-145">Validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>
    -   <span data-ttu-id="96e5a-146">Si le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) est incorrect, construisez un paquet **SoHResponse** avec le code d’erreur [**NAP \_ E \_ \_ Packet non valide**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="96e5a-146">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) is malformed, then construct a **SoHResponse** packet with error code [**NAP\_E\_INVALID\_PACKET**](nap-error-constants.md).</span></span>
    -   <span data-ttu-id="96e5a-147">Si le programme de validation d’intégrité du service utilise uniquement des informations mises en cache pour valider le paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (c’est-à-dire qu’aucune e/s n’est effectuée), il peut alors construire le **SoHResponse**, le définir sur l’objet dans la *demande* et retourner la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="96e5a-147">If the SHV is only using cached information to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet (i.e. no I/O is performed), then it can construct the **SoHResponse**, set it on the object in *request* and return **S\_OK**.</span></span>
    -   <span data-ttu-id="96e5a-148">Si le programme de validation d’intégrité du service effectue des e/s afin de communiquer avec ses serveurs principaux pour valider l’intégrité du client, il doit mettre en file d’attente les e/s et retourner cette fonction avec **E \_ en attente**.</span><span class="sxs-lookup"><span data-stu-id="96e5a-148">If the SHV is performing I/O in order to talk to its back-end servers to validate the client's health, then it must queue up the I/O and return this function with **E\_PENDING**.</span></span> <span data-ttu-id="96e5a-149">Dans ce cas, le validateur d’intégrité des appels doit appeler le [**rappel. OnComplete ()**](inapservercallback-oncomplete-method.md) sur un thread distinct dans le délai d’attente, *hintTimeOutInMsec*.</span><span class="sxs-lookup"><span data-stu-id="96e5a-149">In this case, the SHV must call [**callback.OnComplete()**](inapservercallback-oncomplete-method.md) on a separate thread within the timeout period, *hintTimeOutInMsec*.</span></span> <span data-ttu-id="96e5a-150">Dans le cas contraire, la réponse du SHV sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="96e5a-150">Otherwise, the SHV's response will be dropped.</span></span>
-   <span data-ttu-id="96e5a-151">Ne retournez aucune autre erreur que celles indiquées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="96e5a-151">Do not return any other error other than those listed above.</span></span> <span data-ttu-id="96e5a-152">Si un autre code d’erreur est retourné par le SHV (par exemple,</span><span class="sxs-lookup"><span data-stu-id="96e5a-152">If any other error code is returned by the SHV (eg.</span></span> <span data-ttu-id="96e5a-153">une erreur système), le paquet est ignoré.</span><span class="sxs-lookup"><span data-stu-id="96e5a-153">some system error), the packet will be discarded.</span></span>

<span data-ttu-id="96e5a-154">Un SHV doit retourner un **sohAttributeTypeComplianceResultCodes** ou un **sohAttributeTypeFailureCategory** TLV dans son [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="96e5a-154">An SHV must return either an **sohAttributeTypeComplianceResultCodes** or **sohAttributeTypeFailureCategory** TLV in its [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

-   <span data-ttu-id="96e5a-155">[**SOHATTRIBUTETYPECOMPLIANCERESULTCODES TLV**](sohattributetype-enum.md): si le SHV peut valider l’intégrité du client (par exemple sain ou défectueux), cette TLV est retournée.</span><span class="sxs-lookup"><span data-stu-id="96e5a-155">[**sohAttributeTypeComplianceResultCodes TLV**](sohattributetype-enum.md): If the SHV could validate the health of the client (i.e. healthy or unhealthy), this TLV is returned.</span></span>
-   <span data-ttu-id="96e5a-156">[**SOHATTRIBUTETYPEFAILURECATEGORY TLV**](sohattributetype-enum.md): en cas d’échec de composant ou de communication sur le client ou le serveur, celui-ci doit être indiqué par ce TLV.</span><span class="sxs-lookup"><span data-stu-id="96e5a-156">[**sohAttributeTypeFailureCategory TLV**](sohattributetype-enum.md): If there was any component or communication failure on the client or server, it must be indicated by this TLV.</span></span> <span data-ttu-id="96e5a-157">Ce TLV sera davantage mappé à sain ou défectueux, en fonction de la configuration du SHV.</span><span class="sxs-lookup"><span data-stu-id="96e5a-157">This TLV will further be mapped to healthy or unhealthy depending upon the SHV's configuration.</span></span> <span data-ttu-id="96e5a-158">Pour plus d’informations, consultez l’interface [**INapServerManagement**](inapservermanagement.md) et la structure [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="96e5a-158">For more details, see the [**INapServerManagement**](inapservermanagement.md) interface and the [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>

<span data-ttu-id="96e5a-159">Le SHV ne doit pas contenir de références à la *demande* ou au *rappel* une fois l’appel asynchrone terminé.</span><span class="sxs-lookup"><span data-stu-id="96e5a-159">The SHV must not hold references to *request* or *callback* once the asyncronous call completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e5a-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96e5a-160">Requirements</span></span>



| <span data-ttu-id="96e5a-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96e5a-161">Requirement</span></span> | <span data-ttu-id="96e5a-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="96e5a-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96e5a-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96e5a-163">Minimum supported client</span></span><br/> | <span data-ttu-id="96e5a-164">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="96e5a-164">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="96e5a-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96e5a-165">Minimum supported server</span></span><br/> | <span data-ttu-id="96e5a-166">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96e5a-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96e5a-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="96e5a-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="96e5a-168"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="96e5a-168"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="96e5a-169">MIDL</span><span class="sxs-lookup"><span data-stu-id="96e5a-169">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96e5a-170"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96e5a-170"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e5a-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96e5a-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e5a-172">**INapSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="96e5a-172">**INapSystemHealthValidator**</span></span>](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





