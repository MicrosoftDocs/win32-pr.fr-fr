---
title: Méthode INapSystemHealthAgentCallback NotifySystemIsolationStateChange (NapSystemHealthAgent. h)
description: Est appelé par le NapAgent pour indiquer que l’état d’isolement système ou l’heure de fin de la période d’essai a changé.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Méthode NotifySystemIsolationStateChange NAP
- Méthode NotifySystemIsolationStateChange NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode NotifySystemIsolationStateChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741956"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a><span data-ttu-id="5c16c-106">INapSystemHealthAgentCallback :: NotifySystemIsolationStateChange, méthode</span><span class="sxs-lookup"><span data-stu-id="5c16c-106">INapSystemHealthAgentCallback::NotifySystemIsolationStateChange method</span></span>

> [!Note]  
> <span data-ttu-id="5c16c-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5c16c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5c16c-108">La méthode **INapSystemHealthAgentCallback :: NotifySystemIsolationStateChange** est appelée par le NapAgent pour indiquer que l’état d’isolement système ou l’heure de fin de la période d’essai a changé.</span><span class="sxs-lookup"><span data-stu-id="5c16c-108">The **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange** method is called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c16c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c16c-109">Syntax</span></span>


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a><span data-ttu-id="5c16c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c16c-110">Parameters</span></span>

<span data-ttu-id="5c16c-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5c16c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c16c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c16c-112">Return value</span></span>

<span data-ttu-id="5c16c-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="5c16c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="5c16c-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5c16c-114">Return code</span></span>                                                                          | <span data-ttu-id="5c16c-115">Description</span><span class="sxs-lookup"><span data-stu-id="5c16c-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="5c16c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c16c-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5c16c-117">Indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5c16c-117">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c16c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5c16c-118">Remarks</span></span>

<span data-ttu-id="5c16c-119">Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.</span><span class="sxs-lookup"><span data-stu-id="5c16c-119">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="5c16c-120">L’agent d’intégrité peut interroger l’état du système NAP à l’aide de [**INapSystemHealthAgentBinding :: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="5c16c-120">The health agent can query the system NAP state using the [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c16c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c16c-121">Requirements</span></span>



| <span data-ttu-id="5c16c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c16c-122">Requirement</span></span> | <span data-ttu-id="5c16c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c16c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c16c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c16c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5c16c-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c16c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c16c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c16c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5c16c-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c16c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c16c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c16c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c16c-129"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c16c-129"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c16c-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="5c16c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c16c-131"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c16c-131"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c16c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c16c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c16c-133">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="5c16c-133">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





