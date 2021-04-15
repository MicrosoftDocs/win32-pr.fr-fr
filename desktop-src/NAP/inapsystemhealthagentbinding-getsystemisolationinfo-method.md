---
title: Méthode INapSystemHealthAgentBinding GetSystemIsolationInfo (NapSystemHealthAgent. h)
description: Est appelé par l’SHA pour déterminer l’état de l’isolation du système.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Méthode GetSystemIsolationInfo NAP
- Méthode GetSystemIsolationInfo NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, méthode GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466862"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a><span data-ttu-id="e67c4-106">INapSystemHealthAgentBinding :: GetSystemIsolationInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="e67c4-106">INapSystemHealthAgentBinding::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="e67c4-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e67c4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e67c4-108">La méthode **INapSystemHealthAgentBinding :: GetSystemIsolationInfo** est appelée par l’SHA pour déterminer l’état de l’isolation du système.</span><span class="sxs-lookup"><span data-stu-id="e67c4-108">The **INapSystemHealthAgentBinding::GetSystemIsolationInfo** method is called by SHAs to determine the system isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="e67c4-109">Utilisez [**INapSystemHealthAgentBinding2 :: GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) pour déterminer l’état d’isolement étendu du système.</span><span class="sxs-lookup"><span data-stu-id="e67c4-109">Use [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) in order to determine the extended isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e67c4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e67c4-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a><span data-ttu-id="e67c4-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e67c4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e67c4-112">*isolationInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e67c4-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e67c4-113">Pointeur vers un pointeur vers une structure [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) qui contient l’état d’isolement du système pour les connexions connues.</span><span class="sxs-lookup"><span data-stu-id="e67c4-113">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the isolation state of the system for known connections.</span></span> <span data-ttu-id="e67c4-114">*isolationInfoindicates* si le système est dans un état d’accès restreint, de stage ou d’accès non restreint.</span><span class="sxs-lookup"><span data-stu-id="e67c4-114">*isolationInfoindicates* if the system is in a state of restricted access, probation, or unrestricted access.</span></span>

</dd> <dt>

<span data-ttu-id="e67c4-115">*unknownConnections* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e67c4-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e67c4-116">Pointeur vers un **booléen** qui a la **valeur true** si toutes les connexions sont dans un état inconnu et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e67c4-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e67c4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e67c4-117">Return value</span></span>

<span data-ttu-id="e67c4-118">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="e67c4-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e67c4-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e67c4-119">Return code</span></span>                                                                                             | <span data-ttu-id="e67c4-120">Description</span><span class="sxs-lookup"><span data-stu-id="e67c4-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e67c4-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e67c4-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="e67c4-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e67c4-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="e67c4-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e67c4-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="e67c4-124">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e67c4-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="e67c4-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e67c4-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="e67c4-126">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e67c4-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e67c4-127"><dt>**NAP \_ E \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="e67c4-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="e67c4-128">L’algorithme SHA n’a pas été précédemment initialisé.</span><span class="sxs-lookup"><span data-stu-id="e67c4-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="e67c4-129"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="e67c4-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="e67c4-130">Le NapAgent a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="e67c4-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="e67c4-131">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="e67c4-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e67c4-132">Notes</span><span class="sxs-lookup"><span data-stu-id="e67c4-132">Remarks</span></span>

<span data-ttu-id="e67c4-133">L’algorithme SHA doit appeler [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="e67c4-133">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e67c4-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e67c4-134">Requirements</span></span>



| <span data-ttu-id="e67c4-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e67c4-135">Requirement</span></span> | <span data-ttu-id="e67c4-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e67c4-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e67c4-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e67c4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e67c4-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e67c4-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e67c4-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e67c4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e67c4-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e67c4-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e67c4-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="e67c4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e67c4-142"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="e67c4-142"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="e67c4-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="e67c4-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e67c4-144"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e67c4-144"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="e67c4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e67c4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e67c4-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e67c4-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e67c4-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e67c4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e67c4-148">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="e67c4-148">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





