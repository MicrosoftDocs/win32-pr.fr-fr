---
title: Méthode INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty. h)
description: Obtient une liste des parties de confiance qui sont abonnées.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Méthode GetSubscribedRelyingParties NAP
- Méthode GetSubscribedRelyingParties NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, méthode GetSubscribedRelyingParties
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464490"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a><span data-ttu-id="38abf-106">INapCertRelyingParty :: GetSubscribedRelyingParties, méthode</span><span class="sxs-lookup"><span data-stu-id="38abf-106">INapCertRelyingParty::GetSubscribedRelyingParties method</span></span>

> [!Note]  
> <span data-ttu-id="38abf-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="38abf-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="38abf-108">La méthode **GetSubscribedRelyingParties** obtient une liste des parties de confiance qui sont abonnées.</span><span class="sxs-lookup"><span data-stu-id="38abf-108">The **GetSubscribedRelyingParties** method gets a list of relying parties that have subscribed.</span></span>

## <a name="syntax"></a><span data-ttu-id="38abf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38abf-109">Syntax</span></span>


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a><span data-ttu-id="38abf-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38abf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38abf-111">*nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38abf-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38abf-112">Pointeur vers un [**EnforcementEntityCount**](nap-datatypes.md) qui contient le nombre de parties de confiance abonnées.</span><span class="sxs-lookup"><span data-stu-id="38abf-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of subscribed relying parties.</span></span>

</dd> <dt>

<span data-ttu-id="38abf-113">*relyingParties* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38abf-113">*relyingParties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38abf-114">Pointeur vers un pointeur vers un [**EnforcementEntityId**](nap-datatypes.md) qui contient la liste des parties de confiance abonnées.</span><span class="sxs-lookup"><span data-stu-id="38abf-114">A pointer to a pointer to an [**EnforcementEntityId**](nap-datatypes.md) that contains the list of subscribed relying parties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38abf-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38abf-115">Return value</span></span>

<span data-ttu-id="38abf-116">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="38abf-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="38abf-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="38abf-117">Return code</span></span>                                                                                     | <span data-ttu-id="38abf-118">Description</span><span class="sxs-lookup"><span data-stu-id="38abf-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="38abf-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38abf-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="38abf-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="38abf-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="38abf-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="38abf-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="38abf-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="38abf-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="38abf-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="38abf-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="38abf-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="38abf-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38abf-125">Notes</span><span class="sxs-lookup"><span data-stu-id="38abf-125">Remarks</span></span>

<span data-ttu-id="38abf-126">L’appelant doit libérer le paramètre *relyingParties* à l’aide de **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="38abf-126">The caller must free the *relyingParties* parameter using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="38abf-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38abf-127">Requirements</span></span>



| <span data-ttu-id="38abf-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38abf-128">Requirement</span></span> | <span data-ttu-id="38abf-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="38abf-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38abf-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38abf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="38abf-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38abf-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38abf-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38abf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="38abf-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38abf-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38abf-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="38abf-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="38abf-135"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="38abf-135"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="38abf-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="38abf-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38abf-137"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38abf-137"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38abf-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38abf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38abf-139">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="38abf-139">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





