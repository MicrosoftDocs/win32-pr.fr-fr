---
title: Méthode INapEnforcementClientConnection SetFlags (NapEnforcementClient. h)
description: Est utilisé pour différencier les réponses premières des réponses en raison des SoHRequests mises en cache par les enforceurs. | Méthode INapEnforcementClientConnection SetFlags (NapEnforcementClient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Méthode SetFlags NAP
- Méthode SetFlags NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522920"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a><span data-ttu-id="c7369-107">INapEnforcementClientConnection :: SetFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="c7369-107">INapEnforcementClientConnection::SetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="c7369-108">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c7369-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c7369-109">La méthode **INapEnforcementClientConnection :: SetFlags** est utilisée pour différencier les réponses premières des réponses en raison des SoHRequests mises en cache par les enforceurs.</span><span class="sxs-lookup"><span data-stu-id="c7369-109">The **INapEnforcementClientConnection::SetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7369-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7369-110">Syntax</span></span>


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a><span data-ttu-id="c7369-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7369-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7369-112">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7369-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7369-113">Indicateurs qui déterminent si le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) est dû à un **SoHRequest** mis en cache.</span><span class="sxs-lookup"><span data-stu-id="c7369-113">Flags that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="c7369-114">Si *Flags* a la valeur [**freshSoHRequest**](nap-type-constants.md), il s’agit d’une nouvelle demande ; dans le cas contraire, il s’agit d’une demande mise en cache.</span><span class="sxs-lookup"><span data-stu-id="c7369-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7369-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7369-115">Return value</span></span>

<span data-ttu-id="c7369-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="c7369-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c7369-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c7369-117">Return code</span></span>                                                                                     | <span data-ttu-id="c7369-118">Description</span><span class="sxs-lookup"><span data-stu-id="c7369-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7369-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7369-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c7369-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="c7369-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c7369-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c7369-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c7369-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="c7369-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c7369-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c7369-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c7369-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="c7369-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7369-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c7369-125">Remarks</span></span>

<span data-ttu-id="c7369-126">Cette valeur est définie par NapAgent.</span><span class="sxs-lookup"><span data-stu-id="c7369-126">This value is set by the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7369-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7369-127">Requirements</span></span>



| <span data-ttu-id="c7369-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7369-128">Requirement</span></span> | <span data-ttu-id="c7369-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7369-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7369-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7369-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7369-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7369-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c7369-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7369-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7369-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7369-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c7369-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7369-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7369-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7369-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7369-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="c7369-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7369-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7369-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7369-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c7369-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7369-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7369-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c7369-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7369-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7369-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="c7369-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





