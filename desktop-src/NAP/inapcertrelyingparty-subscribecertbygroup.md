---
title: Méthode INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty. h)
description: S’abonne à un serveur de certificat d’intégrité (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Méthode SubscribeCertByGroup NAP
- Méthode SubscribeCertByGroup NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, méthode SubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511775"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a><span data-ttu-id="5bc9a-106">INapCertRelyingParty :: SubscribeCertByGroup, méthode</span><span class="sxs-lookup"><span data-stu-id="5bc9a-106">INapCertRelyingParty::SubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="5bc9a-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5bc9a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5bc9a-108">La méthode **SubscribeCertByGroup** s’abonne à un serveur de certificat d’intégrité (HCS).</span><span class="sxs-lookup"><span data-stu-id="5bc9a-108">The **SubscribeCertByGroup** method subscribes to a health certificate server (HCS).</span></span> <span data-ttu-id="5bc9a-109">Le HCS doit déjà être inscrit avant l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-109">The HCS must already be registered before subscribing.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc9a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bc9a-110">Syntax</span></span>


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a><span data-ttu-id="5bc9a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bc9a-111">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="5bc9a-112">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bc9a-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc9a-113">[**EnforcementEntityId**](nap-datatypes.md) qui contient l’ID du client de mise en œuvre qui s’abonne.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-113">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is subscribing.</span></span>

</dd> <dt>

<span data-ttu-id="5bc9a-114">*SubscriberName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bc9a-114">*subscriberName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc9a-115">Nom de l'abonné.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-115">The name of the subscriber.</span></span>

> [!Note]  
> <span data-ttu-id="5bc9a-116">Actuellement utilisé uniquement à des fins de journalisation.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-116">This is currently only used for logging purposes.</span></span>

 

</dd> <dt>

<span data-ttu-id="5bc9a-117">*réservé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bc9a-117">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc9a-118">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-118">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5bc9a-119">*certExists* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5bc9a-119">*certExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc9a-120">Indique si un certificat d’intégrité de ce HCS est déjà géré par le NapAgent et s’il est présent dans le magasin de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-120">Indicates whether a health certificate from this HCS is already being maintained by the NapAgent and is present in the machine store.</span></span> <span data-ttu-id="5bc9a-121">Si la **valeur est true**, un certificat d’intégrité est déjà en cours de maintenance et est présent.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-121">If **TRUE**, a health certificate is already being maintained and is present.</span></span> <span data-ttu-id="5bc9a-122">Si la **valeur est false**, un certificat d’intégrité n’est pas actuellement géré et présent.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-122">If **FALSE**, a health certificate is not currently being maintained and present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc9a-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5bc9a-123">Return value</span></span>

<span data-ttu-id="5bc9a-124">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-124">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="5bc9a-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5bc9a-125">Return code</span></span>                                                                                     | <span data-ttu-id="5bc9a-126">Description</span><span class="sxs-lookup"><span data-stu-id="5bc9a-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bc9a-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc9a-127"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5bc9a-128">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-128">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="5bc9a-129"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc9a-129"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5bc9a-130">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-130">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5bc9a-131"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5bc9a-131"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5bc9a-132">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5bc9a-132">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5bc9a-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bc9a-133">Requirements</span></span>



| <span data-ttu-id="5bc9a-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bc9a-134">Requirement</span></span> | <span data-ttu-id="5bc9a-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bc9a-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc9a-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bc9a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc9a-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bc9a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5bc9a-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bc9a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc9a-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bc9a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5bc9a-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="5bc9a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bc9a-141"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bc9a-141"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="5bc9a-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="5bc9a-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5bc9a-143"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5bc9a-143"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc9a-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bc9a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc9a-145">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="5bc9a-145">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





