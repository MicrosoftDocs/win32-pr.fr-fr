---
title: INapSystemHealthAgentBinding Initialize, méthode (NapSystemHealthAgent. h)
description: Initialise l’agent d’intégrité système (SHA) et lie l’algorithme SHA au service NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317133"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a><span data-ttu-id="25ceb-106">INapSystemHealthAgentBinding :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="25ceb-106">INapSystemHealthAgentBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="25ceb-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="25ceb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="25ceb-108">La méthode **INapSystemHealthAgentBinding :: Initialize** Initialise l’agent d’intégrité système (SHA) et lie l’algorithme SHA au service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="25ceb-108">The **INapSystemHealthAgentBinding::Initialize** method initializes the system health agent (SHA) and binds the SHA to the NapAgent service.</span></span> <span data-ttu-id="25ceb-109">Cette méthode doit être appelée avant d’appeler toute autre méthode sur l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="25ceb-109">This method must be called before calling any other method on the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ceb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25ceb-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="25ceb-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25ceb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ceb-112">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25ceb-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ceb-113">[SystemHealthEntityId](nap-datatypes.md) unique qui contient l’ID de l’agent SHA lié au service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="25ceb-113">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA being bound to the NapAgent service.</span></span>

</dd> <dt>

<span data-ttu-id="25ceb-114">*rappel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25ceb-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ceb-115">Pointeur COM vers une interface [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) utilisée par le NapAgent pour rappeler l’agent d’intégrité avec une notification/un processus.</span><span class="sxs-lookup"><span data-stu-id="25ceb-115">A COM pointer to an [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) interface used by the NapAgent to callback the health agent with a notify/process.</span></span> <span data-ttu-id="25ceb-116">Le NapAgent contient une référence à l’objet associé à cette interface jusqu’à ce que [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="25ceb-116">The NapAgent holds a reference to the object associated with this interface until [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ceb-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25ceb-117">Return value</span></span>

<span data-ttu-id="25ceb-118">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="25ceb-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="25ceb-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="25ceb-119">Return code</span></span>                                                                                                | <span data-ttu-id="25ceb-120">Description</span><span class="sxs-lookup"><span data-stu-id="25ceb-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25ceb-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-121"><dt>**S\_OK** </dt></span></span> </dl>                      | <span data-ttu-id="25ceb-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="25ceb-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="25ceb-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>            | <span data-ttu-id="25ceb-124">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="25ceb-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="25ceb-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>             | <span data-ttu-id="25ceb-126">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="25ceb-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="25ceb-127"><dt>**ERREUR \_ déjà \_ initialisée**</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-127"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="25ceb-128">Si l’agent SHA a été initialisé précédemment, cette erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="25ceb-128">If the SHA has initialized previously, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="25ceb-129"><dt>**NAP \_ E \_ non \_ inscrit**</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-129"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>     | <span data-ttu-id="25ceb-130">Si l’agent SHA n’a pas été inscrit précédemment, cette erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="25ceb-130">If the SHA has not registered earlier, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="25ceb-131"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-131"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>        | <span data-ttu-id="25ceb-132">Le NapAgent a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="25ceb-132">The NapAgent has been stopped.</span></span> <span data-ttu-id="25ceb-133">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="25ceb-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25ceb-134">Notes</span><span class="sxs-lookup"><span data-stu-id="25ceb-134">Remarks</span></span>

<span data-ttu-id="25ceb-135">NapAgent ne déclenche pas d’échange SoH en raison de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="25ceb-135">The NapAgent does not trigger a SoH exchange as a result of initialization.</span></span> <span data-ttu-id="25ceb-136">Un agent d’intégrité système doit appeler [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) pour demander un échange de paquets SOH après l’initialisation avec NapAgent.</span><span class="sxs-lookup"><span data-stu-id="25ceb-136">A system health agent must call [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to request an exchange of SoH packets after initializing with the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ceb-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25ceb-137">Requirements</span></span>



| <span data-ttu-id="25ceb-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25ceb-138">Requirement</span></span> | <span data-ttu-id="25ceb-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="25ceb-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25ceb-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25ceb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="25ceb-141">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25ceb-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="25ceb-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25ceb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="25ceb-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25ceb-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="25ceb-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="25ceb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="25ceb-145"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-145"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="25ceb-146">MIDL</span><span class="sxs-lookup"><span data-stu-id="25ceb-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25ceb-147"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-147"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="25ceb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="25ceb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25ceb-149"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25ceb-149"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="25ceb-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25ceb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ceb-151">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="25ceb-151">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





