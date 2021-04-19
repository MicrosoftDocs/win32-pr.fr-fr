---
title: Méthode INapSystemHealthValidationRequest GetSoHResponse (NapSystemHealthValidator. h)
description: Récupère le SoHResponse.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Méthode GetSoHResponse NAP
- Méthode GetSoHResponse NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517324"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a><span data-ttu-id="86dad-106">INapSystemHealthValidationRequest :: GetSoHResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="86dad-106">INapSystemHealthValidationRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="86dad-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="86dad-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="86dad-108">La méthode **INapSystemHealthValidationRequest :: GetSoHResponse** récupère le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="86dad-108">The **INapSystemHealthValidationRequest::GetSoHResponse** method retrieves the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="86dad-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86dad-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="86dad-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86dad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86dad-111">*sohResponse* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="86dad-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86dad-112">Pointeur vers un pointeur vers le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)reçu.</span><span class="sxs-lookup"><span data-stu-id="86dad-112">A pointer to a pointer to the received [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86dad-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86dad-113">Return value</span></span>

<span data-ttu-id="86dad-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="86dad-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="86dad-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="86dad-115">Return code</span></span>                                                                                     | <span data-ttu-id="86dad-116">Description</span><span class="sxs-lookup"><span data-stu-id="86dad-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="86dad-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86dad-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="86dad-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="86dad-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="86dad-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="86dad-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="86dad-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="86dad-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="86dad-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="86dad-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="86dad-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="86dad-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="86dad-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86dad-123">Requirements</span></span>



| <span data-ttu-id="86dad-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86dad-124">Requirement</span></span> | <span data-ttu-id="86dad-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="86dad-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86dad-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86dad-126">Minimum supported client</span></span><br/> | <span data-ttu-id="86dad-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="86dad-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="86dad-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86dad-128">Minimum supported server</span></span><br/> | <span data-ttu-id="86dad-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86dad-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86dad-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="86dad-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="86dad-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="86dad-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="86dad-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="86dad-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86dad-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="86dad-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="86dad-134">DLL</span><span class="sxs-lookup"><span data-stu-id="86dad-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86dad-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86dad-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="86dad-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86dad-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86dad-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="86dad-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





