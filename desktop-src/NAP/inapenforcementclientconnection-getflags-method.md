---
title: INapEnforcementClientConnection GetFlags, méthode (NapEnforcementClient. h)
description: Est utilisé pour différencier les réponses premières des réponses en raison des SoHRequests mises en cache par les enforceurs. | INapEnforcementClientConnection GetFlags, méthode (NapEnforcementClient. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Méthode GetFlags NAP
- GetFlags, méthode NAP, interface INapEnforcementClientConnection
- Interface INapEnforcementClientConnection NAP, méthode GetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106525825"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a><span data-ttu-id="e94d8-107">INapEnforcementClientConnection :: GetFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="e94d8-107">INapEnforcementClientConnection::GetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="e94d8-108">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e94d8-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e94d8-109">La méthode **INapEnforcementClientConnection :: GetFlags** est utilisée pour différencier les réponses premières des réponses en raison des SoHRequests mises en cache par les enforceurs.</span><span class="sxs-lookup"><span data-stu-id="e94d8-109">The **INapEnforcementClientConnection::GetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e94d8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e94d8-110">Syntax</span></span>


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a><span data-ttu-id="e94d8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e94d8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e94d8-112">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e94d8-112">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e94d8-113">Pointeur vers un indicateur qui détermine si le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) est dû à un **SoHRequest** mis en cache.</span><span class="sxs-lookup"><span data-stu-id="e94d8-113">A pointer to a flag that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="e94d8-114">Si *Flags* a la valeur [**freshSoHRequest**](nap-type-constants.md), il s’agit d’une nouvelle demande ; dans le cas contraire, il s’agit d’une demande mise en cache.</span><span class="sxs-lookup"><span data-stu-id="e94d8-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e94d8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e94d8-115">Return value</span></span>

<span data-ttu-id="e94d8-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="e94d8-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e94d8-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e94d8-117">Return code</span></span>                                                                                     | <span data-ttu-id="e94d8-118">Description</span><span class="sxs-lookup"><span data-stu-id="e94d8-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e94d8-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e94d8-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e94d8-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e94d8-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e94d8-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e94d8-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e94d8-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e94d8-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e94d8-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e94d8-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e94d8-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e94d8-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e94d8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e94d8-125">Requirements</span></span>



| <span data-ttu-id="e94d8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e94d8-126">Requirement</span></span> | <span data-ttu-id="e94d8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e94d8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e94d8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e94d8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e94d8-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e94d8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e94d8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e94d8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e94d8-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e94d8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e94d8-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e94d8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e94d8-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e94d8-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e94d8-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="e94d8-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e94d8-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e94d8-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e94d8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e94d8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e94d8-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e94d8-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e94d8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e94d8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e94d8-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e94d8-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





