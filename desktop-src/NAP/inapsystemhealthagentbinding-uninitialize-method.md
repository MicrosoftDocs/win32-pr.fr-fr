---
title: INapSystemHealthAgentBinding méthode Uninitialize (NapSystemHealthAgent. h)
description: Fait en sorte que le NapAgent libère toutes ses références aux pointeurs COM de l’agent d’intégrité système.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Uninitialize la méthode NAP
- Uninitialize Method NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, Uninitialize, méthode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511774"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a><span data-ttu-id="707a8-106">INapSystemHealthAgentBinding :: Uninitialize, méthode</span><span class="sxs-lookup"><span data-stu-id="707a8-106">INapSystemHealthAgentBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="707a8-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="707a8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="707a8-108">La méthode **INapSystemHealthAgentBinding :: Uninitialize** force NapAgent à libérer toutes ses références aux pointeurs com de l’agent d’intégrité système.</span><span class="sxs-lookup"><span data-stu-id="707a8-108">The **INapSystemHealthAgentBinding::Uninitialize** method causes the NapAgent to release all its references to system health agent COM pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="707a8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="707a8-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="707a8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="707a8-110">Parameters</span></span>

<span data-ttu-id="707a8-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="707a8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="707a8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="707a8-112">Return value</span></span>

<span data-ttu-id="707a8-113">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="707a8-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="707a8-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="707a8-114">Return code</span></span>                                                                                             | <span data-ttu-id="707a8-115">Description</span><span class="sxs-lookup"><span data-stu-id="707a8-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="707a8-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="707a8-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="707a8-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="707a8-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="707a8-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="707a8-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="707a8-119">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="707a8-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="707a8-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="707a8-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="707a8-121">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="707a8-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="707a8-122"><dt>**NAP \_ E \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="707a8-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="707a8-123">L’algorithme SHA n’a pas été précédemment initialisé.</span><span class="sxs-lookup"><span data-stu-id="707a8-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="707a8-124"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="707a8-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="707a8-125">Le NapAgent a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="707a8-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="707a8-126">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="707a8-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="707a8-127">Notes</span><span class="sxs-lookup"><span data-stu-id="707a8-127">Remarks</span></span>

<span data-ttu-id="707a8-128">NapAgent bloque l’exécution de cet appel de méthode jusqu’à ce que tous les appels existants sur les interfaces de liaison et de rappel se terminent.</span><span class="sxs-lookup"><span data-stu-id="707a8-128">The NapAgent blocks execution of this method call until all existing calls on the Binding and Callback interfaces complete.</span></span>

<span data-ttu-id="707a8-129">L’algorithme SHA doit appeler [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="707a8-129">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="707a8-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="707a8-130">Requirements</span></span>



| <span data-ttu-id="707a8-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="707a8-131">Requirement</span></span> | <span data-ttu-id="707a8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="707a8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="707a8-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="707a8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="707a8-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="707a8-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="707a8-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="707a8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="707a8-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="707a8-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="707a8-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="707a8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="707a8-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="707a8-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="707a8-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="707a8-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="707a8-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="707a8-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="707a8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="707a8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="707a8-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="707a8-142"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="707a8-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="707a8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707a8-144">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="707a8-144">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





