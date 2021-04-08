---
title: Interface INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: Sont utilisés pour prendre en charge les validateurs d’intégrité du système qui sont définis par le développeur de l’application.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- NAP de l’interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743533"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a><span data-ttu-id="45492-105">Interface INapSystemHealthValidationRequest</span><span class="sxs-lookup"><span data-stu-id="45492-105">INapSystemHealthValidationRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="45492-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="45492-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="45492-107">L’interface **INapSystemHealthValidationRequest** fournit des méthodes qui sont utilisées pour prendre en charge les validateurs d’intégrité du système qui sont définis par le développeur de l’application.</span><span class="sxs-lookup"><span data-stu-id="45492-107">The **INapSystemHealthValidationRequest** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="45492-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) hérite de toutes les méthodes de cette interface et doit être utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="45492-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="45492-109">Membres</span><span class="sxs-lookup"><span data-stu-id="45492-109">Members</span></span>

<span data-ttu-id="45492-110">L’interface **INapSystemHealthValidationRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="45492-110">The **INapSystemHealthValidationRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="45492-111">**INapSystemHealthValidationRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="45492-111">**INapSystemHealthValidationRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="45492-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45492-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="45492-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45492-113">Methods</span></span>

<span data-ttu-id="45492-114">L’interface **INapSystemHealthValidationRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="45492-114">The **INapSystemHealthValidationRequest** interface has these methods.</span></span>



| <span data-ttu-id="45492-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="45492-115">Method</span></span>                                                                                                                               | <span data-ttu-id="45492-116">Description</span><span class="sxs-lookup"><span data-stu-id="45492-116">Description</span></span>                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45492-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="45492-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | <span data-ttu-id="45492-118">Utilisé par les validateurs pour récupérer l’ID de corrélation.</span><span class="sxs-lookup"><span data-stu-id="45492-118">Used by validators to retrieve the correlation ID.</span></span> <span data-ttu-id="45492-119">Le validateur doit ensuite enregistrer ces informations.</span><span class="sxs-lookup"><span data-stu-id="45492-119">The validator must then log this information.</span></span><br/>           |
| [<span data-ttu-id="45492-120">**INapSystemHealthValidationRequest::GetMachineName**</span><span class="sxs-lookup"><span data-stu-id="45492-120">**INapSystemHealthValidationRequest::GetMachineName**</span></span>](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | <span data-ttu-id="45492-121">Utilisé par les validateurs pour récupérer le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="45492-121">Used by validators to retrieve the machine name.</span></span> <span data-ttu-id="45492-122">Le validateur doit ensuite enregistrer ces informations.</span><span class="sxs-lookup"><span data-stu-id="45492-122">The validator must then log this information.</span></span><br/>             |
| [<span data-ttu-id="45492-123">**INapSystemHealthValidationRequest::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="45492-123">**INapSystemHealthValidationRequest::GetPrivateData**</span></span>](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | <span data-ttu-id="45492-124">Autorise le NapServer à récupérer des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="45492-124">Allows the NapServer to retrieve state information.</span></span><br/>                                                        |
| [<span data-ttu-id="45492-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="45492-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span></span>](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | <span data-ttu-id="45492-126">Autorise les validateurs à récupérer et valider les informations SoHRequest.</span><span class="sxs-lookup"><span data-stu-id="45492-126">Allows Validators to retrieve and validate the SoHRequest information.</span></span><br/>                                     |
| [<span data-ttu-id="45492-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="45492-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | <span data-ttu-id="45492-128">Obtient l’objet SoHResponse.</span><span class="sxs-lookup"><span data-stu-id="45492-128">Gets the SoHResponse object.</span></span><br/>                                                                               |
| [<span data-ttu-id="45492-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="45492-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | <span data-ttu-id="45492-130">Utilisé par les validateurs pour récupérer un identificateur Exchange unique.</span><span class="sxs-lookup"><span data-stu-id="45492-130">Used by validators to retrieve a unique exchange identifier.</span></span> <span data-ttu-id="45492-131">Le validateur doit ensuite enregistrer ces informations.</span><span class="sxs-lookup"><span data-stu-id="45492-131">The validator must then log this information.</span></span><br/> |
| [<span data-ttu-id="45492-132">**INapSystemHealthValidationRequest::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="45492-132">**INapSystemHealthValidationRequest::SetPrivateData**</span></span>](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | <span data-ttu-id="45492-133">Permet au NapServer de stocker des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="45492-133">Allows the NapServer to store state information.</span></span><br/>                                                           |
| [<span data-ttu-id="45492-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="45492-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | <span data-ttu-id="45492-135">Autorise les validateurs à définir le SoHResponse.</span><span class="sxs-lookup"><span data-stu-id="45492-135">Allows validators to set the SoHResponse.</span></span><br/>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="45492-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45492-136">Requirements</span></span>



| <span data-ttu-id="45492-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45492-137">Requirement</span></span> | <span data-ttu-id="45492-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="45492-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45492-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45492-139">Minimum supported client</span></span><br/> | <span data-ttu-id="45492-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="45492-140">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="45492-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45492-141">Minimum supported server</span></span><br/> | <span data-ttu-id="45492-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45492-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45492-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="45492-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="45492-144"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="45492-144"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="45492-145">MIDL</span><span class="sxs-lookup"><span data-stu-id="45492-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45492-146"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45492-146"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="45492-147">DLL</span><span class="sxs-lookup"><span data-stu-id="45492-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45492-148"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45492-148"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="45492-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45492-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45492-150">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="45492-150">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="45492-151">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="45492-151">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

