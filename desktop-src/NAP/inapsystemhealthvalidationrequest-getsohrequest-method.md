---
title: Méthode INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator. h)
description: Permet aux programmes de validation d’intégrité système (SHV) de récupérer et de valider les informations de SoHRequest envoyées par leurs homologues de l’agent d’intégrité système (SHA) sur le client.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106417"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a><span data-ttu-id="0ec06-106">INapSystemHealthValidationRequest :: GetSoHRequest, méthode</span><span class="sxs-lookup"><span data-stu-id="0ec06-106">INapSystemHealthValidationRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="0ec06-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0ec06-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0ec06-108">La méthode **INapSystemHealthValidationRequest :: GetSoHRequest** permet aux programmes de validation d’intégrité système (SHV) de récupérer et de valider les informations de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) envoyées par leurs homologues de l’agent d’intégrité système (SHA) sur le client.</span><span class="sxs-lookup"><span data-stu-id="0ec06-108">The **INapSystemHealthValidationRequest::GetSoHRequest** method allows System Health Validators (SHVs) to retrieve and validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) information sent by their System Health Agent (SHA) counterparts on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec06-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ec06-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a><span data-ttu-id="0ec06-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ec06-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ec06-111">*sohRequest* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0ec06-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec06-112">Pointeur vers un pointeur vers une structure [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="0ec06-112">A pointer to a pointer to an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0ec06-113">*napSystemGenerated* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0ec06-113">*napSystemGenerated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec06-114">Valeur **booléenne** qui est **true** si la SoH a été créée par le NapAgent pour le compte de l’algorithme SHA et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0ec06-114">A **BOOL** that is **TRUE** if the SoH was created by the NapAgent on behalf of the SHA and **FALSE** otherwise.</span></span> <span data-ttu-id="0ec06-115">Il est principalement utilisé pour indiquer un échec SHA pour l’intégrité du service.</span><span class="sxs-lookup"><span data-stu-id="0ec06-115">It is primarily used to indicate an SHA failure to the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ec06-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ec06-116">Return value</span></span>

<span data-ttu-id="0ec06-117">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="0ec06-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0ec06-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0ec06-118">Return code</span></span>                                                                                     | <span data-ttu-id="0ec06-119">Description</span><span class="sxs-lookup"><span data-stu-id="0ec06-119">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ec06-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ec06-120"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0ec06-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0ec06-121">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0ec06-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0ec06-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0ec06-123">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0ec06-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0ec06-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0ec06-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0ec06-125">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0ec06-125">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ec06-126">Notes</span><span class="sxs-lookup"><span data-stu-id="0ec06-126">Remarks</span></span>

<span data-ttu-id="0ec06-127">Le paramètre *sohRequest* peut retourner la **valeur null** si le client n’a pas envoyé de [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à l’SHV.</span><span class="sxs-lookup"><span data-stu-id="0ec06-127">The *sohRequest* parameter may return **NULL** if the client did not send an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the SHV.</span></span> <span data-ttu-id="0ec06-128">Dans ce scénario, le SHV peut remplir un **SoHResponse** avec le code d’erreur de l' [**\_ \_ \_ SOH NAP manquant**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0ec06-128">In that scenario the SHV can populate an **SoHResponse** with the error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>

<span data-ttu-id="0ec06-129">Si le paramètre *napSystemGenerated* a la **valeur true**, le format de *SoHRequest* est le suivant :</span><span class="sxs-lookup"><span data-stu-id="0ec06-129">If the *napSystemGenerated* parameter is **TRUE**, the format of *SoHRequest* is as follows:</span></span>

-   <span data-ttu-id="0ec06-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="0ec06-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="0ec06-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="0ec06-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="0ec06-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<SHA-Failure-erreur-code>**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="0ec06-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**<sha-failure-error-code>**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec06-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ec06-133">Requirements</span></span>



| <span data-ttu-id="0ec06-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ec06-134">Requirement</span></span> | <span data-ttu-id="0ec06-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ec06-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec06-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ec06-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec06-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ec06-137">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="0ec06-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ec06-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec06-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ec06-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ec06-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ec06-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ec06-141"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ec06-141"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ec06-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="0ec06-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ec06-143"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ec06-143"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="0ec06-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0ec06-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ec06-145"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ec06-145"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="0ec06-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ec06-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec06-147">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="0ec06-147">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





