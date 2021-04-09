---
title: Méthode INapEnforcementClientConnection GetIsolationInfo (NapEnforcementClient. h)
description: Est utilisé pour récupérer les informations d’isolation du client.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- Méthode GetIsolationInfo NAP
- Méthode GetIsolationInfo NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942870"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a><span data-ttu-id="59c3f-106">INapEnforcementClientConnection :: GetIsolationInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="59c3f-106">INapEnforcementClientConnection::GetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="59c3f-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="59c3f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="59c3f-108">La méthode **INapEnforcementClientConnection :: GetIsolationInfo** est utilisée pour récupérer les informations d’isolation du client.</span><span class="sxs-lookup"><span data-stu-id="59c3f-108">The **INapEnforcementClientConnection::GetIsolationInfo** method is used get the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c3f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59c3f-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="59c3f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59c3f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c3f-111">*isolationInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="59c3f-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3f-112">Pointeur vers un pointeur vers une structure [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) qui contient l’état de connectivité du client.</span><span class="sxs-lookup"><span data-stu-id="59c3f-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c3f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59c3f-113">Return value</span></span>

<span data-ttu-id="59c3f-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="59c3f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="59c3f-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="59c3f-115">Return code</span></span>                                                                                     | <span data-ttu-id="59c3f-116">Description</span><span class="sxs-lookup"><span data-stu-id="59c3f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="59c3f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="59c3f-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="59c3f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="59c3f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="59c3f-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="59c3f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="59c3f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="59c3f-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="59c3f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59c3f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="59c3f-123">Remarks</span></span>

<span data-ttu-id="59c3f-124">Ces informations sont définies par le NapAgent après le traitement d’un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) et ne doivent pas être définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="59c3f-124">This information is set by the NapAgent after processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c3f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59c3f-125">Requirements</span></span>



| <span data-ttu-id="59c3f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59c3f-126">Requirement</span></span> | <span data-ttu-id="59c3f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c3f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c3f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59c3f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="59c3f-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59c3f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="59c3f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59c3f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="59c3f-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59c3f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59c3f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="59c3f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c3f-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c3f-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="59c3f-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="59c3f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59c3f-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="59c3f-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="59c3f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="59c3f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59c3f-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59c3f-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="59c3f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c3f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c3f-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="59c3f-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





