---
title: Méthode INapSystemHealthValidationRequest GetStringCorrelationId (NapSystemHealthValidator. h)
description: Est utilisé par les programmes de validation d’intégrité système (SHV) qui doivent enregistrer ces informations.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- Méthode GetStringCorrelationId NAP
- Méthode GetStringCorrelationId NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 554a5a31f0aa46f6bcbd7a750662d47ab2c78040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519169"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a><span data-ttu-id="1d07a-106">INapSystemHealthValidationRequest :: GetStringCorrelationId, méthode</span><span class="sxs-lookup"><span data-stu-id="1d07a-106">INapSystemHealthValidationRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="1d07a-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1d07a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1d07a-108">La méthode **INapSystemHealthValidationRequest :: GetStringCorrelationId** est utilisée par les programmes de validation d’intégrité système (SHV) qui doivent consigner ces informations.</span><span class="sxs-lookup"><span data-stu-id="1d07a-108">The **INapSystemHealthValidationRequest::GetStringCorrelationId** method is used by System Health Validators (SHVs) which must log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d07a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d07a-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="1d07a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d07a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d07a-111">*CorrelationId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1d07a-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d07a-112">Pointeur vers un pointeur vers un [**StringCorrelationId**](nap-type-constants.md) unique pour l’échange de déclaration d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="1d07a-112">A pointer to a pointer to a unique [**StringCorrelationId**](nap-type-constants.md) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d07a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d07a-113">Return value</span></span>

<span data-ttu-id="1d07a-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="1d07a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1d07a-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1d07a-115">Return code</span></span>                                                                                     | <span data-ttu-id="1d07a-116">Description</span><span class="sxs-lookup"><span data-stu-id="1d07a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d07a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d07a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1d07a-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1d07a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1d07a-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1d07a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1d07a-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1d07a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1d07a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d07a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1d07a-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="1d07a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1d07a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d07a-123">Requirements</span></span>



| <span data-ttu-id="1d07a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d07a-124">Requirement</span></span> | <span data-ttu-id="1d07a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d07a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d07a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d07a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1d07a-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d07a-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="1d07a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d07a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1d07a-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d07a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d07a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d07a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d07a-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d07a-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d07a-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="1d07a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d07a-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d07a-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="1d07a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1d07a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d07a-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d07a-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="1d07a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d07a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d07a-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="1d07a-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





