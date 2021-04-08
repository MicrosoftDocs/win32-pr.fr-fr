---
title: Méthode INapEnforcementClientConnection SetIsolationInfo (NapEnforcementClient. h)
description: Est utilisé par NapAgent pour définir les informations d’isolation du client.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- Méthode SetIsolationInfo NAP
- Méthode SetIsolationInfo NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1cfd7ad227fec6942e0660769f52b3d4f12201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740925"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a><span data-ttu-id="db9f6-106">INapEnforcementClientConnection :: SetIsolationInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="db9f6-106">INapEnforcementClientConnection::SetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="db9f6-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="db9f6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="db9f6-108">La méthode **INapEnforcementClientConnection :: SetIsolationInfo** est utilisée par le NapAgent pour définir les informations d’isolation du client.</span><span class="sxs-lookup"><span data-stu-id="db9f6-108">The **INapEnforcementClientConnection::SetIsolationInfo** method is used by the NapAgent to set the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9f6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db9f6-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="db9f6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db9f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9f6-111">*isolationInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db9f6-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9f6-112">Pointeur vers une structure [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) qui contient l’état de connectivité du client.</span><span class="sxs-lookup"><span data-stu-id="db9f6-112">A pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9f6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db9f6-113">Return value</span></span>

<span data-ttu-id="db9f6-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="db9f6-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="db9f6-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="db9f6-115">Return code</span></span>                                                                                     | <span data-ttu-id="db9f6-116">Description</span><span class="sxs-lookup"><span data-stu-id="db9f6-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="db9f6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db9f6-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="db9f6-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="db9f6-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="db9f6-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="db9f6-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="db9f6-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="db9f6-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="db9f6-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="db9f6-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="db9f6-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="db9f6-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db9f6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="db9f6-123">Remarks</span></span>

<span data-ttu-id="db9f6-124">Ces informations sont définies par NapAgent après le traitement d’un SoHResponse et ne doivent pas être définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="db9f6-124">This information is set by NapAgent after processing an SoHResponse and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9f6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db9f6-125">Requirements</span></span>



| <span data-ttu-id="db9f6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db9f6-126">Requirement</span></span> | <span data-ttu-id="db9f6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="db9f6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db9f6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db9f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="db9f6-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db9f6-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="db9f6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db9f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="db9f6-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db9f6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="db9f6-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="db9f6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9f6-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="db9f6-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="db9f6-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="db9f6-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db9f6-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db9f6-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="db9f6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="db9f6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db9f6-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db9f6-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="db9f6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db9f6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9f6-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="db9f6-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





