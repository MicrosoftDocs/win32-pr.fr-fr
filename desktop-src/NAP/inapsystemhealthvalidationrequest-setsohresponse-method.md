---
title: Méthode INapSystemHealthValidationRequest SetSoHResponse (NapSystemHealthValidator. h)
description: Permet aux programmes de validation d’intégrité système de définir le SoHResponse à envoyer à son homologue de l’agent d’intégrité système (SHA) côté client.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Méthode SetSoHResponse NAP
- Méthode SetSoHResponse NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode SetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385055"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a><span data-ttu-id="20f7f-106">INapSystemHealthValidationRequest :: SetSoHResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="20f7f-106">INapSystemHealthValidationRequest::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="20f7f-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="20f7f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="20f7f-108">La méthode **INapSystemHealthValidationRequest :: SetSoHResponse** permet aux programmes de validation d’intégrité système (SHV) de définir le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) à envoyer à son homologue de l’agent d’intégrité système (SHA) côté client.</span><span class="sxs-lookup"><span data-stu-id="20f7f-108">The **INapSystemHealthValidationRequest::SetSoHResponse** method allows System Health Validators (SHVs) to set the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) to be sent to its System Health Agent (SHA) counterpart on the client-side.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f7f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20f7f-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="20f7f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20f7f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20f7f-111">*sohResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20f7f-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20f7f-112">Pointeur vers une structure [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="20f7f-112">A pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20f7f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20f7f-113">Return value</span></span>

<span data-ttu-id="20f7f-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="20f7f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="20f7f-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="20f7f-115">Return code</span></span>                                                                                     | <span data-ttu-id="20f7f-116">Description</span><span class="sxs-lookup"><span data-stu-id="20f7f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="20f7f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20f7f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="20f7f-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="20f7f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="20f7f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="20f7f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="20f7f-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="20f7f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="20f7f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="20f7f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="20f7f-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="20f7f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="20f7f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20f7f-123">Requirements</span></span>



| <span data-ttu-id="20f7f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20f7f-124">Requirement</span></span> | <span data-ttu-id="20f7f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="20f7f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f7f-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20f7f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="20f7f-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="20f7f-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="20f7f-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20f7f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="20f7f-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20f7f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20f7f-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="20f7f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="20f7f-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="20f7f-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="20f7f-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="20f7f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20f7f-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20f7f-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="20f7f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="20f7f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20f7f-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20f7f-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="20f7f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20f7f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f7f-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="20f7f-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





