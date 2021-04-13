---
title: Méthode INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent. h)
description: Est utilisé par les Sha lorsque leur SoH change.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Méthode NotifySoHChange NAP
- Méthode NotifySoHChange NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, méthode NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509354"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a><span data-ttu-id="72d17-106">INapSystemHealthAgentBinding :: NotifySoHChange, méthode</span><span class="sxs-lookup"><span data-stu-id="72d17-106">INapSystemHealthAgentBinding::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="72d17-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="72d17-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="72d17-108">La méthode **INapSystemHealthAgentBinding :: NotifySoHChange** est utilisée par les Sha lorsque leur SOH change.</span><span class="sxs-lookup"><span data-stu-id="72d17-108">The **INapSystemHealthAgentBinding::NotifySoHChange** method is used by SHAs when their SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d17-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72d17-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="72d17-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72d17-110">Parameters</span></span>

<span data-ttu-id="72d17-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="72d17-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72d17-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72d17-112">Return value</span></span>

<span data-ttu-id="72d17-113">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="72d17-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="72d17-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="72d17-114">Return code</span></span>                                                                                             | <span data-ttu-id="72d17-115">Description</span><span class="sxs-lookup"><span data-stu-id="72d17-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72d17-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="72d17-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="72d17-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="72d17-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="72d17-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="72d17-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="72d17-119">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="72d17-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="72d17-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="72d17-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="72d17-121">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="72d17-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="72d17-122"><dt>**NAP \_ E \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="72d17-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="72d17-123">L’algorithme SHA n’a pas été précédemment initialisé.</span><span class="sxs-lookup"><span data-stu-id="72d17-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="72d17-124"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="72d17-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="72d17-125">Le NapAgent a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="72d17-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="72d17-126">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="72d17-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72d17-127">Notes</span><span class="sxs-lookup"><span data-stu-id="72d17-127">Remarks</span></span>

<span data-ttu-id="72d17-128">SHA ne doit pas appeler cette API de façon spéculative, car cela entraîne un échange SoH sur le câble.</span><span class="sxs-lookup"><span data-stu-id="72d17-128">SHAs must not call this API speculatively since it results in an SoH exchange on the wire.</span></span> <span data-ttu-id="72d17-129">Les appels à cette API doivent être effectués uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="72d17-129">Calls to this API should only be made when necessary.</span></span>

<span data-ttu-id="72d17-130">NapAgent ne contient pas ce thread pour traiter la modification de SoH.</span><span class="sxs-lookup"><span data-stu-id="72d17-130">The NapAgent does not hold this thread to process the SoH change.</span></span> <span data-ttu-id="72d17-131">Au lieu de cela, il retourne immédiatement et traite la modification de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="72d17-131">Instead, it returns immediately and processes the change asynchronously.</span></span>

<span data-ttu-id="72d17-132">L’algorithme SHA doit appeler [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="72d17-132">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d17-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72d17-133">Requirements</span></span>



| <span data-ttu-id="72d17-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72d17-134">Requirement</span></span> | <span data-ttu-id="72d17-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d17-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d17-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d17-136">Minimum supported client</span></span><br/> | <span data-ttu-id="72d17-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72d17-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="72d17-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d17-138">Minimum supported server</span></span><br/> | <span data-ttu-id="72d17-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72d17-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="72d17-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="72d17-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d17-141"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d17-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="72d17-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="72d17-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72d17-143"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72d17-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="72d17-144">DLL</span><span class="sxs-lookup"><span data-stu-id="72d17-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72d17-145"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d17-145"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="72d17-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d17-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d17-147">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="72d17-147">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





