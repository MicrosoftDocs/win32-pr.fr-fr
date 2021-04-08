---
title: Méthode INapEnforcementClientConnection SetConnectionId (NapEnforcementClient. h)
description: Est utilisé pour définir l’ID unique de la connexion et doit être défini par le client de mise en œuvre dès que la connexion est créée.
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- Méthode SetConnectionId NAP
- Méthode SetConnectionId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetConnectionId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9749be304170ec7706b637429f577e77411ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941915"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a><span data-ttu-id="0d9d0-106">INapEnforcementClientConnection :: SetConnectionId, méthode</span><span class="sxs-lookup"><span data-stu-id="0d9d0-106">INapEnforcementClientConnection::SetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="0d9d0-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0d9d0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0d9d0-108">La méthode **INapEnforcementClientConnection :: SetConnectionId** est utilisée pour définir l’ID unique de la connexion et doit être définie par le client de mise en œuvre dès que la connexion est créée.</span><span class="sxs-lookup"><span data-stu-id="0d9d0-108">The **INapEnforcementClientConnection::SetConnectionId** method is used to set the unique ID of the connection and must be set by the enforcement client as soon as the connection is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9d0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d9d0-109">Syntax</span></span>


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="0d9d0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d9d0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d9d0-111">*ID* \[ de la dans\]</span><span class="sxs-lookup"><span data-stu-id="0d9d0-111">*connectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d9d0-112">Pointeur vers un [**ID**](nap-datatypes.md) de connexion qui identifie de façon unique une connexion.</span><span class="sxs-lookup"><span data-stu-id="0d9d0-112">A pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d9d0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d9d0-113">Return value</span></span>

<span data-ttu-id="0d9d0-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="0d9d0-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0d9d0-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0d9d0-115">Return code</span></span>                                                                                     | <span data-ttu-id="0d9d0-116">Description</span><span class="sxs-lookup"><span data-stu-id="0d9d0-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d9d0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d0-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0d9d0-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0d9d0-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0d9d0-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d0-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0d9d0-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0d9d0-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0d9d0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d0-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0d9d0-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0d9d0-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d9d0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="0d9d0-123">Remarks</span></span>

<span data-ttu-id="0d9d0-124">Cet ID de connexion est principalement utilisé à des fins de journalisation.</span><span class="sxs-lookup"><span data-stu-id="0d9d0-124">This ConnectionID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d9d0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d9d0-125">Requirements</span></span>



| <span data-ttu-id="0d9d0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d9d0-126">Requirement</span></span> | <span data-ttu-id="0d9d0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d9d0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9d0-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9d0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9d0-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d9d0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0d9d0-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9d0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9d0-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d9d0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0d9d0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d9d0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d9d0-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d0-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d9d0-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="0d9d0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d9d0-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d0-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d9d0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0d9d0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d9d0-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d0-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0d9d0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d9d0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9d0-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="0d9d0-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





