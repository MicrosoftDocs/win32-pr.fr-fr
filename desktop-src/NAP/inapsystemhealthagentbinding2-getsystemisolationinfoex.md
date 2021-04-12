---
title: Méthode INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent. h)
description: Est appelé par l’SHA pour déterminer l’état d’isolement du système et l’état d’isolement étendu.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Méthode GetSystemIsolationInfoEx NAP
- Méthode GetSystemIsolationInfoEx NAP, interface INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 interface NAP, méthode GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508678"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a><span data-ttu-id="075ba-106">INapSystemHealthAgentBinding2 :: GetSystemIsolationInfoEx, méthode</span><span class="sxs-lookup"><span data-stu-id="075ba-106">INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="075ba-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="075ba-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="075ba-108">La méthode **INapSystemHealthAgentBinding2 :: GetSystemIsolationInfoEx** est appelée par l’SHA pour déterminer l’état d’isolement système et l’état d’isolement étendu.</span><span class="sxs-lookup"><span data-stu-id="075ba-108">The **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** method is called by SHAs to determine the system isolation state and extended isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="075ba-109">Utilisez [**INapSystemHealthAgentBinding :: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) pour déterminer uniquement l’état d’isolement du système.</span><span class="sxs-lookup"><span data-stu-id="075ba-109">Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) in order to only determine the isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="075ba-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="075ba-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="075ba-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="075ba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075ba-112">*isolationInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="075ba-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="075ba-113">Pointeur vers un pointeur vers une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) qui contient l’état d’isolement étendu du système pour les connexions connues.</span><span class="sxs-lookup"><span data-stu-id="075ba-113">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the extended isolation state of the system for known connections.</span></span> <span data-ttu-id="075ba-114">*isolationInfo* indique si le système est dans un état d’accès restreint, de stage ou d’accès non restreint, ainsi que des informations [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .</span><span class="sxs-lookup"><span data-stu-id="075ba-114">*isolationInfo* indicates if the system is in a state of restricted access, probation, or unrestricted access, as well as [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) information.</span></span>

</dd> <dt>

<span data-ttu-id="075ba-115">*unknownConnections* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="075ba-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="075ba-116">Pointeur vers un **booléen** qui a la **valeur true** si toutes les connexions sont dans un état inconnu et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="075ba-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075ba-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="075ba-117">Return value</span></span>

<span data-ttu-id="075ba-118">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="075ba-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="075ba-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="075ba-119">Return code</span></span>                                                                                             | <span data-ttu-id="075ba-120">Description</span><span class="sxs-lookup"><span data-stu-id="075ba-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="075ba-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="075ba-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="075ba-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="075ba-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="075ba-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="075ba-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="075ba-124">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="075ba-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="075ba-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="075ba-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="075ba-126">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="075ba-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="075ba-127"><dt>**NAP \_ E \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="075ba-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="075ba-128">L’algorithme SHA n’a pas été précédemment initialisé.</span><span class="sxs-lookup"><span data-stu-id="075ba-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="075ba-129"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="075ba-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="075ba-130">Le NapAgent a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="075ba-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="075ba-131">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="075ba-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="075ba-132">Notes</span><span class="sxs-lookup"><span data-stu-id="075ba-132">Remarks</span></span>

<span data-ttu-id="075ba-133">L’algorithme SHA doit libérer la structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) en appelant [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="075ba-133">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

<span data-ttu-id="075ba-134">L’algorithme SHA doit appeler [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="075ba-134">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="075ba-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="075ba-135">Requirements</span></span>



| <span data-ttu-id="075ba-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="075ba-136">Requirement</span></span> | <span data-ttu-id="075ba-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="075ba-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="075ba-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="075ba-138">Minimum supported client</span></span><br/> | <span data-ttu-id="075ba-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="075ba-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="075ba-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="075ba-140">Minimum supported server</span></span><br/> | <span data-ttu-id="075ba-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="075ba-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="075ba-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="075ba-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="075ba-143"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="075ba-143"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="075ba-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="075ba-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="075ba-145"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="075ba-145"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="075ba-146">DLL</span><span class="sxs-lookup"><span data-stu-id="075ba-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="075ba-147"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="075ba-147"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="075ba-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="075ba-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075ba-149">**INapSystemHealthAgentBinding2**</span><span class="sxs-lookup"><span data-stu-id="075ba-149">**INapSystemHealthAgentBinding2**</span></span>](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





