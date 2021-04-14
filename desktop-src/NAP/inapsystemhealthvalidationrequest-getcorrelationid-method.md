---
title: Méthode INapSystemHealthValidationRequest GetCorrelationId (NapSystemHealthValidator. h)
description: Est utilisé par les programmes de validation d’intégrité système (SHV) pour récupérer l’ID de corrélation. Le SHV doit ensuite consigner ces informations.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- Méthode GetCorrelationId NAP
- Méthode GetCorrelationId NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465142"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a><span data-ttu-id="e8395-107">INapSystemHealthValidationRequest :: GetCorrelationId, méthode</span><span class="sxs-lookup"><span data-stu-id="e8395-107">INapSystemHealthValidationRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="e8395-108">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e8395-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e8395-109">La méthode **INapSystemHealthValidationRequest :: GetCorrelationId** est utilisée par les programmes de validation d’intégrité système (SHV) pour récupérer l’ID de corrélation.</span><span class="sxs-lookup"><span data-stu-id="e8395-109">The **INapSystemHealthValidationRequest::GetCorrelationId** method is used by System Health Validators (SHVs) to retrieve the correlation ID.</span></span> <span data-ttu-id="e8395-110">Le SHV doit ensuite consigner ces informations.</span><span class="sxs-lookup"><span data-stu-id="e8395-110">The SHV must then log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8395-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8395-111">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="e8395-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8395-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8395-113">*CorrelationId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e8395-113">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8395-114">Pointeur vers un ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid) unique pour l’échange de déclaration d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="e8395-114">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8395-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8395-115">Return value</span></span>

<span data-ttu-id="e8395-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="e8395-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e8395-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e8395-117">Return code</span></span>                                                                                     | <span data-ttu-id="e8395-118">Description</span><span class="sxs-lookup"><span data-stu-id="e8395-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8395-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8395-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e8395-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e8395-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e8395-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e8395-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e8395-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e8395-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e8395-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e8395-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e8395-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e8395-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8395-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8395-125">Requirements</span></span>



| <span data-ttu-id="e8395-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8395-126">Requirement</span></span> | <span data-ttu-id="e8395-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8395-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8395-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8395-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e8395-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8395-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="e8395-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8395-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e8395-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8395-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8395-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8395-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8395-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8395-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8395-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="e8395-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8395-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8395-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="e8395-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e8395-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8395-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8395-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="e8395-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8395-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8395-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="e8395-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





