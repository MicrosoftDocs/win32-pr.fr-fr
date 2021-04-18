---
title: Interface INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Fournit des méthodes qui sont utilisées pour prendre en charge les validateurs d’intégrité du système qui sont définis par le développeur de l’application.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- NAP de l’interface INapSystemHealthValidationRequest2
- INapSystemHealthValidationRequest2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513044"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a><span data-ttu-id="5e3f1-105">Interface INapSystemHealthValidationRequest2</span><span class="sxs-lookup"><span data-stu-id="5e3f1-105">INapSystemHealthValidationRequest2 interface</span></span>

> [!Note]  
> <span data-ttu-id="5e3f1-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5e3f1-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5e3f1-107">L’interface **INapSystemHealthValidationRequest2** fournit des méthodes qui sont utilisées pour prendre en charge les validateurs d’intégrité du système qui sont définis par le développeur de l’application.</span><span class="sxs-lookup"><span data-stu-id="5e3f1-107">The **INapSystemHealthValidationRequest2** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="5e3f1-108">Cette interface hérite de toutes les méthodes de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) et doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="5e3f1-108">This interface inherits all the methods of [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="5e3f1-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5e3f1-109">Members</span></span>

<span data-ttu-id="5e3f1-110">L’interface **INapSystemHealthValidationRequest2** hérite de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span><span class="sxs-lookup"><span data-stu-id="5e3f1-110">The **INapSystemHealthValidationRequest2** interface inherits from [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span></span> <span data-ttu-id="5e3f1-111">**INapSystemHealthValidationRequest2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5e3f1-111">**INapSystemHealthValidationRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="5e3f1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5e3f1-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5e3f1-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5e3f1-113">Methods</span></span>

<span data-ttu-id="5e3f1-114">L’interface **INapSystemHealthValidationRequest2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5e3f1-114">The **INapSystemHealthValidationRequest2** interface has these methods.</span></span>



| <span data-ttu-id="5e3f1-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="5e3f1-115">Method</span></span>                                                                                                    | <span data-ttu-id="5e3f1-116">Description</span><span class="sxs-lookup"><span data-stu-id="5e3f1-116">Description</span></span>                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="5e3f1-117">**INapSystemHealthValidationRequest2::GetConfigId**</span><span class="sxs-lookup"><span data-stu-id="5e3f1-117">**INapSystemHealthValidationRequest2::GetConfigId**</span></span>](inapsystemhealthvalidationrequest2-getconfigid.md) | <span data-ttu-id="5e3f1-118">Récupère l’ID de configuration dans une demande de validation.</span><span class="sxs-lookup"><span data-stu-id="5e3f1-118">Retrieves the configuration id in a validation request.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e3f1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5e3f1-119">Remarks</span></span>

<span data-ttu-id="5e3f1-120">Si un SHV ne prend pas en charge [**INapComponentConfig3**](inapcomponentconfig3.md), cette interface ne s’applique pas.</span><span class="sxs-lookup"><span data-stu-id="5e3f1-120">If an SHV doesn t support [**INapComponentConfig3**](inapcomponentconfig3.md), this interface doesn t apply.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e3f1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e3f1-121">Requirements</span></span>



| <span data-ttu-id="5e3f1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e3f1-122">Requirement</span></span> | <span data-ttu-id="5e3f1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e3f1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3f1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e3f1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3f1-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e3f1-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="5e3f1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e3f1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3f1-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e3f1-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5e3f1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e3f1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e3f1-129"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e3f1-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e3f1-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="5e3f1-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e3f1-131"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e3f1-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e3f1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5e3f1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e3f1-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e3f1-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="5e3f1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e3f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e3f1-135">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="5e3f1-135">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[<span data-ttu-id="5e3f1-136">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="5e3f1-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="5e3f1-137">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="5e3f1-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





