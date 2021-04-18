---
title: Méthode INapSystemHealthAgentBinding FlushCache (NapSystemHealthAgent. h)
description: Est appelé par un SHA pour vider son cache SoH.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- Méthode FlushCache NAP
- Méthode FlushCache NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, méthode FlushCache
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512355"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a><span data-ttu-id="e4a4b-106">INapSystemHealthAgentBinding :: FlushCache, méthode</span><span class="sxs-lookup"><span data-stu-id="e4a4b-106">INapSystemHealthAgentBinding::FlushCache method</span></span>

> [!Note]  
> <span data-ttu-id="e4a4b-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e4a4b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e4a4b-108">La méthode **INapSystemHealthAgentBinding :: FlushCache** est appelée par un SHA pour vider son cache SOH.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-108">The **INapSystemHealthAgentBinding::FlushCache** method is called by an SHA to flush its SoH cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a4b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4a4b-109">Syntax</span></span>


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a><span data-ttu-id="e4a4b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4a4b-110">Parameters</span></span>

<span data-ttu-id="e4a4b-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4a4b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4a4b-112">Return value</span></span>

<span data-ttu-id="e4a4b-113">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e4a4b-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e4a4b-114">Return code</span></span>                                                                                         | <span data-ttu-id="e4a4b-115">Description</span><span class="sxs-lookup"><span data-stu-id="e4a4b-115">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4a4b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4b-116"><dt>**S\_OK** </dt></span></span> </dl>               | <span data-ttu-id="e4a4b-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="e4a4b-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4b-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>     | <span data-ttu-id="e4a4b-119">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="e4a4b-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4b-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>      | <span data-ttu-id="e4a4b-121">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e4a4b-122"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4b-122"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e4a4b-123">Le NapAgent a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-123">The NapAgent has been stopped.</span></span> <span data-ttu-id="e4a4b-124">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-124">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4a4b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e4a4b-125">Remarks</span></span>

<span data-ttu-id="e4a4b-126">NapAgent gère un cache des SoHs récents fournis par des SHA différents.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-126">The NapAgent maintains a cache of recent SoHs provided by different SHAs.</span></span> <span data-ttu-id="e4a4b-127">Ce cache est utile pour optimiser les performances au moment de l’amorçage, lorsque l’SHA peut ou non être lié au système.</span><span class="sxs-lookup"><span data-stu-id="e4a4b-127">This cache is useful to optimize boot-time performance, when SHAs may or may not be bound to the system.</span></span>

<span data-ttu-id="e4a4b-128">L’algorithme SHA doit appeler [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="e4a4b-128">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a4b-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4a4b-129">Requirements</span></span>



| <span data-ttu-id="e4a4b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4a4b-130">Requirement</span></span> | <span data-ttu-id="e4a4b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4a4b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a4b-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4a4b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a4b-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4a4b-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e4a4b-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4a4b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a4b-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4a4b-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e4a4b-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4a4b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a4b-137"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4b-137"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4a4b-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="e4a4b-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4a4b-139"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4b-139"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="e4a4b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e4a4b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4a4b-141"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4a4b-141"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e4a4b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4a4b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a4b-143">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="e4a4b-143">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





