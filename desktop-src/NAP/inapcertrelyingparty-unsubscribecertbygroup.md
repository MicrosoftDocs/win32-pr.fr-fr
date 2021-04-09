---
title: Méthode INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty. h)
description: Annule l’abonnement à un serveur de certificat d’intégrité (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Méthode UnSubscribeCertByGroup NAP
- Méthode UnSubscribeCertByGroup NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, méthode UnSubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942270"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a><span data-ttu-id="1d8ab-106">INapCertRelyingParty :: UnSubscribeCertByGroup, méthode</span><span class="sxs-lookup"><span data-stu-id="1d8ab-106">INapCertRelyingParty::UnSubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="1d8ab-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1d8ab-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1d8ab-108">La méthode **UnSubscribeCertByGroup** se désabonne d’un serveur de certificat d’intégrité (HCS).</span><span class="sxs-lookup"><span data-stu-id="1d8ab-108">The **UnSubscribeCertByGroup** method unsubscribes from a health certificate server (HCS).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d8ab-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d8ab-109">Syntax</span></span>


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a><span data-ttu-id="1d8ab-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d8ab-110">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="1d8ab-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d8ab-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d8ab-112">[**EnforcementEntityId**](nap-datatypes.md) qui contient l’ID du client de mise en œuvre qui annule l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d8ab-112">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is unsubscribing.</span></span>

</dd> <dt>

 <span data-ttu-id="1d8ab-113">*réservé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d8ab-113">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d8ab-114">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1d8ab-114">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d8ab-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d8ab-115">Return value</span></span>

<span data-ttu-id="1d8ab-116">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="1d8ab-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="1d8ab-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1d8ab-117">Return code</span></span>                                                                                     | <span data-ttu-id="1d8ab-118">Description</span><span class="sxs-lookup"><span data-stu-id="1d8ab-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d8ab-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d8ab-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1d8ab-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="1d8ab-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="1d8ab-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1d8ab-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1d8ab-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1d8ab-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1d8ab-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d8ab-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1d8ab-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="1d8ab-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d8ab-125">Notes</span><span class="sxs-lookup"><span data-stu-id="1d8ab-125">Remarks</span></span>

<span data-ttu-id="1d8ab-126">S’il n’y a pas d’autres abonnés à HCS, NapAgent supprimera les certificats d’intégrité correspondants du magasin de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1d8ab-126">If there are no other subscribers to the HCS, the NapAgent will delete the corresponding health certificates from the local machine store.</span></span>

<span data-ttu-id="1d8ab-127">Avant d’appeler cette méthode, appelez [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span><span class="sxs-lookup"><span data-stu-id="1d8ab-127">Before calling this method, call [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d8ab-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d8ab-128">Requirements</span></span>



| <span data-ttu-id="1d8ab-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d8ab-129">Requirement</span></span> | <span data-ttu-id="1d8ab-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d8ab-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8ab-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d8ab-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1d8ab-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d8ab-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d8ab-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d8ab-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1d8ab-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d8ab-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1d8ab-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d8ab-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d8ab-136"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d8ab-136"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d8ab-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="1d8ab-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d8ab-138"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d8ab-138"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d8ab-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d8ab-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d8ab-140">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="1d8ab-140">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





