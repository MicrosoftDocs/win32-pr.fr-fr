---
title: Interface INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Doit être implémentée par les développeurs SHV pour permettre au système NAP de communiquer avec un SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- NAP de l’interface INapSystemHealthValidator
- INapSystemHealthValidator interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740901"
---
# <a name="inapsystemhealthvalidator-interface"></a><span data-ttu-id="f2827-105">Interface INapSystemHealthValidator</span><span class="sxs-lookup"><span data-stu-id="f2827-105">INapSystemHealthValidator interface</span></span>

> [!Note]  
> <span data-ttu-id="f2827-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f2827-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f2827-107">**INapSystemHealthValidator** fournit des méthodes qui doivent être implémentées par les développeurs SHV pour permettre au système NAP de communiquer avec un SHV.</span><span class="sxs-lookup"><span data-stu-id="f2827-107">The **INapSystemHealthValidator** provides methods that must be implemented by SHV developers to enable the NAP system to communicate with an SHV.</span></span>

## <a name="members"></a><span data-ttu-id="f2827-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f2827-108">Members</span></span>

<span data-ttu-id="f2827-109">L’interface **INapSystemHealthValidator** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f2827-109">The **INapSystemHealthValidator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f2827-110">**INapSystemHealthValidator** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f2827-110">**INapSystemHealthValidator** also has these types of members:</span></span>

-   [<span data-ttu-id="f2827-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f2827-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f2827-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f2827-112">Methods</span></span>

<span data-ttu-id="f2827-113">L’interface **INapSystemHealthValidator** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f2827-113">The **INapSystemHealthValidator** interface has these methods.</span></span>



| <span data-ttu-id="f2827-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="f2827-114">Method</span></span>                                                                                   | <span data-ttu-id="f2827-115">Description</span><span class="sxs-lookup"><span data-stu-id="f2827-115">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2827-116">**INapSystemHealthValidator :: Validate**</span><span class="sxs-lookup"><span data-stu-id="f2827-116">**INapSystemHealthValidator::Validate**</span></span>](inapsystemhealthvalidator-validate-method.md) | <span data-ttu-id="f2827-117">Le système NAP appelle cette méthode définie par l’application pour valider les [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) reçus d’un client.</span><span class="sxs-lookup"><span data-stu-id="f2827-117">The NAP system calls this application defined method to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="f2827-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2827-118">Requirements</span></span>



| <span data-ttu-id="f2827-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2827-119">Requirement</span></span> | <span data-ttu-id="f2827-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2827-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2827-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2827-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2827-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2827-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="f2827-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2827-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2827-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2827-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2827-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2827-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2827-126"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2827-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2827-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="f2827-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2827-128"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2827-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2827-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2827-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2827-130">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="f2827-130">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f2827-131">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="f2827-131">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

