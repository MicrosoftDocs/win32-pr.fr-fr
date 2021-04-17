---
title: INapServerCallback OnComplete, méthode (NapSystemHealthValidator. h)
description: Utilisé par les validateurs d’intégrité du système pour signaler la fin de la requête asynchrone.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- OnComplete, méthode NAP
- OnComplete méthode NAP, interface INapServerCallback
- Interface INapServerCallback NAP, méthode OnComplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467059"
---
# <a name="inapservercallbackoncomplete-method"></a><span data-ttu-id="307d8-106">INapServerCallback :: OnComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="307d8-106">INapServerCallback::OnComplete method</span></span>

> [!Note]  
> <span data-ttu-id="307d8-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="307d8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="307d8-108">La méthode **INapServerCallback :: OnComplete** est utilisée par les validateurs de validation pour signaler la fin de la requête asynchrone.</span><span class="sxs-lookup"><span data-stu-id="307d8-108">The **INapServerCallback::OnComplete** method is used by SHVs to signal asynchronous request completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="307d8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="307d8-109">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="307d8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="307d8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="307d8-111">*demande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="307d8-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="307d8-112">Pointeur vers un objet [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) qui représente une demande de validation.</span><span class="sxs-lookup"><span data-stu-id="307d8-112">A pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that represents a validation request.</span></span>

</dd> <dt>

<span data-ttu-id="307d8-113">*ErrorCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="307d8-113">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="307d8-114">[**Code d’erreur NAP**](nap-error-constants.md) qui indique la raison pour laquelle la validation n’a pas pu être effectuée.</span><span class="sxs-lookup"><span data-stu-id="307d8-114">A [**NAP error code**](nap-error-constants.md) that indicates the reason why the validation could not be performed.</span></span>

> [!Note]  
> <span data-ttu-id="307d8-115">En règle générale, la valeur de retour de la méthode [**INapSystemHealthValidationRequest :: SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) est passée à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="307d8-115">Typically, the return value of the [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) method is passed to this parameter.</span></span> <span data-ttu-id="307d8-116">Toutefois, si **SetSoHResponse** n’a pas pu être appelé en raison d’un échec de retraitement, la valeur retournée par la commande ayant échoué est passée.</span><span class="sxs-lookup"><span data-stu-id="307d8-116">However, if **SetSoHResponse** could not be called due to a reprocessing failure, the value returned by the failed command is passed.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="307d8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="307d8-117">Return value</span></span>

<span data-ttu-id="307d8-118">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="307d8-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="307d8-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="307d8-119">Return code</span></span>                                                                                     | <span data-ttu-id="307d8-120">Description</span><span class="sxs-lookup"><span data-stu-id="307d8-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="307d8-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="307d8-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="307d8-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="307d8-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="307d8-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="307d8-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="307d8-124">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="307d8-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="307d8-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="307d8-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="307d8-126">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="307d8-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="307d8-127">Notes</span><span class="sxs-lookup"><span data-stu-id="307d8-127">Remarks</span></span>

<span data-ttu-id="307d8-128">Les validateurs doivent retourner la \_ valeur OK si la validation [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) peut être effectuée, que le **SoHRequest** ait réussi ou non le contrôle d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="307d8-128">Validators must return S\_OK if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) validation could be completed, regardless of whether the **SoHRequest** passed the health check.</span></span>

## <a name="requirements"></a><span data-ttu-id="307d8-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="307d8-129">Requirements</span></span>



| <span data-ttu-id="307d8-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="307d8-130">Requirement</span></span> | <span data-ttu-id="307d8-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="307d8-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307d8-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="307d8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="307d8-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="307d8-133">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="307d8-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="307d8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="307d8-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="307d8-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="307d8-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="307d8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="307d8-137"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="307d8-137"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="307d8-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="307d8-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="307d8-139"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="307d8-139"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="307d8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="307d8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="307d8-141"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="307d8-141"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="307d8-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="307d8-142">See also</span></span>

<dl> <span data-ttu-id="307d8-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="307d8-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="307d8-144">**INapServerCallback**</span><span class="sxs-lookup"><span data-stu-id="307d8-144">**INapServerCallback**</span></span>](inapservercallback.md)
</dt> <dt>

[<span data-ttu-id="307d8-145">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="307d8-145">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





